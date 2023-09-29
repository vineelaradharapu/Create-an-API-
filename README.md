# Create-an-API-
// models/Doctor.js
const mongoose = require('mongoose');

const doctorSchema = new mongoose.Schema({
  name: { type: String, required: true },
  speciality: { type: String, required: true },
  // Add more fields as needed, e.g., location, consultation fee, etc.
  schedule: [
    {
      dayOfWeek: { type: String, required: true },
      maxAppointments: { type: Number, required: true },
      // Add more schedule-related fields as needed, e.g., start time, end time
    },
  ],
});

module.exports = mongoose.model('Doctor', doctorSchema);

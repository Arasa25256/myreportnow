
// File: src/App.js import React from "react"; import { BrowserRouter as Router, Routes, Route } from "react-router-dom"; import Home from "./pages/Home"; import ReportForm from "./pages/ReportForm"; import ReportList from "./pages/ReportList"; import MapPage from "./pages/MapPage"; import AdminDashboard from "./pages/AdminDashboard";

function App() { return ( <Router> <Routes> <Route path="/" element={<Home />} /> <Route path="/lapor" element={<ReportForm />} /> <Route path="/senarai-aduan" element={<ReportList />} /> <Route path="/peta" element={<MapPage />} /> <Route path="/admin" element={<AdminDashboard />} /> </Routes> </Router> ); }

export default App;

// File: src/pages/Home.js import React from "react"; import { Link } from "react-router-dom";

function Home() { return ( <div className="p-6 text-center"> <h1 className="text-3xl font-bold mb-4">REPORTNOW</h1> <p className="mb-4 italic">"Rakyat Prihatin, Malaysia Sejahtera"</p> <div className="space-x-4"> <Link to="/lapor" className="btn">Lapor Aduan</Link> <Link to="/senarai-aduan" className="btn">Senarai Aduan</Link> <Link to="/peta" className="btn">Peta Aduan</Link> <Link to="/admin" className="btn">Admin</Link> </div> <footer className="mt-8 text-sm">by Arasa</footer> </div> ); }

export default Home;

// File: src/pages/ReportForm.js import React, { useState } from "react";

function ReportForm() { const [form, setForm] = useState


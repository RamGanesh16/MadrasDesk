# MadrasDesk
import React from "react";
import { BrowserRouter as Router, Route, Routes, Link } from "react-router-dom";
import { Button } from "@/components/ui/button";

const Home = () => (
  <section className="text-center p-10 bg-gray-100 min-h-screen">
    <h1 className="text-4xl font-bold text-blue-800">MadrasDesk</h1>
    <p className="mt-4 text-lg text-gray-600">Chennai’s Smartest Portable Workspace</p>
    <Button className="mt-6 bg-blue-800 text-white px-6 py-2 rounded-lg">Book a Pod</Button>
  </section>
);

const About = () => (
  <section className="p-10 min-h-screen">
    <h2 className="text-3xl font-bold text-gray-800">About Us</h2>
    <p className="mt-4 text-gray-600">MadrasDesk provides smart workspace pods for freelancers, students, and professionals in Chennai. Designed for convenience, productivity, and affordability.</p>
  </section>
);

const Features = () => (
  <section className="p-10 min-h-screen bg-gray-50">
    <h2 className="text-3xl font-bold text-gray-800">Features</h2>
    <ul className="mt-4 text-gray-600 list-disc pl-5">
      <li>High-Speed WiFi</li>
      <li>Soundproof Pods</li>
      <li>Comfortable Seating</li>
      <li>Power & Charging Points</li>
      <li>Affordable Pricing</li>
    </ul>
  </section>
);

const Pricing = () => (
  <section className="p-10 min-h-screen">
    <h2 className="text-3xl font-bold text-gray-800">Pricing</h2>
    <p className="mt-4 text-gray-600">Starting at just ₹50/hour. Choose from daily, weekly, or monthly plans.</p>
  </section>
);

const Testimonials = () => (
  <section className="p-10 min-h-screen bg-gray-50">
    <h2 className="text-3xl font-bold text-gray-800">What Our Users Say</h2>
    <p className="mt-4 text-gray-600 italic">"MadrasDesk has transformed the way I work. Convenient and affordable!" - A Happy Customer</p>
    <p className="mt-4 text-gray-600 italic">"A quiet and productive space in the heart of Chennai. Highly recommended!" - Freelancer</p>
  </section>
);

const Contact = () => (
  <section className="p-10 min-h-screen bg-gray-100">
    <h2 className="text-3xl font-bold text-gray-800">Contact Us</h2>
    <p className="mt-4 text-gray-600">Email: contact@madrasdesk.com</p>
    <p>Phone: +91-XXXXXXXXXX</p>
  </section>
);

const Navbar = () => (
  <nav className="bg-white shadow-md p-4 flex justify-between">
    <Link to="/" className="text-xl font-bold text-blue-800">MadrasDesk</Link>
    <div className="space-x-4">
      <Link to="/about" className="text-gray-700">About</Link>
      <Link to="/features" className="text-gray-700">Features</Link>
      <Link to="/pricing" className="text-gray-700">Pricing</Link>
      <Link to="/testimonials" className="text-gray-700">Testimonials</Link>
      <Link to="/contact" className="text-gray-700">Contact</Link>
    </div>
  </nav>
);

const App = () => {
  return (
    <Router>
      <Navbar />
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/features" element={<Features />} />
        <Route path="/pricing" element={<Pricing />} />
        <Route path="/testimonials" element={<Testimonials />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </Router>
  );
};

export default App;

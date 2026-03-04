# Swimming-pool-care
Hello, We provide professional swimming pool cleaning and maintenance services from Bark Emdad. We make sure your pool stays clean, safe, and ready to use at all times.  Our Services: ✅ Full pool cleaning ✅ Water balancing &amp; chemical treatment ✅ Filter &amp; pump check/maintenance ✅ Algae removal ✅ Weekly / Monthly maintenance 
import React from "react";
import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Phone, MessageCircle, MapPin } from "lucide-react";

export default function BarkEmdadWebsite() {
  return (
    <div className="min-h-screen bg-blue-50 text-gray-800">
      {/* Hero Section */}
      <section className="bg-gradient-to-r from-blue-600 to-cyan-500 text-white py-20 px-6 text-center">
        <div className="flex flex-col items-center justify-center mb-6">
          <img
            src="/mnt/data/1000361670.png"
            alt="Swimming Pool Care Logo"
            className="w-64 md:w-80 mb-4"
          />
          <motion.h1
            initial={{ opacity: 0, y: -20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.8 }}
            className="text-4xl md:text-5xl font-bold"
          >
            Swimming Pool Care
          </motion.h1>
        </div>
        <p className="text-lg md:text-xl mb-6">
          Professional Swimming Pool Cleaning & Maintenance Services
        </p>
        <div className="flex justify-center gap-4 flex-wrap">
          <a href="tel:+9660554617186">
            <Button className="rounded-2xl px-6 py-3 text-lg">
              <Phone className="mr-2" /> Call Now
            </Button>
          </a>
          <a href="https://wa.me/9660554617186" target="_blank" rel="noopener noreferrer">
            <Button variant="secondary" className="rounded-2xl px-6 py-3 text-lg">
              <MessageCircle className="mr-2" /> WhatsApp
            </Button>
          </a>
        </div>
      </section>

      {/* About Section */}
      <section className="py-16 px-6 max-w-5xl mx-auto text-center">
        <h2 className="text-3xl font-bold mb-6">About Us</h2>
        <p className="text-lg leading-relaxed">
          We provide professional swimming pool cleaning and maintenance services in
          Al Khobar Shamalia and Dammam. We make sure your pool stays clean, safe,
          and ready to use at all times.
        </p>
      </section>

      {/* Services Section */}
      <section className="py-16 bg-white px-6">
        <h2 className="text-3xl font-bold text-center mb-12">Our Services</h2>
        <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-6 max-w-6xl mx-auto">
          {[
            "Full Pool Cleaning",
            "Water Balancing & Chemical Treatment",
            "Filter & Pump Check / Maintenance",
            "Algae Removal",
            "Weekly Maintenance Packages",
            "Monthly Maintenance Packages",
          ].map((service, index) => (
            <Card key={index} className="rounded-2xl shadow-lg">
              <CardContent className="p-6 text-center text-lg font-medium">
                {service}
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Arabic Section */}
      <section className="py-16 px-6 bg-blue-100 text-right" dir="rtl">
        <h2 className="text-3xl font-bold mb-6 text-center">خدماتنا</h2>
        <div className="max-w-4xl mx-auto space-y-4 text-lg">
          <p>نحن في Swimming Pool Care نقدم خدمات احترافية لتنظيف وصيانة المسابح.</p>
          <ul className="list-disc pr-6 space-y-2">
            <li>تنظيف المسبح بالكامل</li>
            <li>موازنة المياه والمعالجة الكيميائية</li>
            <li>فحص وصيانة الفلتر والمضخة</li>
            <li>إزالة الطحالب</li>
            <li>باقات صيانة أسبوعية / شهرية</li>
          </ul>
        </div>
      </section>

      {/* Contact Section */}
      <section className="py-16 px-6 text-center bg-white">
        <h2 className="text-3xl font-bold mb-6">Contact Us</h2>
        <p className="text-lg mb-4">Reliable & Affordable Pool Service</p>
        <div className="flex justify-center items-center gap-2 text-lg mb-2">
          <Phone /> <span>+9660554617186</span>
        </div>
        <div className="flex justify-center items-center gap-2 text-lg">
          <MapPin /> <span>Al Khobar Shamalia, Dammam</span>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-blue-600 text-white text-center py-6">
        <p>© {new Date().getFullYear()} Swimming Pool Care. All Rights Reserved.</p>
      </footer>
    </div>
  );
}

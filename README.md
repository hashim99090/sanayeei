// مشروع صناييعي - النسخة الأولية (MVP) // هذا الملف يمثل صفحة رئيسية لعرض الخدمات وطلب الصيانة

import React from "react"; import { BrowserRouter as Router, Routes, Route } from "react-router-dom"; import HomePage from "./pages/HomePage"; import ServiceDetails from "./pages/ServiceDetails"; import RequestForm from "./pages/RequestForm"; import LoginPage from "./pages/LoginPage"; import Dashboard from "./pages/Dashboard"; import UserRequestsPage from "./pages/UserRequests";

export default function App() { return ( <Router> <Routes> <Route path="/" element={<HomePage />} /> <Route path="/login" element={<LoginPage />} /> <Route path="/services/:id" element={<ServiceDetails />} /> <Route path="/request/:id" element={<RequestForm />} /> <Route path="/dashboard" element={<Dashboard />} /> <Route path="/my-requests" element={<UserRequestsPage />} /> </Routes> </Router> ); }

// المجلدات الداعمة تشمل: // pages/HomePage.jsx - لعرض كل الخدمات // pages/ServiceDetails.jsx - تفاصيل كل خدمة // pages/RequestForm.jsx - نموذج طلب صيانة // pages/LoginPage.jsx - الدخول برقم أو بريد // pages/Dashboard.jsx - لوحة مزود الخدمة // pages/UserRequests.jsx - صفحة طلبات المستخدم

// المشروع يستخدم Firebase للمصادقة وقاعدة البيانات // سيتم ربطه لاحقًا بـ .env ورفع إلى GitHub


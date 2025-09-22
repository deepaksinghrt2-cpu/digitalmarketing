<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alex Riley - Digital Marketing Manager</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .hero-bg {
            background-color: #111827;
        }
        /* Sidebar active link style */
        .sidebar-link.active {
            background-color: #1F2937; /* bg-gray-900 */
            color: #F9FAFB; /* text-gray-100 */
        }
        /* Style for editable text */
        .editable-content {
            outline: 2px dashed #3B82F6; /* blue-500 */
            padding: 4px;
            border-radius: 4px;
            cursor: text;
        }
        /* Style for editable images container */
        .editable-image-container {
            position: relative;
            display: inline-block;
        }
        .edit-image-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease;
            cursor: pointer;
            border-radius: inherit; /* For rounded images */
        }
        .body.edit-mode-active .editable-image-container:hover .edit-image-overlay {
            opacity: 1;
        }
        /* Customer Chat Styles */
        .chat-bubble-sent {
            background-color: #4F46E5; /* indigo-600 */
            color: white;
            border-radius: 1rem 1rem 0.25rem 1rem;
        }
        .chat-bubble-received {
            background-color: #E5E7EB; /* gray-200 */
            color: #1F2937; /* gray-800 */
            border-radius: 1rem 1rem 1rem 0.25rem;
        }
        .chat-user-list-item.active {
            background-color: #374151; /* gray-700 */
        }
        .login-bg {
             background-image: url('https://images.unsplash.com/photo-1542281286-9e0a16bb7366?q=80&w=2070&auto=format&fit=crop');
             background-size: cover;
             background-position: center;
        }
        /* .dropdown:hover .dropdown-menu {
            display: block;
        } */ /* Removed hover effect */
    </style>
</head>
<body class="bg-gray-50 text-gray-800">

    <!-- =========== MAIN WEBSITE VIEW =========== -->
    <div id="main-website">
        <!-- Header / Navbar -->
        <header class="bg-white shadow-sm sticky top-0 z-40">
            <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
                <a href="#" id="brand-name" data-editable class="text-2xl font-bold text-gray-900">Alex Riley</a>
                <div class="hidden md:flex space-x-6 items-center">
                    <a href="#services" class="text-gray-600 hover:text-indigo-600">Services</a>
                    <a href="#portfolio" class="text-gray-600 hover:text-indigo-600">Portfolio</a>
                    <a href="#about" class="text-gray-600 hover:text-indigo-600">About</a>
                    <a href="#contact" class="text-gray-600 hover:text-indigo-600">Contact</a>
                    <div class="relative dropdown">
                        <button id="login-dropdown-btn" class="bg-indigo-600 text-white px-4 py-2 rounded-md hover:bg-indigo-700 transition">Login</button>
                        <div id="login-dropdown-menu" class="dropdown-menu absolute right-0 mt-2 w-48 bg-white rounded-md shadow-lg z-50 hidden">
                            <a href="#" id="customer-login-link" data-login-type="customer" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Customer Login</a>
                            <a href="#" id="admin-login-link" data-login-type="admin" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">Admin Login</a>
                        </div>
                    </div>
                </div>
                <div class="md:hidden">
                    <button class="text-gray-900 focus:outline-none">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
                    </button>
                </div>
            </nav>
        </header>

        <main>
            <!-- Hero Section -->
            <section class="hero-bg text-white py-20 md:py-32">
                <div class="container mx-auto px-6 text-center">
                    <div class="editable-image-container rounded-full">
                         <img id="hero-image" data-editable-img src="https://placehold.co/128x128/E0E7FF/4F46E5?text=AR" alt="Alex Riley" class="w-32 h-32 rounded-full mx-auto mb-6 border-4 border-indigo-500">
                    </div>
                    <h1 id="hero-title" data-editable class="text-4xl md:text-6xl font-extrabold leading-tight">Data-Driven Digital Marketing That Grows Your Business</h1>
                    <p id="hero-subtitle" data-editable class="mt-4 text-lg md:text-xl text-gray-300 max-w-3xl mx-auto">I help service-based businesses increase their leads and sales through targeted online strategies.</p>
                    <a href="#contact" class="mt-8 inline-block bg-indigo-600 text-white px-8 py-3 rounded-md text-lg font-semibold hover:bg-indigo-700 transition">Book a Free Consultation</a>
                </div>
            </section>

            <!-- Services Section -->
            <section id="services" class="py-20 bg-white">
                <div class="container mx-auto px-6">
                    <div class="text-center mb-12">
                        <h2 id="services-title" data-editable class="text-3xl md:text-4xl font-bold text-gray-900">My Services</h2>
                        <p id="services-subtitle" data-editable class="mt-4 text-gray-600 max-w-2xl mx-auto">I offer a complete suite of digital marketing services to help you succeed online.</p>
                    </div>
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                        <div class="bg-gray-50 p-8 rounded-lg shadow-md hover:shadow-xl transition-shadow">
                            <h3 id="service-1-title" data-editable class="text-xl font-bold mb-2">Search Engine Optimization (SEO)</h3>
                            <p id="service-1-desc" data-editable class="text-gray-600">Rank higher than your competitors and attract ready-to-buy customers with strategic, long-term SEO.</p>
                        </div>
                        <div class="bg-gray-50 p-8 rounded-lg shadow-md hover:shadow-xl transition-shadow">
                            <h3 id="service-2-title" data-editable class="text-xl font-bold mb-2">Pay-Per-Click (PPC) Ads</h3>
                            <p id="service-2-desc" data-editable class="text-gray-600">Generate immediate, high-quality traffic and leads with targeted Google and social media ad campaigns.</p>
                        </div>
                        <div class="bg-gray-50 p-8 rounded-lg shadow-md hover:shadow-xl transition-shadow">
                            <h3 id="service-3-title" data-editable class="text-xl font-bold mb-2">Social Media Marketing</h3>
                            <p id="service-3-desc" data-editable class="text-gray-600">Build a strong brand presence and engage with your community on platforms where they spend their time.</p>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Portfolio Section -->
            <section id="portfolio" class="py-20">
                <div class="container mx-auto px-6">
                    <div class="text-center mb-12">
                        <h2 id="portfolio-title" data-editable class="text-3xl md:text-4xl font-bold text-gray-900">Proven Results</h2>
                        <p id="portfolio-subtitle" data-editable class="mt-4 text-gray-600">Actions speak louder than words. Here's a look at my work.</p>
                    </div>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                        <div class="bg-white rounded-lg shadow-md overflow-hidden">
                             <div class="editable-image-container">
                                <img id="portfolio-1-image" data-editable-img src="https://placehold.co/600x400/111827/FFFFFF?text=Project+1" alt="Portfolio Item 1" class="w-full h-64 object-cover">
                            </div>
                            <div class="p-6">
                                <h3 id="portfolio-1-title" data-editable class="text-xl font-bold mb-2">E-commerce Sales Growth</h3>
                                <p id="portfolio-1-desc" data-editable class="text-gray-600 mb-4">Increased online sales by 300% in 6 months for a retail client through targeted SEO and PPC.</p>
                                <a href="#" class="text-indigo-600 font-semibold hover:underline">View Case Study &rarr;</a>
                            </div>
                        </div>
                        <div class="bg-white rounded-lg shadow-md overflow-hidden">
                            <div class="editable-image-container">
                                <img id="portfolio-2-image" data-editable-img src="https://placehold.co/600x400/4F46E5/FFFFFF?text=Project+2" alt="Portfolio Item 2" class="w-full h-64 object-cover">
                            </div>
                            <div class="p-6">
                                <h3 id="portfolio-2-title" data-editable class="text-xl font-bold mb-2">Local Lead Generation</h3>
                                <p id="portfolio-2-desc" data-editable class="text-gray-600 mb-4">Generated 50+ new high-quality leads per month for a local service business using Google Ads.</p>
                                <a href="#" class="text-indigo-600 font-semibold hover:underline">View Case Study &rarr;</a>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- About Section -->
            <section id="about" class="py-20 bg-white">
                <div class="container mx-auto px-6 text-center">
                    <h2 id="about-title" data-editable class="text-3xl md:text-4xl font-bold text-gray-900">About Me</h2>
                    <div class="editable-image-container rounded-full">
                        <img id="about-image" data-editable-img src="https://placehold.co/128x128/E0E7FF/4F46E5?text=AR" alt="Alex Riley" class="w-32 h-32 rounded-full mx-auto my-6">
                    </div>
                    <p id="about-desc" data-editable class="mt-4 text-gray-600 max-w-3xl mx-auto">With over 8 years of experience in the digital marketing industry, I am passionate about helping businesses navigate the complexities of the online world. My approach is built on transparency, data-driven decisions, and a genuine commitment to my clients' success.</p>
                </div>
            </section>
            
            <!-- Contact Section with Form -->
            <section id="contact" class="py-20 bg-gray-100">
                <div class="container mx-auto px-6">
                    <div class="text-center mb-12">
                        <h2 id="contact-title" data-editable class="text-3xl md:text-4xl font-bold text-gray-900">Ready to Grow Your Business?</h2>
                        <p id="contact-subtitle" data-editable class="mt-4 text-gray-600 max-w-2xl mx-auto">Fill out the form below and I'll get back to you within 24 hours.</p>
                    </div>
                    <div class="max-w-3xl mx-auto bg-white p-8 rounded-lg shadow-md">
                        <form id="customer-contact-form">
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                                <div>
                                    <label for="customer-name" class="block text-gray-700 mb-2">Full Name</label>
                                    <input type="text" id="customer-name" class="w-full px-4 py-2 border rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                                </div>
                                <div>
                                    <label for="customer-email" class="block text-gray-700 mb-2">Email Address</label>
                                    <input type="email" id="customer-email" class="w-full px-4 py-2 border rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-500" required>
                                </div>
                                <div>
                                    <label for="customer-website" class="block text-gray-700 mb-2">Website URL</label>
                                    <input type="url" id="customer-website" class="w-full px-4 py-2 border rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-500" placeholder="https://example.com">
                                </div>
                                <div>
                                    <label for="customer-budget" class="block text-gray-700 mb-2">Your Monthly Budget (₹)</label>
                                    <input type="number" id="customer-budget" class="w-full px-4 py-2 border rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-500" placeholder="e.g., 50000" required>
                                </div>
                            </div>
                            <div class="mt-6">
                                <label for="customer-service" class="block text-gray-700 mb-2">Which service are you interested in?</label>
                                <select id="customer-service" class="w-full px-4 py-2 border rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-500">
                                    <option>Search Engine Optimization (SEO)</option>
                                    <option>Pay-Per-Click (PPC) Ads</option>
                                    <option>Social Media Marketing</option>
                                    <option>Not Sure Yet</option>
                                </select>
                            </div>
                            <div class="mt-6">
                                <label for="customer-message" class="block text-gray-700 mb-2">Tell me about your project</label>
                                <textarea id="customer-message" rows="5" class="w-full px-4 py-2 border rounded-md focus:outline-none focus:ring-2 focus:ring-indigo-500" required></textarea>
                            </div>
                            <div class="mt-6 text-center">
                                <button type="submit" class="bg-indigo-600 text-white px-8 py-3 rounded-md text-lg font-semibold hover:bg-indigo-700 transition">Submit Inquiry</button>
                            </div>
                        </form>
                        <div id="contact-success-message" class="hidden text-center mt-6 p-4 bg-green-100 text-green-800 rounded-md">
                            <h3 class="font-bold text-lg">Thank you!</h3>
                            <p>Your inquiry has been sent. I will get back to you shortly.</p>
                        </div>
                    </div>
                </div>
            </section>
        </main>

        <!-- Footer -->
        <footer class="bg-gray-800 text-white py-8">
            <div class="container mx-auto px-6 text-center">
                <p>&copy; 2025 Alex Riley. All Rights Reserved.</p>
            </div>
        </footer>
    </div>
    
    <!-- =========== ADMIN DASHBOARD VIEW (Initially Hidden) =========== -->
    <div id="admin-panel" class="hidden">
        <div class="flex h-screen bg-gray-100">
            <!-- Sidebar -->
            <aside class="w-64 bg-gray-800 text-white flex flex-col">
                <div class="px-6 py-4 border-b border-gray-700">
                    <h2 class="text-xl font-bold">Admin Panel</h2>
                </div>
                <nav class="flex-1 px-4 py-4 space-y-2">
                    <a href="#" id="dashboard-link" class="sidebar-link active flex items-center px-4 py-2 rounded-md"><svg class="w-6 h-6 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>Dashboard</a>
                    <a href="#" id="edit-website-link" class="sidebar-link flex items-center px-4 py-2 text-gray-300 hover:bg-gray-700 rounded-md"><svg class="w-6 h-6 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15.232 5.232l3.536 3.536m-2.036-5.036a2.5 2.5 0 113.536 3.536L6.5 21.036H3v-3.572L16.732 3.732z"></path></svg>Edit Website</a>
                    <a href="#" id="users-link" class="sidebar-link flex items-center px-4 py-2 text-gray-300 hover:bg-gray-700 rounded-md"><svg class="w-6 h-6 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M15 21a6 6 0 00-9-5.197m0 0A10.999 10.999 0 0012 12c4.472 0 8.268 2.943 9.542 7a11.024 11.024 0 00-2.542-1.121M15 21H3v-1a6 6 0 0112 0v1z"></path></svg>Users</a>
                    <a href="#" id="projects-link" class="sidebar-link flex items-center px-4 py-2 text-gray-300 hover:bg-gray-700 rounded-md"><svg class="w-6 h-6 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>Projects</a>
                    <a href="#" id="chat-link" class="sidebar-link flex items-center px-4 py-2 text-gray-300 hover:bg-gray-700 rounded-md"><svg class="w-6 h-6 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path></svg>Chat</a>
                    <a href="#" id="budgets-link" class="sidebar-link flex items-center px-4 py-2 text-gray-300 hover:bg-gray-700 rounded-md"><svg class="w-6 h-6 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v.01M12 6v-1m0-1V4m0 2.01M12 14c-1.657 0-3-.895-3-2s1.343-2 3-2 3-.895 3-2 1.343-2 3-2m0 8c1.11 0 2.08-.402 2.599-1M12 14v1m0 1v1m0-2.01M12 18v-1m0-1v-1"></path></svg>Budgets</a>
                </nav>
                <div class="px-4 py-4 border-t border-gray-700 mt-auto">
                     <button id="logout-btn" class="flex w-full items-center px-4 py-2 text-gray-300 hover:bg-gray-700 rounded-md"><svg class="w-6 h-6 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1"></path></svg>Logout</button>
                </div>
            </aside>

            <!-- Main Content -->
            <main class="flex-1 p-6 lg:p-10 overflow-y-auto">
                <!-- VIEW 1: Dashboard Home -->
                <div id="dashboard-view">
                    <h1 class="text-3xl font-bold text-gray-800">Admin Dashboard</h1>
                    <p class="text-gray-600 mt-2">Welcome back, Admin! Manage your website from here.</p>
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 mt-6">
                        <div id="visitors-card" class="bg-white p-6 rounded-lg shadow-md cursor-pointer hover:shadow-xl transition-shadow"><h3 class="text-lg font-semibold text-gray-700">Total Visitors</h3><p class="text-3xl font-bold text-indigo-600 mt-2">1,257</p></div>
                        <div id="messages-card" class="bg-white p-6 rounded-lg shadow-md cursor-pointer hover:shadow-xl transition-shadow"><h3 class="text-lg font-semibold text-gray-700">Messages</h3><p class="text-3xl font-bold text-indigo-600 mt-2">0</p></div>
                        <div id="portfolio-card" class="bg-white p-6 rounded-lg shadow-md cursor-pointer hover:shadow-xl transition-shadow"><h3 class="text-lg font-semibold text-gray-700">Portfolio Clicks</h3><p class="text-3xl font-bold text-indigo-600 mt-2">482</p></div>
                        <div id="budgets-card" class="bg-white p-6 rounded-lg shadow-md cursor-pointer hover:shadow-xl transition-shadow"><h3 class="text-lg font-semibold text-gray-700">Customer Budgets</h3><p class="text-3xl font-bold text-indigo-600 mt-2">0 Active</p></div>
                    </div>
                     <div class="mt-10 bg-white p-6 rounded-lg shadow-md">
                        <h2 class="text-xl font-bold text-gray-800 mb-4">Quick Actions</h2>
                         <div class="flex flex-wrap gap-4">
                             <button id="view-projects-btn" class="bg-purple-500 text-white px-4 py-2 rounded-md hover:bg-purple-600">Manage Projects</button>
                             <button id="view-users-btn" class="bg-blue-500 text-white px-4 py-2 rounded-md hover:bg-blue-600">Manage Users</button>
                             <button id="view-website-btn" class="bg-gray-500 text-white px-4 py-2 rounded-md hover:bg-gray-600">View Website</button>
                         </div>
                    </div>
                </div>
                <!-- Other Views (hidden by default) -->
                <div id="users-view" class="hidden">
                    <h1 class="text-3xl font-bold text-gray-800 mb-6">Users & Applicants</h1>
                     <div class="bg-white p-6 rounded-lg shadow-md mb-8">
                        <h2 class="text-xl font-bold text-gray-800 mb-4">Create New Customer Account</h2>
                        <form id="create-customer-form" class="grid grid-cols-1 md:grid-cols-3 gap-4 items-end">
                            <div>
                                <label for="new-customer-name" class="block text-sm font-medium text-gray-700">Customer Name</label>
                                <input type="text" id="new-customer-name" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500" required>
                            </div>
                            <div>
                                <label for="new-customer-email" class="block text-sm font-medium text-gray-700">Customer Email (Username)</label>
                                <input type="email" id="new-customer-email" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500" required>
                            </div>
                            <div>
                                <label for="new-customer-password" class="block text-sm font-medium text-gray-700">Password</label>
                                <input type="password" id="new-customer-password" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500" required>
                            </div>
                            <div class="md:col-span-3 text-right">
                                <button type="submit" class="bg-indigo-600 text-white px-4 py-2 rounded-md hover:bg-indigo-700">Create Account</button>
                            </div>
                        </form>
                    </div>
                    <div class="bg-white p-6 rounded-lg shadow-md">
                         <h2 class="text-xl font-bold text-gray-800 mb-4">User List</h2>
                        <table class="w-full text-left">
                            <thead>
                                <tr class="bg-gray-50 border-b">
                                    <th class="py-3 px-4">Name</th>
                                    <th class="py-3 px-4">Email</th>
                                    <th class="py-3 px-4">Status</th>
                                    <th class="py-3 px-4">Actions</th>
                                </tr>
                            </thead>
                            <tbody>
                                <!-- Data will be populated by JavaScript -->
                            </tbody>
                        </table>
                    </div>
                </div>
                <!-- PROJECTS VIEW FOR ADMIN -->
                 <div id="projects-view" class="hidden">
                     <h1 class="text-3xl font-bold text-gray-800 mb-6">Manage Customer Projects</h1>
                     <div class="flex h-[calc(100vh-12rem)] bg-white rounded-lg shadow-md">
                        <!-- Customer List -->
                        <div class="w-1/3 border-r border-gray-200">
                            <div class="p-4 border-b font-semibold text-lg">Customers</div>
                            <ul id="project-customer-list" class="overflow-y-auto h-[calc(100%-4.5rem)]">
                                <!-- Customer list will be populated by JS -->
                            </ul>
                        </div>
                        <!-- Project Details Window -->
                        <div class="w-2/3 flex flex-col">
                            <div id="project-details-placeholder" class="flex-1 flex items-center justify-center text-gray-500">
                                Select a customer to view their project.
                            </div>
                            <div id="project-details-area" class="hidden flex-1 flex flex-col">
                                <div class="p-4 border-b">
                                    <h2 id="project-customer-name" class="text-xl font-semibold"></h2>
                                </div>
                                <div id="project-tasks-list" class="flex-1 p-6 space-y-4 overflow-y-auto">
                                    <!-- Project tasks will be populated by JS -->
                                </div>
                                <div class="p-4 border-t bg-gray-50">
                                    <h3 class="font-semibold mb-2">Add New Task</h3>
                                    <form id="add-task-form" class="flex items-center gap-2">
                                        <input type="text" id="new-task-name" placeholder="Task Name" class="flex-grow px-3 py-2 border rounded-md" required>
                                        <input type="number" id="new-task-progress" placeholder="Progress %" class="w-24 px-3 py-2 border rounded-md" min="0" max="100" value="0" required>
                                        <button type="submit" class="bg-green-500 text-white px-4 py-2 rounded-md hover:bg-green-600">Add</button>
                                    </form>
                                </div>
                            </div>
                        </div>
                     </div>
                </div>
                <!-- CHAT VIEW FOR ADMIN -->
                <div id="chat-view" class="hidden">
                     <h1 class="text-3xl font-bold text-gray-800 mb-6">Customer Chats</h1>
                     <div class="flex h-[calc(100vh-12rem)] bg-white rounded-lg shadow-md">
                        <!-- Chat User List -->
                        <div class="w-1/3 border-r border-gray-200">
                            <div class="p-4 border-b font-semibold text-lg">Conversations</div>
                            <ul id="admin-chat-user-list" class="overflow-y-auto h-[calc(100%-4.5rem)]">
                                <!-- User list will be populated by JS -->
                            </ul>
                        </div>
                        <!-- Chat Window -->
                        <div id="admin-chat-window" class="w-2/3 flex flex-col">
                            <div id="admin-chat-placeholder" class="flex-1 flex items-center justify-center text-gray-500">
                                Select a conversation to start chatting.
                            </div>
                            <div id="admin-chat-area" class="hidden flex-1 flex flex-col">
                                <div class="p-4 border-b flex items-center">
                                    <h2 id="admin-chat-with-name" class="text-lg font-semibold"></h2>
                                </div>
                                <div id="admin-chat-box" class="flex-1 p-6 space-y-4 overflow-y-auto">
                                    <!-- Admin chat messages will be populated by JS -->
                                </div>
                                <form id="admin-chat-form" class="p-4 border-t flex items-center bg-gray-50">
                                    <input type="text" id="admin-chat-input" class="w-full px-4 py-2 border rounded-l-md focus:outline-none focus:ring-2 focus:ring-indigo-500" placeholder="Type your reply..." required>
                                    <button type="submit" class="bg-indigo-600 text-white px-4 py-2 rounded-r-md hover:bg-indigo-700">Send</button>
                                </form>
                            </div>
                        </div>
                     </div>
                </div>
                <div id="budgets-view" class="hidden">
                    <h1 class="text-3xl font-bold text-gray-800 mb-6">Customer Budgets</h1>
                    <div class="bg-white p-6 rounded-lg shadow-md">
                        <table class="w-full text-left">
                            <thead>
                                <tr class="bg-gray-50 border-b">
                                    <th class="py-3 px-4">Customer</th>
                                    <th class="py-3 px-4">Monthly Budget</th>
                                    <th class="py-3 px-4">Amount Spent</th>
                                    <th class="py-3 px-4">Status</th>
                                </tr>
                            </thead>
                            <tbody>
                                <!-- Data will be populated by JavaScript -->
                            </tbody>
                        </table>
                    </div>
                </div>
            </main>
        </div>
    </div>
    
    <!-- =========== CUSTOMER DASHBOARD VIEW (Initially Hidden) =========== -->
    <div id="customer-panel" class="hidden">
        <div class="flex flex-col h-screen bg-gray-100">
            <header class="bg-white shadow-md">
                <div class="container mx-auto px-6 py-4 flex justify-between items-center">
                    <h1 id="customer-welcome-title" class="text-2xl font-bold text-gray-800">Customer Dashboard</h1>
                    <button id="customer-logout-btn" class="bg-red-500 text-white px-4 py-2 rounded-md hover:bg-red-600">Logout</button>
                </div>
            </header>
            <main class="flex-1 p-6 lg:p-10 grid grid-cols-1 lg:grid-cols-3 gap-8">
                <div class="lg:col-span-2 bg-white p-6 rounded-lg shadow-md">
                    <h2 class="text-2xl font-bold text-gray-800 mb-6">Project Progress</h2>
                    <div id="customer-progress-container" class="space-y-6">
                       <!-- Dynamic progress bars will be inserted here -->
                    </div>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mt-8">
                        <div class="bg-gray-50 p-4 rounded-lg text-center">
                            <h3 class="text-lg font-semibold text-gray-600">Keyword Rankings</h3>
                            <p class="text-4xl font-bold text-gray-800 mt-2">+15</p>
                            <p class="text-sm text-gray-500">since last week</p>
                        </div>
                         <div class="bg-gray-50 p-4 rounded-lg text-center">
                            <h3 class="text-lg font-semibold text-gray-600">Ad Clicks</h3>
                            <p class="text-4xl font-bold text-gray-800 mt-2">1,204</p>
                            <p class="text-sm text-gray-500">this month</p>
                        </div>
                    </div>
                </div>
                <div class="bg-white rounded-lg shadow-md flex flex-col">
                    <h2 class="text-2xl font-bold text-gray-800 p-6 border-b">Direct Chat with Admin</h2>
                    <div id="chat-box" class="flex-1 p-6 space-y-4 overflow-y-auto">
                       <!-- Chat messages will be dynamically inserted here -->
                    </div>
                    <form id="customer-chat-form" class="p-4 border-t flex items-center">
                        <input type="text" id="chat-message-input" class="w-full px-4 py-2 border rounded-l-md focus:outline-none focus:ring-2 focus:ring-indigo-500" placeholder="Type your message..." required>
                        <button type="submit" class="bg-indigo-600 text-white px-4 py-2 rounded-r-md hover:bg-indigo-700">
                            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 5l7 7-7 7M5 5l7 7-7 7"></path></svg>
                        </button>
                    </form>
                </div>
            </main>
        </div>
    </div>


    <!-- DYNAMIC LOGIN PAGE -->
    <div id="login-page" class="hidden">
        <div class="min-h-screen flex items-center justify-center login-bg">
            <div class="absolute inset-0 bg-black opacity-50"></div>
            <div class="relative w-full max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-2 bg-white shadow-2xl rounded-lg overflow-hidden">
                <div class="p-8 md:p-12 text-gray-800">
                    <a href="#" id="back-to-website-link" class="text-sm text-indigo-600 hover:underline">&larr; Back to Website</a>
                    <h2 id="login-title" class="text-3xl font-bold mt-6">Sign In</h2>
                    <form id="login-form" class="mt-8 space-y-6">
                         <div>
                            <label for="email" class="block text-sm font-medium text-gray-700">Email Address</label>
                            <input type="email" id="email" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500" required>
                        </div>
                        <div>
                            <label for="password" class="block text-sm font-medium text-gray-700">Password</label>
                            <input type="password" id="password" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500" required>
                        </div>
                        <div class="flex items-center justify-between">
                            <div class="flex items-center">
                                <input id="remember-me" name="remember-me" type="checkbox" class="h-4 w-4 text-indigo-600 focus:ring-indigo-500 border-gray-300 rounded">
                                <label for="remember-me" class="ml-2 block text-sm text-gray-900">Remember me</label>
                            </div>
                            <div class="text-sm">
                                <a href="#" class="font-medium text-indigo-600 hover:text-indigo-500">Forgot your password?</a>
                            </div>
                        </div>
                        <div>
                            <button type="submit" class="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">Sign in now</button>
                        </div>
                         <p id="error-message" class="text-red-500 text-sm text-center hidden">Invalid email or password. Please try again.</p>
                    </form>
                </div>
                <div class="p-12 text-white bg-gray-900 bg-opacity-50 flex flex-col justify-center">
                    <h1 class="text-4xl font-extrabold">Welcome Back</h1>
                    <p class="mt-4 text-gray-300">It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.</p>
                     <div class="mt-8 flex space-x-4">
                        <a href="#" class="text-gray-300 hover:text-white"><svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M22.46,6C21.69,6.35 20.86,6.58 20,6.69C20.88,6.16 21.56,5.32 21.88,4.31C21.05,4.81 20.13,5.16 19.16,5.36C18.37,4.5 17.26,4 16,4C13.65,4 11.73,5.92 11.73,8.29C11.73,8.63 11.77,8.96 11.84,9.27C8.28,9.09 5.11,7.38 3,4.79C2.63,5.42 2.42,6.16 2.42,6.94C2.42,8.43 3.17,9.75 4.33,10.5C3.62,10.5 2.96,10.3 2.38,10C2.38,10 2.38,10 2.38,10.03C2.38,12.11 3.86,13.85 5.82,14.24C5.46,14.34 5.08,14.39 4.69,14.39C4.42,14.39 4.15,14.36 3.89,14.31C4.43,16.03 5.99,17.26 7.89,17.29C6.43,18.45 4.58,19.13 2.56,19.13C2.22,19.13 1.88,19.11 1.54,19.07C3.44,20.29 5.7,21 8.12,21C16,21 20.33,14.46 20.33,8.79C20.33,8.6 20.33,8.42 20.32,8.23C21.16,7.63 21.88,6.87 22.46,6Z"></path></svg></a>
                        <a href="#" class="text-gray-300 hover:text-white"><svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M12,2.04C6.5,2.04 2,6.53 2,12.06C2,17.06 5.66,21.21 10.44,21.96V14.96H7.9V12.06H10.44V9.85C10.44,7.32 11.93,5.96 14.22,5.96C15.31,5.96 16.45,6.15 16.45,6.15V8.62H15.19C13.95,8.62 13.56,9.39 13.56,10.18V12.06H16.34L15.89,14.96H13.56V21.96C18.34,21.21 22,17.06 22,12.06C22,6.53 17.5,2.04 12,2.04Z"></path></svg></a>
                     </div>
                </div>
            </div>
        </div>
    </div>


    <!-- FLOATING EDIT BAR (Initially Hidden) -->
    <div id="edit-mode-bar" class="hidden fixed bottom-5 right-5 z-50 bg-gray-800 text-white p-4 rounded-lg shadow-lg flex items-center gap-4">
        <span class="font-bold">Edit Mode Enabled</span>
        <div id="save-notification" class="hidden absolute -top-10 right-0 bg-green-500 text-white px-3 py-1 rounded-md">Changes Saved!</div>
        <button id="save-changes-btn" class="bg-green-500 hover:bg-green-600 px-4 py-2 rounded-md">Save Changes</button>
        <button id="exit-edit-mode-btn" class="bg-red-500 hover:bg-red-600 px-4 py-2 rounded-md">Exit Edit Mode</button>
    </div>


    <script>
        document.addEventListener('DOMContentLoaded', function () {
            // State
            let currentLoggedInCustomer = null;
            let currentAdminChatTarget = null;
            let currentProjectCustomer = null;

            // Views
            const mainWebsiteView = document.getElementById('main-website');
            const adminPanelView = document.getElementById('admin-panel');
            const customerPanelView = document.getElementById('customer-panel');
            const editModeBar = document.getElementById('edit-mode-bar');
            const loginPageView = document.getElementById('login-page');

            // Login Page elements
            const backToWebsiteLink = document.getElementById('back-to-website-link');
            const loginTitle = document.getElementById('login-title');
            const adminLoginLink = document.getElementById('admin-login-link');
            const customerLoginLink = document.getElementById('customer-login-link');
            const loginDropdownBtn = document.getElementById('login-dropdown-btn');
            const loginDropdownMenu = document.getElementById('login-dropdown-menu');

            // Form elements
            const loginForm = document.getElementById('login-form');
            const emailInput = document.getElementById('email');
            const passwordInput = document.getElementById('password');
            const errorMessage = document.getElementById('error-message');
            const customerContactForm = document.getElementById('customer-contact-form');
            const contactSuccessMessage = document.getElementById('contact-success-message');
            const createCustomerForm = document.getElementById('create-customer-form');

            // Admin Panel Elements
            const adminLogoutBtn = document.getElementById('logout-btn');
            const editWebsiteLink = document.getElementById('edit-website-link');
            const usersTableBody = document.querySelector('#users-view table tbody');
            const budgetsTableBody = document.querySelector('#budgets-view table tbody');
            const messagesCountEl = document.querySelector('#messages-card p');
            const budgetsCountEl = document.querySelector('#budgets-card p');
            const adminChatUserList = document.getElementById('admin-chat-user-list');
            const adminChatBox = document.getElementById('admin-chat-box');
            const adminChatForm = document.getElementById('admin-chat-form');
            const adminChatInput = document.getElementById('admin-chat-input');
            const adminChatWithName = document.getElementById('admin-chat-with-name');
            const adminChatPlaceholder = document.getElementById('admin-chat-placeholder');
            const adminChatArea = document.getElementById('admin-chat-area');
            const projectCustomerList = document.getElementById('project-customer-list');
            const projectDetailsPlaceholder = document.getElementById('project-details-placeholder');
            const projectDetailsArea = document.getElementById('project-details-area');
            const projectCustomerName = document.getElementById('project-customer-name');
            const projectTasksList = document.getElementById('project-tasks-list');
            const addTaskForm = document.getElementById('add-task-form');


            // Customer Panel Elements
            const customerLogoutBtn = document.getElementById('customer-logout-btn');
            const customerWelcomeTitle = document.getElementById('customer-welcome-title');
            const chatBox = document.getElementById('chat-box');
            const customerChatForm = document.getElementById('customer-chat-form');
            const chatMessageInput = document.getElementById('chat-message-input');
            const customerProgressContainer = document.getElementById('customer-progress-container');
            
            // Edit Mode Elements
            const saveChangesBtn = document.getElementById('save-changes-btn');
            const exitEditModeBtn = document.getElementById('exit-edit-mode-btn');
            const saveNotification = document.getElementById('save-notification');
            const editableTextElements = document.querySelectorAll('[data-editable]');
            const editableImageElements = document.querySelectorAll('[data-editable-img]');

            // --- LOCAL STORAGE FUNCTIONS ---
            function saveChanges() {
                editableTextElements.forEach(el => localStorage.setItem(el.id, el.innerHTML));
                editableImageElements.forEach(el => localStorage.setItem(el.id, el.src));

                saveNotification.classList.remove('hidden');
                setTimeout(() => saveNotification.classList.add('hidden'), 2000);
            }

            function loadChanges() {
                 editableTextElements.forEach(el => {
                    const savedContent = localStorage.getItem(el.id);
                    if (savedContent) el.innerHTML = savedContent;
                });
                editableImageElements.forEach(el => {
                    const savedSrc = localStorage.getItem(el.id);
                    if (savedSrc) el.src = savedSrc;
                });
            }

            // --- Function to render admin data ---
            function renderAdminData() {
                const submissions = JSON.parse(localStorage.getItem('customerSubmissions')) || [];
                const customers = JSON.parse(localStorage.getItem('customerAccounts')) || [];
                
                messagesCountEl.textContent = submissions.length;
                budgetsCountEl.textContent = `${submissions.length} Active`;

                usersTableBody.innerHTML = '';
                budgetsTableBody.innerHTML = '';
                
                if (customers.length === 0 && submissions.length === 0) {
                     usersTableBody.innerHTML = `<tr><td colspan="4" class="text-center py-4 text-gray-500">No users found.</td></tr>`;
                }

                customers.forEach(user => {
                     const userRow = `
                        <tr class="border-b">
                            <td class="py-3 px-4">${user.name}</td>
                            <td class="py-3 px-4">${user.email}</td>
                            <td class="py-3 px-4"><span class="bg-green-100 text-green-800 text-xs font-medium px-2 py-1 rounded-full">Registered User</span></td>
                            <td class="py-3 px-4"><button data-email="${user.email}" class="chat-with-user-btn text-indigo-600 hover:underline text-sm">Chat</button></td>
                        </tr>`;
                    usersTableBody.insertAdjacentHTML('beforeend', userRow);
                });

                submissions.forEach(sub => {
                    const userRow = `
                        <tr class="border-b">
                            <td class="py-3 px-4">${sub.name}</td>
                            <td class="py-3 px-4">${sub.email}</td>
                            <td class="py-3 px-4"><span class="bg-yellow-100 text-yellow-800 text-xs font-medium px-2 py-1 rounded-full">Applicant</span></td>
                            <td class="py-3 px-4"><button class="text-gray-400 text-sm cursor-not-allowed">N/A</button></td>
                        </tr>`;
                    usersTableBody.insertAdjacentHTML('beforeend', userRow);

                    const budgetRow = `
                        <tr class="border-b">
                            <td class="py-3 px-4">${sub.name}</td>
                            <td class="py-3 px-4">₹${parseInt(sub.budget).toLocaleString('en-IN')}</td>
                            <td class="py-3 px-4">₹0</td>
                            <td class="py-3 px-4"><span class="bg-blue-100 text-blue-800 text-xs font-medium px-2 py-1 rounded-full">New</span></td>
                        </tr>`;
                    budgetsTableBody.insertAdjacentHTML('beforeend', budgetRow);
                });

                document.querySelectorAll('.chat-with-user-btn').forEach(button => {
                    button.addEventListener('click', (e) => {
                        const userEmail = e.currentTarget.dataset.email;
                        showAdminView('chat');
                        openAdminChatFor(userEmail);
                    });
                });
            }
            
            // --- EDIT MODE TOGGLE ---
            function handleImageClick(event) {
                const imageElement = event.currentTarget;
                const newSrc = prompt("Nayi image ka URL daalein:", imageElement.src);
                if (newSrc && newSrc.trim() !== '') imageElement.src = newSrc;
            }

            function toggleEditMode(enable) {
                document.body.classList.toggle('edit-mode-active', enable);
                mainWebsiteView.classList.toggle('hidden', !enable);
                adminPanelView.classList.toggle('hidden', enable);
                customerPanelView.classList.add('hidden');
                editModeBar.classList.toggle('hidden', !enable);

                editableTextElements.forEach(el => {
                    el.contentEditable = enable;
                    el.classList.toggle('editable-content', enable);
                });

                if (enable) {
                    editableImageElements.forEach(img => {
                        if (!img.parentElement.classList.contains('editable-image-container')) {
                            const wrapper = document.createElement('div');
                            wrapper.className = 'editable-image-container';
                            if(img.classList.contains('rounded-full')) wrapper.classList.add('rounded-full');
                            img.parentNode.insertBefore(wrapper, img);
                            wrapper.appendChild(img);
                        }
                        img.parentElement.addEventListener('click', () => handleImageClick({currentTarget: img}));
                    });
                }
            }

            loadChanges();

            function showLoginPage(type) {
                loginForm.dataset.loginType = type;
                loginTitle.textContent = type === 'admin' ? 'Admin Sign In' : 'Customer Sign In';
                mainWebsiteView.classList.add('hidden');
                adminPanelView.classList.add('hidden');
                customerPanelView.classList.add('hidden');
                loginPageView.classList.remove('hidden');
            }

             function hideLoginPage() {
                loginPageView.classList.add('hidden');
                mainWebsiteView.classList.remove('hidden');
            }
            
            adminLoginLink.addEventListener('click', (e) => {
                e.preventDefault();
                showLoginPage('admin');
                loginDropdownMenu.classList.add('hidden');
            });

            customerLoginLink.addEventListener('click', (e) => {
                e.preventDefault();
                showLoginPage('customer');
                loginDropdownMenu.classList.add('hidden');
            });
            
             // NEW LOGIN DROPDOWN LOGIC
            loginDropdownBtn.addEventListener('click', (e) => {
                e.stopPropagation();
                loginDropdownMenu.classList.toggle('hidden');
            });

            window.addEventListener('click', (e) => {
                if (!loginDropdownBtn.contains(e.target)) {
                    loginDropdownMenu.classList.add('hidden');
                }
            });

            backToWebsiteLink.addEventListener('click', (e) => {
                e.preventDefault();
                hideLoginPage();
            });

            // Universal Login Logic
            loginForm.addEventListener('submit', function (e) {
                e.preventDefault();
                const type = loginForm.dataset.loginType;
                const email = emailInput.value;
                const password = passwordInput.value;
                let loginSuccess = false;

                if (type === 'admin') {
                    if (email === 'deepaksinghrt2@gmail.com' && password === 'Anshika@123') {
                        loginPageView.classList.add('hidden');
                        adminPanelView.classList.remove('hidden');
                        renderAdminData();
                        loginSuccess = true;
                    }
                } else { // Customer Login
                    const customers = JSON.parse(localStorage.getItem('customerAccounts')) || [];
                    const foundCustomer = customers.find(c => c.email === email && c.password === password);
                    if (foundCustomer) {
                        currentLoggedInCustomer = foundCustomer;
                        loginPageView.classList.add('hidden');
                        customerPanelView.classList.remove('hidden');
                        customerWelcomeTitle.textContent = `Welcome, ${foundCustomer.name}`;
                        renderCustomerProjectProgress();
                        renderCustomerChat();
                        loginSuccess = true;
                    }
                }
                
                if (loginSuccess) {
                    errorMessage.classList.add('hidden');
                    loginForm.reset();
                } else {
                    errorMessage.classList.remove('hidden');
                }
            });
            
            customerContactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                const submissions = JSON.parse(localStorage.getItem('customerSubmissions')) || [];
                const newSubmission = {
                    name: document.getElementById('customer-name').value,
                    email: document.getElementById('customer-email').value,
                    website: document.getElementById('customer-website').value,
                    budget: document.getElementById('customer-budget').value,
                    service: document.getElementById('customer-service').value,
                    message: document.getElementById('customer-message').value,
                    date: new Date().toLocaleDateString('en-IN', { day: '2-digit', month: '2-digit', year: 'numeric'})
                };
                submissions.push(newSubmission);
                localStorage.setItem('customerSubmissions', JSON.stringify(submissions));
                customerContactForm.classList.add('hidden');
                contactSuccessMessage.classList.remove('hidden');
            });
            
            createCustomerForm.addEventListener('submit', function(e) {
                e.preventDefault();
                const customers = JSON.parse(localStorage.getItem('customerAccounts')) || [];
                 const projects = JSON.parse(localStorage.getItem('projectData')) || {};
                const newCustomer = {
                    name: document.getElementById('new-customer-name').value,
                    email: document.getElementById('new-customer-email').value,
                    password: document.getElementById('new-customer-password').value,
                };
                customers.push(newCustomer);
                 // Initialize project data for the new customer
                if (!projects[newCustomer.email]) {
                    projects[newCustomer.email] = {
                        tasks: [
                            { name: "SEO Keyword Ranking", progress: 10 },
                            { name: "PPC Ad Campaign Setup", progress: 25 },
                        ]
                    };
                }
                localStorage.setItem('customerAccounts', JSON.stringify(customers));
                localStorage.setItem('projectData', JSON.stringify(projects));
                alert('Customer account created successfully!');
                createCustomerForm.reset();
                renderAdminData();
            });

            // Universal Logout logic
            function performLogout() {
                if (document.body.classList.contains('edit-mode-active')) toggleEditMode(false);
                
                adminPanelView.classList.add('hidden');
                customerPanelView.classList.add('hidden');
                loginPageView.classList.add('hidden');
                mainWebsiteView.classList.remove('hidden');
                currentLoggedInCustomer = null;
                currentAdminChatTarget = null;
                currentProjectCustomer = null;
            }

            adminLogoutBtn.addEventListener('click', performLogout);
            customerLogoutBtn.addEventListener('click', performLogout);
            
            // Edit mode event listeners
            editWebsiteLink.addEventListener('click', (e) => {
                e.preventDefault();
                toggleEditMode(true);
            });
            saveChangesBtn.addEventListener('click', saveChanges);
            exitEditModeBtn.addEventListener('click', () => {
                toggleEditMode(false);
                renderAdminData();
            });
            
            // --- CHAT LOGIC ---
            function getChatHistory() {
                return JSON.parse(localStorage.getItem('chatHistory')) || {};
            }

            function saveChatHistory(history) {
                localStorage.setItem('chatHistory', JSON.stringify(history));
            }

            function renderCustomerChat() {
                chatBox.innerHTML = '';
                const history = getChatHistory();
                const userChat = history[currentLoggedInCustomer.email] || [];
                userChat.forEach(msg => {
                    const bubble = document.createElement('div');
                    bubble.textContent = msg.text;
                    bubble.className = `p-3 max-w-xs ${msg.sender === 'customer' ? 'chat-bubble-sent self-end' : 'chat-bubble-received self-start'}`;
                    chatBox.appendChild(bubble);
                });
                chatBox.scrollTop = chatBox.scrollHeight;
            }
            
            customerChatForm.addEventListener('submit', function(e) {
                e.preventDefault();
                const text = chatMessageInput.value;
                if (!text.trim()) return;

                const history = getChatHistory();
                if (!history[currentLoggedInCustomer.email]) {
                    history[currentLoggedInCustomer.email] = [];
                }
                history[currentLoggedInCustomer.email].push({ sender: 'customer', text: text, timestamp: new Date() });
                saveChatHistory(history);
                renderCustomerChat();
                chatMessageInput.value = '';
            });

            function renderAdminChatUserList() {
                adminChatUserList.innerHTML = '';
                const history = getChatHistory();
                const customers = JSON.parse(localStorage.getItem('customerAccounts')) || [];
                
                Object.keys(history).forEach(email => {
                    const customer = customers.find(c => c.email === email);
                    const userName = customer ? customer.name : email;
                    const listItem = document.createElement('li');
                    listItem.innerHTML = `<button data-email="${email}" class="chat-user-list-item w-full text-left p-4 hover:bg-gray-700">${userName}</button>`;
                    adminChatUserList.appendChild(listItem);
                });
            }

            function openAdminChatFor(email) {
                currentAdminChatTarget = email;
                const customers = JSON.parse(localStorage.getItem('customerAccounts')) || [];
                const customer = customers.find(c => c.email === email);
                adminChatWithName.textContent = customer ? customer.name : email;

                adminChatBox.innerHTML = '';
                const history = getChatHistory();
                const userChat = history[email] || [];
                userChat.forEach(msg => {
                    const bubble = document.createElement('div');
                    bubble.textContent = msg.text;
                    bubble.className = `p-3 max-w-xs ${msg.sender === 'admin' ? 'chat-bubble-sent self-end' : 'chat-bubble-received self-start'}`;
                    adminChatBox.appendChild(bubble);
                });
                adminChatBox.scrollTop = adminChatBox.scrollHeight;

                adminChatPlaceholder.classList.add('hidden');
                adminChatArea.classList.remove('hidden');
            }
            
             adminChatUserList.addEventListener('click', (e) => {
                if (e.target.matches('.chat-user-list-item, .chat-user-list-item *')) {
                    const button = e.target.closest('.chat-user-list-item');
                    openAdminChatFor(button.dataset.email);
                }
            });

            adminChatForm.addEventListener('submit', function(e){
                e.preventDefault();
                const text = adminChatInput.value;
                if (!text.trim() || !currentAdminChatTarget) return;

                const history = getChatHistory();
                if (!history[currentAdminChatTarget]) {
                    history[currentAdminChatTarget] = [];
                }
                history[currentAdminChatTarget].push({ sender: 'admin', text: text, timestamp: new Date() });
                saveChatHistory(history);
                openAdminChatFor(currentAdminChatTarget); // Re-render chat for current user
                adminChatInput.value = '';
            });
            
            // --- PROJECT MANAGEMENT LOGIC ---
            function renderProjectCustomerList() {
                projectCustomerList.innerHTML = '';
                const customers = JSON.parse(localStorage.getItem('customerAccounts')) || [];
                customers.forEach(customer => {
                    const listItem = document.createElement('li');
                    listItem.innerHTML = `<button data-email="${customer.email}" class="project-customer-list-item w-full text-left p-4 hover:bg-gray-100">${customer.name}</button>`;
                    projectCustomerList.appendChild(listItem);
                });
            }

            function openProjectDetailsFor(email) {
                currentProjectCustomer = email;
                const customers = JSON.parse(localStorage.getItem('customerAccounts')) || [];
                const customer = customers.find(c => c.email === email);
                projectCustomerName.textContent = `Project for: ${customer.name}`;
                
                renderProjectTasks(email);

                projectDetailsPlaceholder.classList.add('hidden');
                projectDetailsArea.classList.remove('hidden');
            }

            function renderProjectTasks(email) {
                projectTasksList.innerHTML = '';
                const projects = JSON.parse(localStorage.getItem('projectData')) || {};
                const customerProject = projects[email] || { tasks: [] };

                if (customerProject.tasks.length === 0) {
                     projectTasksList.innerHTML = `<div class="text-gray-500 p-4">No tasks assigned yet.</div>`;
                }

                customerProject.tasks.forEach((task, index) => {
                    const taskElement = document.createElement('div');
                    taskElement.className = 'flex items-center gap-4 p-2 bg-gray-50 rounded';
                    taskElement.innerHTML = `
                        <span class="flex-grow font-medium">${task.name}</span>
                        <input type="number" value="${task.progress}" min="0" max="100" data-task-index="${index}" class="task-progress-input w-20 text-center border rounded">
                        <span>%</span>
                    `;
                    projectTasksList.appendChild(taskElement);
                });

                // Add save button at the end
                const saveBtn = document.createElement('button');
                saveBtn.id = 'save-progress-btn';
                saveBtn.className = 'mt-4 bg-indigo-600 text-white px-4 py-2 rounded-md hover:bg-indigo-700';
                saveBtn.textContent = 'Save Progress';
                projectTasksList.appendChild(saveBtn);
                
                document.getElementById('save-progress-btn').addEventListener('click', saveProjectProgress);
            }

            function saveProjectProgress() {
                const projects = JSON.parse(localStorage.getItem('projectData')) || {};
                const inputs = document.querySelectorAll('.task-progress-input');
                inputs.forEach(input => {
                    const taskIndex = parseInt(input.dataset.taskIndex);
                    const newProgress = parseInt(input.value);
                    projects[currentProjectCustomer].tasks[taskIndex].progress = newProgress;
                });
                localStorage.setItem('projectData', JSON.stringify(projects));
                alert('Progress saved!');
            }

            projectCustomerList.addEventListener('click', (e) => {
                if(e.target.matches('.project-customer-list-item')) {
                    openProjectDetailsFor(e.target.dataset.email);
                }
            });

            addTaskForm.addEventListener('submit', (e) => {
                e.preventDefault();
                if (!currentProjectCustomer) return;

                const projects = JSON.parse(localStorage.getItem('projectData')) || {};
                const taskName = document.getElementById('new-task-name').value;
                const taskProgress = document.getElementById('new-task-progress').value;
                
                projects[currentProjectCustomer].tasks.push({ name: taskName, progress: parseInt(taskProgress) });
                localStorage.setItem('projectData', JSON.stringify(projects));
                
                renderProjectTasks(currentProjectCustomer);
                addTaskForm.reset();
            });
            
            // --- RENDER CUSTOMER'S PROJECT PROGRESS ---
            function renderCustomerProjectProgress() {
                customerProgressContainer.innerHTML = '';
                const projects = JSON.parse(localStorage.getItem('projectData')) || {};
                const project = projects[currentLoggedInCustomer.email];

                if (!project || project.tasks.length === 0) {
                    customerProgressContainer.innerHTML = `<p class="text-gray-600">Your project tasks will appear here once assigned.</p>`;
                    return;
                }
                
                const colors = ['indigo', 'green', 'blue', 'purple', 'pink'];
                project.tasks.forEach((task, index) => {
                    const color = colors[index % colors.length];
                    const progressEl = document.createElement('div');
                    progressEl.innerHTML = `
                        <div class="flex justify-between mb-1">
                            <span class="text-base font-medium text-${color}-700">${task.name}</span>
                            <span class="text-sm font-medium text-${color}-700">${task.progress}%</span>
                        </div>
                        <div class="w-full bg-gray-200 rounded-full h-4">
                            <div class="bg-${color}-600 h-4 rounded-full" style="width: ${task.progress}%"></div>
                        </div>`;
                    customerProgressContainer.appendChild(progressEl);
                });
            }

            // --- Admin Panel Internal Script ---
            const links = {
                dashboard: document.getElementById('dashboard-link'),
                users: document.getElementById('users-link'),
                projects: document.getElementById('projects-link'),
                chat: document.getElementById('chat-link'),
                budgets: document.getElementById('budgets-link'),
            };
            const cards = {
                messages: document.getElementById('messages-card'),
                portfolio: document.getElementById('portfolio-card'),
                budgets: document.getElementById('budgets-card')
            };
            const quickActionButtons = {
                'projects': document.getElementById('view-projects-btn'),
                'users': document.getElementById('view-users-btn'),
                'website': document.getElementById('view-website-btn')
            };
            const adminViews = {
                dashboard: document.getElementById('dashboard-view'),
                users: document.getElementById('users-view'),
                projects: document.getElementById('projects-view'),
                chat: document.getElementById('chat-view'),
                budgets: document.getElementById('budgets-view'),
            };
            const allSidebarLinks = document.querySelectorAll('.sidebar-link');

            function showAdminView(viewToShow) {
                Object.values(adminViews).forEach(view => view.classList.add('hidden'));
                if (adminViews[viewToShow]) adminViews[viewToShow].classList.remove('hidden');
                
                allSidebarLinks.forEach(link => link.classList.remove('active'));
                if (links[viewToShow]) links[viewToShow].classList.add('active');
                else links.dashboard.classList.add('active');

                if (viewToShow === 'chat') {
                    renderAdminChatUserList();
                    if (!currentAdminChatTarget) {
                        adminChatPlaceholder.classList.remove('hidden');
                        adminChatArea.classList.add('hidden');
                    }
                }
                if (viewToShow === 'projects') {
                    renderProjectCustomerList();
                    if(!currentProjectCustomer) {
                        projectDetailsPlaceholder.classList.remove('hidden');
                        projectDetailsArea.classList.add('hidden');
                    }
                }
            }

            Object.keys(links).forEach(key => links[key].addEventListener('click', (e) => {
                e.preventDefault();
                showAdminView(key);
            }));

            cards.messages.addEventListener('click', () => showAdminView('users'));
            cards.portfolio.addEventListener('click', () => showAdminView('portfolio'));
            cards.budgets.addEventListener('click', () => showAdminView('budgets'));
            
            quickActionButtons['projects'].addEventListener('click', () => showAdminView('projects'));
            quickActionButtons['users'].addEventListener('click', () => showAdminView('users'));
            quickActionButtons['website'].addEventListener('click', performLogout);

            if (!localStorage.getItem('customerAccounts')) {
                const defaultCustomers = [{name: 'Test Customer', email: 'customer@example.com', password: 'password'}];
                localStorage.setItem('customerAccounts', JSON.stringify(defaultCustomers));
                const defaultProjects = {
                    "customer@example.com": {
                        tasks: [
                            { name: "SEO Keyword Ranking", progress: 75 },
                            { name: "PPC Ad Campaign Setup", progress: 90 },
                            { name: "Social Media Content Plan", progress: 45 }
                        ]
                    }
                };
                 localStorage.setItem('projectData', JSON.stringify(defaultProjects));
            }
        });
    </script>
</body>
</html>


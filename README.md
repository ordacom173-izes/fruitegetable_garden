# fruitegetable_garden
a repository or Fruitegetable VineYard for the sustenance of physical, mental, spiritual souls


<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fruitegetable Garden | Shop Produce & Design Services</title>
<style>
:root {
  --fg-green: #2E7D32;
  --fg-orange: #FF6F00;
  --fg-yellow: #FFC107;
  --fg-light: #F1F8E9;
  --sc-purple: #6A1B9A;
  --sc-pink: #E91E63;
  --sc-blue: #1E88E5;
  --sc-orange: #FF5722;
  --sc-yellow: #FFEB3B;
  --dark: #1a1a;
  --gray-100: #f8f9fa;
  --gray-600: #6c757d;
  --gray-900: #212529;
  --transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  --shadow-sm: 0 2px 8px rgba(0,0,0,0.08);
  --shadow-md: 0 4px 16px rgba(0,0,0,0.12);
  --shadow-lg: 0 8px 32px rgba(0,0,0,0.16);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: Poppins, Arial, sans-serif;
  color: var(--gray-900);
  background: #fff;
  line-height: 1.6;
  overflow-x: hidden;
}

.container {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 1.5rem;
}

/* Header */
header {
  position: sticky;
  top: 0;
  z-index: 1000;
  background: rgba(255,255,0.95);
  backdrop-filter: blur(12px);
  box-shadow: var(--shadow-sm);
  transition: var(--transition);
}

.header-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 0;
}

.logo-wrap {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.logo-wrap img {
  height: 50px;
  width: 50px;
  object-fit: contain;
  border-radius: 12px;
}

.brand-name {
  font-size: 1.5rem;
  font-weight: 800;
  background: linear-gradient(135deg, var(--fg-green), var(--fg-orange));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.nav-tabs {
  display: flex;
  gap: 0.5rem;
  background: var(--gray-100);
  padding: 0.4rem;
  border-radius: 50px;
}

.nav-tab {
  padding: 0.6rem 1.5rem;
  border: none;
  background: transparent;
  border-radius: 50px;
  font-family: Poppins, Arial, sans-serif;
  font-weight: 600;
  font-size: 0.95rem;
  cursor: pointer;
  transition: var(--transition);
  color: var(--gray-600);
}

.nav-tab.active {
  background: linear-gradient(135deg, var(--fg-green), var(--fg-orange));
  color: white;
  box-shadow: var(--shadow-sm);
}

.nav-tab[data-tab="design"].active {
  background: linear-gradient(135deg, var(--sc-purple), var(--sc-pink));
}

.mobile-menu-btn {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0.5rem;
}

.mobile-menu-btn svg {
  width: 28px;
  height: 28px;
}

/* Hero Section */
.hero {
  position: relative;
  min-height: 90vh;
  display: flex;
  align-items: center;
  overflow: hidden;
  padding: 4rem 0;
}

.hero-bg {
  position: absolute;
  inset: 0;
  opacity: 0;
  transition: opacity 0.8s ease;
  z-index: -1;
}

.hero-bg.produce {
  background: linear-gradient(135deg, #E8F5E9 0%, #FFF3E0 50%, #FFFDE7 100%);
  opacity: 1;
}

.hero-bg.design {
  background: 
    radial-gradient(circle at 20% 30%, rgba(106,27,154,0.15) 0%, transparent 50%),
    radial-gradient(circle at 80% 70%, rgba(233,30,99,0.15) 0%, transparent 50%),
    radial-gradient(circle at 50% 50%, rgba(30,136,229,0.1) 0%, transparent 50%),
    linear-gradient(135deg, #F3E5F5 0%, #FCE4EC 100%);
}

.hero-bg.design.active {
  opacity: 1;
}

.hero-content {
  position: relative;
  z-index: 2;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  align-items: center;
}

.hero-text h1 {
  font-size: clamp(2.5rem, 5vw, 4rem);
  font-weight: 800;
  line-height: 1.1;
  margin-bottom: 1.5rem;
}

.hero-produce {
  display: block;
}

.hero-design {
  display: none;
}

body.design-mode .hero-produce {
  display: none;
}

body.design-mode .hero-design {
  display: block;
}

.hero-text h1 .highlight-produce {
  background: linear-gradient(135deg, var(--fg-green), var(--fg-orange));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-text h1 .highlight-design {
  background: linear-gradient(135deg, var(--sc-purple), var(--sc-pink), var(--sc-blue));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-text p {
  font-size: 1.15rem;
  color: var(--gray-600);
  margin-bottom: 2rem;
  max-width: 500px;
}

.hero-cta {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.btn {
  padding: 0.9rem 2rem;
  border-radius: 50px;
  font-weight: 600;
  font-size: 1rem;
  cursor: pointer;
  border: none;
  transition: var(--transition);
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
}

.btn-primary {
  background: linear-gradient(135deg, var(--fg-green), var(--fg-orange));
  color: white;
  box-shadow: var(--shadow-md);
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
}

body.design-mode .btn-primary {
  background: linear-gradient(135deg, var(--sc-purple), var(--sc-pink));
}

.btn-secondary {
  background: white;
  color: var(--gray-900);
  box-shadow: var(--shadow-sm);
}

.btn-secondary:hover {
  box-shadow: var(--shadow-md);
}

.hero-image {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero-image img {
  max-width: 100%;
  height: auto;
  border-radius: 24px;
  box-shadow: var(--shadow-lg);
  transition: var(--transition);
}

.hero-splash {
  position: absolute;
  width: 400px;
  height: 400px;
  background: linear-gradient(135deg, var(--sc-purple), var(--sc-pink), var(--sc-blue), var(--sc-yellow));
  border-radius: 30% 70% 30% / 30% 30% 70% 70%;
  filter: blur(60px);
  opacity: 0.3;
  animation: morph 8s ease-in-out infinite;
}

@keyframes morph {
  0%, 100% { border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%; }
 50% { border-radius: 70% 30% 70% / 70% 70% 30% 30%; }
}

/* Tab Content */
.tab-content {
  display: none;
}

.tab-content.active {
  display: block;
  animation: fadeIn 0.5s ease;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Section */
.section {
  padding: 5rem 0;
}

.section-header {
  text-align: center;
  max-width: 700px;
  margin: 0 auto 3.5rem;
}

.section-badge {
  display: inline-block;
  padding: 0.4rem 1.2rem;
  background: var(--gray-100);
  border-radius: 50px;
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--fg-green);
  margin-bottom: 1rem;
  text-transform: uppercase;
  letter-spacing: 1px;
}

body.design-mode .section-badge {
  color: var(--sc-purple);
}

.section-header h2 {
  font-size: clamp(2rem, 4vw, 3rem);
  font-weight: 800;
  margin-bottom: 1rem;
}

.section-header p {
  font-size: 1.1rem;
  color: var(--gray-600);
}

/* Filter Bar */
.filter-bar {
  display: flex;
  gap: 1rem;
  margin-bottom: 2.5rem;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
}

.filter-group {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
}

.filter-btn {
  padding: 0.6rem 1.3rem;
  border: 2px solid var(--gray-100);
  background: white;
  border-radius: 50px;
  font-family: Poppins, Arial, sans-serif;
  font-weight: 600;
  font-size: 0.9rem;
  cursor: pointer;
  transition: var(--transition);
  color: var(--gray-600);
}

.filter-btn.active {
  background: var(--fg-green);
  border-color: var(--fg-green);
  color: white;
}

body.design-mode .filter-btn.active {
  background: var(--sc-purple);
  border-color: var(--sc-purple);
}

.search-input {
  padding: 0.7rem 1.3rem;
  border: 2px solid var(--gray-100);
  border-radius: 50px;
  font-family: Poppins, Arial, sans-serif;
  font-size: 0.95rem;
  min-width: 250px;
  transition: var(--transition);
}

.search-input:focus {
  outline: none;
  border-color: var(--fg-green);
}

body.design-mode .search-input:focus {
  border-color: var(--sc-purple);
}

/* Product Grid */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 2rem;
}

.card {
  background: white;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: var(--shadow-sm);
  transition: var(--transition);
  position: relative;
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-lg);
}

.card-image {
  height: 220px;
  position: relative;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

.card-image svg {
  width: 120px;
  height: 120px;
}

.card-badge {
  position: absolute;
  top: 1rem;
  right: 1rem;
  background: var(--fg-orange);
  color: white;
  padding: 0.3rem 0.8rem;
  border-radius: 50px;
  font-size: 0.75rem;
  font-weight: 700;
}

.card-badge.sale {
  background: #e53935;
  left: 1rem;
  right: auto;
}

.card-badge.bestseller {
  background: var(--fg-yellow);
  color: var(--dark);
}

.card-content {
  padding: 1.5rem;
}

.card-title {
  font-size: 1.25rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.card-desc {
  color: var(--gray-600);
  font-size: 0.95rem;
  margin-bottom: 1.2rem;
}

.card-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.price-wrap {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
}

.price {
  font-size: 1.5rem;
  font-weight: 800;
  color: var(--fg-green);
}

.old-price {
  font-size: 1rem;
  color: var(--gray-600);
  text-decoration: line-through;
}

.btn-sm {
  padding: 0.6rem 1.3rem;
  font-size: 0.9rem;
}

/* Service Cards */
.service-card {
  position: relative;
  padding: 2.5rem 2rem;
  border-radius: 24px;
  color: white;
  overflow: hidden;
  min-height: 320px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.service-card::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, var(--sc-purple), var(--sc-pink));
  z-index: -2;
}

.service-card:nth-child(2)::before {
  background: linear-gradient(135deg, var(--sc-blue), var(--sc-purple));
}

.service-card:nth-child(3)::before {
  background: linear-gradient(135deg, var(--sc-pink), var(--sc-orange));
}

.service-splash {
  position: absolute;
  width: 200px;
  height: 200px;
  border-radius: 50%;
  filter: blur(40px);
  opacity: 0.4;
  z-index: -1;
}

.service-splash:nth-child(1) {
  top: -50px;
  right: -50px;
  background: var(--sc-yellow);
}

.service-splash:nth-child(2) {
  bottom: -50px;
  left: -50px;
  background: var(--sc-blue);
}

.service-icon {
  width: 60px;
  height: 60px;
  background: rgba(255,255,0.2);
  border-radius: 16px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
  backdrop-filter: blur(10px);
}

.service-icon svg {
  width: 32px;
  height: 32px;
  color: white;
}

.service-card h3 {
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

.service-card p {
  opacity: 0.95;
  margin-bottom: 1.5rem;
}

/* Portfolio */
.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 2rem;
}

.portfolio-item {
  position: relative;
  border-radius: 20px;
  overflow: hidden;
  height: 280px;
  cursor: pointer;
  box-shadow: var(--shadow-md);
}

.portfolio-item::before {
  content: '';
  position: absolute;
  inset: 0;
  transition: var(--transition);
}

.portfolio-item:nth-child(1)::before { background: linear-gradient(135deg, #6A1B9A, #E91E63); }
.portfolio-item:nth-child(2)::before { background: linear-gradient(135deg, #1E88E5, #00ACC1); }
.portfolio-item:nth-child(3)::before { background: linear-gradient(135deg, #FF6F00, #FFC107); }
.portfolio-item:nth-child(4)::before { background: linear-gradient(135deg, #E91E63, #FF5722); }
.portfolio-item:nth-child(5)::before { background: linear-gradient(135deg, #2E7D32, #43A047); }
.portfolio-item:nth-child(6)::before { background: linear-gradient(135deg, #5E35B1, #3949AB); }

.portfolio-item svg {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 80px;
  height: 80px;
  color: rgba(255,255,255,0.5);
}

.portfolio-overlay {
  position: absolute;
  inset: 0;
  background: rgba(0,0,0,0.85);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: var(--transition);
  color: white;
  font-weight: 700;
  font-size: 1.2rem;
}

.portfolio-item:hover .portfolio-overlay {
  opacity: 1;
}

/* Testimonials */
.testimonial-slider {
  position: relative;
  max-width: 900px;
  margin: 0 auto;
  overflow: hidden;
}

.testimonial-track {
  display: flex;
  transition: transform 0.5s ease;
}

.testimonial {
  min-width: 100%;
  padding: 3rem;
  background: white;
  border-radius: 24px;
  box-shadow: var(--shadow-md);
  text-align: center;
}

.testimonial-stars {
  color: var(--fg-yellow);
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
}

.testimonial-text {
  font-size: 1.2rem;
  line-height: 1.8;
  color: var(--gray-600);
  margin-bottom: 2rem;
  font-style: italic;
}

.testimonial-author {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
}

.testimonial-avatar {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: linear-gradient(135deg, var(--fg-green), var(--fg-orange));
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-weight: 700;
  font-size: 1.5rem;
}

body.design-mode .testimonial-avatar {
  background: linear-gradient(135deg, var(--sc-purple), var(--sc-pink));
}

.testimonial-info h4 {
  font-size: 1.1rem;
  margin-bottom: 0.2rem;
}

.testimonial-info p {
  color: var(--gray-600);
  font-size: 0.9rem;
}

.slider-controls {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-top: 2rem;
}

.slider-btn {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  border: 2px solid var(--gray-100);
  background: white;
  cursor: pointer;
  transition: var(--transition);
  display: flex;
  align-items: center;
  justify-content: center;
}

.slider-btn:hover {
  background: var(--fg-green);
  border-color: var(--fg-green);
  color: white;
}

body.design-mode .slider-btn:hover {
  background: var(--sc-purple);
  border-color: var(--sc-purple);
}

.slider-dots {
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  margin-top: 1.5rem;
}

.slider-dot {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: var(--gray-100);
  cursor: pointer;
  transition: var(--transition);
}

.slider-dot.active {
  background: var(--fg-green);
  width: 30px;
  border-radius: 6px;
}

body.design-mode .slider-dot.active {
  background: var(--sc-purple);
}

/* Benefits */
.benefits-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2.5rem;
}

.benefit {
  text-align: center;
  padding: 2rem;
}

.benefit-icon {
  width: 80px;
  height: 80px;
  background: linear-gradient(135deg, var(--fg-green), var(--fg-orange));
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1.5rem;
}

body.design-mode .benefit-icon {
  background: linear-gradient(135deg, var(--sc-purple), var(--sc-pink));
}

.benefit-icon svg {
  width: 40px;
  height: 40px;
  color: white;
}

.benefit h3 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.benefit p {
  color: var(--gray-600);
}

/* FAQ */
.faq-list {
  max-width: 900px;
  margin: 0 auto;
}

.faq-item {
  background: white;
  border-radius: 16px;
  margin-bottom: 1rem;
  box-shadow: var(--shadow-sm);
  overflow: hidden;
}

.faq-question {
  padding: 1.5rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  cursor: pointer;
  font-weight: 600;
  font-size: 1.1rem;
  transition: var(--transition);
}

.faq-question:hover {
  background: var(--gray-100);
}

.faq-icon {
  transition: var(--transition);
}

.faq-item.active .faq-icon {
  transform: rotate(180deg);
}

.faq-answer {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease;
}

.faq-answer-content {
  padding: 0 2rem 1.5rem;
  color: var(--gray-600);
  line-height: 1.8;
}

.faq-item.active .faq-answer {
  max-height: 500px;
}

/* Blog */
.blog-card {
  border-radius: 20px;
  overflow: hidden;
  box-shadow: var(--shadow-sm);
  transition: var(--transition);
}

.blog-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-lg);
}

.blog-image {
  height: 200px;
  position: relative;
}

.blog-content {
  padding: 1.5rem;
  background: white;
}

.blog-tag {
  display: inline-block;
  padding: 0.3rem 0.8rem;
  background: var(--gray-100);
  border-radius: 50px;
  font-size: 0.75rem;
  font-weight: 600;
  margin-bottom: 0.8rem;
  color: var(--fg-green);
}

.blog-card h3 {
  font-size: 1.3rem;
  margin-bottom: 0.8rem;
}

.blog-meta {
  font-size: 0.85rem;
  color: var(--gray-600);
}

.load-more-wrap {
  text-align: center;
  margin-top: 3rem;
}

/* Contact Form */
.contact-form {
  max-width: 700px;
  margin: 0 auto;
  background: white;
  padding: 3rem;
  border-radius: 24px;
  box-shadow: var(--shadow-lg);
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 0.9rem 1.3rem;
  border: 2px solid var(--gray-100);
  border-radius: 12px;
  font-family: Poppins, Arial, sans-serif;
  font-size: 1rem;
  transition: var(--transition);
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--fg-green);
}

body.design-mode .form-group input:focus,
body.design-mode .form-group textarea:focus {
  border-color: var(--sc-purple);
}

.form-group textarea {
  min-height: 150px;
  resize: vertical;
}

.form-error {
  color: #e53935;
  font-size: 0.85rem;
  margin-top: 0.3rem;
  display: none;
}

/* Newsletter */
.newsletter {
  background: linear-gradient(135deg, var(--fg-green), var(--fg-orange));
  border-radius: 30px;
  padding: 4rem 3rem;
  color: white;
  text-align: center;
  position: relative;
  overflow: hidden;
}

body.design-mode .newsletter {
  background: linear-gradient(135deg, var(--sc-purple), var(--sc-pink));
}

.newsletter::before {
  content: '';
  position: absolute;
  width: 300px;
  height: 300px;
  background: rgba(255,255,255,0.1);
  border-radius: 50%;
  top: -100px;
  right: -100px;
}

.newsletter h3 {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  position: relative;
}

.newsletter p {
  font-size: 1.1rem;
  opacity: 0.95;
  margin-bottom: 2rem;
  position: relative;
}

.newsletter-form {
  display: flex;
  gap: 1rem;
  max-width: 550px;
  margin: 0 auto;
  position: relative;
}

.newsletter-form input {
  flex: 1;
  padding: 1rem 1.5rem;
  border-radius: 50px;
  border: 2px solid rgba(255,0.3);
  background: rgba(255,255,255,0.2);
  color: white;
  font-family: Poppins, Arial, sans-serif;
  font-size: 1rem;
  backdrop-filter: blur(10px);
}

.newsletter-form input::placeholder {
  color: rgba(255,255,0.8);
}

.newsletter-form input:focus {
  outline: none;
  border-color: white;
}

.newsletter-form button {
  white-space: nowrap;
}

/* Footer */
footer {
  background: var(--dark);
  color: rgba(255,255,255,0.8);
  padding: 4rem 0 2rem;
  margin-top: 5rem;
}

.footer-grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1fr;
  gap: 3rem;
  margin-bottom: 3rem;
}

.footer-brand img {
  height: 50px;
  border-radius: 12px;
  margin-bottom: 1rem;
}

.footer-brand p {
  font-size: 0.95rem;
  line-height: 1.7;
  margin-bottom: 1.5rem;
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-links a {
  width: 40px;
  height: 40px;
  background: rgba(255,255,255,0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: var(--transition);
}

.social-links a:hover {
  background: var(--fg-green);
  transform: translateY(-3px);
}

.footer-col h4 {
  color: white;
  font-size: 1.1rem;
  margin-bottom: 1.2rem;
}

.footer-col ul {
  list-style: none;
}

.footer-col ul li {
  margin-bottom: 0.8rem;
}

.footer-col a {
  color: rgba(255,255,255,0.7);
  text-decoration: none;
  transition: var(--transition);
}

.footer-col a:hover {
  color: var(--fg-orange);
}

.contact-item {
  
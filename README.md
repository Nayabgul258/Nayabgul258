
import { motion } from 'framer-motion';
import { Github, Linkedin, Mail } from 'lucide-react';

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-slate-950 text-white font-[Poppins]">
      {/* Header */}
      <header className="flex justify-between items-center p-6 border-b border-slate-800">
        <h1 className="text-2xl font-bold text-blue-400">NAYAB GUL</h1>
        <nav className="flex gap-6 text-sm">
          <a href="#skills" className="hover:text-blue-400">Skills</a>
          <a href="#projects" className="hover:text-blue-400">Projects</a>
          <a href="#contact" className="hover:text-blue-400">Contact</a>
        </nav>
      </header>

      {/* Hero Section */}
      <section className="flex flex-col justify-center items-center text-center py-24 px-4">
        <motion.h2 initial={{opacity:0, y:20}} animate={{opacity:1, y:0}} transition={{duration:0.6}} className="text-3xl sm:text-5xl font-bold mb-4">
          Full Stack Developer (MERN)
        </motion.h2>
        <p className="max-w-2xl text-slate-400 mb-6">
          Passionate and detail-oriented Full-Stack Developer with experience in building responsive, scalable web applications using React.js, Node.js, Express.js, and MongoDB.
        </p>
        <div className="flex gap-4">
          <a href="https://github.com/" target="_blank" rel="noreferrer" className="p-2 rounded-full border border-slate-700 hover:bg-slate-800">
            <Github />
          </a>
          <a href="https://linkedin.com/" target="_blank" rel="noreferrer" className="p-2 rounded-full border border-slate-700 hover:bg-slate-800">
            <Linkedin />
          </a>
          <a href="mailto:nayabgul258@gmail.com" className="p-2 rounded-full border border-slate-700 hover:bg-slate-800">
            <Mail />
          </a>
        </div>
      </section>

      {/* Skills */}
      <section id="skills" className="py-16 px-6 max-w-5xl mx-auto">
        <h3 className="text-2xl font-semibold mb-6 text-blue-400">Technical Skills</h3>
        <div className="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4 text-slate-300">
          {['React.js','Node.js','Express.js','MongoDB','Tailwind CSS','HTML5','CSS3','JavaScript (ES6+)','REST APIs','Git & GitHub','Postman','Unit Testing'].map(skill => (
            <div key={skill} className="p-3 border border-slate-800 rounded-lg text-center hover:bg-slate-800">{skill}</div>
          ))}
        </div>
      </section>

      {/* Projects */}
      <section id="projects" className="py-16 px-6 bg-slate-900">
        <h3 className="text-2xl font-semibold mb-8 text-blue-400 text-center">Projects</h3>
        <div className="grid sm:grid-cols-2 gap-8 max-w-5xl mx-auto">
          <motion.div whileHover={{scale:1.02}} className="bg-slate-800 p-6 rounded-2xl">
            <h4 className="text-xl font-semibold mb-2">ChatWithAI</h4>
            <p className="text-slate-400 text-sm mb-4">A scalable SPA built with React.js, Node.js, and MongoDB, featuring secure authentication, email service, and optimized performance.</p>
            <a href="https://github.com/" target="_blank" rel="noreferrer" className="text-blue-400 text-sm">View Code →</a>
          </motion.div>

          <motion.div whileHover={{scale:1.02}} className="bg-slate-800 p-6 rounded-2xl">
            <h4 className="text-xl font-semibold mb-2">Learning Management System</h4>
            <p className="text-slate-400 text-sm mb-4">Developed modular components with React Hooks and Tailwind for responsive UI and maintainable, bug-free experience.</p>
            <a href="https://github.com/" target="_blank" rel="noreferrer" className="text-blue-400 text-sm">View Code →</a>
          </motion.div>
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="py-16 px-6 text-center">
        <h3 className="text-2xl font-semibold text-blue-400 mb-4">Let’s Connect</h3>
        <p className="text-slate-400 mb-6">I'm open to collaboration, internship, or full-time roles in MERN development.</p>
        <a href="mailto:nayabgul258@gmail.com" className="px-6 py-3 bg-blue-500 text-white rounded-full hover:bg-blue-600">Send Message</a>
      </section>

      <footer className="text-center py-6 text-slate-500 border-t border-slate-800 text-sm">
        © 2025 Nayab Gul — Built with React & Tailwind
      </footer>
    </div>
  );
}

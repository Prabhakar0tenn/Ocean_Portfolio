// Sticky Navbar
let header = document.querySelector('header');

window.addEventListener('scroll', () => {
    header.classList.toggle('sticky', window.scrollY > 100);
});

// Menu Icon
let menuIcon = document.querySelector('#menu-icon');
let navbar = document.querySelector('.navbar');

menuIcon.onclick = () => {
    menuIcon.classList.toggle('fa-x');
    navbar.classList.toggle('active');
};

// Remove menu when clicking nav links
document.querySelectorAll('header nav a').forEach(link => {
    link.addEventListener('click', () => {
        menuIcon.classList.remove('fa-x');
        navbar.classList.remove('active');
    });
});

// Scroll Sections
let sections = document.querySelectorAll('section');
let navLinks = document.querySelectorAll('header nav a');

window.onscroll = () => {
    sections.forEach(sec => {
        let top = window.scrollY;
        let offset = sec.offsetTop - 100;
        let height = sec.offsetHeight;
        let id = sec.getAttribute('id');
        
        if(top >= offset && top < offset + height) {
            // Active Navbar Links
            navLinks.forEach(links => {
                links.classList.remove('active');
                document.querySelector(`header nav a[href*=${id}]`).classList.add('active');
            });
            
            // Active Sections for Animation on Scroll
            sec.classList.add('show-animate');
        }
        // If want to use animation that repeats on scroll use this
        else {
            sec.classList.remove('show-animate');
        }
    });
    
    // Animation Footer on Scroll
    let footer = document.querySelector('footer');
    footer.classList.toggle('show-animate', this.innerHeight + this.scrollY >= document.scrollingElement.scrollHeight);
};

// Typed JS
const typed = new Typed('.multiple-text', {
    strings: ['Web Developer', 'UI/UX Designer', 'Tech Explorer', 'Creative Coder'],
    typeSpeed: 100,
    backSpeed: 100,
    backDelay: 1000,
    loop: true
});

// Scroll Reveal Animation
ScrollReveal({ 
    reset: true,
    distance: '80px',
    duration: 2000,
    delay: 200
});

ScrollReveal().reveal('.home-content, .heading', { origin: 'top' });
ScrollReveal().reveal('.home-img, .skills-container, .project-box, .contact-container', { origin: 'bottom' });
ScrollReveal().reveal('.home-content h1, .about-img', { origin: 'left' });
ScrollReveal().reveal('.home-content p, .about-content', { origin: 'right' });

// Create random stars for background
function createStars() {
    const space = document.querySelector('.space');
    const starCount = 50;
    
    for (let i = 0; i < starCount; i++) {
        const star = document.createElement('div');
        star.className = 'star';
        
        // Random position
        const x = Math.random() * 100;
        const y = Math.random() * 100;
        
        // Random size
        const size = Math.random() * 3 + 1;
        
        // Random opacity
        const opacity = Math.random() * 0.5 + 0.5;
        
        // Random animation duration
        const duration = Math.random() * 10 + 5;
        
        star.style.left = `${x}%`;
        star.style.top = `${y}%`;
        star.style.width = `${size}px`;
        star.style.height = `${size}px`;
        star.style.opacity = opacity;
        star.style.animation = `twinkle ${duration}s infinite ${Math.random() > 0.5 ? 'alternate' : 'alternate-reverse'}`;
        star.style.borderRadius = '50%';
        star.style.backgroundColor = 'white';
        star.style.boxShadow = `0 0 ${size*2}px white`;
        star.style.position = 'absolute';
        
        space.appendChild(star);
    }
}

// Initialize stars
createStars();
function toggleMenu() {
    const menu = document.querySelector(".menu-links");
    const icon = document.querySelector(".hamburger-icon");
    menu.classList.toggle("open");
    icon.classList.toggle("open");
}



// Smooth scroll to next section on scroll
document.addEventListener('DOMContentLoaded', function() {
    const sections = document.querySelectorAll('section');
    
    window.addEventListener('scroll', function() {
        let currentSection = null;
        
        // Find the current section
        sections.forEach(function(section) {
            const sectionTop = section.offsetTop;
            const sectionBottom = sectionTop + section.offsetHeight;
            const scrollPosition = window.scrollY;
            
            if (scrollPosition >= sectionTop && scrollPosition < sectionBottom) {
                currentSection = section;
            }
        });
        
        // Find the next section
        const nextSection = currentSection.nextElementSibling;
        
        // Scroll to the next section smoothly
        if (nextSection) {
            nextSection.scrollIntoView({ behavior: 'smooth' });
        }
    });
});



document.addEventListener('DOMContentLoaded', () => {
    class Cursor {
      constructor(options) {
        this.targets = options.targets || [];
        this.cursorElement = document.querySelector('[data-cursor]');
        this.init();
      }
  
     init() {
    this.targets.forEach(target => {
      const elements = document.querySelectorAll(target);
      elements.forEach(element => {
        element.addEventListener('mouseenter', () => {
          this.cursorElement.classList.add('cursor-hover');
        });
        element.addEventListener('mouseleave', () => {
          this.cursorElement.classList.remove('cursor-hover');
        });
      });
    });
  
    document.addEventListener('mousemove', (event) => {
      this.moveCursor(event);
    });
  }
  
      moveCursor(event) {
        const x = event.clientX;
        const y = event.clientY;
  
        this.cursorElement.style.left = `${x}px`;
        this.cursorElement.style.top = `${y}px`;
      }
    }
  
    new Cursor({
      targets: ['a']
    });
  });
  
  
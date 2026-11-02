/* =========================================
   DANIELA WAKHU — DEVELOPER PORTFOLIO
   Theme: Dark Cyberpunk / Neon Green
========================================= */

/* 1. CSS VARIABLES */
:root {
    --bg-color: #080c10;
    --secondary-bg: #101820;
    --card-bg: #111b23;
    --accent: #00ff99;
    --accent-hover: #00cc7a;
    --text-color: #f1f5f9;
    --muted-color: #9caab7;
    --border-color: rgba(0, 255, 153, 0.18);
    --transition: 0.3s ease;
}

/* 2. RESET */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 90px;
}

body {
    font-family: "Segoe UI", Arial, sans-serif;
    background: var(--bg-color);
    color: var(--text-color);
    line-height: 1.7;
    overflow-x: hidden;
}

a {
    text-decoration: none;
    color: inherit;
}

ul {
    list-style: none;
}

h1, h2, h3 {
    line-height: 1.2;
}

p {
    color: var(--muted-color);
}

/* 3. NAVIGATION BAR */
header {
    width: 100%;
    position: sticky;
    top: 0;
    z-index: 1000;
    background: rgba(8, 12, 16, 0.92);
    backdrop-filter: blur(15px);
    border-bottom: 1px solid var(--border-color);
}

nav {
    max-width: 1200px;
    margin: auto;
    padding: 18px 6%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 25px;
}

nav h2 {
    font-size: 1.8rem;
    color: var(--accent);
    letter-spacing: 2px;
}

nav ul {
    display: flex;
    align-items: center;
    gap: 28px;
}

nav ul li a {
    color: var(--text-color);
    font-size: 0.95rem;
    transition: var(--transition);
    position: relative;
}

nav ul li a::after {
    content: "";
    position: absolute;
    left: 0;
    bottom: -6px;
    width: 0;
    height: 2px;
    background: var(--accent);
    transition: var(--transition);
}

nav ul li a:hover {
    color: var(--accent);
}

nav ul li a:hover::after {
    width: 100%;
}

/* 4. HERO SECTION */
#hero {
    min-height: 85vh;
    padding: 100px 8%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 60px;
    position: relative;
    isolation: isolate;
    overflow: hidden;
}

#hero::before {
    content: "";
    position: absolute;
    width: 450px;
    height: 450px;
    top: 10%;
    right: -120px;
    background: var(--accent);
    opacity: 0.07;
    filter: blur(130px);
    border-radius: 50%;
    z-index: -1;
}

.hero-text {
    flex: 1;
    max-width: 650px;
    animation: fadeInUp 0.9s ease both;
}

.hero-text h1 {
    font-size: clamp(2.8rem, 6vw, 5rem);
    font-weight: 800;
    letter-spacing: -2px;
    margin-bottom: 15px;
}

.hero-text h2 {
    color: var(--accent);
    font-size: clamp(1.3rem, 3vw, 2rem);
    margin-bottom: 25px;
}

.hero-text p {
    font-size: 1.1rem;
    max-width: 570px;
    margin-bottom: 35px;
    line-height: 1.9;
}

/* HERO BUTTONS */
.hero-text a {
    display: inline-block;
    padding: 13px 25px;
    margin: 0 12px 12px 0;
    border: 1px solid var(--accent);
    border-radius: 6px;
    font-weight: 600;
    transition: var(--transition);
}

.hero-text a:first-of-type {
    background: var(--accent);
    color: #06110c;
}

.hero-text a:first-of-type:hover {
    background: var(--accent-hover);
    box-shadow: 0 0 25px rgba(0, 255, 153, 0.3);
    transform: translateY(-3px);
}

.hero-text a:last-of-type {
    color: var(--accent);
}

.hero-text a:last-of-type:hover {
    background: rgba(0, 255, 153, 0.1);
    transform: translateY(-3px);
}

/* HERO IMAGE PLACEHOLDER */
.hero-image {
    flex: 1;
    max-width: 400px;
    min-height: 400px;
    border: 1px solid var(--border-color);
    border-radius: 20px;
    background:
        radial-gradient(circle at center,
        rgba(0, 255, 153, 0.12), transparent 65%),
        var(--secondary-bg);
    box-shadow: 0 0 50px rgba(0, 255, 153, 0.05);
    position: relative;
    overflow: hidden;
}

.hero-image::after {
    content: "</>";
    position: absolute;
    inset: 0;
    display: grid;
    place-items: center;
    color: var(--accent);
    font-family: Consolas, monospace;
    font-size: 5rem;
    opacity: 0.6;
}

/* 5. GENERAL SECTION STYLING */
main section:not(#hero) {
    padding: 90px 8%;
    max-width: 1400px;
    margin: auto;
}

main section:not(#hero) > h2 {
    font-size: clamp(2rem, 4vw, 2.8rem);
    margin-bottom: 30px;
    position: relative;
    display: inline-block;
}

main section:not(#hero) > h2::after {
    content: "";
    display: block;
    width: 65px;
    height: 4px;
    margin-top: 12px;
    border-radius: 4px;
    background: var(--accent);
}

#about {
    background: var(--secondary-bg);
    border-radius: 16px;
}

#about p {
    max-width: 850px;
    font-size: 1.08rem;
    line-height: 2;
}

/* 6. SKILLS, PROJECTS & DESIGNS */
.skill-container,
.project-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 25px;
    margin-top: 25px;
}

/* Add this class to individual skill or project cards */
.skill-card,
.project-card {
    padding: 28px;
    background: var(--card-bg);
    border: 1px solid var(--border-color);
    border-radius: 12px;
    transition: var(--transition);
}

.skill-card:hover,
.project-card:hover {
    transform: translateY(-7px);
    border-color: var(--accent);
    box-shadow: 0 10px 35px rgba(0, 255, 153, 0.08);
}

.skill-card h3,
.project-card h3 {
    color: var(--accent);
    margin-bottom: 12px;
}

.skill-card p,
.project-card p {
    font-size: 0.95rem;
}

.project-card a {
    display: inline-block;
    color: var(--accent);
    margin-top: 18px;
    font-weight: 600;
}

.project-card a:hover {
    text-decoration: underline;
}

/* 7. EDUCATION & CERTIFICATIONS */
#education,
#certifications,
#learning {
    border-top: 1px solid rgba(255, 255, 255, 0.04);
}

/* 8. CONTACT SECTION */
#contact {
    text-align: center;
    background:
        radial-gradient(ellipse at top,
        rgba(0, 255, 153, 0.06), transparent 65%);
}

#contact > h2::after {
    margin-left: auto;
    margin-right: auto;
}

#contact .project-container {
    justify-content: center;
}

/* 9. FOOTER */
footer {
    text-align: center;
    padding: 28px 6%;
    background: #05080b;
    border-top: 1px solid var(--border-color);
}

footer p {
    font-size: 0.9rem;
}

/* 10. ANIMATIONS */
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(25px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* 11. TABLET RESPONSIVENESS */
@media (max-width: 900px) {
    nav {
        flex-direction: column;
        gap: 15px;
    }

    nav ul {
        justify-content: center;
        flex-wrap: wrap;
        gap: 15px 22px;
    }

    #hero {
        min-height: auto;
        padding: 80px 6%;
        gap: 35px;
    }

    .hero-image {
        min-height: 300px;
    }

    main section:not(#hero) {
        padding: 70px 6%;
    }
}

/* 12. MOBILE RESPONSIVENESS */
@media (max-width: 600px) {
    nav {
        padding: 18px 5%;
    }

    nav h2 {
        font-size: 1.6rem;
    }

    nav ul {
        gap: 12px 16px;
    }

    nav ul li a {
        font-size: 0.85rem;
    }

    #hero {
        flex-direction: column;
        align-items: stretch;
        padding: 70px 6%;
        text-align: center;
    }

    .hero-text p {
        font-size: 1rem;
        margin-left: auto;
        margin-right: auto;
    }

    .hero-text a {
        margin: 5px;
        padding: 12px 17px;
        font-size: 0.9rem;
    }

    .hero-image {
        width: 100%;
        max-width: none;
        min-height: 240px;
    }

    main section:not(#hero) {
        padding: 60px 6%;
    }

    .skill-container,
    .project-container {
        grid-template-columns: 1fr;
    }

    main section:not(#hero) > h2 {
        font-size: 2rem;
    }
}

/* 13. ACCESSIBILITY */
a:focus-visible {
    outline: 2px solid var(--accent);
    outline-offset: 5px;
}

@media (prefers-reduced-motion: reduce) {
    *,
    *::before,
    *::after {
        scroll-behavior: auto !important;
        animation-duration: 0.01ms !important;
        transition-duration: 0.01ms !important;
    }
}

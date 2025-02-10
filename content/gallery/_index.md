---
title: Gallery
description: 
archivesSlug: archives
permalink: /gallery/
---

<!-- ![Alt text](/site/images/nitw.JPG) -->

<div class="gallery-container">
    <div class="gallery-grid">
        <figure class="gallery-item">
            <img 
                src="/site/images/gallery-1.png" 
                alt="Photo 1"
                loading="lazy"
                width="800"
                height="600"
                class="gallery-image"
            >
            <figcaption class="gallery-caption">Photo 1</figcaption>
        </figure>
        <figure class="gallery-item">
            <img 
                src="/site/images/nitw.JPG"
                alt="Photo 2" 
                loading="lazy"
                width="800"
                height="600"
                class="gallery-image"
            >
            <figcaption class="gallery-caption">Photo 2</figcaption>
        </figure>
        <figure class="gallery-item">
            <img 
                src="/site/images/gallery-3.png"
                alt="Photo 3"
                loading="lazy" 
                width="800"
                height="600"
                class="gallery-image"
            >
            <figcaption class="gallery-caption">Photo 3</figcaption>
        </figure>
        <figure class="gallery-item">
            <img 
                src="/site/images/gallery-4.png"
                alt="Photo 4"
                loading="lazy"
                width="800"
                height="600"
                class="gallery-image"
            >
            <figcaption class="gallery-caption">Photo 4</figcaption>
        </figure>
    </div>
</div>

<style>
.gallery-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2rem;
}

.gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

.gallery-item {
    position: relative;
    margin: 0;
    border-radius: 12px;
    overflow: hidden;
    background: #fff;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.gallery-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}

.gallery-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
    aspect-ratio: 4/3;
    transition: transform 0.3s ease;
}

.gallery-caption {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 1rem;
    background: rgba(255,255,255,0.9);
    backdrop-filter: blur(10px);
    color: #333;
    font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, sans-serif;
    font-size: 0.9rem;
    opacity: 0;
    transform: translateY(100%);
    transition: all 0.3s ease;
}

.gallery-item:hover .gallery-caption {
    opacity: 1;
    transform: translateY(0);
}

@media (max-width: 768px) {
    .gallery-grid {
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 1rem;
    }
}
</style>


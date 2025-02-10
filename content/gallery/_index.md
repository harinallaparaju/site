---
title: Gallery
description: 
archivesSlug: archives
permalink: /gallery/
---

<!-- ![Alt text](/site/images/nitw.JPG) -->

<div class="photo-grid">
    <img src="/site/images/gallery-1.png" alt="Photo 1">
    <img src="/site/images/nitw.JPG" alt="Photo 2">
    <img src="/site/images/gallery-3.png" alt="Photo 3">
    <img src="/site/images/gallery-4.png" alt="Photo 4">
    <!-- Add more photos here -->
</div>

<script src="https://unpkg.com/masonry-layout@4/dist/masonry.pkgd.min.js"></script>
<script src="https://unpkg.com/imagesloaded@5/imagesloaded.pkgd.min.js"></script>

<style>
.photo-grid {
    margin: 0 auto;
}

.grid-item {
    width: 300px;
    margin-bottom: 20px;
    break-inside: avoid;
}

.grid-item img {
    display: block;
    width: 100%;
    height: auto;
    border-radius: 8px;
    transition: transform 0.3s ease;
    opacity: 0;
}

.grid-item img.loaded {
    opacity: 1;
}

.grid-item img:hover {
    transform: scale(1.03);
}

@media (max-width: 600px) {
    .grid-item {
        width: calc(50% - 10px);
    }
}
</style>

<div class="photo-grid">
    <div class="grid-item"><img src="/site/images/gallery-1.png" alt="Photo 1" loading="lazy"></div>
    <div class="grid-item"><img src="/site/images/nitw.JPG" alt="Photo 2" loading="lazy"></div>
    <div class="grid-item"><img src="/site/images/gallery-3.png" alt="Photo 3" loading="lazy"></div>
    <div class="grid-item"><img src="/site/images/gallery-4.png" alt="Photo 4" loading="lazy"></div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    var grid = document.querySelector('.photo-grid');
    var msnry = new Masonry(grid, {
        itemSelector: '.grid-item',
        columnWidth: '.grid-item',
        percentPosition: true,
        gutter: 20
    });

    imagesLoaded(grid).on('progress', function(instance, image) {
        image.img.classList.add('loaded');
        msnry.layout();
    });
});
</script>

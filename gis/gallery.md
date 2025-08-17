---
layout: default
title: GIS Gallery
---

<style>
.gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px; padding: 20px; }
.gallery-item { position: relative; cursor: pointer; border-radius: 8px; overflow: hidden; box-shadow: 0 4px 8px rgba(0,0,0,0.1); transition: transform 0.3s ease; }
.gallery-item:hover { transform: scale(1.02); }
.gallery-item img { width: 100%; height: 200px; object-fit: cover; display: block; }
.gallery-item .caption { position: absolute; bottom: 0; left: 0; right: 0; background: linear-gradient(transparent, rgba(0,0,0,0.7)); color: white; padding: 20px 10px 10px; font-size: 14px; text-align: center; }
.lightbox { display: none; position: fixed; z-index: 999; left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0,0,0,0.9); }
.lightbox-content { position: relative; margin: auto; display: block; max-width: 90%; max-height: 90%; margin-top: 50px; }
.close { position: absolute; top: 15px; right: 35px; color: #f1f1f1; font-size: 40px; font-weight: bold; cursor: pointer; }
.close:hover { color: #bbb; }
.lightbox-caption { text-align: center; color: #ccc; padding: 10px 0; height: 150px; }
</style>

# {{ page.title }}

## Fire Management Analysis
<div class="gallery">
<div class="gallery-item" onclick="openLightbox('/assets/gis/AZFires_1_9.png', 'Arizona Fires 2019 - Fire history mapping')">
<img src="/assets/gis/AZFires_1_9.png" alt="Arizona Fires 2019">
<div class="caption">Arizona Fires 2019</div>
</div>
<div class="gallery-item" onclick="openLightbox('/assets/gis/Desert_Fires_3_19.jpg', 'Desert Fires Analysis')">
<img src="/assets/gis/Desert_Fires_3_19.jpg" alt="Desert Fires Analysis">
<div class="caption">Desert Fires Analysis</div>
</div>
<div class="gallery-item" onclick="openLightbox('/assets/gis/Peak_Fires_10_2_24.png', 'Peak Fires Analysis')">
<img src="/assets/gis/Peak_Fires_10_2_24.png" alt="Peak Fires Analysis">
<div class="caption">Peak Fires Analysis</div>
</div>
</div>

## Vegetation Analysis
<div class="gallery">
<div class="gallery-item" onclick="openLightbox('/assets/gis/Annual_grasses_S1.jpg', 'Annual Grasses - Seasonal distribution')">
<img src="/assets/gis/Annual_grasses_S1.jpg" alt="Annual Grasses">
<div class="caption">Annual Grasses</div>
</div>
<div class="gallery-item" onclick="openLightbox('/assets/gis/Annual_herbs_S2.jpg', 'Annual Herbs - Species mapping')">
<img src="/assets/gis/Annual_herbs_S2.jpg" alt="Annual Herbs">
<div class="caption">Annual Herbs</div>
</div>
<div class="gallery-item" onclick="openLightbox('/assets/gis/Perennial_bunch_grassess_S3.jpg', 'Perennial Bunch Grasses')">
<img src="/assets/gis/Perennial_bunch_grassess_S3.jpg" alt="Perennial Bunch Grasses">
<div class="caption">Perennial Bunch Grasses</div>
</div>
<div class="gallery-item" onclick="openLightbox('/assets/gis/Grassland_5_11.png', 'Grassland Distribution')">
<img src="/assets/gis/Grassland_5_11.png" alt="Grassland Distribution">
<div class="caption">Grassland Distribution</div>
</div>
</div>

## Geographic Mapping
<div class="gallery">
<div class="gallery-item" onclick="openLightbox('/assets/gis/CFFC_Directions_Map_8_23_24.png', 'CFFC Directions Map')">
<img src="/assets/gis/CFFC_Directions_Map_8_23_24.png" alt="CFFC Directions Map">
<div class="caption">CFFC Directions</div>
</div>
<div class="gallery-item" onclick="openLightbox('/assets/gis/AZWL_AOF_7_3_24.png', 'Arizona Wildland Interface')">
<img src="/assets/gis/AZWL_AOF_7_3_24.png" alt="Arizona Wildland Interface">
<div class="caption">Wildland Interface</div>
</div>
<div class="gallery-item" onclick="openLightbox('/assets/gis/US_Rangelands_and_Forests.png', 'US Rangelands and Forests')">
<img src="/assets/gis/US_Rangelands_and_Forests.png" alt="US Rangelands and Forests">
<div class="caption">US Rangelands</div>
</div>
</div>

<div id="lightbox" class="lightbox" onclick="closeLightbox()">
<span class="close" onclick="closeLightbox()">&times;</span>
<img class="lightbox-content" id="lightbox-img">
<div class="lightbox-caption" id="lightbox-caption"></div>
</div>

<script>
function openLightbox(src, caption) {
document.getElementById('lightbox').style.display = 'block';
document.getElementById('lightbox-img').src = src;
document.getElementById('lightbox-caption').innerHTML = caption;
}
function closeLightbox() {
document.getElementById('lightbox').style.display = 'none';
}
document.addEventListener('keydown', function(event) {
if (event.key === 'Escape') { closeLightbox(); }
});
</script>
# solar-system

The Earth surface texture `earth-blue-marble.jpg` is NASA's Blue Marble: Next Generation July global base map. Credit: NASA Earth Observatory. Source: https://science.nasa.gov/earth/earth-observatory/blue-marble-next-generation/base-map/

## Moon and Mars missions

Choose **月球與火星任務** in the Layers panel to view eleven selected lunar and Mars missions. Ten have sampled heliocentric vectors from JPL Horizons. Selecting a mission starts its recorded timeline; use the date controls to run or accelerate playback. After arrival, orbiters follow an animated nominal mission-era orbit and landers/rovers are placed on the target surface. Spacecraft models use physical vehicle-to-target diameter ratios against the displayed target body, so they are extremely small until focused. Local orbits are representative reconstructions from nominal parameters, not full high-precision historical SPICE trajectories. MAVEN's trajectory samples end at the last available pre-loss ephemeris point (2025-11-16). Apollo 11 has an explicitly labeled illustrative route. This is a curated selection, not a complete catalogue of every historical mission.

NASA 3D models are included under `models/`; `GLTFLoader.js` is the Three.js r128 loader. Keep the assets next to `index.html` when opening or hosting the site. Model credits: [LRO](https://science.nasa.gov/3d-resources/lunar-reconnaissance-orbiter-b/), [Mars Odyssey](https://science.nasa.gov/3d-resources/mars-odyssey/), [Curiosity](https://science.nasa.gov/resource/curiosity-3d-model/), and [Perseverance](https://science.nasa.gov/3d-resources/mars-2020-perseverance-rover/).

Mission-era orbit reference pages: [NASA LRO](https://science.nasa.gov/mission/lro/about/), [NASA Mars Odyssey](https://mars.nasa.gov/system/downloadable_items/44749_odysseyarrival1.pdf), [ESA Mars Express](https://www.esa.int/articles/about-us/directorates/science/mars-express/the-mission), [NASA MRO](https://mars.nasa.gov/system/downloadable_items/44745_mro-arrival.pdf), and [NASA MAVEN](https://science.nasa.gov/mission/maven/).

## Visible stars and exoplanets

The background now uses 8,355 stellar entries from NASA HEASARC's Bright Star Catalog (BSC5P), selected at apparent magnitude under 6.5. J2000 right ascension and declination set each star's sky direction; magnitude sets its rendered brightness, and B−V color provides an approximate tint. The brightest stars with common names are labeled. Click a star or search by its catalog name/HR number to open its information panel. The panel includes catalog designation, magnitude, spectral type, distance when the catalog has parallax, and matched confirmed exoplanets with NASA Exoplanet Archive links. Planet matches use host HD numbers plus aliases for several common nearby systems. “No confirmed planet was matched” means the catalog match did not find one; it does not mean the star has no planets.

The catalog is a naked-eye-threshold catalogue, not a guarantee that every entry is individually resolvable under every observing condition; close multiple stars may appear as one point. The star backdrop preserves J2000 sky directions but does not place stars at real distances from the Solar System. Star colors and dot sizes are visual approximations. `bright-stars.js` is required beside `index.html` and is loaded locally, so the star field works without a runtime data request.

Data sources: [NASA HEASARC Bright Star Catalog (BSC5P)](https://heasarc.gsfc.nasa.gov/W3Browse/all/bsc5p.html) and [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/). The confirmed-planet snapshot is based on the Archive's `PSCompPars` table.

## Visual and interaction features

- Earth, Venus, and Saturn have a subtle additive atmospheric rim; the Sun glow pulses gently; the star field uses catalog sky positions rather than generated random points.
- Turn off **跟隨選取天體** to keep the camera on the Sun when selecting a planet, then watch it move along its orbit. Turn on **顯示歷史軌跡殘影** while time is playing to draw its recent path.
- The time bar includes **即時**, **1 日/秒**, and **1 年/秒** presets. The former speed-slider values are migrated when saved preferences are loaded.
- Planet information includes a simplified internal-structure diagram, labeled as not to scale. Comparison shows two selected bodies with diameter-proportional disks plus the existing measurements table.

## Scale modes

The default **物理比例** mode uses one common unit scale: the Sun radius is 4 scene units, 1 AU is about 860.13 scene units, and every planet and moon radius is converted from kilometers using the same factor. The planets' semi-major axes, eccentricities, inclinations, and secular rates use NASA/JPL's approximate Keplerian elements for 1800–2050. Their instantaneous Sun distances vary around those semi-major axes along elliptical orbits. This is an approximate model, not a JPL Horizons ephemeris. Planets are tiny in the full-system overview by design; select one by its label or search to zoom in. The planet-size and moon-orbit expansion sliders are disabled in physical mode. The optional **線性 AU 展示** keeps orbital distances linear and enlarges planet sizes for visibility. Earlier compressed-distance preferences migrate to physical scale.

Orbital elements: [NASA/JPL Approximate Positions of the Planets](https://ssd.jpl.nasa.gov/planets/approx_pos.html). NASA's [planet distance guide](https://science.nasa.gov/solar-system/planet-sizes-and-locations-in-our-solar-system/) lists rounded average distances in kilometers.

The atmosphere, solar animation, approximate star colors and point sizes, and body scale diagrams are illustrative visualizations, not photorealistic or scale-complete scientific renders.

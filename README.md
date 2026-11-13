# solar-system

The Earth surface texture `earth-blue-marble.jpg` is NASA's Blue Marble: Next Generation July global base map. Credit: NASA Earth Observatory. Source: https://science.nasa.gov/earth/earth-observatory/blue-marble-next-generation/base-map/

## Moon and Mars missions

Choose **月球與火星任務** in the Layers panel to view eleven selected lunar and Mars missions. Ten have sampled heliocentric vectors from JPL Horizons. Selecting a mission starts its recorded timeline; use the date controls to run or accelerate playback. After arrival, orbiters follow an animated nominal mission-era orbit and landers/rovers are placed on the target surface. Spacecraft models use physical vehicle-to-target diameter ratios against the displayed target body, so they are extremely small until focused. Local orbits are representative reconstructions from nominal parameters, not full high-precision historical SPICE trajectories. MAVEN's trajectory samples end at the last available pre-loss ephemeris point (2025-11-16). Apollo 11 has an explicitly labeled illustrative route. This is a curated selection, not a complete catalogue of every historical mission.

NASA 3D models are included under `models/`; `GLTFLoader.js` is the Three.js r128 loader. Keep the assets next to `index.html` when opening or hosting the site. Model credits: [LRO](https://science.nasa.gov/3d-resources/lunar-reconnaissance-orbiter-b/), [Mars Odyssey](https://science.nasa.gov/3d-resources/mars-odyssey/), [Curiosity](https://science.nasa.gov/resource/curiosity-3d-model/), and [Perseverance](https://science.nasa.gov/3d-resources/mars-2020-perseverance-rover/).

Mission-era orbit reference pages: [NASA LRO](https://science.nasa.gov/mission/lro/about/), [NASA Mars Odyssey](https://mars.nasa.gov/system/downloadable_items/44749_odysseyarrival1.pdf), [ESA Mars Express](https://www.esa.int/articles/about-us/directorates/science/mars-express/the-mission), [NASA MRO](https://mars.nasa.gov/system/downloadable_items/44745_mro-arrival.pdf), and [NASA MAVEN](https://science.nasa.gov/mission/maven/).

## Visual and interaction features

- Earth, Venus, and Saturn have a subtle additive atmospheric rim; the Sun glow pulses gently; the star field includes a clustered Milky Way band.
- Turn off **跟隨選取天體** to keep the camera on the Sun when selecting a planet, then watch it move along its orbit. Turn on **顯示歷史軌跡殘影** while time is playing to draw its recent path.
- The time bar includes **即時**, **1 日/秒**, and **1 年/秒** presets. The former speed-slider values are migrated when saved preferences are loaded.
- Planet information includes a simplified internal-structure diagram, labeled as not to scale. Comparison shows two selected bodies with diameter-proportional disks plus the existing measurements table.

## Scale modes

The default **物理比例** mode uses one common unit scale: the Sun radius is 4 scene units, 1 AU is about 860.0 scene units, and every planet and moon radius is converted from kilometers using the same factor. Planetary and lunar orbit distances therefore remain in physical proportion to their bodies. Planets are nearly invisible in the full-system overview by design; use the visible labels/search or select a planet to zoom in. The planet-size and moon-orbit expansion sliders are disabled in this mode. **AU 線性距離** keeps linear AU spacing while enlarging planets, and **展示模式** compresses distances for readability. Older saved default settings are migrated to physical scale; a previously chosen compressed view is preserved.

The atmosphere, solar animation, star-band clustering, and body scale diagrams are illustrative visualizations, not photorealistic or scale-complete scientific renders.

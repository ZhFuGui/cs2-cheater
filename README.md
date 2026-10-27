<div align="center">

# CS2 Cheater

*External CS2 tools and libraries*

[![License](https://img.shields.io/badge/license-MIT-yellow.svg?style=flat-square)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows-0078D4.svg?style=flat-square&logo=windows&logoColor=white)](#)

English | [中文](README.zh-CN.md)

</div>

---

## Projects

This repository brings together project overviews, previews, and source links. **cs2-external-traceline** is the first project added to the collection. Each project maintains its source and build configuration in its own repository.

| Project | Features | Platform |
|:--------|:---------|:---------|
| [cs2-external-traceline](https://github.com/ZhFuGui/cs2-external-traceline) | External ray queries / Cover checks / Penetration damage prediction | Windows x64 |

---

<div align="center">

## cs2-external-traceline

**External Ray Queries · Cover Checks · Penetration Damage Prediction**

[![C++](https://img.shields.io/badge/C++-20-00599C.svg?style=flat-square&logo=c%2B%2B&logoColor=white)](https://github.com/ZhFuGui/cs2-external-traceline)
[![Library](https://img.shields.io/badge/library-DLL-555555.svg?style=flat-square)](https://github.com/ZhFuGui/cs2-external-traceline)

</div>

Queries A → B segments outside the game process using map collision geometry and a BVH acceleration structure. Supplies occlusion, collision hits, traversal thickness, and damage predictions to other tools.

| Capability | Description |
|:-----------|:------------|
| Cover checks | Detect scene occlusion between two points; return the closest hit or all hits |
| Traversal thickness | Return entry/exit intervals and path thickness where the geometry supports reliable volume queries |
| Damage prediction | Use weapon and material parameters for range falloff and penetration loss, with target hit-group and armor calculations |
| Scene caching | Import physics text or triangle data; build, save, and load collision scene caches |
| Integration | C API and C++ wrapper, with concurrent read-only queries on the same scene |

The library handles queries and calculations. The caller supplies scenes, weapon/material parameters, and target state; the consuming application draws skeletons, names, and other visuals. Damage predictions use the supplied static scene and parameters; full live-fire validation is still pending.

<div align="center">

### Preview

<a href="assets/videos/traceline/cover-detection.mp4">
  <img src="assets/images/traceline/cover-detection.png" alt="cs2-external-traceline cover detection demo; click to watch the 1080p video" width="85%" />
</a>

<br />
<sub>Figure 1: Cover detection · Click the cover to watch in 1080p / 30 FPS</sub>

<br /><br />

[![Repo](https://img.shields.io/badge/_View_Repo_cs2--external--traceline_-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ZhFuGui/cs2-external-traceline)

</div>

**Build environment:** Visual Studio 2022 · MSVC v143 · Windows SDK · C++20. Builds an x64 DLL; see the [public headers](https://github.com/ZhFuGui/cs2-external-traceline/tree/main/include/cs2-external-traceline) and [Visual Studio solution](https://github.com/ZhFuGui/cs2-external-traceline/blob/main/cs2-external-traceline.sln) in the project repository.

---

<div align="center">

#### Disclaimer

This repository is for educational and research purposes only.<br />
Users assume all responsibility for any consequences arising from its use.

<br />

<sub>License · MIT &nbsp;|&nbsp; Maintained by [ZhFuGui](https://github.com/ZhFuGui)</sub>

</div>

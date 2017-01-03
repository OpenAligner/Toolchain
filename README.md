# Creating an open source toolchain for clear dental aligners

Clear aligners are orthodontic devices that use incremental transparent aligners to adjust teeth as an alternative to traditional dental braces. Each aligner moves teeth a fraction of a millimeter.
Clear-aligner treatment can be successful for mild to moderate crowding (up to 6 mm) and mild to moderate spacing (up to 6 mm), in cases where there are no discrepancies of the jawbone. It's also being used in case of a relapse after fixed orthodontic treatment.<sup id="a1">[1](#f1)</sup>

# Toolchain

Read and contribute in the Wiki: https://github.com/OpenAligner/Toolchain/wiki

# Production

Mass Customization and Design For Manufacturability are key.

## Acquire patient data

### Intraoral 3D scanner

### Positive model cast in gipsum / plaster of paris etc

#### with an alginate impression forming a mold
#### with a PVS (poly vinyl siloxone) impression

### 3D scanning the positive model

SFM (Structure From Motion) Photogrammetry.
 1. Pair wise matching of many cameras
 1. Create a point set
 1.  Simplification, outlier removal, smoothing
 1. Calculate oriented normals of all points
 1. Reconstruction of geometry;
  Best choice right now seems to be the Poisson Surface Reconstruction method. It solves for an approximate indicator function of the inferred solid, whose gradient best matches the input normals.
 1. Contouring, surface mesh generation

## CAD/CAM

### SLA/SLS

### CNC milling

<b id="f1">1</b> https://books.google.com/books?id=lksG08hp1sgC&pg=PA162 [↩](#a1)

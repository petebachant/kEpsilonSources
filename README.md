kEpsilonSources
===============

Modified kEpsilon turbulence model for OpenFOAM, which uses fvOptions for 
adding source terms.

## Installing

Clone and move into this repository, then run `wmake libso`:

    cd $WM_PROJECT_USER_DIR
    git clone https://github.com/petebachant/kEpsilonSources.git
    cd kEpsilonSources
    wmake libso

## Usage

Add `"libmyIncompressibleRASModels.so"` to `libs` in your case's
`system/controlDict`, and in `constant/RASProperties` use

    RASModel            kEpsilonSources;

For an example, see
https://github.com/petebachant/actuatorSurface-OpenFOAM/tree/kEpsilonSources

# Whirling of Shafts — Virtual Laboratory

An interactive 3D laboratory on the whirling of shafts and critical speeds, made for the **Dynamics of Machines** course.

**Raj Pandya · 24BME091 · Batch A-5**

Open the live laboratory: the GitHub Pages link for this repository.

## What it does

- **Guided briefing.** Seven short chapters (aim, unbalance, equilibrium, critical speed, self-centring, end conditions and Dunkerley's method, procedure). The 3D model acts out each idea.
- **3D apparatus** (Three.js). Motor, flexible coupling, bearings or clamps, a shaft that bows in its true deflected shape, and a disc with a visible unbalance and mass centre *G*. You can orbit and zoom, and pick from five camera views.
- **Four end conditions:** simply supported, fixed–pinned, fixed–fixed and cantilever. Stiffness comes from a Macaulay beam solution with four boundary conditions, checked against the textbook formulas.
- **Live results:** *N*c (Dunkerley), disc-alone and shaft-alone critical speeds, stiffness, static deflection, whirl amplitude, phase, *OG*, bearing load, bending stress and factor of safety.
- **Analysis:** amplitude, phase, bearing-load and stress curves against speed, for a family of damping ratios.
- **Transient run-up and coast-down:** the 2-D equations of motion are integrated with fourth-order Runge–Kutta while the rotor accelerates through *N*c, then replayed in 3D.
- **Modes:** the first three whirling modes of the bare shaft for each end condition, which can also be animated in 3D.
- **Working:** every formula, worked through with the current numbers.
- **Lab sheet:** an observation table with error against theory and CSV copy.
- **Viva:** eight questions with explanations.
- **Customisation:** Paper, Drafting and Blueprint themes; four accent inks; disc finishes; labels, orbit, safety guard and shadows; deflection scale, exaggeration and animation rate; rpm, rad/s or Hz.

Keyboard: `Space` pause · `←/→` speed · `C` critical speed · `R` run-up · `1–6` tabs · `V` camera · `S` settings · `F` full screen · `?` help.

## Model

Jeffcott rotor: a disc of mass *m* with eccentricity *e* on an elastic shaft of stiffness *k* with viscous damping ζ.

y = e·r² / √[(1 − r²)² + (2ζr)²],  tan φ = 2ζr / (1 − r²),  r = ω/ωc

with 1/ωc² = 1/ωd² + 1/ωs² (Dunkerley), ωd = √(k/m) and ωs = (βL)²√(EI/ρAL⁴).

A single self-contained `index.html`. The only external code is Three.js r147 from jsDelivr.

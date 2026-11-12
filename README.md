# Single-stage helical gearbox (CATIA V5)

My year project for the Machine Elements course at Transilvania University of Brașov. The brief was a speed reducer for something like a car lift or a brake test stand, driven by an induction motor, with shock loads:

| Input power | Input speed | Ratio | Required life | Shaft layout |
|---|---|---|---|---|
| 12.5 kW | 2500 rpm | 3.5 | 12,000 h | horizontal |

I did the calculations, picked the standard parts, modeled everything in CATIA V5 and made the assembly and manufacturing drawings.

<img width="727" height="799" alt="gear_stage" src="https://github.com/user-attachments/assets/1d9bd937-7b96-41c8-a7ef-b5b3076bd931" />

## Gears

The pinion has 22 teeth and the wheel 77, which gives exactly 3.5. Both are case-hardened 17MoCrNi14 steel, with the teeth shaped before carburizing and ground after hardening.

From the contact and bending stress calculations I got a normal module of 1.7 mm and went up to the standard 2.5 mm, with a 10° helix angle. That gave a reference centre distance of 125.66 mm. To get the standard 125 mm I applied a profile shift of −0.407 on the wheel. I checked the shifted gear pair in CATIA by modeling the tooth profiles and simulating the mesh to confirm that contact stays continuous.

The output shaft turns at about 714 rpm with a torque of about 159 Nm.

## Shafts, bearings and keys

The shafts were sized for torsion first, then checked in MDESIGN once their shape was set in CATIA. For the input shaft:

- static safety factor 22.1 and fatigue safety factor 7.4, against a minimum of 1.2
- maximum deflection 0.015 mm, against an allowed 0.045 mm
- critical speeds far above the running speed

The shafts run on deep groove ball bearings. The most loaded one on the input shaft comes out at 12,025 h of life, just over the 12,000 h required. The gear and the shaft ends are fixed with parallel keys, checked for crushing and shear.

## CAD and drawings

The model is fully parametric: shafts with the pinion and the wheel, bearings, a split housing with centering pins and lifting eyes, inspection cover, oil sight glass, drain and breather plugs, shaft seals and ISO standard fasteners (ISO 4017 screws, ISO 4034 nuts). I also built a kinematic model of the mechanism in CATIA DMU Kinematics.

The drawings include the assembly drawing and manufacturing drawings for the input shaft with the pinion and for the wheel, with tolerances, geometric tolerances, surface finish, gear data tables and heat treatment notes.

<img width="2203" height="768" alt="drawings" src="https://github.com/user-attachments/assets/9520e072-9cd6-48d7-95a0-8f4893e28c94" />

## Folders

- `CAD/`: CATIA parts (.CATPart) and assemblies (.CATProduct). `Ansamblu H.CATProduct` is the full gearbox.
- `Drawings/`: assembly and manufacturing drawings (.CATDrawing)
- `Docs/`: the full technical report with all calculations (in Romanian)

Claudiu Fugulin · [LinkedIn](https://www.linkedin.com/in/claudiufugulin)

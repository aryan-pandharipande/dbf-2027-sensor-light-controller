# Sensor Lights Controller for AIAA Design Build Fly Competition 2027 Problem Statement

Light controller PCB for the towed sensor on the 2027 AIAA Design/Build/Fly aircraft.

- **Modes:** OFF / SOLID ON / FLASHING ON
- **MCU:** ATtiny13A-SSU (SOIC-8)
- **PCB tool:** KiCad 10 (two-layer board)
- **Connectors:** JST PH 2-pin. J1 battery, J2 towline, J3/J4/J5 forward/center/aft light arrays

![PCB in 3D View](https://github.com/user-attachments/assets/c24b274d-cd3b-4aed-a361-460250807eaf)

![PCB in KiCAD](https://github.com/user-attachments/assets/ec0c8e67-deb9-4d24-8c51-105c0cc0711f)

![PCB in Onshape](https://github.com/user-attachments/assets/b6f36511-817d-4884-a52e-ea2aaab788af)
## Repository layout
dbf-sensor-lights/
├── README.md                     (overview, schematic image, layout table, TODO)
├── .gitignore                    (KiCad-friendly)
├── hardware/
│   ├── kicad/                    .kicad_pro, .kicad_pcb, .sch, 2× .kicad_prl
│   └── fabrication/              (empty, for Gerbers/BOM later)
├── firmware/README.md            (placeholder for the ATtiny13A code)
├── cad/
│   ├── sensor_light_controller.step
│   └── drawings/sensor_light_controller_1_Drawing_1.pdf
└── docs/
    ├── report/PCB_Report.pdf
    └── images/                   schematic, KiCad PCB view, KiCad 3D view, Onshape import

| Path | Contents |
|------|----------|
| `hardware/kicad/` | KiCad project: `.kicad_pro`, `.kicad_pcb`, `.sch` (legacy format, reconstructed from the PCB netlist) |
| `hardware/fabrication/` | Gerbers, drill files, BOM, pick-and-place exports (to be generated) |
| `firmware/` | ATtiny13A firmware (to be added) |
| `cad/` | STEP model of the assembled PCB and the Onshape drawing PDF |
| `docs/report/` | `PCB_Report.pdf`, the PCB proposal report |
| `docs/images/` | Schematic, PCB editor, 3D view and Onshape screenshots |

## Notes

- The `.sch` file is a reconstruction of the PCB netlist, not an ERC-verified source schematic. Open it in KiCad and save as `.kicad_sch`.
- The two `.kicad_prl` files in `hardware/kicad/` are local KiCad UI state and can be deleted.

## TODO

- [ ] Add firmware source
- [ ] Generate fabrication outputs into `hardware/fabrication/`
- [ ] Reconcile report and schematic (board dimensions, D1/D2 part values, ATtiny85 mentions)

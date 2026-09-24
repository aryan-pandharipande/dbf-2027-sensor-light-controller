# DBF Sensor Lights

Light controller PCB for the towed sensor on the 2027 AIAA Design/Build/Fly aircraft.

- **Modes:** OFF / SOLID ON / FLASHING ON
- **MCU:** ATtiny13A-SSU (SOIC-8)
- **PCB tool:** KiCad 10 (two-layer board)
- **Connectors:** JST PH 2-pin. J1 battery, J2 towline, J3/J4/J5 forward/center/aft light arrays

![PCB in 3D View](<img width="1280" height="763" alt="Screenshot 2026-09-23 170502" src="https://github.com/user-attachments/assets/953d8ac7-fedd-49ed-abf6-9d3300efac92" />
)
![PCB in KiCAD](<img width="1280" height="766" alt="Screenshot 2026-09-23 170355" src="https://github.com/user-attachments/assets/821c01bc-180f-431a-9e5a-984e0cbf4e8c" />
)
![PCB in Onshape](<img width="1280" height="669" alt="Screenshot 2026-09-24 162343" src="https://github.com/user-attachments/assets/ead19186-4186-40a2-85b8-2f772c1689b2" />
)
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

# voron2.4-klipper-backup
Automated backup of klipper config

Voron 2.4 250mm v2.1906

discord: WarCorgi

# Features
- [Can Bus - SHT36 v2](https://github.com/bigtreetech/EBB)
- [Magic Phoenix Kit w/CNC parts](https://github.com/MagicPhoenix/MPX-VORON-24R2-KIT)
- [Git backup](https://github.com/th33xitus/kiauh/wiki/How-to-autocommit-config-changes-to-github%3F) - using [SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) authentication
- [Nozzle Scrubber](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/edwardyeeks/Decontaminator_Purge_Bucket_&_Nozzle_Scrubber)
- [Resonance testing with image processing](https://www.klipper3d.org/Measuring_Resonances.html) - pushing to [github](resonances) to view them is pretty easy
- [Klicky Probe](https://github.com/jlas1/Klicky-Probe)
- [Stealthburner with Orbiter 2.0 & filament sensor](https://vorondesign.com/voron_stealthburner)
- [Voron Revo](https://e3d-online.com/products/revo-voron)
- [Probe Accuracy Tests](https://github.com/sporkus/probe_accuracy_tests) - have to be run from command line
- [FUTURE - ERCF](https://github.com/EtteGit/EnragedRabbitProject)
- [FUTURE - ERCF-Software-V3 "Happy Hare"](https://github.com/moggieuk/ERCF-Software-V3)
- [Adaptive Bed Mesh](https://github.com/Frix-x/klipper-voron-V2/blob/main/doc/features/adaptive_bed_mesh.md)
- [Calibrating Klipper z offset](https://github.com/protoloft/klipper_z_calibration)

# Links
## Main mod repos
- [Voron User Mods](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods)  
- [https://voronregistry.com/mods](https://voronregistry.com/mods) - Also nice website for same by discord:exceptionptr  
- [https://vorondesign.com/](https://vorondesign.com/)  

## Software
- [Klipper](https://www.klipper3d.org/)
- [Plater optimal part layout](https://github.com/Rhoban/Plater)
- [Measure_thermal_behavior - the need for backers](https://github.com/tanaes/measure_thermal_behavior)

## Hardware
- [BTT Octopus GitHub](https://github.com/bigtreetech/BIGTREETECH-OCTOPUS-V1.0)
- [nxutil filament encoder](https://github.com/nexx/nxencoder-util)
- [LED strip power injection calculator](http://spikerlights.com/calcpower.aspx)

## Voron parts
- [Planetary Z drive](https://github.com/CarlosRodriguess/Galileo-Z_Modify)
- [Rama's Voron Mods inc the new idlers](https://github.com/Ramalama2/Voron-2-Mods)

## Klipper configs
- [lcd_tweaks.cfg](https://github.com/VoronDesign/Voron-Documentation/blob/4a825a8704a3c8467606f58fb45ac4c377779842/community/howto/alchemyEngine/lcd_tweaks.cfg)
- [Live LED update using klipper and display_template](https://github.com/whoim2/w-mini-corexy/blob/main/klipper/led_progress.cfg)
- [https://github.com/alchemyEngine/klipper_frame_expansion_comp](https://github.com/alchemyEngine/klipper_frame_expansion_comp)

## Misc
- [Ellis' SuperSlicer Profiles](https://github.com/AndrewEllis93/Ellis-SuperSlicer-Profiles)
- [Ellis' Print Tuning Guide](https://ellis3dp.com/Print-Tuning-Guide/)
- [hartk1213 various repos](https://github.com/hartk1213)

## ERCF
- [Mods including Quiver and Top Handle extrusion mount](https://github.com/SkiBikePrint/ERCF_Mods)
- [Upsidedown buffer array and other mods](https://github.com/geoffrey-young/3D-Printing/tree/main/models/voron/ercf)
- [Metal Buffer](https://github.com/sloscotty/Metal-Buffer)
- [Top gimbal mount and other mods](https://github.com/DeBau/VoronMods)

# Other klipper backups I've found useful
- [https://github.com/AndrewEllis93/v2.247_backup_klipper_config](https://github.com/AndrewEllis93/v2.247_backup_klipper_config)
- [https://github.com/pushc6/VoronConfig](https://github.com/pushc6/VoronConfig)
- [https://github.com/kageurufu/3dp-voron2/tree/master/printer](https://github.com/kageurufu/3dp-voron2/tree/master/printer)
- [https://github.com/wile-e1/klipper_config](https://github.com/wile-e1/klipper_config)
- [https://github.com/th33xitus/klipper_config](https://github.com/th33xitus/klipper_config)
- [https://github.com/jktightwad/Klipper24Config](https://github.com/jktightwad/Klipper24Config)
- [https://github.com/mjoconr/Voron2.4-Config](https://github.com/mjoconr/Voron2.4-Config)
- [https://github.com/zellneralex/klipper_config](https://github.com/zellneralex/klipper_config)
- [https://github.com/Frix-x/klipper-voron-V2](https://github.com/Frix-x/klipper-voron-V2)
    
# CAN Bus for EBB3.6 with UCI

allow-hotplug can0
iface can0 can static
    bitrate 250000
    up ifconfig $IFACE txqueuelen 128

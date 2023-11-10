# Zybo Z7-10 Pcam 5C Reference Design

## Intro

Digilent provides Pcam reference design for the Zybo board. Unfortunately the design is delivered in a non-versioncontrollable way (ZIP files) and does not build out of the box and hence it is a bad starting point for student projects.

This repo contains the exact same reference design without any functional changes, just cleaned up and made version-control friendly.

## Vivado Guide

A *.gitignore* file ignoring all non version controlled files is provided,

### Check-Out

After a fresh clone follow the steps below to build the vivado project:

1. Open Vivado 2023.1
2. In the Vivado TCL shell, navigate to *[root]/vivado* (using  `cd <dir>`)
3. In the Vivado TCL shell, type `source ./projectNew.tcl`

### Check-In

1. In the Vivado TCL shell, navigate to *[root]/vivado* (using  `cd <dir>`)
2. In the Vivado TCL shell, type `write_project_tcl -paths_relative_to . -origin_dir_override . -force ./projectNew.tcl`

## Vitis Guide

### Check-Out

After a fresh clone follow the steps below to build the vitis project:

1. Open Vitis 2023.1 - use the old GUI (not the experimental one)
2. Open a new workspace, anywhere on your filesystem (outside of the version controlled working-copy)
3. Menu-entry *File > Import ....*
4. Select *Eclipse workspace or ZIP file*
5. Select the directory *[root]/vitis/ws*
6. Select all projects, **unselect _Copy projects into workspace_ checkbox**
7. Menu entry *Vitis > XSCT Console*
8. In the XSCT Console, navigate to *[root]/vitis/ws* (using  `cd <dir>`)
9. In the XSCT Console, type `source ./regenerate.tcl`

### Check-In

None, just commit the modified files in *[root]/vitis/ws*.


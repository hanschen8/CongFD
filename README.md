# CongFDeezNuts

## "Back To The Basics" - Hans Chen, Dave Laygo, Alex Yeh

## Geometry:

- SpaceClaim water tight geometry
- Project rectangles over the vents’
- Get rid of return air cad
- need to distinguish sidewalls from roof and floors for conduction and convection


## Meshing:
- Added local sizing
- Mesh sizes: Inlet & Outlet (15), Wall size (50)
- Growth Rate: 1.2
- Size Control Type: Face Size
- Describe Geometry: The geometry consists of only fluid regions with no voids, no change all fluid-fluid boundary layers from "wall" to "internal", yes to apply shared topology
- Must change to shared topology in space claim not in fluent

## Solution (Domain):
- Viscous _ SST k-omega
- gravity in z = 9.81
- Energy on
- Species off
- Discrete Phase off
- Materials: Air (leave as normal)
- inlet conditions (mass flow inlet: 2.429 kg/s, 20 C or 293K, Standard Everything else)
- the mass flow rate of people talking is .002 kg/s and 300 
- outlet conditions (mass flow outlet, since system pumps out the same amount of mass of air that it pumps in)
- roof and floor (heat flux = 60 [W/m2])
- sidewalls (convection, HTC = 5, Temp = 303K)
- People heat flux at 500 w/m2
- everything else = 0 for boundary conditions
- Spec Dissipation Rate and Energy set to first order upwind
- first two = .5 , and set Turb KE, Spec Dissipation Rate, Energy = .75
- everything else is standard
- 2000 iterations 
- press run calc in results, and set the solution to all zones, set to 1000 iterations
- wait and have fun yay

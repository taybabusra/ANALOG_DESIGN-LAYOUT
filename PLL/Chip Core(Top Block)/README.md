# 3rd approach in the top block:
<img width="153" height="186" alt="image" src="https://github.com/user-attachments/assets/9da902b1-fe19-44d9-aeb8-76e2d07d75ea" />

Major change I have made in the layout:
1. The placement of the charge pump is directly changed.Why? Reason is that the VN and VP comming from the opm needs to be closer in the charge pump.
2. The control signal should be  in the intended place of the routing.
3. Current problem in this layout is that.
      1. In the digital block VDD_Device in between there would be no routing and all routing shold be in the middle of the device.
      2. VDD,VSS are thin they should be thick
      3.  UP and DOWN for the PFD are not in the symmetric place. These two signal needs to be symmetric.

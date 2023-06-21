# PET-Diagnostic-Clip
This is a modern remake of the two Commodore Diagnostic Clips

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3934_-_diagnostic_clip_set.JPG" width="300" alt="Diagnostic Clip (complete)"><br>Complete Diagnostic Clip Set

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3933_-_test_in_3016.JPG" width="300" alt="Diagnostic Clip in CBM3016"><br>Diagnostic Clip installed in a CBM3016 (non CRTC machine)

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3827_-_test_clipv2_8032.JPG" width="300" alt="Diagnostic Clip in CBM8032"><br>Diagnostic Clip installed in a CBM8032 (CRTC machine)

# PET Diagnostic Software (40 column, non CRTC):<br>
<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3815_-_diag320350g_start.JPG" width="300" alt="40col non CRTC Start"><br>Opening Screen

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3816_-_diag_320350g_loop1.JPG" width="300" alt="40col non CRTC Tests"><br>Actual tests

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3817_-_diag_320350g_loop2.JPG" width="300" alt="40col non CRTC Tests"><br>Actual tests (continued)



# PET Diagnostic Software (80 column, CRTC):<br>
<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3824_-_80col_diag_v1.1_start.JPG" width="300" alt="80col CRTC Start"><br>Opening Screen

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3826_-_80col_diag_v1.1_loop.JPG" width="300" alt="80col CRTC Tests"><br>Actual tests

# Binaries for the EPROM
The name of the combined file is "80colCRCTv1.1_40colCRCTv2.0_diag3202350g_diag320350g.bin". It contains:
<table>
  <thead>
    <tr>
      <th>EPROM Offset</th><th>Software</th><th>DIP Switch</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>$0000</td><td>80_col_diagnostic_v1.1.bin</td><td>A[15..12]: 0000 =  ON  ON  ON  ON</td>
    </tr>
    <tr>
      <td>$1000</td><td>40_col_diagnostic_v2.0.bin</td><td>A[15..12]: 0001 =  ON  ON  ON  OFF</td>
    </tr>
    <tr>
      <td>$2000</td><td>901447-30_diagnostic_320350g_$9000.bin</td><td>A[15..12]: 0010 =  ON  ON  OFF ON</td>
    </tr>
    <tr>
      <td>$3000</td><td>901447-30_diagnostic_320350g_$9000.bin</td><td>A[15..12]: 0011 =  ON  ON  OFF OFF</td>
    </tr>
 </tbody>
</table>    
    
The Diagnostic 320350g is double. The reason is, the computer would crash if an empty slot is selected. So all slots, that can be selected with the two low switches of the dip switch are occupied.

In a subdirectory, there are some "PETtester" Softwares. These are not a complete test. The (vice) screen shots are included. It could also be installed on the clip, if desired. 
# CBM8296
This part of the project is not tested yet. <b>The release is preliminary</b>.

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/CBM8296_Harness/CBM%20Diagnostics%20Top%20%20Level/pictures/5138_-_CBM8296_Diagnostic_Harness.JPG" width="300" alt="CBM8296 Diagnostic Harness (complete)"><br>CBM8296 Diagnostic Harness (complete)

The diagnostic software for the CBM8296 is contained in the respective folder. There is also a merged binary file ("80colCRCTv1.1_40colCRCTv2.0_diag3202350g_diag320350g_8296.bin") which contains the 324806-01.bin at offset address $4000 (A[15..12]: 0100 =  ON  OFF  ON ON).

<b>State of testing:</b><br>
14.06.2023:<br>
* all dongles work with the original (Commodore) clip
* the cassette dongle case reqires modification
21.06.2023:<br>
The CBM8296 can actively switch the /NOROM signal (register @$FFF0). It does so to access the RAM underneath the ROMs. As a result, the diagnostic ROM in the clip is getting visible, which interferes with the test of the upper RAM banks.

A solution is switching off the /NOROM signal in the clip by using the 2nd stage of the external switch. The /NOROM trace at J1, pin 9 has to be cut open and connected to the middle pin of the said switch, the right pin ("active" position) has to be connected to the clip's internal /NOROM signal, e.g. at SW4.  

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/CBM8296_Harness/CBM%20Diagnostics%20Top%20%20Level/pictures/8296_clipv2_mod.png" width="300" alt="Diagnostic Clip (complete)"><br>/NOROM modification of Clip Rev. 2

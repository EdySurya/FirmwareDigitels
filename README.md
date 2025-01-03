# FirmwareDigitels

## Cheat Sheet Update Feature 2025

### Over the Air (OTA) Update Firmware

| Description     | Payload                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------|
| OTA SGW-WIFI    | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":1,"action":1,"OK":0}`     |
| OTA SGW-NOW     | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":2,"action":1,"OK":0}`     |
| OTA SLAVE 1 (L) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":9,"action":1,"OK":0}`     |
| OTA SLAVE 2 (M) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":10,"action":1,"OK":0}`    |
| OTA SLAVE 3 (G) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":11,"action":1,"OK":0}`    |
| OTA LVGL 1 (L)  | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":14,"action":1,"OK":0}`    |
| OTA LVGL 2 (M)  | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":15,"action":1,"OK":0}`    |
| OTA LVGL 3 (G)  | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":16,"action":1,"OK":0}`    |
| OTA KIN (L)     | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":5,"action":1,"OK":0}`     |
| OTA KIN (M)     | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":2,"OTA":4,"action":1,"OK":0}`     |
| OTA KIN (G)     | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":3,"OTA":4,"action":1,"OK":0}`     |

### Download IR Copy Data Hisense Off

| Description  | Payload                                                                                           |
|--------------|---------------------------------------------------------------------------------------------------|
| IR COPY SL 1 | `{"data":"IRACdata","CMD":1010,"Time":1001,"address":1,"AC":2,"brand":"Hisense","slot":"Copy4","OK":0}` |
| IR COPY SL 2 | `{"data":"IRACdata","CMD":1010,"Time":1001,"address":1,"AC":3,"brand":"Hisense","slot":"Copy4","OK":0}` |
| IR COPY SL 3 | `{"data":"IRACdata","CMD":1010,"Time":1001,"address":1,"AC":4,"brand":"Hisense","slot":"Copy4","OK":0}` |

### Config LCD Masking Bit 8 to Copy Data Bit 12 Off

#### 1BR

| Description       | Payload                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------|
| LVGL 1 (L) 1BR    | `{"data":"typePanel","CMD":1062,"Time":1001,"address":1,"slave":0,"LCD":1,"panel":1,"mask_AC":[0,0,0,0,0,0,0,12],"OK":0}` |

#### 2BR

| Description       | Payload                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------|
| LVGL 1 (L) 2 BR   | `{"data":"typePanel","CMD":1062,"Time":1001,"address":1,"slave":0,"LCD":1,"panel":2,"mask_AC":[0,0,0,0,0,0,0,12],"OK":0}` |
| LVGL 2 (M) 2 BR   | `{"data":"typePanel","CMD":1062,"Time":1001,"address":1,"slave":0,"LCD":2,"panel":3,"mask_AC":[0,0,0,0,0,0,0,12],"OK":0}` |
| LVGL 3 (G) 2 BR   | `{"data":"typePanel","CMD":1062,"Time":1001,"address":1,"slave":0,"LCD":3,"panel":3,"mask_AC":[0,0,0,0,0,0,0,12],"OK":0}` |

### Exclude Masterlight - Balcony & Storage

#### 1BR

| Description    | Payload                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------|
| BALCONY 1BR    | `{"data":"masterLight","CMD":1067,"Time":1001,"address":1,"slave":0,"bit":8,"status":0,"OK":0}`   |
| STORAGE 1BR    | `{"data":"masterLight","CMD":1067,"Time":1001,"address":1,"slave":0,"bit":9,"status":0,"OK":0}`   |

#### 2BR

| Description    | Payload                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------|
| BALCONY 2BR    | `{"data":"masterLight","CMD":1067,"Time":1001,"address":1,"slave":0,"bit":7,"status":0,"OK":0}`   |
| STORAGE 2BR    | `{"data":"masterLight","CMD":1067,"Time":1001,"address":1,"slave":0,"bit":8,"status":0,"OK":0}`   |


### Update Switch Toilet Prevent Stuck

#### 1BR (RF CODE : LM = L+1, RM=R+1)

| Description    | Payload                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------|
| LEFT & MIDDLE - DOWNLIGHT 2    | `{"data":"pairSwitch","CMD":4000,"Time":1001,"address":1,"slave":0,"gang":2,"bit":7,"rfcode":[255,255,255,0],"OK":0}`   |
| RIGHT & MIDDLE - SMART GLASS 2 | `{"data":"pairSwitch","CMD":4000,"Time":1001,"address":1,"slave":0,"gang":2,"bit":8,"rfcode":[255,255,255,0],"OK":0}`   |

#### 2BR MASTER (RF CODE : LM = L+1, RM=R+1)

| Description    | Payload                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------|
| LEFT & MIDDLE - DOWNLIGHT 2    | `{"data":"pairSwitch","CMD":4000,"Time":1001,"address":1,"slave":2,"gang":1,"bit":7,"rfcode":[255,255,255,0],"OK":0}`   |
| RIGHT & MIDDLE - SMART GLASS 2 | `{"data":"pairSwitch","CMD":4000,"Time":1001,"address":1,"slave":2,"gang":1,"bit":9,"rfcode":[255,255,255,0],"OK":0}`   |

#### 2BR GUEST (RF CODE : LM = L+1, RM=R+1)

| Description    | Payload                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------|
| LEFT & MIDDLE - DOWNLIGHT 2    | `{"data":"pairSwitch","CMD":4000,"Time":1001,"address":1,"slave":3,"gang":1,"bit":7,"rfcode":[255,255,255,0],"OK":0}`   |
| RIGHT & MIDDLE - SMART GLASS 2 | `{"data":"pairSwitch","CMD":4000,"Time":1001,"address":1,"slave":3,"gang":1,"bit":9,"rfcode":[255,255,255,0],"OK":0}`   |

### Update Scenario Relax 1BR

#### 1 BR Dim 25%, Bed Head Off, Sym Bright 25%

| Description             | Payload                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------|
| BIT 1,2,3,5,10 25% 1BR  | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":4,"type":1,"bit":1,"status":20,"OK":0}` |
| BIT 4,6,7,11,12 25% 1BR | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":4,"type":1,"bit":4,"status":64,"OK":0}` |
| BIT 13 OFF 1BR          | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":4,"type":2,"bit":13,"status":0,"OK":0}` |
| SYM 0-1 BRIGHT 25%      | `{"data":"sympScenario","CMD":1078,"Time":1001,"address":1,"slave":0,"scenario":4,"symphony":0,"R":255,"G":89,"B":11,"speed":35,"bright":64,"mode":1,"LedPoint":40,"OK":0}` |

### Update Scenario Balcony - Storage Off 1BR

#### 1 BR Scene Read, Work, Relax

| Description             | Payload                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------|
| BIT 8 - Scenario 2,3,4  | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":2,"type":1,"bit":8,"status":0,"OK":0}` |
| BIT 9 - Scenario 2,3,4  | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":2,"type":1,"bit":9,"status":0,"OK":0}` |

### Update Scenario Relax 2BR

#### 2 BR Living Dim 25%, All Kinetic Off

| Description             | Payload                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------|
| BIT 1,3,4, 25% 2BR      | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":4,"type":1,"bit":1,"status":20,"OK":0}` |
| BIT 2,5,6 25% 2BR       | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":4,"type":1,"bit":2,"status":64,"OK":0}` |
| BIT 13,14,15 OFF 2BR    | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":4,"type":2,"bit":13,"status":0,"OK":0}` |
| SYM 0-1 BRIGHT 25%      | `{"data":"sympScenario","CMD":1078,"Time":1001,"address":1,"slave":0,"scenario":4,"symphony":0,"R":255,"G":89,"B":11,"speed":35,"bright":64,"mode":1,"LedPoint":85,"OK":0}` |

#### 2 BR Master Dim 25%, Bed Head & Bed Track Off, Sym 2 Bright 25%

| Description             | Payload                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------|
| BIT 1, 25% 2BR          | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":2,"scenario":4,"type":1,"bit":1,"status":20,"OK":0}` |
| BIT 2,3 25% 2BR         | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":2,"scenario":4,"type":1,"bit":2,"status":64,"OK":0}` |
| BIT 7,9 OFF 2BR         | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":2,"scenario":4,"type":2,"bit":7,"status":0,"OK":0}` |
| SYM 2 (MASTER) BRIGHT 25% | `{"data":"sympScenario","CMD":1078,"Time":1001,"address":1,"slave":2,"scenario":4,"symphony":2,"R":255,"G":89,"B":11,"speed":35,"bright":64,"mode":1,"LedPoint":50,"OK":0}` |

#### 2 BR Guest Dim 25%, Bed Head & Bed Track Off, Sym 3 Bright 25%

| Description             | Payload                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------|
| BIT 1, 25% 2BR          | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":3,"scenario":4,"type":1,"bit":1,"status":20,"OK":0}` |
| BIT 2,3 25% 2BR         | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":3,"scenario":4,"type":1,"bit":2,"status":64,"OK":0}` |
| BIT 7,9 OFF 2BR         | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":3,"scenario":4,"type":2,"bit":7,"status":0,"OK":0}` |
| SYM 3 (GUEST) BRIGHT 25% | `{"data":"sympScenario","CMD":1078,"Time":1001,"address":1,"slave":3,"scenario":4,"symphony":3,"R":255,"G":89,"B":11,"speed":35,"bright":64,"mode":1,"LedPoint":50,"OK":0}` |

### Update Scenario Balcony - Storage Off 2BR

#### 2 BR Scene Read, Work, Relax

| Description             | Payload                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------|
| BIT 7 - Scenario 2,3,4  | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":2,"type":1,"bit":7,"status":0,"OK":0}` |
| BIT 8 - Scenario 2,3,4  | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":2,"type":1,"bit":8,"status":0,"OK":0}` |

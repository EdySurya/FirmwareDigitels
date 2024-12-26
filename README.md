# FirmwareDigitels

# CHEAT SHEET UPDATE FEATURE 2025 

# OVER THE AIR (OTA) Update Firmware
| Description | Payload |
|---------|-------------|
| OTA SGW-WIFI | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":1,"action":1,"OK":0}` |
| OTA SGW-NOW | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":2,"action":1,"OK":0}` |

| Description | Payload |
|---------|-------------|
| OTA SLAVE 1 (L) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":9,"action":1,"OK":0}` |
| OTA SLAVE 2 (M) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":10,"action":1,"OK":0}` |
| OTA SLAVE 3 (G) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":11,"action":1,"OK":0}` |

| Description | Payload |
|---------|-------------|
| OTA LVGL 1 (L) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":14,"action":1,"OK":0}` |
| OTA LVGL 2 (M) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":15,"action":1,"OK":0}` |
| OTA LVGL 3 (G) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":16,"action":1,"OK":0}` |

| Description | Payload |
|---------|-------------|
| OTA DIM 1 (L) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":3,"action":1,"OK":0}` |
| OTA DIM 2 (L) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":4,"action":1,"OK":0}` |
| OTA KIN (L) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":0,"OTA":5,"action":1,"OK":0}` |

| Description | Payload |
|---------|-------------|
| OTA DIM (M) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":2,"OTA":3,"action":1,"OK":0}` |
| OTA KIN (M) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":2,"OTA":4,"action":1,"OK":0}` |

| Description | Payload |
|---------|-------------|
| OTA DIM (G) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":3,"OTA":3,"action":1,"OK":0}` |
| OTA KIN (G) | `{"data":"updateOTA","CMD":1111,"Time":1001,"address":1,"slave":3,"OTA":4,"action":1,"OK":0}` |

# Download IR Copy Data
| Description | Payload |
|---------|-------------|
| IR COPY SL 1 | `{"data":"IRACdata","CMD":1010,"Time":1001,"address":1,"AC":2,"brand":"Hisense","slot":"Copy4","OK":0}` |
| IR COPY SL 2 | `{"data":"IRACdata","CMD":1010,"Time":1001,"address":1,"AC":3,"brand":"Hisense","slot":"Copy4","OK":0}` |
| IR COPY SL 3 | `{"data":"IRACdata","CMD":1010,"Time":1001,"address":1,"AC":4,"brand":"Hisense","slot":"Copy4","OK":0}` |

# Config LCD masking bit 8 to copy data bit 12 0ff
## 1BR
| Description | Payload |
|---------|-------------|
| LVGL 1 (L) 1BR | `{"data":"typePanel","CMD":1062,"Time":1001,"address":1,"slave":0,"LCD":1,"panel":1,"mask_AC":[0,0,0,0,0,0,0,12],"OK":0}` |
## 2BR
| Description | Payload |
|---------|-------------|
| LVGL 1 (L) 2 BR | `{"data":"typePanel","CMD":1062,"Time":1001,"address":1,"slave":0,"LCD":1,"panel":2,"mask_AC":[0,0,0,0,0,0,0,12],"OK":0}` |
| LVGL 2 (M) 2 BR | `{"data":"typePanel","CMD":1062,"Time":1001,"address":1,"slave":0,"LCD":2,"panel":3,"mask_AC":[0,0,0,0,0,0,0,12],"OK":0}` |
| LVGL 3 (G) 2 BR | `{"data":"typePanel","CMD":1062,"Time":1001,"address":1,"slave":0,"LCD":3,"panel":3,"mask_AC":[0,0,0,0,0,0,0,12],"OK":0}` |

# EXCLUDE MASTERLIGHT - BALCONY & STORAGE
## 1BR
| Description | Payload |
|---------|-------------|
| BALCONY 1BR | `{"data":"masterLight","CMD":1067,"Time":1001,"address":1,"slave":0,"bit":8,"status":0,"OK":0}` |
| STORAGE 1BR | `{"data":"masterLight","CMD":1067,"Time":1001,"address":1,"slave":0,"bit":9,"status":0,"OK":0}` |
## 2BR
| Description | Payload |
|---------|-------------|
| BALCONY 2BR | `{"data":"masterLight","CMD":1067,"Time":1001,"address":1,"slave":0,"bit":7,"status":0,"OK":0}` |
| STORAGE 2BR | `{"data":"masterLight","CMD":1067,"Time":1001,"address":1,"slave":0,"bit":8,"status":0,"OK":0}` |

# UPDATE SCENARIO RELAX 
## 1 BR DIM 25%, BED HEAD OFF, SYM BRIGHT 25%
| Description | Payload |
|---------|-------------|
| BIT 1,2,3,5,10 25% 1BR | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":4,"type":1,"bit":1,"status":20,"OK":0}` |
| BIT 4,6,7,11,12 25% 1BR | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":4,"type":1,"bit":4,"status":64,"OK":0}` |
| BIT 13 OFF 1BR | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":4,"type":1,"bit":1,"status":20,"OK":0}` |
| SYM 0-1 BRIGHT 25% | `{"data":"sympScenario","CMD":1078,"Time":1001,"address":1,"slave":0,"scenario":4,"symphony":0,"R":255,"G":89,"B":11,"speed":35,"bright":64,"mode":1,"LedPoint":40,"OK":0}` |

# UPDATE SCENARIO BALCONY - STORAGE OFF 
## 1 BR SCENE READ, WORK, RELAX
| Description | Payload |
|---------|-------------|
| BIT 8 - Scenario 2,3,4 | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":2,"type":1,"bit":8,"status":0,"OK":0}` |
| BIT 9 - Scenario 2,3,4 | `{"data":"seqScenario","CMD":1077,"Time":1001,"address":1,"slave":0,"scenario":2,"type":1,"bit":9,"status":0,"OK":0}` |
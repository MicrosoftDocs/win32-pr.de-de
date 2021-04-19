---
description: Die phonefeature- \_ Konstanten Listen die Vorgänge auf, die auf einem Telefon mithilfe dieser API aufgerufen werden können. Jeder der phonefeature- \_ Werte (außer phonefeature \_ genericphone) entspricht einer TAPI-Funktion mit identischem oder ähnlichem Namen.
ms.assetid: 361b3080-3650-48a2-a1b7-f05d72777f9a
title: PHONEFEATURE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6e0333135df4185348f3471aa4184a0cd93e907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374043"
---
# <a name="phonefeature_-constants"></a>Phonefeature- \_ Konstanten

Die **phonefeature \_** -Konstanten Listen die Vorgänge auf, die auf einem Telefon mithilfe dieser API aufgerufen werden können. Jeder der phonefeature- \_ Werte (außer phonefeature \_ genericphone) entspricht einer TAPI-Funktion mit identischem oder ähnlichem Namen.



| Konstante/Wert                                                                                                                                                                                                                                                                            | BESCHREIBUNG                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PHONEFEATURE_GETBUTTONINFO"></span><span id="phonefeature_getbuttoninfo"></span><dl> <dt>**Phonefeature \_ Getbuttoninfo**</dt> <dt>0x00000001</dt> </dl>                      | [**phonegetbuttoninfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)<br/>                             |
| <span id="PHONEFEATURE_GETDATA"></span><span id="phonefeature_getdata"></span><dl> <dt>**Phonefeature \_ GetData**</dt> <dt>0x00000002</dt> </dl>                                        | [**phonegetdata**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata)<br/>                                         |
| <span id="PHONEFEATURE_GETDISPLAY"></span><span id="phonefeature_getdisplay"></span><dl> <dt>**Phonefeature \_ Getdisplay**</dt> <dt>0x00000004</dt> </dl>                               | [**phonegetdisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay)<br/>                                   |
| <span id="PHONEFEATURE_GETGAINHANDSET"></span><span id="phonefeature_getgainhandset"></span><dl> <dt>**Phonefeature \_ Getgainhandset**</dt> <dt>0x00000008</dt> </dl>                   | [**phonegetgewinn**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) phonehuokswitchdev- \_ Mobiltelefon<br/>             |
| <span id="PHONEFEATURE_GETGAINSPEAKER"></span><span id="phonefeature_getgainspeaker"></span><dl> <dt>**Phonefeature \_ Getgainspeaker**</dt> <dt>0x00000010</dt> </dl>                   | [**phonegetgewinn**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) phonehuokswitchdev- \_ Sprecher<br/>             |
| <span id="PHONEFEATURE_GETGAINHEADSET"></span><span id="phonefeature_getgainheadset"></span><dl> <dt>**Phonefeature \_ Getgainheadset**</dt> <dt>0x00000020</dt> </dl>                   | [**phonegetgewinn**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) phonehuokswitchdev- \_ Headset<br/>             |
| <span id="PHONEFEATURE_GETHOOKSWITCHHANDSET"></span><span id="phonefeature_gethookswitchhandset"></span><dl> <dt>**Phonefeature \_ Gethookswitchhandset**</dt> <dt>0x00000040</dt> </dl> | [**phonegethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) phonehuokswitchdev- \_ Mobiltelefon<br/> |
| <span id="PHONEFEATURE_GETHOOKSWITCHSPEAKER"></span><span id="phonefeature_gethookswitchspeaker"></span><dl> <dt>**Phonefeature \_ Gethookswitchspeaker**</dt> <dt>0x00000080</dt> </dl> | [**phonegethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) phonehuokswitchdev- \_ Mobiltelefon<br/> |
| <span id="PHONEFEATURE_GETHOOKSWITCHHEADSET"></span><span id="phonefeature_gethookswitchheadset"></span><dl> <dt>**Phonefeature \_ Gethookswitchheadset**</dt> <dt>0x00000100</dt> </dl> | [**phonegethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) phonehuokswitchdev- \_ Mobiltelefon<br/> |
| <span id="PHONEFEATURE_GETLAMP"></span><span id="phonefeature_getlamp"></span><dl> <dt>**Phonefeature \_ Getlamp**</dt> <dt>0x00000200</dt> </dl>                                        | [**phonegetlamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp)<br/>                                         |
| <span id="PHONEFEATURE_GETRING"></span><span id="phonefeature_getring"></span><dl> <dt>**Phonefeature \_ Getralling**</dt> <dt>0x00000400</dt> </dl>                                        | [**phonegetralling**](/windows/desktop/api/Tapi/nf-tapi-phonegetring)<br/>                                         |
| <span id="PHONEFEATURE_GETVOLUMEHANDSET"></span><span id="phonefeature_getvolumehandset"></span><dl> <dt>**Phonefeature \_ Getvolumehandset**</dt> <dt>0x00000800</dt> </dl>             | [**phonegetvolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) phonehuokswitchdev- \_ Mobiltelefon<br/>         |
| <span id="PHONEFEATURE_GETVOLUMESPEAKER"></span><span id="phonefeature_getvolumespeaker"></span><dl> <dt>**Phonefeature \_ Getvolumespeaker**</dt> <dt>0x00001000</dt> </dl>             | [**phonegetvolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) phonehuokswitchdev- \_ Sprecher<br/>         |
| <span id="PHONEFEATURE_GETVOLUMEHEADSET"></span><span id="phonefeature_getvolumeheadset"></span><dl> <dt>**Phonefeature \_ Getvolumeheadset**</dt> <dt>0x00002000</dt> </dl>             | [**phonegetvolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) phonehuokswitchdev- \_ Headset<br/>         |
| <span id="PHONEFEATURE_SETBUTTONINFO"></span><span id="phonefeature_setbuttoninfo"></span><dl> <dt>**Phonefeature \_ SetButtonInfo**</dt> <dt>0x00004000</dt> </dl>                      | [**phonesetbuttoninfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo)<br/>                             |
| <span id="PHONEFEATURE_SETDATA"></span><span id="phonefeature_setdata"></span><dl> <dt>**Phonefeature \_ SetData**</dt> <dt>0x00008000</dt> </dl>                                        | [**phonesetdata**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata)<br/>                                         |
| <span id="PHONEFEATURE_SETDISPLAY"></span><span id="phonefeature_setdisplay"></span><dl> <dt>**Phonefeature \_ Setdisplay**</dt> <dt>0x00010000 bis</dt> </dl>                               | [**phonesetdisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay)<br/>                                   |
| <span id="PHONEFEATURE_SETGAINHANDSET"></span><span id="phonefeature_setgainhandset"></span><dl> <dt>**Phonefeature \_ Setgainhandset**</dt> <dt>0x00020000</dt> </dl>                   | [**phonesetgewinn**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) phonehuokswitchdev- \_ Mobiltelefon<br/>             |
| <span id="PHONEFEATURE_SETGAINSPEAKER"></span><span id="phonefeature_setgainspeaker"></span><dl> <dt>**Phonefeature \_ Setgainspeaker**</dt> <dt>0x00040000</dt> </dl>                   | [**phonesetgewinn**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) phonehuokswitchdev- \_ Sprecher<br/>             |
| <span id="PHONEFEATURE_SETGAINHEADSET"></span><span id="phonefeature_setgainheadset"></span><dl> <dt>**Phonefeature \_ Setgainheadset**</dt> <dt>0x00080000</dt> </dl>                   | [**phonesetgewinn**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) phonehuokswitchdev- \_ Headset<br/>             |
| <span id="PHONEFEATURE_SETHOOKSWITCHHANDSET"></span><span id="phonefeature_sethookswitchhandset"></span><dl> <dt>**Phonefeature \_**</dt>"*", " <dt>00100000</dt> " </dl> | [**phonesethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) phonehuokswitchdev- \_ Mobiltelefon<br/> |
| <span id="PHONEFEATURE_SETHOOKSWITCHSPEAKER"></span><span id="phonefeature_sethookswitchspeaker"></span><dl> <dt>**Phonefeature \_**</dt>" <dt>00200000</dt> " für "" </dl> | [**phonesethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) phonehuokswitchdev- \_ Sprecher<br/> |
| <span id="PHONEFEATURE_SETHOOKSWITCHHEADSET"></span><span id="phonefeature_sethookswitchheadset"></span><dl> <dt>**Phonefeature \_**</dt>"*", " <dt>00400000</dt> " </dl> | [**phonesethookswitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) phonehuokswitchdev- \_ Headset<br/> |
| <span id="PHONEFEATURE_SETLAMP"></span><span id="phonefeature_setlamp"></span><dl> <dt>**Phonefeature \_ Setlamp**</dt> <dt>0x00800000</dt> </dl>                                        | [**phonesetlamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp)<br/>                                         |
| <span id="PHONEFEATURE_SETRING"></span><span id="phonefeature_setring"></span><dl> <dt>**Phonefeature \_**</dt>"- <dt>0x01000000</dt> " </dl>                                        | [**phonesetring**](/windows/desktop/api/Tapi/nf-tapi-phonesetring)<br/>                                         |
| <span id="PHONEFEATURE_SETVOLUMEHANDSET"></span><span id="phonefeature_setvolumehandset"></span><dl> <dt>**Phonefeature \_ Setvolumehandset**</dt> <dt>0x02000000</dt> </dl>             | [**phonesetvolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) phonehuokswitchdev- \_ Mobiltelefon<br/>         |
| <span id="PHONEFEATURE_SETVOLUMESPEAKER"></span><span id="phonefeature_setvolumespeaker"></span><dl> <dt>**Phonefeature \_ Setvolumespeaker**</dt> <dt>0x04000000</dt> </dl>             | [**phonesetvolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) phonehuokswitchdev- \_ Sprecher<br/>         |
| <span id="PHONEFEATURE_SETVOLUMEHEADSET"></span><span id="phonefeature_setvolumeheadset"></span><dl> <dt>**Phonefeature \_ Setvolumeheadset**</dt> <dt>0x08000000</dt> </dl>             | [**phonesetvolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) phonehuokswitchdev- \_ Headset<br/>         |
| <span id="PHONEFEATURE_GENERICPHONE"></span><span id="phonefeature_genericphone"></span><dl> <dt>**Phonefeature \_ Genericphone**</dt> <dt>0x10000000</dt> </dl>                         | (nur für Anwendungen relevant, die TAPI 3,0 und höher verwenden)<br/>                     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 





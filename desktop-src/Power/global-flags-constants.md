---
description: Die globalen Flagkonstanten werden verwendet, um Power Policy-Optionen für Benutzer zu aktivieren oder zu deaktivieren.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Globale Flagkonstanten (PowrProf.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2dfd23559959bee72e8572cc700a948df1e92dcdb37a03c41b52cdca4d578c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143531"
---
# <a name="global-flags-constants"></a>Globale Flagkonstanten

Die globalen Flagkonstanten werden verwendet, um Power Policy-Optionen für Benutzer zu aktivieren oder zu deaktivieren.



| Konstante/Wert                                                                                                                                                                                                                                                                                         | Beschreibung                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <dt>**EnableMultiBatteryDisplay-0x02**</dt> <dt></dt> </dl> | Aktiviert oder deaktiviert die Anzeige mehrerer Akkus im Systemleistungszähler.<br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <dt>**EnablePasswordLogon**</dt> <dt>0x04</dt> </dl>                         | Aktiviert oder deaktiviert die Kennwortanmeldung, wenn das System aus dem Standby- oder Ruhezustand fortgesetzt wird.<br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt> </dl> | Aktiviert oder deaktiviert das Akkustandssymbol in der Taskleiste. Wenn dieses Flag gelöscht wird, wird das Akkuzählersymbol nicht angezeigt.<br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <dt>**EnableVideoDimDisplay-0x10**</dt> <dt></dt> </dl>                 | Aktiviert oder deaktiviert die Unterstützung für das Abblenden der Videoanzeige, wenn sich das System von der Stromversorgung in den Akkubetrieb ändert.<br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <dt>**EnableWakeOnRing-0x08**</dt> <dt></dt> </dl>                                     | Aktiviert oder deaktiviert die Aktivierungsunterstützung für Ringe.<br/>                                                                                               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>PowrProf.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GLOBALE \_ \_ \_ BENUTZER-POWER POLICY**](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 





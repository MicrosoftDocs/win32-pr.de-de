---
title: Systemmonitor. updateingeterval (Eigenschaft)
description: Ruft den Zeitraum ab oder legt den Zeitraum fest, den sysmon wartet, bevor er das nächste Mal Daten sammelt und das Diagramm oder den Bericht aktualisiert.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Updateingeterval-Eigenschaft (Sysmon)
- Updateingeterval-Eigenschaft sysmon, Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, updateingeterval (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949801"
---
# <a name="systemmonitorupdateinterval-property"></a>Systemmonitor. updateingeterval (Eigenschaft)

Ruft den Zeitraum ab oder legt den Zeitraum fest, den sysmon wartet, bevor er das nächste Mal Daten sammelt und das Diagramm oder den Bericht aktualisiert.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a>Eigenschaftswert

Zeitraum (in Sekunden), den sysmon wartet, bevor er das nächste Mal Daten sammelt und das Diagramm oder den Bericht aktualisiert. Das minimale Intervall beträgt 1 Sekunde (Dies ist auch der Standardwert). Der Höchstwert ist 1 Million.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nur relevant, wenn [**Systemmonitor. ManualUpdate**](systemmonitor-manualupdate.md) auf false festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> </dl>

 

 






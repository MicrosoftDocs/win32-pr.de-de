---
title: Systemmonitor. monitordupli-Einhaltungen (Eigenschaft)
description: Ruft einen Wert ab, der bestimmt, ob mehrere Instanzen eines Leistungsindikators überwacht werden können, oder legt ihn fest.
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- Monitordupliplateinhaltungen-Eigenschaft (Sysmon)
- Monitordupliplateinhaltungen-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", monitordupliplateinhaltungen (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391810"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a>Systemmonitor. monitordupli-Einhaltungen (Eigenschaft)

Ruft einen Wert ab, der bestimmt, ob mehrere Instanzen eines Leistungsindikators überwacht werden können, oder legt ihn fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass mehrere Instanzen eines Zählers überwacht werden können ("true" ist die Standardeinstellung). False gibt an, dass nur eine Instanz eines Zählers überwacht werden kann.

## <a name="remarks"></a>Bemerkungen

Der System Monitor fügt \# n an jeden Instanznamen an, mit Ausnahme des ersten, wenn mehrere Instanzen vorhanden sind. Die Seriennummer n beginnt mit einem und wird für jede neue Instanz um eins erhöht. Wenn Sie z. b. " \\ Process ( \* ) \\ % Processor Time" angeben, sollte die zählungssammlung mehrere Instanzen von svchost enthalten. Das erste Vorkommen ist svchost, das nächste Vorkommen lautet svchost \# 1 usw.

Doppelte Instanzen werden nur überwacht, wenn Sie das Platzhalter Zeichen ( \* ) für den Instanznamen verwenden. Wenn Sie " \\ Process (SVCHOST) \\ % Processor Time" angegeben haben, wird nur die erste Instanz von svchost überwacht, nicht alle Instanzen von svchost.

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

 

 






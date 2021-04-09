---
title: Systemmonitor. MaximumScale (Eigenschaft)
description: Ruft den maximalen Wert der vertikalen Achse (Y-Achse) des Diagramms ab oder legt diesen fest.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- MaximumScale-Eigenschaft (Sysmon)
- MaximumScale-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, MaximumScale (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37740802fac4d89bbcbe9d5c105e357b55ab481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949745"
---
# <a name="systemmonitormaximumscale-property"></a>Systemmonitor. MaximumScale (Eigenschaft)

Ruft den maximalen Wert der vertikalen Achse (Y-Achse) des Diagramms ab oder legt diesen fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a>Eigenschaftswert

Positiver maximaler Wert der vertikalen Achse des Diagramms. Der maximale Standardwert für die vertikale Skala beträgt 100. Der niedrigste Wert, auf den Sie den maximalen Wert festlegen können, ist ein Wert, der größer als der [**MinimumScale**](systemmonitor-minimumscale.md) -Wert ist. Der höchste Wert, auf den Sie den maximalen Wert festlegen können, ist 999.999.999.

## <a name="remarks"></a>Bemerkungen

Das-Steuerelement passt automatisch die Position der Skalierungs Nummern an, die auf der vertikalen Skala entsprechend der Größe des angezeigten Steuer Elements angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**System Monitor**](systemmonitor.md)
</dt> <dt>

[**Systemmonitor. MinimumScale**](systemmonitor-minimumscale.md)
</dt> <dt>

[**Systemmonitor. showscalelabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 






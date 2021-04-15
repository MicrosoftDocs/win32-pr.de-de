---
title: Systemmonitor. MinimumScale (Eigenschaft)
description: Ruft den Mindestwert der vertikalen Achse (Y-Achse) des Diagramms ab oder legt diesen fest.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- MinimumScale-Eigenschaft (Sysmon)
- MinimumScale-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", MinimumScale-Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476575"
---
# <a name="systemmonitorminimumscale-property"></a>Systemmonitor. MinimumScale (Eigenschaft)

Ruft den Mindestwert der vertikalen Achse (Y-Achse) des Diagramms ab oder legt diesen fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a>Eigenschaftswert

Positiver Minimalwert der vertikalen Achse des Diagramms. Der Standard Minimalwert der vertikalen Skala ist 0 (null). Der höchste Wert, auf den der minimale Wert festgelegt werden kann, ist ein Wert kleiner als [**MaximumScale**](systemmonitor-maximumscale.md) .

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

[**Systemmonitor. MaximumScale**](systemmonitor-maximumscale.md)
</dt> <dt>

[**Systemmonitor. showscalelabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 






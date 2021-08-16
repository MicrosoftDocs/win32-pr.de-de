---
title: SystemMonitor.MaximumScale-Eigenschaft
description: Ruft den maximalen Wert der vertikalen Achse (Y) des Diagramms ab oder legt diese fest.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- MaximumScale-Eigenschaft SysMon
- MaximumScale-Eigenschaft SysMon , SystemMonitor-Klasse
- SystemMonitor-Klasse SysMon , MaximumScale-Eigenschaft
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
ms.openlocfilehash: 176ebab3b2879b3d158310ec61fa9e65df45f8b502029ede1c58c2c1dd33f225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882029"
---
# <a name="systemmonitormaximumscale-property"></a>SystemMonitor.MaximumScale-Eigenschaft

Ruft den maximalen Wert der vertikalen Achse (Y) des Diagramms ab oder legt diese fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a>Eigenschaftswert

Positiver Maximalwert der vertikalen Achse des Diagramms. Der Maximale Standardwert der vertikalen Skala ist 100. Der niedrigste Wert, auf den Sie den Maximalwert festlegen können, ist ein Wert, der größer als der [**MinimumScale-Wert**](systemmonitor-minimumscale.md) ist. Der höchste Wert, den Sie auf festlegen können, ist 999.999.999.

## <a name="remarks"></a>Hinweise

Das -Steuerelement passt die Position der auf der vertikalen Skala angezeigten Skalierungsnummern automatisch an die Größe des angezeigten Steuerelements an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.MinimumScale**](systemmonitor-minimumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 






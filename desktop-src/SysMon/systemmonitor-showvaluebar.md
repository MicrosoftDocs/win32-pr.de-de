---
title: SystemMonitor.ShowValueBar-Eigenschaft
description: Ruft einen Wert ab, der bestimmt, ob der Wertbalken (der Satz statistischer Werte unterhalb des Diagramms) auf dem Steuerelement angezeigt wird, oder legt diesen fest.
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- ShowValueBar-Eigenschaft SysMon
- ShowValueBar-Eigenschaft SysMon , SystemMonitor-Klasse
- SystemMonitor-Klasse SysMon , ShowValueBar-Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4ca65a3083a9c46b900d1791f79973fc61de2b7cfc552a3314ca8444e813602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954863"
---
# <a name="systemmonitorshowvaluebar-property"></a>SystemMonitor.ShowValueBar-Eigenschaft

Ruft einen Wert ab, der bestimmt, ob der Wertbalken (der Satz statistischer Werte unterhalb des Diagramms) auf dem Steuerelement angezeigt wird, oder legt diesen fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass die Wertleiste auf dem Steuerelement angezeigt wird. andernfalls FALSE. Der Standardwert dieser Eigenschaft ist „TRUE“.

## <a name="remarks"></a>Hinweise

Die angezeigten Statistiken enthalten den letzten Wert, den Durchschnittswert sowie die minimalen und maximalen Werte des aktuell ausgewählten Leistungsindikators im angezeigten Zeitintervall. Um die anzuzeigende Indikatorwerte auszuwählen, muss der Benutzer den Indikator im Legendenbereich des Steuerelements auswählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 






---
title: Systemmonitor. hervorzuheben (Eigenschaft)
description: Ruft einen Wert ab, der angibt, ob die Werte der ausgewählten Indikatoren im Diagramm hervorgehoben sind, oder legt diesen fest.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Eigenschaften-sysmon hervorheben
- Eigenschaften-sysmon, Systemmonitor-Klasse hervorheben
- Systemmonitor-Klasse (Sysmon), Eigenschaft hervorheben
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858916"
---
# <a name="systemmonitorhighlight-property"></a>Systemmonitor. hervorzuheben (Eigenschaft)

Ruft einen Wert ab, der angibt, ob die Werte der ausgewählten Indikatoren im Diagramm hervorgehoben sind, oder legt diesen fest.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass die Werte der ausgewählten Indikatoren im Diagramm hervorgehoben werden. andernfalls false. Der Standardwert ist False.

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen oder mehrere Leistungsindikatoren auswählen möchten, können [**Sie als "true" festlegen,**](counteritem-selected.md) oder der Benutzer kann die Indikatoren aus der Liste der in der Legende angezeigten Indikatoren auswählen.

**Vor Windows Vista:** Leistungsindikatoren können nicht Programm gesteuert ausgewählt werden, und der Benutzer kann nur einen Indikator aus der Liste der in der Legende angezeigten Indikatoren auswählen.

Die Hervorhebung kann abhängig vom Wert der [**BackColor**](systemmonitor-backcolor.md) -Eigenschaft schwarz oder weiß sein. Die Hervorhebung wird automatisch auf die Farbe festgelegt, die einen ausreichenden Kontrast zwischen Hervorhebungs Farbe und Hintergrundfarbe bereitstellt.

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

[**"Zählelement. ausgewählt"**](counteritem-selected.md)
</dt> </dl>

 

 






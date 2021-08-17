---
title: CounterItem.Color-Eigenschaft
description: Ruft die Farbe ab, die zum Diagramm des Indikatorwerts verwendet wird, oder legt diese fest.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Color-Eigenschaft SysMon
- Color-Eigenschaft SysMon , CounterItem-Klasse
- CounterItem-Klasse SysMon , Color-Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcc51862c57312f9b923ea6a80f9814182bbc6aef707dab994b135ace9637754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883867"
---
# <a name="counteritemcolor-property"></a>CounterItem.Color-Eigenschaft

Ruft die Farbe ab, die zum Diagramm des Indikatorwerts verwendet wird, oder legt diese fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a>Eigenschaftswert

Farbe, die zum Diagramm des Indikatorwerts verwendet wird.

## <a name="remarks"></a>Hinweise

Wenn Sie die zu verwendende Farbe nicht angeben, wählt SYSMON Farben für die ersten 16 Leistungsindikatoren aus. Wenn Sie mehr als 16 Leistungsindikatoren angeben, verwendet SYSMON die gleichen Farben wie die ersten 16 Leistungsindikatoren. Um die Leistungsindikatoren voneinander zu unterscheiden, [](counteritem-linestyle.md) ändert SYSMON den Linienstil, der für jedes Vielfache von 16 Leistungsindikatoren verwendet wird, bis zu den ersten 80 Leistungsindikatoren. Die ersten 16 Leistungsindikatoren verwenden z. B. einen durchgestrichenen Linienstil, die nächsten 16 einen Strichlinienstil und so weiter. SYSMON legt dann [](counteritem-width.md) die Linienbreite für die Leistungsindikatoren 81 bis 96 auf 2 und für die Leistungsindikatoren 96 bis 112 auf 3 fest. Wenn die Auflistung mehr als 112 Leistungsindikatoren enthält, enthalten die Leistungsindikatoren doppelte Werte für Farbe, Linienformat und Breite.

**Vor der Windows Vista:** Wenn Sie die zu verwendende Farbe nicht angeben, wählt SYSMON Farben für die ersten 16 Leistungsindikatoren aus. Wenn Sie mehr als 16 Leistungsindikatoren angeben, verwendet SYSMON die gleichen Farben wie die ersten 16 Leistungsindikatoren. Um die Leistungsindikatoren voneinander zu unterscheiden, [](counteritem-width.md) erhöht SYSMON die Linienbreite der ersten drei Leistungsindikatoren, die die gleiche Farbzuweisung erhalten. Wenn mehr als drei Leistungsindikatoren dieselbe Farbe verwenden, wählt SYSMON nach dem Zufallsprinzip die Linienbreite aus, die für den Zähler verwendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 






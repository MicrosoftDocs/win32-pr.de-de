---
title: Count. Color-Eigenschaft
description: Ruft die Farbe ab oder legt Sie fest, die zum Diagramm des Leistungsindikators verwendet wird.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Color-Eigenschaft (Sysmon)
- Color-Eigenschaft (Sysmon), ratteritem-Klasse
- Namteritem Class sysmon, Color-Eigenschaft
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
ms.openlocfilehash: ada0a2266c4cf53e9706f1330e2336e6a38386b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741920"
---
# <a name="counteritemcolor-property"></a>Count. Color-Eigenschaft

Ruft die Farbe ab oder legt Sie fest, die zum Diagramm des Leistungsindikators verwendet wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a>Eigenschaftswert

Die zum Diagramm des Leistungs Zählers verwendete Farbe.

## <a name="remarks"></a>Bemerkungen

Wenn Sie die zu verwendende Farbe nicht angeben, wählt sysmon Farben für die ersten 16 Indikatoren aus. Wenn Sie mehr als sechzehn Zähler angeben, werden die gleichen Farben von sysmon von den ersten 16 Leistungsindikatoren wieder verwendet. Um die Indikatoren voneinander zu unterscheiden, ändert sysmon den [**Linienstil**](counteritem-linestyle.md) , der für jedes Vielfache von sechzehn Leistungsindikatoren verwendet wird, bis zu den ersten 80-Leistungsindikatoren. Beispielsweise verwenden die ersten 16 Indikatoren eine solide Linienart, die nächsten sechzehn einen Strich Linienstil usw. Sysmon legt dann die [**Linien**](counteritem-width.md) Stärke auf 2 für die Leistungsindikatoren 81-96 und auf 3 für die Zähler 96-112 fest. Wenn die Sammlung mehr als 112 Leistungsindikatoren enthält, enthalten die Indikatoren doppelte Werte für Farbe, Linienart und Breite.

**Vor Windows Vista:** Wenn Sie die zu verwendende Farbe nicht angeben, wählt sysmon Farben für die ersten 16 Indikatoren aus. Wenn Sie mehr als sechzehn Zähler angeben, werden die gleichen Farben von sysmon von den ersten 16 Leistungsindikatoren wieder verwendet. Zur besseren Unterscheidung der Leistungsindikatoren erhöht sysmon die [**Linien**](counteritem-width.md) Stärke der ersten drei Leistungsindikatoren, die die gleiche Farb Zuweisung erhalten. Wenn mehr als drei Leistungsindikatoren dieselbe Farbe verwenden, wählt sysmon die für den Indikator zu verwendende Linienbreite nach dem Zufallsprinzip aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ratteritem**](counteritem.md)
</dt> </dl>

 

 






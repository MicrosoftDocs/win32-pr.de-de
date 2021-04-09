---
title: Count. Width-Eigenschaft
description: Ruft die Linienbreite ab, die zum Diagramm des Leistungsindikators verwendet wird, oder legt diese fest
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Width-Eigenschaft (Sysmon)
- Width-Eigenschaft (Sysmon), ratteritem-Klasse
- Namteritem Class sysmon, Width-Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741785"
---
# <a name="counteritemwidth-property"></a>Count. Width-Eigenschaft

Ruft die Linienbreite ab, die zum Diagramm des Leistungsindikators verwendet wird, oder legt diese fest

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Property Width As Long
```



## <a name="property-value"></a>Eigenschaftswert

In einem Liniendiagramm verwendete Linienstärke. Gültige Werte reichen von 1 bis 3, wobei 1 (der Standardwert) die enge Breite ist.

**Vor Windows Vista:** Gültige Werte liegen zwischen 1 und 9. Verwenden Sie keinen Wert für die Breite, der größer als 3 ist, wenn Ihre Anwendung unter Windows Vista ausgeführt wird.

## <a name="exceptions"></a>Ausnahmen



| Ausnahmetyp               | Bedingung                              |
|------------------------------|----------------------------------------|
| **System.ArgumentException** | Die angegebene Zeilenbreite ist ungültig. |



 

## <a name="remarks"></a>Bemerkungen

Die Standardlinien Stärke für die ersten 16 Leistungsindikatoren, die Sie hinzufügen, ist 1. Die Standardlinienbreite für die nächsten 16 Leistungsindikatoren (Zähler 17-32), die Sie hinzufügen, ist 2. Die Standardlinienbreite für die nächsten 16 Leistungsindikatoren (Zähler 33-48), die Sie hinzufügen, ist 3. Danach wählt sysmon die Linienbreite nach dem Zufallsprinzip aus. Weitere Informationen finden Sie unter " [**ratteritem. Color**](counteritem-color.md)".

Um einen anderen [**Linienstil**](counteritem-linestyle.md) als Solid anzugeben, muss die Breite 1 lauten. Wenn Sie einen Wert größer als 1 angeben und einen nicht einstufigen Linienstil angeben, ignoriert sysmon die angegebene Linienbreite.

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

 

 






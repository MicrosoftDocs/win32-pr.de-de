---
title: CounterItem.Width-Eigenschaft
description: Ruft die Linienbreite ab, die zum Graphen des Indikatorwerts verwendet wird, oder legt diese fest.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Width-Eigenschaft SysMon
- Width-Eigenschaft SysMon , CounterItem-Klasse
- CounterItem-Klasse SysMon , Width-Eigenschaft
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
ms.openlocfilehash: 5deca3d7fa188c834f2ca952c9b6c4760a3a1b56c83eb8250e343257b8108de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883506"
---
# <a name="counteritemwidth-property"></a>CounterItem.Width-Eigenschaft

Ruft die Linienbreite ab, die zum Graphen des Indikatorwerts verwendet wird, oder legt diese fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Property Width As Long
```



## <a name="property-value"></a>Eigenschaftswert

In einem Liniendiagramm verwendete Linienbreite. Gültige Werte liegen zwischen 1 und 3, wobei 1 (Standardwert) die kleinste Breite ist.

**Vor Windows Vista:** Gültige Werte liegen zwischen 1 und 9. Verwenden Sie keinen Breitenwert größer als 3, wenn Ihre Anwendung auf Windows Vista ausgeführt wird.

## <a name="exceptions"></a>Ausnahmen



| Ausnahmetyp               | Bedingung                              |
|------------------------------|----------------------------------------|
| **System.ArgumentException** | Die angegebene Linienbreite ist ungültig. |



 

## <a name="remarks"></a>Hinweise

Die Standardlinienbreite für die ersten 16 Leistungsindikatoren, die Sie hinzufügen, ist 1. Die Standardlinienbreite für die nächsten 16 Indikatoren (Indikatoren 17 bis 32), die Sie hinzufügen, ist 2. Die Standardlinienbreite für die nächsten 16 Indikatoren (Indikatoren 33 bis 48), die Sie hinzufügen, ist 3. Anschließend wählt SYSMON nach dem Zufallsprinzip die Linienbreite aus. Weitere Informationen finden Sie unter [**CounterItem.Color**](counteritem-color.md).

Um einen anderen [**Linienstil**](counteritem-linestyle.md) als "solid" anzugeben, muss die Breite 1 sein. Wenn Sie einen Wert größer als 1 und einen nicht durchgezogenen Linienstil angeben, ignoriert SYSMON die angegebene Linienbreite.

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

 

 






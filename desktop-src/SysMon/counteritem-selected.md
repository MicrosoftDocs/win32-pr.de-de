---
title: CounterItem.Selected-Eigenschaft
description: Ruft einen Wert ab, der angibt, ob der Zähler ausgewählt ist, oder legt diesen fest.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Ausgewählte SysMon-Eigenschaft
- Ausgewählte SysMon-Eigenschaft, CounterItem-Objekt
- CounterItem-Objekt SysMon , Selected-Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e5cfcc65c54f882f10e87a0f2aaebad0e1a55c94b6581031b034799987bc6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956959"
---
# <a name="counteritemselected-property"></a>CounterItem.Selected-Eigenschaft

Ruft einen Wert ab, der angibt, ob der Zähler ausgewählt ist, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True, wenn der Zähler ausgewählt ist. andernfalls FALSE.

## <a name="remarks"></a>Hinweise

Sie können einen oder mehrere Leistungsindikatoren aus der Sammlung von Indikatoren auswählen. Wenn Sie einen Indikator auswählen, wählt den Indikator in der Legende aus, macht den Indikator in der Legende sichtbar und generiert ein [**OnCounterSelected-Ereignis.**](-systemmonitor-oncounterselected.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 






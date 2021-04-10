---
title: Count. Selected-Eigenschaft
description: Ruft einen Wert ab, der angibt, ob der Leistungsindikators ausgewählt ist, oder legt ihn fest
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Ausgewählte Eigenschaften-sysmon
- Ausgewählte Eigenschaft "sysmon", "zähltem"-Objekt
- Objekt "sysmon" für das-Objekt, ausgewählte Eigenschaft
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
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956571"
---
# <a name="counteritemselected-property"></a>Count. Selected-Eigenschaft

Ruft einen Wert ab, der angibt, ob der Leistungsindikators ausgewählt ist, oder legt ihn fest

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True, wenn der Counter ausgewählt ist. andernfalls false.

## <a name="remarks"></a>Bemerkungen

Sie können einen oder mehrere Indikatoren aus der Sammlung der Leistungsindikatoren auswählen. Wenn Sie einen Indikator auswählen, wählt den Indikator in der Legende aus, macht den Indikator in der Legende sichtbar und generiert ein [**oncounterselected**](-systemmonitor-oncounterselected.md) -Ereignis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ratteritem**](counteritem.md)
</dt> </dl>

 

 






---
title: TriggerCollection. Item-Eigenschaft
description: Ruft bei der Skripterstellung den angegebenen-Auslösers aus der Auflistung ab.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Element Eigenschaft Taskplaner
- Element Eigenschaft Taskplaner, TriggerCollection-Objekt
- TriggerCollection-Objekt Taskplaner, Element Eigenschaft
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740776"
---
# <a name="triggercollectionitem-property"></a>TriggerCollection. Item-Eigenschaft

Ruft bei der Skripterstellung den angegebenen-Auslösers aus der Auflistung ab.

## <a name="syntax"></a>Syntax


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**Auslöserobjekt**](trigger.md) , das den angeforderten-Auslösers darstellt

## <a name="remarks"></a>Bemerkungen

Sammlungen sind 1-basiert. Anders ausgedrückt: der Index für das erste Element in der Auflistung ist 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






---
title: TriggerCollection.Item-Eigenschaft
description: Ruft für die Skripterstellung den angegebenen Trigger aus der Auflistung ab.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Elementeigenschaft Taskplaner
- Item-Eigenschaft Taskplaner , TriggerCollection-Objekt
- TriggerCollection-Objekt Taskplaner , Item-Eigenschaft
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
ms.openlocfilehash: aee0460d79ef239c8dacbf7fbd45573dac8ba03ad9b53e6e9881dded1bf01030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001958"
---
# <a name="triggercollectionitem-property"></a>TriggerCollection.Item-Eigenschaft

Ruft für die Skripterstellung den angegebenen Trigger aus der Auflistung ab.

## <a name="syntax"></a>Syntax


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**Trigger-Objekt,**](trigger.md) das den angeforderten Trigger darstellt.

## <a name="remarks"></a>Hinweise

Auflistungen sind 1-basiert. Anders ausgedrückt: Der Index für das erste Element in der Auflistung ist 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






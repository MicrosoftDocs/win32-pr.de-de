---
title: RunningTaskCollection.Item-Eigenschaft
description: Ruft für die Skripterstellung den angegebenen Task aus der Auflistung ab.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Elementeigenschaft Taskplaner
- Item-Eigenschaft Taskplaner , RunningTaskCollection-Objekt
- RunningTaskCollection-Objekt Taskplaner , Item-Eigenschaft
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7e2ca7abf5f1daa936509d5fae71211e8b139537fa1782daac6c08bf9a1017f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866780"
---
# <a name="runningtaskcollectionitem-property"></a>RunningTaskCollection.Item-Eigenschaft

Ruft für die Skripterstellung den angegebenen Task aus der Auflistung ab.

## <a name="syntax"></a>Syntax


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**RunningTask-Objekt,**](runningtask.md) das den angeforderten Kontext enthält.

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

 

 






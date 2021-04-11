---
title: Runningtaskcollection. Item-Eigenschaft
description: Ruft bei der Skripterstellung die angegebene Aufgabe aus der Auflistung ab.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Element Eigenschaft Taskplaner
- Item-Eigenschaft Taskplaner, runningtaskcollection-Objekt
- Runningtaskcollection-Objekt Taskplaner, Element Eigenschaft
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
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104649"
---
# <a name="runningtaskcollectionitem-property"></a>Runningtaskcollection. Item-Eigenschaft

Ruft bei der Skripterstellung die angegebene Aufgabe aus der Auflistung ab.

## <a name="syntax"></a>Syntax


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**runningtask**](runningtask.md) -Objekt, das den angeforderten Kontext enthält.

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

 

 






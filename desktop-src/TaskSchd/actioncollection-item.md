---
title: ActionCollection.Item-Eigenschaft
description: Für die Skripterstellung ruft eine angegebene Aktion aus der Auflistung ab.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Elementeigenschafts-Taskplaner
- Elementeigenschaft Taskplaner , ActionCollection-Objekt
- ActionCollection-Objekt Taskplaner , Item-Eigenschaft
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff95b707a4a99ce54cba4d175ce9fd094f7a6bd400147d7942a42a39d65bb7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796640"
---
# <a name="actioncollectionitem-property"></a>ActionCollection.Item-Eigenschaft

Für die Skripterstellung ruft eine angegebene Aktion aus der Auflistung ab.

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**Action-Objekt,**](action.md) das die angeforderte Aktion darstellt.

## <a name="remarks"></a>Hinweise

Sammlungen sind 1-basiert. Anders ausgedrückt: Der Index für das erste Element in der Auflistung ist 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 






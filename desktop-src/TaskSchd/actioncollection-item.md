---
title: Aktions Collection. Item-Eigenschaft
description: Ruft bei der Skripterstellung eine angegebene Aktion aus der Auflistung ab.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Element Eigenschaft Taskplaner
- Item-Eigenschaft Taskplaner, Aktions Sammlungsobjekt
- Aktions Sammlungsobjekt Taskplaner, Element Eigenschaft
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
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392089"
---
# <a name="actioncollectionitem-property"></a>Aktions Collection. Item-Eigenschaft

Ruft bei der Skripterstellung eine angegebene Aktion aus der Auflistung ab.

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**Aktions**](action.md) Objekt, das die angeforderte Aktion darstellt.

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
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 






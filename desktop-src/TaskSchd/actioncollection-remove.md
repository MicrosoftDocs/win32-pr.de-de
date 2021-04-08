---
title: Aktioncollection. Remove-Methode
description: Entfernt bei der Skripterstellung die angegebene Aktion aus der Auflistung.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Remove-Methode Taskplaner
- Remove-Methode Taskplaner, Aktions Sammlungsobjekt
- Aktions Sammlungsobjekt Taskplaner, Methode entfernen
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e110f870f4f192051b47cb3b65f0ebb41a490708
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742464"
---
# <a name="actioncollectionremove-method"></a>Aktioncollection. Remove-Methode

Entfernt bei der Skripterstellung die angegebene Aktion aus der Auflistung.

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Der Index der zu entfernenden Aktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Beachten Sie beim Entfernen von Elementen, dass der Index für das erste Element in der Auflistung 1 ist und der Index für das letzte Element der Wert der Eigenschaft " [**Aktions Auflistung. count**](actioncollection-count.md) " ist.

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

 

 






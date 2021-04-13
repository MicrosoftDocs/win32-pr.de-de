---
title: TriggerCollection. Remove-Methode
description: Bei der Skripterstellung wird der angegebene Trigger aus der Auflistung der vom Task verwendeten Trigger entfernt.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- Trigger Taskplaner, entfernen
- Remove-Methode Taskplaner
- Remove-Methode Taskplaner, TriggerCollection-Objekt
- TriggerCollection-Objekt Taskplaner, Methode entfernen
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340608"
---
# <a name="triggercollectionremove-method"></a>TriggerCollection. Remove-Methode

Bei der Skripterstellung wird der angegebene Trigger aus der Auflistung der vom Task verwendeten Trigger entfernt.

## <a name="syntax"></a>Syntax


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Der Index des zu entfernenden Auslösers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Beachten Sie beim Entfernen von Elementen, dass der Index für das erste Element in der Auflistung 1 ist und der Index für das letzte Element der Wert der [**TriggerCollection. count**](triggercollection-count.md) -Eigenschaft ist.

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

 

 






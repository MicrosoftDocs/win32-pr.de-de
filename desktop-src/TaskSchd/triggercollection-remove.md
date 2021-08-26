---
title: TriggerCollection.Remove-Methode
description: Für die Skripterstellung entfernt den angegebenen Trigger aus der Auflistung der von der Aufgabe verwendeten Trigger.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- löst Taskplaner aus und entfernt
- Entfernen von methoden Taskplaner
- Entfernen der Methode Taskplaner , TriggerCollection-Objekt
- TriggerCollection-Objekt Taskplaner , Remove-Methode
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
ms.openlocfilehash: d1ff3fda5119f4b487ba7f04546ea94e0a601a4749e1aa6aad7a9120907cd6cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099644"
---
# <a name="triggercollectionremove-method"></a>TriggerCollection.Remove-Methode

Für die Skripterstellung entfernt den angegebenen Trigger aus der Auflistung der von der Aufgabe verwendeten Trigger.

## <a name="syntax"></a>Syntax


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Der Index des zu entfernenden Triggers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Beachten Sie beim Entfernen von Elementen, dass der Index für das erste Element in der Auflistung 1 und der Index für das letzte Element der Wert der [**TriggerCollection.Count-Eigenschaft**](triggercollection-count.md) ist.

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

 

 






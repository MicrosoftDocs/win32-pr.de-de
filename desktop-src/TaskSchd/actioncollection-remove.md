---
title: ActionCollection.Remove-Methode
description: Für Skripts entfernt die angegebene Aktion aus der Auflistung.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Entfernen von methoden Taskplaner
- Entfernen der Methode Taskplaner , ActionCollection-Objekt
- ActionCollection-Objekt Taskplaner , Remove-Methode
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
ms.openlocfilehash: c0c176f41c59bd473e25e82082ada1934a25641e6144f4187e7f25075779b25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011740"
---
# <a name="actioncollectionremove-method"></a>ActionCollection.Remove-Methode

Für Skripts entfernt die angegebene Aktion aus der Auflistung.

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Der Index der zu entfernenden Aktion.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Beachten Sie beim Entfernen von Elementen, dass der Index für das erste Element in der Auflistung 1 und der Index für das letzte Element der Wert der [**ActionCollection.Count-Eigenschaft**](actioncollection-count.md) ist.

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
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 






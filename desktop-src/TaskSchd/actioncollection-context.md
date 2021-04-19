---
title: Eigenschaft "Aktions Sammlung. Context"
description: Ruft bei der Skripterstellung den Bezeichner des Prinzipals für den Task ab oder legt ihn fest.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- Kontext Eigenschaft Taskplaner
- Kontext Eigenschaft Taskplaner, Aktions Sammlungsobjekt
- Aktions Sammlungsobjekt Taskplaner, Kontext Eigenschaft
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339349"
---
# <a name="actioncollectioncontext-property"></a>Eigenschaft "Aktions Sammlung. Context"

Ruft bei der Skripterstellung den Bezeichner des Prinzipals für den Task ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Bezeichner des Prinzipals für die Aufgabe. Der hier angegebene Bezeichner muss mit dem Bezeichner identisch sein, der in der ID-Eigenschaft der IPrincipal-Schnittstelle angegeben ist, die den Prinzipal definiert.

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

 

 






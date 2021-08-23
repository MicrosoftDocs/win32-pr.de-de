---
title: ActionCollection.Context-Eigenschaft
description: Für die Skripterstellung ruft den Bezeichner des Prinzipals für die Aufgabe ab oder legt diesen fest.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- Kontexteigenschafts-Taskplaner
- Kontexteigenschaft Taskplaner , ActionCollection-Objekt
- ActionCollection-Objekt Taskplaner , Context-Eigenschaft
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
ms.openlocfilehash: ff495e4ef2742a6a05570308f2976c014026941d290d44c39bdd087ce3e13a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772750"
---
# <a name="actioncollectioncontext-property"></a>ActionCollection.Context-Eigenschaft

Für die Skripterstellung ruft den Bezeichner des Prinzipals für die Aufgabe ab oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Bezeichner des Prinzipals für die Aufgabe. Der hier angegebene Bezeichner muss mit dem Bezeichner übereinstimmen, der in der Id-Eigenschaft der IPrincipal-Schnittstelle angegeben ist, die den Prinzipal definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 






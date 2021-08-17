---
title: RegistrationInfo.Version-Eigenschaft
description: Ruft für die Skripterstellung die Versionsnummer des Tasks ab oder legt sie fest.
ms.assetid: 5f200948-b4ff-495c-9578-2a93b34fd75b
keywords:
- Versionseigenschaft Taskplaner
- Versionseigenschaft Taskplaner , RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner , Version-Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.Version
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08ef170004b7c9791f18cf65360c2446d5c87a6b835fb6fbcb048f47892c470
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059988"
---
# <a name="registrationinfoversion-property"></a>RegistrationInfo.Version-Eigenschaft

Ruft für die Skripterstellung die Versionsnummer des Tasks ab oder legt sie fest.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Version As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Versionsnummer des Tasks.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Versionsnummer des Tasks mithilfe des [**Versionselements**](taskschedulerschema-version-registrationinfotype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






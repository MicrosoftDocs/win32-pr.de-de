---
title: RegistrationInfo.SecurityDescriptor-Eigenschaft
description: Ruft für die Skripterstellung den Sicherheitsdeskriptor der Aufgabe ab oder legt diese fest.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- SecurityDescriptor-Eigenschaft Taskplaner
- SecurityDescriptor-Eigenschaft Taskplaner , RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner , SecurityDescriptor-Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c3aa83bc05952007d9114ad9812068de5b5b0bd82a4ce9e14e4d5ba1025bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759561"
---
# <a name="registrationinfosecuritydescriptor-property"></a>RegistrationInfo.SecurityDescriptor-Eigenschaft

Ruft für die Skripterstellung den Sicherheitsdeskriptor der Aufgabe ab oder legt diese fest. Wenn während der Aufgabenregistrierung ein anderer Sicherheitsdeskriptor angegeben wird, wird der mit dieser Eigenschaft festgelegte Sicherheitsdeskriptor ersetzt.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Sicherheitsdeskriptor, der der Aufgabe zugeordnet ist.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Sicherheitsdeskriptor des Tasks mithilfe des [**SecurityDescriptor-Elements**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) des Taskplaner Schemas angegeben.

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

 

 






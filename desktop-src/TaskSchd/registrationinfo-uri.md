---
title: RegistrationInfo.URI(Eigenschaft)
description: Für die Skripterstellung ruft den URI der Aufgabe ab oder legt diesen fest.
ms.assetid: 49085ee4-65e1-412c-ac1c-9c0f9efe5679
keywords:
- URI-Taskplaner
- URI-Eigenschaft Taskplaner , RegistrationInfo-Objekt
- RegistrationInfo-Taskplaner , URI-Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.URI
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c34c5dee30115ee430ad072d26e4bd67879988a9f2633cf9da9304e31324b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034080"
---
# <a name="registrationinfouri-property"></a>RegistrationInfo.URI(Eigenschaft)

Für die Skripterstellung ruft den URI der Aufgabe ab oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.URI As String
```



## <a name="property-value"></a>Eigenschaftswert

Der URI der Aufgabe.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Task-URI mithilfe des [**URI-Elements**](taskschedulerschema-uri-registrationinfotype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 






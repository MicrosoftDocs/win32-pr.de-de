---
title: RegistrationInfo.Date-Eigenschaft
description: Ruft für die Skripterstellung das Datum und die Uhrzeit der Registrierung des Tasks ab oder legt diese fest.
ms.assetid: ecff01b6-a1de-458a-9728-34169f17d42b
keywords:
- Taskplaner der Date-Eigenschaft
- Date-Eigenschaft Taskplaner , RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner , Date-Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.Date
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc0982eeba16d5760af5ba4a7334ed3e5050b3b730d727f7a10cb4b4a260d956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059998"
---
# <a name="registrationinfodate-property"></a>RegistrationInfo.Date-Eigenschaft

Ruft für die Skripterstellung das Datum und die Uhrzeit der Registrierung des Tasks ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Date As String
```



## <a name="property-value"></a>Eigenschaftswert

Das Registrierungsdatum der Aufgabe.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Registrierungsdatum mit dem [**Date-Element**](taskschedulerschema-date-registrationinfotype-element.md) des Taskplaner Schemas angegeben.

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

 

 






---
title: RegistrationInfo. Version (Eigenschaft)
description: Ruft die Versionsnummer der Aufgabe für die Skripterstellung ab oder legt Sie fest.
ms.assetid: 5f200948-b4ff-495c-9578-2a93b34fd75b
keywords:
- Versions Eigenschaft Taskplaner
- Versions Eigenschaft Taskplaner, RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner, Version-Eigenschaft
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
ms.openlocfilehash: 4c312878383c5361317a765cbf84a503244c188a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040284"
---
# <a name="registrationinfoversion-property"></a>RegistrationInfo. Version (Eigenschaft)

Ruft die Versionsnummer der Aufgabe für die Skripterstellung ab oder legt Sie fest.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Version As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Versionsnummer der Aufgabe.

## <a name="remarks"></a>Bemerkungen

Wenn Sie XML für eine Aufgabe lesen oder schreiben, wird die Versionsnummer der Aufgabe mit dem [**Versions**](taskschedulerschema-version-registrationinfotype-element.md) Element des Taskplaner Schemas angegeben.

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

 

 






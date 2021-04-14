---
title: RegistrationInfo. Uri (Eigenschaft)
description: Bei der Skripterstellung wird der URI der Aufgabe abgerufen oder festgelegt.
ms.assetid: 49085ee4-65e1-412c-ac1c-9c0f9efe5679
keywords:
- Uri-Eigenschaft Taskplaner
- Uri-Eigenschaft Taskplaner, RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner, Uri-Eigenschaft
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
ms.openlocfilehash: 77598d556fdec29f41004529471c8098314a6faf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518494"
---
# <a name="registrationinfouri-property"></a>RegistrationInfo. Uri (Eigenschaft)

Bei der Skripterstellung wird der URI der Aufgabe abgerufen oder festgelegt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.URI As String
```



## <a name="property-value"></a>Eigenschaftswert

Der URI der Aufgabe.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Task-URI mit dem [**URI**](taskschedulerschema-uri-registrationinfotype-element.md) -Element des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 






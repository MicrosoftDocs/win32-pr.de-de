---
title: RegistrationInfo. Date (Eigenschaft)
description: Ruft bei der Skripterstellung das Datum und die Uhrzeit der Registrierung der Aufgabe ab oder legt diese fest.
ms.assetid: ecff01b6-a1de-458a-9728-34169f17d42b
keywords:
- Date-Eigenschaft Taskplaner
- Date-Eigenschaft Taskplaner, RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner, Date-Eigenschaft
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
ms.openlocfilehash: adfdfa8b2dd3f8dcaa3b2fd5778b1e50dabfab51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340303"
---
# <a name="registrationinfodate-property"></a>RegistrationInfo. Date (Eigenschaft)

Ruft bei der Skripterstellung das Datum und die Uhrzeit der Registrierung der Aufgabe ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Date As String
```



## <a name="property-value"></a>Eigenschaftswert

Das Registrierungsdatum der Aufgabe.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Registrierungsdatum mit dem [**Date**](taskschedulerschema-date-registrationinfotype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 






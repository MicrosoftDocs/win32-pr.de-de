---
title: Logonauslöst. UserId-Eigenschaft
description: Ruft bei der Skripterstellung den Bezeichner des Benutzers ab oder legt ihn fest.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- UserID-Eigenschaft Taskplaner
- UserID-Eigenschaft Taskplaner, LOGON-Auslöserobjekt
- Logon-Auslöserobjekt Taskplaner, UserID-Eigenschaft
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391636"
---
# <a name="logontriggeruserid-property"></a>Logonauslöst. UserId-Eigenschaft

Ruft bei der Skripterstellung den Bezeichner des Benutzers ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Bezeichner des Benutzers. Beispiel: "mydomain \\ myname" oder für ein lokales Konto "Administrator".

Diese Eigenschaft kann in einem der folgenden Formate vorliegen:

-   Benutzername oder SID: der Task wird gestartet, wenn sich der Benutzer am Computer anmeldet.
-   NULL: der Task wird gestartet, wenn sich ein Benutzer am Computer anmeldet.

## <a name="remarks"></a>Bemerkungen

Wenn ein Task ausgelöst werden soll, wenn sich ein Mitglied einer Gruppe beim Computer anmeldet, anstatt sich zu anmelden, wenn sich ein bestimmter Benutzer anmeldet, weisen Sie der **logontrigger. UserID** -Eigenschaft keinen Wert zu. Erstellen Sie stattdessen einen LOGON-und eine leere **logonauslöst. UserID** -Eigenschaft, und weisen Sie dem Prinzipal für die Aufgabe mithilfe der [**Principal. GroupID**](principal-groupid.md) -Eigenschaft einen Wert zu.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Anmelde Benutzer-ID mit dem [**UserID**](taskschedulerschema-userid-logontriggertype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Logonauslöst**](logontrigger.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






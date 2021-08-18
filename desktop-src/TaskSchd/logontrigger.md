---
title: LogonTrigger-Objekt
description: Skripterstellungsobjekt, das einen Trigger darstellt, der eine Aufgabe startet, wenn sich ein Benutzer anmeldet.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- Logon trigger Taskplaner , object
- LogonTrigger-Taskplaner
- LogonTrigger-Objekt Taskplaner , beschrieben
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aed10ba9c0c792a5e4f882988ca07770c4ac568cb893b8ffac16a3a24efd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760097"
---
# <a name="logontrigger-object"></a>LogonTrigger-Objekt

Skripterstellungsobjekt, das einen Trigger darstellt, der eine Aufgabe startet, wenn sich ein Benutzer anmeldet. Wenn der Taskplaner-Dienst gestartet wird, werden alle angemeldeten Benutzer aufzählt, und alle mit Anmeldetriggern registrierten Aufgaben, die mit dem angemeldeten Benutzer übereinstimmen, werden ausgeführt.

## <a name="members"></a>Member

Das **LogonTrigger-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **LogonTrigger-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | Beschreibung                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](logontrigger-delay.md)<br/>                      | Lesen/Schreiben<br/> | Ruft einen Wert ab, der die Zeit zwischen der Anmeldung des Benutzers und dem Start des Auftrags angibt, oder legt diesen fest.<br/>                                                                              |
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft einen booleschen Wert ab, der angibt, ob der Trigger aktiviert ist, oder legt diesen fest.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft das Datum und die Uhrzeit der Deaktivierung des Triggers ab oder legt diese fest. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft die maximale Zeitdauer ab, für die die vom Trigger gestartete Aufgabe ausgeführt werden darf, oder legt diese fest.<br/>                                         |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft den Bezeichner für den Trigger ab oder legt den Bezeichner fest.<br/>                                                                                             |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft einen Wert ab, der angibt, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde, oder legt diesen fest.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft das Datum und die Uhrzeit der Aktivierung des Triggers ab oder legt diese fest.<br/>                                                                            |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Geerbt vom [**Trigger-Objekt.**](trigger.md) Ruft den Typ des Triggers ab.<br/>                                                                                                            |
| [**Userid**](logontrigger-userid.md)<br/>                    | Lesen/Schreiben<br/> | Ruft den Bezeichner des Benutzers ab oder legt ihn fest.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Hinweise

Wenn Sie möchten, dass eine Aufgabe ausgelöst wird, wenn sich ein Mitglied einer Gruppe am Computer anmeldet, anstatt wenn sich ein bestimmter Benutzer anmeldet, weisen Sie der [**LogonTrigger.UserId-Eigenschaft**](logontrigger-userid.md) keinen Wert zu. Erstellen Sie stattdessen einen Logon-Trigger mit einer leeren **LogonTrigger.UserId-Eigenschaft,** und weisen Sie dem Prinzipal mithilfe der [**Principal.GroupId-Eigenschaft**](principal-groupid.md) einen Wert für den Task zu.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird mithilfe des [**LogonTrigger-Elements**](taskschedulerschema-logontrigger-triggergroup-element.md) des Taskplaner angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Logon Trigger Example (Scripting) .](logon-trigger-example--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Trigger**](trigger.md)
</dt> </dl>

 

 






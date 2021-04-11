---
title: Logon-Auslöserobjekt
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn sich ein Benutzer anmeldet.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- Logon-auslöserTaskplaner, Objekt
- Logon-Auslöserobjekt Taskplaner
- Logon-Auslöserobjekt Taskplaner, beschrieben
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
ms.openlocfilehash: 9b9c4b2031b39a6dfd483b039023ad9114271b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956766"
---
# <a name="logontrigger-object"></a>Logon-Auslöserobjekt

Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn sich ein Benutzer anmeldet. Wenn der Taskplaner-Dienst gestartet wird, werden alle angemeldeten Benutzer aufgezählt, und alle mit LOGON-Triggern registrierten Tasks, die dem angemeldeten Benutzer entsprechen, werden ausgeführt.

## <a name="members"></a>Member

Das **Logon-Auslöserobjekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Logon-Auslöserobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](logontrigger-delay.md)<br/>                      | Lesen/Schreiben<br/> | Ruft einen Wert ab oder legt einen Wert fest, der die Zeitspanne zwischen dem Zeitpunkt der Anmeldung des Benutzers und dem Start des Auftrags angibt.<br/>                                                                              |
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.<br/>                                                              |
| [**Endgrenze**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/>               |
| [**Executiontimelimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.<br/>                                         |
| [**Name**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Bezeichner für den-Typ ab oder legt ihn fest.<br/>                                                                                             |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.<br/>                                                                            |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Typ des Auslösers ab.<br/>                                                                                                            |
| [**UserID**](logontrigger-userid.md)<br/>                    | Lesen/Schreiben<br/> | Ruft den Bezeichner des Benutzers ab oder legt ihn fest.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein Task ausgelöst werden soll, wenn sich ein Mitglied einer Gruppe beim Computer anmeldet, anstatt sich zu anmelden, wenn sich ein bestimmter Benutzer anmeldet, weisen Sie der [**logontrigger. UserID**](logontrigger-userid.md) -Eigenschaft keinen Wert zu. Erstellen Sie stattdessen einen LOGON-und eine leere **logonauslöst. UserID** -Eigenschaft, und weisen Sie dem Prinzipal für die Aufgabe mithilfe der [**Principal. GroupID**](principal-groupid.md) -Eigenschaft einen Wert zu.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird ein LOGON-Vorgang mit dem [**Logon-Auslöserelement**](taskschedulerschema-logontrigger-triggergroup-element.md) des Taskplaner-Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [Logon-auslöserbeispiel (Skripterstellung)](logon-trigger-example--scripting-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Trigger**](trigger.md)
</dt> </dl>

 

 






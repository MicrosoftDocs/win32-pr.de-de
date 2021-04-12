---
title: Registration-Auslöserobjekt
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn der Task registriert oder aktualisiert wird.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- Taskplaner des Registrierungs Auslösers, Objekt
- Registration-Auslöserobjekt Taskplaner
- Registration-Auslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08bf84fa92b1736b2989c1920abb8f0af2c0b97c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518080"
---
# <a name="registrationtrigger-object"></a>Registration-Auslöserobjekt

Skript Objekt, das einen-Auslösers darstellt, der einen Task startet, wenn der Task registriert oder aktualisiert wird.

## <a name="members"></a>Member

Das **Registration-Auslöserobjekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Registration-Auslöserobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](registrationtrigger-delay.md)<br/>               | Lesen/Schreiben<br/> | Ruft die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe ab oder legt diese fest.<br/>                                                                                |
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.<br/>                                                |
| [**Endgrenze**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/> |
| [**Executiontimelimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.<br/>                           |
| [**Name**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Bezeichner für den-Typ ab oder legt ihn fest.<br/>                                                                               |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.<br/>                                                              |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Typ des Auslösers ab.<br/>                                                                                              |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen eigenen XML-Code für eine Aufgabe erstellen, wird mit dem [**Registration-Auslöserelement**](taskschedulerschema-registrationtrigger-triggergroup-element.md) des Taskplaner Schemas ein Registrierungs--Vorgang angegeben.

Wenn eine Aufgabe mit einem verzögerten Registrierungs Ausfall registriert ist und der Computer, auf dem der Task registriert ist, während der Verzögerung heruntergefahren oder neu gestartet wird, bevor der Task ausgeführt wird, wird der Task nicht ausgeführt, und die Verzögerung geht verloren.

## <a name="examples"></a>Beispiele

Weitere Informationen und ein Codebeispiel für dieses Skript Objekt finden Sie unter [Beispiel für Registrierungs Beispiel (Skripterstellung)](registration-trigger-example--scripting-.md).

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
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 






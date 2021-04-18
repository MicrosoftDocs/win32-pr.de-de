---
title: Sessionstatechange-Objekt
description: Skript Objekt, das Aufgaben für die Konsolen Verbindung oder die Verbindung, die Remote Verbindung oder die Verbindung oder die Sperre von Arbeitsstations sperren oder entsperren auslöst.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- Sessionstatechange-Objekt Taskplaner
- Sessionstatechangeauslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337723"
---
# <a name="sessionstatechangetrigger-object"></a>Sessionstatechange-Objekt

Skript Objekt, das Aufgaben für die Konsolen Verbindung oder die Verbindung, die Remote Verbindung oder die Verbindung oder die Sperre von Arbeitsstations sperren oder entsperren auslöst.

## <a name="members"></a>Member

Das **sessionstatechange-** Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **sessionstatechange-** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](sessionstatechangetrigger-delay.md)<br/>             | Lesen/Schreiben<br/> | Ruft einen Wert ab oder legt einen Wert fest, der angibt, wie lange eine Verzögerung stattfindet, bevor eine Aufgabe gestartet wird, nachdem eine Terminal Server-Sitzungs Zustandsänderung erkannt wurde.<br/>                                         |
| [**Aktiviert**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.<br/>                                                              |
| [**Endgrenze**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/>               |
| [**Executiontimelimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den maximalen Zeitraum ab, in dem der Task vom-Vorgang gestartet werden kann, oder legt diesen fest.<br/>                                                 |
| [**Name**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Bezeichner für den-Typ ab oder legt ihn fest.<br/>                                                                                             |
| [**Wiederholen**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.<br/> |
| [**StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.<br/>                                                                            |
| [**StateChange**](sessionstatechangetrigger-statechange.md)<br/> | Lesen/Schreiben<br/> | Ruft die Art der Sitzungs Änderung für Terminal Server ab, die einen Task Start auslöst, oder legt Sie fest.<br/>                                                                                                      |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | Schreibgeschützt<br/>  | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Typ des Auslösers ab.<br/>                                                                                                            |
| [**UserID**](sessionstatechangetrigger-userid.md)<br/>           | Lesen/Schreiben<br/> | Ruft den Benutzer für die Terminal Server Sitzung ab oder legt ihn fest. Wenn eine Sitzungs Zustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.<br/>                                                               |



 

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird ein Sitzungs Status Änderungs--Vorgang mit dem [**sessionstatechange-**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 






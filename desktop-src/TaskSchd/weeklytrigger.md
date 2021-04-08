---
title: Weeklyauslöserobjekt
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task auf der Grundlage eines wöchentlichen Zeitplans startet.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- wöchentlicher auslöserTaskplaner, Objekt
- Weeklyauslöserobjekt Taskplaner
- Weeklyauslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58dec9172d38b53f779f44a048b39bc709dbd54f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743849"
---
# <a name="weeklytrigger-object"></a>Weeklyauslöserobjekt

Skript Objekt, das einen-Auslösers darstellt, der einen Task auf der Grundlage eines wöchentlichen Zeitplans startet. Der Task beginnt beispielsweise um 8:00 Uhr. an einem bestimmten Wochentag oder jeder anderen Woche.

## <a name="members"></a>Member

Das **Weekly-Auslöserobjekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Weekly-Auslöserobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek**](weeklytrigger-daysofweek.md)<br/>           | Lesen/Schreiben<br/> | Ruft die Wochentage ab, an denen der Task ausgeführt wird, oder legt diese fest.<br/>                                                                                                                        |
| [**Aktiviert**](trigger-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.<br/>                                                |
| [**Endgrenze**](trigger-endboundary.md)<br/>               | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/> |
| [**Executiontimelimit**](trigger-executiontimelimit.md)<br/> | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.<br/>                           |
| [**Name**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Bezeichner für den-Typ ab oder legt ihn fest.<br/>                                                                               |
| [**Randomdelay**](weeklytrigger-randomdelay.md)<br/>         | Lesen/Schreiben<br/> | Ruft eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.<br/>                                                                                               |
| [**Wiederholen**](trigger-repetition.md)<br/>                 | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.<br/>                                                              |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Schreibgeschützt<br/>  | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Typ des Auslösers ab.<br/>                                                                                              |
| [**Weeksinterval**](weeklytrigger-weeksinterval.md)<br/>     | Lesen/Schreiben<br/> | Ruft das Intervall zwischen den Wochen im Zeitplan ab oder legt es fest.<br/>                                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Die Uhrzeit, zu der die Aufgabe gestartet wird, wird von der [**StartBoundary**](trigger-startboundary.md) -Eigenschaft festgelegt.

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird ein wöchentlicher-Auslösers mit dem [**schedulebyweek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und ein Codebeispiel für dieses Skript Objekt finden Sie unter [Beispiel für ein wöchentliches Beispiel (Skripterstellung)](weekly-trigger-example--scripting-.md).

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

 

 






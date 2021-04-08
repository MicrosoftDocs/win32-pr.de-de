---
title: Monthly-Auslöserobjekt
description: Skript Objekt, das einen-Auslösers darstellt, der einen Task auf der Grundlage eines monatlichen Zeitplans startet.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- Monatlicher auslöserTaskplaner, Objekt
- Monthly-Auslöserobjekt Taskplaner
- Monthly-Auslöserobjekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce433f626fbe45e209f881c00787495cc6343bc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741881"
---
# <a name="monthlytrigger-object"></a>Monthly-Auslöserobjekt

Skript Objekt, das einen-Auslösers darstellt, der einen Task auf der Grundlage eines monatlichen Zeitplans startet. Beispielsweise wird die Aufgabe an bestimmten Tagen eines bestimmten Monats gestartet.

## <a name="members"></a>Member

Das **Monthly-Auslöserobjekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Monthly-Auslöserobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                     | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DaysOfMonth**](monthlytrigger-daysofmonth.md)<br/>                 | Lesen/Schreiben<br/> | Ruft die Tage des Monats ab, in denen die Aufgabe ausgeführt wird, oder legt Sie fest.<br/>                                                                                                                   |
| [**Aktiviert**](trigger-enabled.md)<br/>                                | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft einen booleschen Wert ab, der angibt, ob der-Wert aktiviert ist, oder legt ihn fest.<br/>                                                |
| [Endgrenze](trigger-endboundary.md)<br/>                            | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Deaktivierung des Auslösers ab oder legt diese fest. Der-Vorgang kann die Aufgabe nicht starten, nachdem Sie deaktiviert wurde.<br/> |
| [**Executiontimelimit**](trigger-executiontimelimit.md)<br/>          | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.<br/>                           |
| [**Name**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Bezeichner für den-Typ ab oder legt ihn fest.<br/>                                                                               |
| [**MONTHSOFYEAR**](monthlytrigger-monthsofyear.md)<br/>               | Lesen/Schreiben<br/> | Ruft die Monate des Jahres ab, in denen die Aufgabe ausgeführt wird, oder legt Sie fest.<br/>                                                                                                                  |
| [**Randomdelay**](monthlytrigger-randomdelay.md)<br/>                 | Lesen/Schreiben<br/> | Ruft eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.<br/>                                                                                               |
| [**Wiederholen**](trigger-repetition.md)<br/>                          | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft ab oder legt fest, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.<br/>          |
| [**Runonlastdayosmonth**](monthlytrigger-runonlastdayofmonth.md)<br/> | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass der Task am letzten Tag des Monats ausgeführt wird, oder legt ihn fest.<br/>                                                                                     |
| [**StartBoundary**](trigger-startboundary.md)<br/>                    | Lesen/Schreiben<br/> | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft das Datum und die Uhrzeit der Aktivierung des Auslösers ab oder legt diese fest.<br/>                                                              |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | Schreibgeschützt<br/>  | Wird vom- [**Auslöserobjekt**](trigger.md) geerbt. Ruft den Typ des Auslösers ab.<br/>                                                                                              |



 

## <a name="remarks"></a>Bemerkungen

Die Uhrzeit, zu der die Aufgabe gestartet wird, wird von der [**StartBoundary**](trigger-startboundary.md) -Eigenschaft festgelegt.

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird ein monatlicher-Auslösers mit dem [**schedulebymonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) -Element des Taskplaner-Schemas angegeben.

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

[Taskplaner Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 






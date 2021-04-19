---
title: Tasksettings-Objekt
description: Ein Skript Objekt, das die Einstellungen bereitstellt, die der Taskplaner-Dienst zum Ausführen der Aufgabe verwendet.
ms.assetid: f2ba952b-7864-467d-8709-eb6995dd5df5
keywords:
- Tasksettings-Objekt Taskplaner
- Task Settings-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7690ba59b4794f952ca3b381fc28247f0dfb4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338524"
---
# <a name="tasksettings-object"></a>Tasksettings-Objekt

Ein Skript Objekt, das die Einstellungen bereitstellt, die der Taskplaner-Dienst zum Ausführen der Aufgabe verwendet.

## <a name="members"></a>Member

Das **tasksettings** -Objekt verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **tasksettings** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                                 | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Allowdemandstart**](tasksettings-allowdemandstart.md)<br/>                     | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass der Task entweder mithilfe des Befehls "ausführen" oder des Kontextmenüs gestartet werden kann, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                     |
| [**Zuweisung aufheben**](tasksettings-allowhardterminate.md)<br/>                 | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Aufgabe mithilfe von [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)beendet werden kann, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                               |
| [**Kompatibilität**](tasksettings-compatibility.md)<br/>                           | Lesen/Schreiben<br/> | Ruft einen ganzzahligen Wert ab, der angibt, mit welcher Version von Taskplaner eine Aufgabe kompatibel ist, oder legt ihn fest<br/>                                                                                                                                                                                                                                                                                                           |
| [**Deleteexpiredtaskafter**](tasksettings-deleteexpiredtaskafter.md)<br/>         | Lesen/Schreiben<br/> | Ruft die Zeitspanne ab oder legt diese fest, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird.<br/>                                                                                                                                                                                                                                                                                                      |
| [**Disallowstartifonakkus**](tasksettings-disallowstartifonbatteries.md)<br/> | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass der Task nicht gestartet wird, wenn der Computer im Akku Betrieb ausgeführt wird, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                        |
| [**Aktiviert**](tasksettings-enabled.md)<br/>                                       | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass der Task aktiviert ist, oder legt diesen fest. Der Task kann nur ausgeführt werden, wenn diese Einstellung auf "true" festgelegt ist.<br/>                                                                                                                                                                                                                                                                                   |
| [**Executiontimelimit**](tasksettings-executiontimelimit.md)<br/>                 | Lesen/Schreiben<br/> | Ruft die Zeitspanne ab, die zum Ausführen der Aufgabe zulässig ist, oder legt diese fest.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**Verbirgt**](tasksettings-hidden.md)<br/>                                         | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Aufgabe in der Benutzeroberfläche nicht sichtbar ist, oder legt diesen fest. Administratoren können diese Einstellung jedoch überschreiben, indem Sie einen "Master Switch" verwenden, der alle Aufgaben in der Benutzeroberfläche sichtbar macht.<br/>                                                                                                                                                                                           |
| [**Idlesettings**](tasksettings-idlesettings.md)<br/>                             | Lesen/Schreiben<br/> | Ruft die Informationen ab, die angeben, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet, oder legt diese Informationen fest.<br/>                                                                                                                                                                                                                                                                                          |
| [**Multipleinhaltungen**](tasksettings-multipleinstances.md)<br/>                   | Lesen/Schreiben<br/> | Ruft die Richtlinie ab oder legt Sie fest, die definiert, wie die Taskplaner mit mehreren Instanzen der Aufgabe umgeht.<br/>                                                                                                                                                                                                                                                                                                            |
| [**NetworkSettings**](tasksettings-networksettings.md)<br/>                       | Lesen/Schreiben<br/> | Ruft das Netzwerk Einstellungs Objekt ab, das einen Netzwerk Profil Bezeichner und-Namen enthält, oder legt dieses fest. Wenn die [**runonlyifnetworkavailable**](tasksettings-runonlyifnetworkavailable.md) -Eigenschaft von **tasksettings** den Wert **true** hat und in der [**networksettings**](tasksettings-networksettings.md) -Eigenschaft eine Netzwerk-propfile angegeben ist, wird die Aufgabe nur ausgeführt, wenn das angegebene Netzwerk Profil verfügbar ist.<br/> |
| [**Priorität**](tasksettings-priority.md)<br/>                                     | Lesen/Schreiben<br/> | Ruft die Prioritätsstufe der Aufgabe ab oder legt Sie fest.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| [**RestartCount**](tasksettings-restartcount.md)<br/>                             | Lesen/Schreiben<br/> | Ruft ab oder legt fest, wie oft das Taskplaner versucht, den Task neu zu starten.<br/>                                                                                                                                                                                                                                                                                                                        |
| [**Restartinterval**](tasksettings-restartinterval.md)<br/>                       | Lesen/Schreiben<br/> | Ruft einen Wert ab oder legt einen Wert fest, der angibt, wie lange der Taskplaner versucht, den Task neu zu starten.<br/>                                                                                                                                                                                                                                                                                                                 |
| [**Runonlyifdle**](tasksettings-runonlyifidle.md)<br/>                           | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe nur dann ausführen soll, wenn sich der Computer im Leerlauf befindet, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                   |
| [**Runonlyifnetworkavailable**](tasksettings-runonlyifnetworkavailable.md)<br/>   | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Taskplaner den Task nur dann ausführen, wenn ein Netzwerk verfügbar ist, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                           |
| [**Startvor verfügbar**](tasksettings-startwhenavailable.md)<br/>                 | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe jederzeit nach dem geplanten Zeitpunkt starten kann, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                           |
| [**Stopifgoingonakkus**](tasksettings-stopifgoingonbatteries.md)<br/>         | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass der Task angehalten wird, wenn der Computer im Akku Betrieb ausgeführt wird, oder legt ihn fest.<br/>                                                                                                                                                                                                                                                                                         |
| [**WakeToRun**](tasksettings-waketorun.md)<br/>                                   | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, dass der Taskplaner den Computer reaktivieren soll, wenn die Aufgabe ausgeführt wird.<br/>                                                                                                                                                                                                                                                                                       |
| [**XmlText**](tasksettings-xmltext.md)<br/>                                       | Lesen/Schreiben<br/> | Ruft eine XML-formatierte Definition der Task Einstellungen ab oder legt Sie fest.<br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Standardmäßig wird eine Aufgabe 72 Stunden nach dem Start angehalten. Sie können dies ändern, indem Sie die Einstellung [**executiontimelimit**](tasksettings-executiontimelimit.md) ändern.

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Aufgaben Einstellungen im [**Einstellungs**](taskschedulerschema-settings-tasktype-element.md) Element des Taskplaner Schemas definiert.

## <a name="examples"></a>Beispiele

Weitere Informationen und ein Codebeispiel für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).

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
</dt> <dt>

[**Task Definition**](taskdefinition.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> <dt>

[**Idlesettings**](idlesettings.md)
</dt> </dl>

 


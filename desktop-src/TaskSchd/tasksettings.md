---
title: TaskSettings-Objekt
description: Ein Skriptobjekt, das die Einstellungen bereitstellt, die der Taskplaner Dienst zum Ausführen der Aufgabe verwendet.
ms.assetid: f2ba952b-7864-467d-8709-eb6995dd5df5
keywords:
- TaskSettings-Objekt Taskplaner
- TaskSettings-Objekt Taskplaner beschrieben
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
ms.openlocfilehash: a687e82248598d9732e91acfd40e9f3dd4d6d3c3fe6c4954cb8706489c814126
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738100"
---
# <a name="tasksettings-object"></a>TaskSettings-Objekt

Ein Skriptobjekt, das die Einstellungen bereitstellt, die der Taskplaner Dienst zum Ausführen der Aufgabe verwendet.

## <a name="members"></a>Member

Das **TaskSettings-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **TaskSettings-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                 | Zugriffstyp           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowDemandStart**](tasksettings-allowdemandstart.md)<br/>                     | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Aufgabe entweder mit dem Befehl Ausführen oder mithilfe des Kontextmenüs gestartet werden kann, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                     |
| [**AllowHardTerminate**](tasksettings-allowhardterminate.md)<br/>                 | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass der Task mit [**terminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)beendet werden kann, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                               |
| [**Kompatibilität**](tasksettings-compatibility.md)<br/>                           | Lesen/Schreiben<br/> | Ruft einen ganzzahligen Wert ab, der angibt, mit welcher Version von Taskplaner ein Task kompatibel ist, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                                           |
| [**DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md)<br/>         | Lesen/Schreiben<br/> | Ruft die Zeitspanne ab, die der Taskplaner wartet, bevor der Task nach ablaufen wird, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                                      |
| [**DisallowStartIfOnFolgens**](tasksettings-disallowstartifonbatteries.md)<br/> | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Aufgabe nicht gestartet wird, wenn der Computer im Akkubetrieb ausgeführt wird, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                        |
| [**Aktiviert**](tasksettings-enabled.md)<br/>                                       | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Aufgabe aktiviert ist, oder legt diesen fest. Die Aufgabe kann nur ausgeführt werden, wenn diese Einstellung auf True festgelegt ist.<br/>                                                                                                                                                                                                                                                                                   |
| [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md)<br/>                 | Lesen/Schreiben<br/> | Ruft den Zeitraum ab, der zum Abschließen der Aufgabe zulässig ist, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**Versteckte**](tasksettings-hidden.md)<br/>                                         | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass der Task auf der Benutzeroberfläche nicht sichtbar ist, oder legt diesen fest. Administratoren können diese Einstellung jedoch überschreiben, indem sie einen "Masterschalter" verwenden, der alle Aufgaben auf der Benutzeroberfläche sichtbar macht.<br/>                                                                                                                                                                                           |
| [**IdleSettings**](tasksettings-idlesettings.md)<br/>                             | Lesen/Schreiben<br/> | Ruft die Informationen ab, die angeben, wie der Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet, oder legt diese fest.<br/>                                                                                                                                                                                                                                                                                          |
| [**MultipleInstances**](tasksettings-multipleinstances.md)<br/>                   | Lesen/Schreiben<br/> | Ruft die Richtlinie ab, die definiert, wie die Taskplaner mit mehreren Instanzen der Aufgabe umgeht, oder legt sie fest.<br/>                                                                                                                                                                                                                                                                                                            |
| [**NetworkSettings**](tasksettings-networksettings.md)<br/>                       | Lesen/Schreiben<br/> | Ruft das Netzwerkeinstellungsobjekt ab, das einen Netzwerkprofilbezeichner und -namen enthält, oder legt dieses fest. Wenn die [**RunOnlyIfNetworkAvailable-Eigenschaft**](tasksettings-runonlyifnetworkavailable.md) von **TaskSettings** **true** ist und eine Netzwerkpropfile in der [**NetworkSettings-Eigenschaft**](tasksettings-networksettings.md) angegeben ist, wird der Task nur ausgeführt, wenn das angegebene Netzwerkprofil verfügbar ist.<br/> |
| [**Priorität**](tasksettings-priority.md)<br/>                                     | Lesen/Schreiben<br/> | Ruft die Prioritätsebene des Tasks ab oder legt diese fest.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| [**RestartCount**](tasksettings-restartcount.md)<br/>                             | Lesen/Schreiben<br/> | Ruft ab oder legt fest, wie oft der Taskplaner versucht, den Task neu zu starten.<br/>                                                                                                                                                                                                                                                                                                                        |
| [**RestartInterval**](tasksettings-restartinterval.md)<br/>                       | Lesen/Schreiben<br/> | Ruft einen Wert ab, der angibt, wie lange die Taskplaner versucht, den Task neu zu starten, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                                                 |
| [**RunOnlyIfIdle**](tasksettings-runonlyifidle.md)<br/>                           | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Taskplaner den Task nur dann ausführen, wenn sich der Computer im Leerlauf befindet, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                   |
| [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)<br/>   | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Taskplaner den Task nur dann ausführen, wenn ein Netzwerk verfügbar ist, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                           |
| [**StartWhenAvailable**](tasksettings-startwhenavailable.md)<br/>                 | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass der Taskplaner die Aufgabe jederzeit nach Ablauf der geplanten Zeit starten kann, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                           |
| [**StopIfGoingOnRiegels**](tasksettings-stopifgoingonbatteries.md)<br/>         | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Aufgabe beendet wird, wenn der Computer im Akkubetrieb ausgeführt wird, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                         |
| [**WakeToRun**](tasksettings-waketorun.md)<br/>                                   | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, dass die Taskplaner den Computer aktiviert, wenn die Aufgabe ausgeführt werden soll, oder legt diesen fest.<br/>                                                                                                                                                                                                                                                                                       |
| [**Xmltext**](tasksettings-xmltext.md)<br/>                                       | Lesen/Schreiben<br/> | Ruft eine XML-formatierte Definition der Taskeinstellungen ab oder legt diese fest.<br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Hinweise

Standardmäßig wird eine Aufgabe 72 Stunden nach beginn der Ausführung beendet. Sie können dies ändern, indem Sie die [**Einstellung ExecutionTimeLimit**](tasksettings-executiontimelimit.md) ändern.

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Taskeinstellungen im [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) -Element des Taskplaner-Schemas definiert.

## <a name="examples"></a>Beispiele

Weitere Informationen und ein Codebeispiel für dieses Skriptobjekt finden Sie unter [Time Trigger Example (Scripting) (Zeittriggerbeispiel (Skripterstellung)).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 


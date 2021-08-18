---
title: Einstellungen (taskType) -Element
description: Gibt die Einstellungen an, die der Taskplaner zum Ausführen der Aufgabe verwendet.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Einstellungen element Taskplaner
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea754aa883f9c80c4a436357cc159c588bde375aaa66a229b358723b74b9e070
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002238"
---
# <a name="settings-tasktype-element"></a>Einstellungen (taskType) -Element

Gibt die Einstellungen an, die der Taskplaner zum Ausführen der Aufgabe verwendet.

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

Das **Einstellungen** element wird durch den [**komplexen taskType-Typ**](taskschedulerschema-tasktype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                          | Abgeleitet von                                                 | Beschreibung                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Aufgabe**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Gibt den Task an, der vom Dienst Taskplaner wird.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                          | type                                                                                              | Beschreibung                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | boolean                                                                                           | Gibt an, dass der Task mit TerminateProcess beendet werden kann.<br/>                                         |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | boolean                                                                                           | Gibt an, dass die Aufgabe mit dem Befehl Ausführen oder dem Kontextmenü gestartet werden kann.<br/>                  |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | duration                                                                                          | Gibt die Zeit an, die der Taskplaner, bevor der Task nach ablaufen gelöscht wird.<br/> |
| [**DisallowStartIfOn Wies**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | boolean                                                                                           | Gibt an, dass der Task nicht gestartet wird, wenn der Computer mit Akkus ausgeführt wird.<br/>                      |
| [**Aktiviert**](taskschedulerschema-enabled-settingstype-element.md)                                              | boolean                                                                                           | Gibt an, dass die Aufgabe aktiviert ist. Die Aufgabe kann nur ausgeführt werden, wenn diese Einstellung true ist.<br/>             |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | duration                                                                                          | Zulässige Zeit zum Abschließen der Aufgabe.<br/>                                                              |
| [**Versteckte**](taskschedulerschema-hidden-settingstype-element.md)                                                | boolean                                                                                           | Gibt an, dass der Task standardmäßig nicht auf der Benutzeroberfläche angezeigt wird.<br/>                                         |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/>                    |
| [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)        | Gibt an, wie die Taskplaner während der automatischen Wartung Aufgaben ausführt.<br/>                             |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Gibt die Richtlinie an, die definiert, wie Taskplaner mehrere Instanzen der Aufgabe behandelt.<br/>       |
| [**Priorität**](taskschedulerschema-priority-settingstype-element.md)                                            | [**priorityType**](taskschedulerschema-prioritytype-simpletype.md)                               | Gibt die Prioritätsebene für den Task an.<br/>                                                                |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [**restartType**](taskschedulerschema-restarttype-complextype.md)                                | Gibt an, dass der Taskplaner versucht, den Task neu zu starten, wenn der Task aus irgendeinem Grund fehlschlägt.<br/>      |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | boolean                                                                                           | Gibt an, dass der Task nur ausgeführt wird, wenn sich der Computer im Leerlauf befindet.<br/>                                |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | boolean                                                                                           | Gibt an, dass Taskplaner Die Aufgabe nur ausgeführt wird, wenn ein Netzwerk verfügbar ist.<br/>                     |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | boolean                                                                                           | Gibt an, dass Taskplaner aufgabe jederzeit starten kann, nachdem die geplante Zeit verstrichen ist.<br/>     |
| [**StopIfGoingOnStopps (settingsType)**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | boolean                                                                                           | Gibt an, dass die Aufgabe beendet wird, wenn der Computer in Akkus gerät.<br/>                          |
| [**Volatil**](taskschedulerschema-volatile-element.md)                                                         | boolean                                                                                           | Gibt an, ob die Aufgabe automatisch deaktiviert wird, indem Taskplaner beim Windows wird.<br/>                     |
| [**WakeToRun (settingsType)**](taskschedulerschema-waketorun-settingstype-element.md)                           | boolean                                                                                           | Gibt an, Taskplaner computer reaktiviert wird, wenn es An der Zeit ist, den Task auszuführen.<br/>                     |



## <a name="remarks"></a>Hinweise

Sie können eines oder mehrere der untergeordneten Elemente auswählen, auf die oben verwiesen wird.

Für die C++-Entwicklung werden die Registrierungsinformationen einer Aufgabe mithilfe der Einstellungen [**von ITaskDefinition angegeben.**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings)

Für die Skriptentwicklung werden die Registrierungsinformationen einer Aufgabe mithilfe der [**TaskDefinition.Einstellungen**](taskdefinition-settings.md) angegeben.

## <a name="examples"></a>Beispiele

Im folgenden XML-Codebeispiel wird ein Einstellungselement definiert, das eine harte Beendigung der Aufgabe zulässt.


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



Weitere Informationen und ein vollständiges Beispiel für xml zum Festlegen von Aufgabeneinstellungen finden Sie unter [Time Trigger Example (XML) .](time-trigger-example--xml-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






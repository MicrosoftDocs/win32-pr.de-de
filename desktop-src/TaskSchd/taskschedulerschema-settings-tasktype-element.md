---
title: Settings (TaskType)-Element
description: Gibt die Einstellungen an, die vom Taskplaner zum Ausführen der Aufgabe verwendet werden.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Settings-Element Taskplaner
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9133d536aef692a5f9928e10963dff8c454f25fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391761"
---
# <a name="settings-tasktype-element"></a>Settings (TaskType)-Element

Gibt die Einstellungen an, die vom Taskplaner zum Ausführen der Aufgabe verwendet werden.

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

Das **Settings** -Element wird durch den komplexen [**TaskType**](taskschedulerschema-tasktype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                          | Abgeleitet von                                                 | BESCHREIBUNG                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Aufgabe**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Gibt die Aufgabe an, die vom Taskplaner-Dienst ausgeführt wird.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                          | type                                                                                              | BESCHREIBUNG                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**Zuweisung aufheben**](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | boolean                                                                                           | Gibt an, dass die Aufgabe mithilfe von TerminateProcess beendet werden kann.<br/>                                         |
| [**Allowstartondemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | boolean                                                                                           | Gibt an, dass der Task entweder über den Befehl ausführen oder über das Kontextmenü gestartet werden kann.<br/>                  |
| [**Deleteexpiredtaskafter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | duration                                                                                          | Gibt die Zeitspanne an, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird.<br/> |
| [**Disallowstartifonakkus**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | boolean                                                                                           | Gibt an, dass der Task nicht gestartet wird, wenn der Computer unter "Akkus" ausgeführt wird.<br/>                      |
| [**Aktiviert**](taskschedulerschema-enabled-settingstype-element.md)                                              | boolean                                                                                           | Gibt an, dass der Task aktiviert ist. Der Task kann nur ausgeführt werden, wenn diese Einstellung auf "true" festgelegt ist.<br/>             |
| [**Executiontimelimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | duration                                                                                          | Die Zeitspanne, die zum Ausführen der Aufgabe zulässig ist.<br/>                                                              |
| [**Verbirgt**](taskschedulerschema-hidden-settingstype-element.md)                                                | boolean                                                                                           | Gibt an, dass die Aufgabe nicht standardmäßig in der Benutzeroberfläche angezeigt wird.<br/>                                         |
| [**Idlesettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md)                      | Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/>                    |
| [**Maintenancesettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [**maintenancesettingstype**](taskschedulerschema-maintenancesettingstype-complextype.md)        | Gibt an, wie das Taskplaner während der automatischen Wartung Tasks ausführt.<br/>                             |
| [**Multipleinstancespolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [**multipleinstancespolicytype**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Gibt die Richtlinie an, mit der definiert wird, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt.<br/>       |
| [**Priorität**](taskschedulerschema-priority-settingstype-element.md)                                            | [**prioritytype**](taskschedulerschema-prioritytype-simpletype.md)                               | Gibt die Prioritätsstufe für den Task an.<br/>                                                                |
| [**Neustartonfailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [**neustarttype**](taskschedulerschema-restarttype-complextype.md)                                | Gibt an, dass der Taskplaner den Task neu starten soll, wenn die Aufgabe aus irgendeinem Grund fehlschlägt.<br/>      |
| [**Runonlyifdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | boolean                                                                                           | Gibt an, dass der Task nur ausgeführt wird, wenn sich der Computer im Leerlauf befindet.<br/>                                |
| [**Runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | boolean                                                                                           | Gibt an, dass der Taskplaner die Aufgabe nur dann ausgeführt wird, wenn ein Netzwerk verfügbar ist.<br/>                     |
| [**Startvor verfügbar**](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | boolean                                                                                           | Gibt an, dass die Taskplaner die Aufgabe jederzeit starten kann, nachdem die geplante Zeit abgelaufen ist.<br/>     |
| [**Stopifgoingonakkus (settingstype)**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | boolean                                                                                           | Gibt an, dass der Task angehalten wird, wenn der Computer auf die Batterie geht.<br/>                          |
| [**Ständigem**](taskschedulerschema-volatile-element.md)                                                         | boolean                                                                                           | Gibt an, ob die Aufgabe beim Windows-Start automatisch durch Taskplaner deaktiviert wird.<br/>                     |
| [**Waketor (settingstype)**](taskschedulerschema-waketorun-settingstype-element.md)                           | boolean                                                                                           | Gibt an, dass der Computer von Taskplaner reaktiviert wird, wenn der Task ausgeführt werden soll.<br/>                     |



## <a name="remarks"></a>Bemerkungen

Sie können mindestens ein untergeordnetes Element auswählen, auf das oben verwiesen wird.

Bei der C++-Entwicklung werden die Registrierungsinformationen einer Aufgabe mithilfe der [**Settings-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings)angegeben.

Bei der Skripterstellung werden die Registrierungsinformationen einer Aufgabe mithilfe der [**Task Definition. Settings**](taskdefinition-settings.md) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Im folgenden XML-Codebeispiel wird ein Einstellungs Element definiert, das eine harte Beendigung der Aufgabe ermöglicht.


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



Weitere Informationen und ein umfassendes Beispiel für den XML-Code zum Festlegen von Task Einstellungen finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






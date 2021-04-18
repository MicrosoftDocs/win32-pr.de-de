---
title: komplexer settingstype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das Settings (TaskType)-Element.
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- komplexer settingstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3c2b3128a35ee0e46c56d19badd431400d4d862
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345308"
---
# <a name="settingstype-complex-type"></a>komplexer settingstype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**Settings (TaskType)**](taskschedulerschema-settings-tasktype-element.md) -Element.

``` syntax
<xs:complexType name="settingsType">
    <xs:all>
        <xs:element name="AllowStartOnDemand"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnFailure"
            type="restartType"
            minOccurs="0"
         />
        <xs:element name="MultipleInstancesPolicy"
            type="multipleInstancesPolicyType"
            default="IgnoreNew"
            minOccurs="0"
         />
        <xs:element name="DisallowStartIfOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StopIfGoingOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="AllowHardTerminate"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartWhenAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="NetworkProfileName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfNetworkAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="WakeToRun"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="Hidden"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DeleteExpiredTaskAfter"
            type="duration"
            default="PT0S"
            minOccurs="0"
         />
        <xs:element name="IdleSettings"
            type="idleSettingsType"
            minOccurs="0"
         />
        <xs:element name="NetworkSettings"
            type="networkSettingsType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
        <xs:element name="Priority"
            type="priorityType"
            default="7"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="UseUnifiedSchedulingEngine"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DisallowStartOnRemoteAppSession"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                             | type                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zuweisung aufheben**](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | boolean                                                                                           | Gibt an, ob der Taskplaner Dienstanbieter das harte Beenden der Aufgabe zulässt.<br/>                                                                                                                                                                                                                             |
| [**Allowstartondemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | boolean                                                                                           | Gibt an, dass der Task entweder mithilfe des Befehls ausführen oder des Kontextmenüs gestartet werden kann. <br/>                                                                                                                                                                                                             |
| [**Deleteexpiredtaskafter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | duration                                                                                          | Gibt die Zeitspanne an, die der Taskplaner wartet, bevor der Task nach Ablauf gelöscht wird. Wenn für dieses Element kein Wert angegeben wird, wird der Task vom Taskplaner-Dienst nicht gelöscht.<br/>                                                                                           |
| [**Disallowstartifonakkus**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | boolean                                                                                           | Gibt an, dass der Task nicht gestartet wird, wenn der Computer im Akku Betrieb ausgeführt wird.<br/>                                                                                                                                                                                                                 |
| [**Disallowstartonremoteappsession**](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | boolean                                                                                           | Gibt an, dass der Task nicht gestartet werden soll, wenn die Aufgabe für die Durchführung in einer lokalen (Schiene) Remote Anwendung ausgelöst wird.<br/>                                                                                                                                                                     |
| [**Aktiviert**](taskschedulerschema-enabled-settingstype-element.md)                                                 | boolean                                                                                           | Gibt an, dass der Task aktiviert ist. Der Task kann nur ausgeführt werden, wenn diese Einstellung auf " **true**" festgelegt ist.<br/>                                                                                                                                                                                                        |
| [**Executiontimelimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | duration                                                                                          | Gibt die Zeitspanne an, die zum Ausführen der Aufgabe zulässig ist.<br/>                                                                                                                                                                                                                                               |
| [**Verbirgt**](taskschedulerschema-hidden-settingstype-element.md)                                                   | boolean                                                                                           | Gibt standardmäßig an, dass die Aufgabe in der Benutzeroberfläche (UI) nicht angezeigt wird.<br/>                                                                                                                                                                                                                     |
| [**Idlesettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md)                      | Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/>                                                                                                                                                                                                                   |
| [**Multipleinstancespolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [**multipleinstancespolicytype**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Gibt die Richtlinie an, mit der definiert wird, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt. <br/>                                                                                                                                                                                                     |
| [**Network Profile Name**](taskschedulerschema-networkprofilename-settingstype-element.md)                           | Zeichenfolge                                                                                            | Gibt den Namen eines Netzwerk Profils an. Der Taskplaner-Dienst überprüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist. Der Name wird zu Anzeige Zwecken verwendet.<br/>        |
| [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md)                                 | [**Network settingstype**](taskschedulerschema-networksettingstype-complextype.md)                | Gibt die Einstellungen an, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden. Der Taskplaner Dienst prüft die Verfügbarkeit dieses Netzwerks, wenn das [**runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) -Element auf " **true**" festgelegt ist.<br/> |
| [**Priorität**](taskschedulerschema-priority-settingstype-element.md)                                               | [**prioritytype**](taskschedulerschema-prioritytype-simpletype.md)                               | Gibt die Prioritätsstufe für den Task an.<br/>                                                                                                                                                                                                                                                               |
| [**Neustartonfailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [**neustarttype**](taskschedulerschema-restarttype-complextype.md)                                | Gibt an, dass der Taskplaner versucht, den Task neu zu starten, wenn er aus irgendeinem Grund fehlschlägt. <br/>                                                                                                                                                                                                          |
| [**Runonlyifdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | boolean                                                                                           | Gibt an, dass der Task nur ausgeführt wird, wenn sich der Computer im Leerlauf befindet.<br/>                                                                                                                                                                                                                               |
| [**Runonlyifnetworkavailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | boolean                                                                                           | Gibt an, dass der Taskplaner die Aufgabe nur dann ausgeführt wird, wenn ein Netzwerk verfügbar ist.<br/>                                                                                                                                                                                                                    |
| [**Startvor verfügbar**](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | boolean                                                                                           | Gibt an, dass die Taskplaner die Aufgabe jederzeit starten kann, nachdem die geplante Zeit abgelaufen ist.<br/>                                                                                                                                                                                                    |
| [**Stopifgoingonakkus**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | boolean                                                                                           | Gibt an, dass der Task angehalten wird, wenn der Computer in den Akku Betrieb wechselt. <br/>                                                                                                                                                                                                                      |
| [**Useunifedschedulingengine**](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | boolean                                                                                           | Gibt an, dass der Task mithilfe der Unified Scheduling-Engine ausgeführt wird.<br/>                                                                                                                                                                                                                                   |
| [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md)                                             | boolean                                                                                           | Gibt an, dass Taskplaner den Computer vor dem Ausführen der Aufgabe reaktivieren wird.<br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komplexe Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






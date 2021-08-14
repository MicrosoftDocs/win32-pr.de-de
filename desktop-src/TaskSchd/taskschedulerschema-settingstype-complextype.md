---
title: settingsType Complex Type
description: Definiert die untergeordneten Elemente und Sequenzinformationen für das Einstellungen (taskType)-Element.
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- settingsType complex type Taskplaner
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a48a124230a27a0c23cc9c2a9fa983b6ef3088b8ec22e8ac03fc371caadf0f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356352"
---
# <a name="settingstype-complex-type"></a>settingsType Complex Type

Definiert die untergeordneten Elemente und Sequenzierungsinformationen für das [**Einstellungen (taskType)-Element.**](taskschedulerschema-settings-tasktype-element.md)

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
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | boolean                                                                                           | Gibt an, ob der Taskplaner Dienst eine harte Beendigung der Aufgabe zulässt.<br/>                                                                                                                                                                                                                             |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | boolean                                                                                           | Gibt an, dass der Task entweder mit dem Befehl Ausführen oder mithilfe des Kontextmenüs gestartet werden kann. <br/>                                                                                                                                                                                                             |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | duration                                                                                          | Gibt die Zeitspanne an, die der Taskplaner wartet, bevor der Task gelöscht wird, nachdem er abläuft. Wenn für dieses Element kein Wert angegeben ist, löscht der Taskplaner Dienst den Task nicht.<br/>                                                                                           |
| [**DisallowStartIfOnFolgens**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | boolean                                                                                           | Gibt an, dass die Aufgabe nicht gestartet wird, wenn der Computer im Akkubetrieb ausgeführt wird.<br/>                                                                                                                                                                                                                 |
| [**DisallowStartOnRemoteAppSession**](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | boolean                                                                                           | Gibt an, dass der Task nicht gestartet werden soll, wenn die Ausführung des Tasks in einer Rail-Sitzung (Remote Applications Integrated Locally) ausgelöst wird.<br/>                                                                                                                                                                     |
| [**Aktiviert**](taskschedulerschema-enabled-settingstype-element.md)                                                 | boolean                                                                                           | Gibt an, dass der Task aktiviert ist. Die Aufgabe kann nur ausgeführt werden, wenn diese Einstellung **true** ist.<br/>                                                                                                                                                                                                        |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | duration                                                                                          | Gibt den Zeitraum an, der zum Abschließen der Aufgabe zulässig ist.<br/>                                                                                                                                                                                                                                               |
| [**Versteckte**](taskschedulerschema-hidden-settingstype-element.md)                                                   | boolean                                                                                           | Gibt standardmäßig an, dass die Aufgabe auf der Benutzeroberfläche (UI) nicht sichtbar ist.<br/>                                                                                                                                                                                                                     |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Gibt an, wie der Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.<br/>                                                                                                                                                                                                                   |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Gibt die Richtlinie an, die definiert, wie die Taskplaner mit mehreren Instanzen der Aufgabe umgeht. <br/>                                                                                                                                                                                                     |
| [**NetworkProfileName**](taskschedulerschema-networkprofilename-settingstype-element.md)                           | Zeichenfolge                                                                                            | Gibt den Namen eines Netzwerkprofils an. Der Taskplaner-Dienst überprüft die Verfügbarkeit dieses Netzwerks, wenn das [**RunOnlyIfNetworkAvailable-Element**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) auf **True** festgelegt ist. Der Name wird zu Anzeigezwecken verwendet.<br/>        |
| [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md)                                 | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md)                | Gibt die Einstellungen an, die der Taskplaner Dienst zum Abrufen eines Netzwerkprofils verwendet. Der Taskplaner-Dienst überprüft die Verfügbarkeit dieses Netzwerks, wenn das [**RunOnlyIfNetworkAvailable-Element**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) auf **True** festgelegt ist.<br/> |
| [**Priorität**](taskschedulerschema-priority-settingstype-element.md)                                               | [**priorityType**](taskschedulerschema-prioritytype-simpletype.md)                               | Gibt die Prioritätsebene für den Task an.<br/>                                                                                                                                                                                                                                                               |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [**restartType**](taskschedulerschema-restarttype-complextype.md)                                | Gibt an, dass der Taskplaner versucht, den Task neu zu starten, wenn er aus irgendeinem Grund fehlschlägt. <br/>                                                                                                                                                                                                          |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | boolean                                                                                           | Gibt an, dass der Task nur ausgeführt wird, wenn sich der Computer im Leerlauf befindet.<br/>                                                                                                                                                                                                                               |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | boolean                                                                                           | Gibt an, dass die Taskplaner den Task nur dann ausführen, wenn ein Netzwerk verfügbar ist.<br/>                                                                                                                                                                                                                    |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | boolean                                                                                           | Gibt an, dass die Taskplaner die Aufgabe jederzeit starten kann, nachdem die geplante Zeit abgelaufen ist.<br/>                                                                                                                                                                                                    |
| [**StopIfGoingOnRiegels**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | boolean                                                                                           | Gibt an, dass die Aufgabe beendet wird, wenn der Computer in den Akkubetrieb wechselt. <br/>                                                                                                                                                                                                                      |
| [**UseUnifiedSchedulingEngine**](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | boolean                                                                                           | Gibt an, dass der Task mithilfe der einheitlichen Zeitplanungs-Engine ausgeführt wird.<br/>                                                                                                                                                                                                                                   |
| [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md)                                             | boolean                                                                                           | Gibt an, dass Taskplaner den Computer reaktiviert, bevor er die Aufgabe ausführt.<br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[komplexe Schematypen Taskplaner](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






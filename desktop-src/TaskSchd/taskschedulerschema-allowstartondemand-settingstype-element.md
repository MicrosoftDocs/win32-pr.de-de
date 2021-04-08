---
title: Allowstartondemand-Element (settingstype)
description: Gibt an, dass der Task entweder über den Befehl ausführen oder über das Kontextmenü gestartet werden kann.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Allowstartondemand-Element Taskplaner
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949575"
---
# <a name="allowstartondemand-settingstype-element"></a>Allowstartondemand-Element (settingstype)

Gibt an, dass der Task entweder über den Befehl ausführen oder über das Kontextmenü gestartet werden kann.

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

Das **allowstartondemand** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Wenn dieses Element auf true festgelegt ist, kann der Task unabhängig von gestartet werden, wenn ein Trigger den Task startet.

Informationen zur C++-Entwicklung finden Sie unter der [**allowdemandstart-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. allowdemandstart**](tasksettings-allowdemandstart.md).

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die den Start von Anforderungen ermöglicht, finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 






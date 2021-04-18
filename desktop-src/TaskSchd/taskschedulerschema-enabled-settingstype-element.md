---
title: Aktiviertes (settingstype)-Element
description: Gibt an, dass der Task aktiviert ist. Der Task kann nur ausgeführt werden, wenn diese Einstellung auf "true" festgelegt ist.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Aktiviertes Element Taskplaner
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc86b25fa29345fe120ac5e59d55d847b01c352e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340372"
---
# <a name="enabled-settingstype-element"></a>Aktiviertes (settingstype)-Element

Gibt an, dass der Task aktiviert ist. Der Task kann nur ausgeführt werden, wenn diese Einstellung auf "true" festgelegt ist.

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

Das **aktivierte** Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Einstellungen**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**aktivierte Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).

Informationen zur Skript Entwicklung finden Sie unter [**tasksettings. aktiviert**](tasksettings-enabled.md).

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine aktivierte Aufgabe finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 






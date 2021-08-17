---
title: NetworkSettings-Objekt
description: Für die Skripterstellung stellt die Einstellungen zur Verfügung, die der Taskplaner verwendet, um ein Netzwerkprofil zu erhalten.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- NetworkSettings-Taskplaner
- NetworkSettings-Objekt Taskplaner , beschrieben
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc5e247ad3de50268c6075f8956687f92800c4e901788b5098a0cef868bb202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759692"
---
# <a name="networksettings-object"></a>NetworkSettings-Objekt

Für die Skripterstellung stellt die Einstellungen zur Verfügung, die der Taskplaner verwendet, um ein Netzwerkprofil zu erhalten.

## <a name="members"></a>Member

Das **NetworkSettings-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **NetworkSettings-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                        | Zugriffstyp           | Beschreibung                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Id**](networksettings-id.md)<br/>     | Lesen/Schreiben<br/> | Ruft einen GUID-Wert ab, der ein Netzwerkprofil identifiziert, oder legt diesen fest.<br/>                        |
| [**Name**](networksettings-name.md)<br/> | Lesen/Schreiben<br/> | Ruft den Namen eines Netzwerkprofils ab oder legt den Namen fest. Der Name wird zu Anzeigezwecken verwendet. <br/> |



 

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben eigener XML-Daten für eine Aufgabe werden Netzwerkeinstellungen mithilfe des [**NetworkSettings-Elements**](taskschedulerschema-networksettings-settingstype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






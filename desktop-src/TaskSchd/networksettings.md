---
title: Network Settings-Objekt
description: Gibt für die Skripterstellung die Einstellungen an, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Network Settings-Objekt Taskplaner
- Network Settings-Objekt Taskplaner, beschrieben
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
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477202"
---
# <a name="networksettings-object"></a>Network Settings-Objekt

Gibt für die Skripterstellung die Einstellungen an, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.

## <a name="members"></a>Member

Das **Network Settings** -Objekt verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Network Settings** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                        | Zugriffstyp           | BESCHREIBUNG                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Name**](networksettings-id.md)<br/>     | Lesen/Schreiben<br/> | Ruft einen GUID-Wert ab, der ein Netzwerk Profil identifiziert, oder legt ihn fest.<br/>                        |
| [**Name**](networksettings-name.md)<br/> | Lesen/Schreiben<br/> | Ruft den Namen eines Netzwerk Profils ab oder legt ihn fest. Der Name wird zu Anzeige Zwecken verwendet. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe werden Netzwerkeinstellungen mit dem [**networksettings**](taskschedulerschema-networksettings-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 






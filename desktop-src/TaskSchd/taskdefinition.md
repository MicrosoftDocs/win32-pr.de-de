---
title: Taskdefinition-Objekt
description: Skript Objekt, das alle Komponenten einer Aufgabe definiert, z. b. die Aufgaben Einstellungen, Trigger, Aktionen und Registrierungsinformationen.
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- Taskdefinition-Objekt Taskplaner
- Task Definition-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518077"
---
# <a name="taskdefinition-object"></a>Taskdefinition-Objekt

Skript Objekt, das alle Komponenten einer Aufgabe definiert, z. b. die Aufgaben Einstellungen, Trigger, Aktionen und Registrierungsinformationen.

## <a name="members"></a>Member

Das **Taskdefinition** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Taskdefinition** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                               | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktionen**](taskdefinition-actions.md)<br/>                   | Lesen/Schreiben<br/> | Ruft eine Auflistung von Aktionen ab, die vom Task ausgeführt werden, oder legt diese fest.<br/>                                                                                                         |
| [**Daten**](taskdefinition-data.md)<br/>                         | Lesen/Schreiben<br/> | Ruft die Daten ab, die der Aufgabe zugeordnet sind, oder legt Sie fest. Diese Daten werden vom Taskplaner-Dienst ignoriert, aber von Drittanbietern verwendet, die das Aufgaben Format erweitern möchten.<br/> |
| [**Prinzipal**](taskdefinition-principal.md)<br/>               | Lesen/Schreiben<br/> | Ruft den Prinzipal für die Aufgabe ab, die die Sicherheits Anmelde Informationen für den Task bereitstellt, oder legt ihn fest<br/>                                                                                 |
| [**RegistrationInfo**](taskdefinition-registrationinfo.md)<br/> | Lesen/Schreiben<br/> | Ruft die Registrierungsinformationen ab, die zum Beschreiben einer Aufgabe verwendet werden, z. b. die Beschreibung der Aufgabe, den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist, oder legt Sie fest.<br/> |
| [**Einstellungen**](taskdefinition-settings.md)<br/>                 | Lesen/Schreiben<br/> | Ruft die Einstellungen ab, die definieren, wie der Taskplaner-Dienst die Aufgabe ausführt, oder legt diese fest.<br/>                                                                                      |
| [**Trigger**](taskdefinition-triggers.md)<br/>                 | Lesen/Schreiben<br/> | Ruft eine Auflistung von Triggern ab, die zum Starten einer Aufgabe verwendet werden, oder legt diese fest.<br/>                                                                                                         |
| [**XmlText**](taskdefinition-xmltext.md)<br/>                   | Lesen/Schreiben<br/> | Ruft die XML-formatierte Definition der Aufgabe ab oder legt Sie fest.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird eine Aufgabendefinition mithilfe des [**Task**](taskschedulerschema-task-element.md) -Elements des Taskplaner Schemas angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md) , [Ereignis auslöserbeispiel (Skripterstellung)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Beispiel für den täglichen Auslösung [(Skripterstellung)](daily-trigger-example--scripting-.md), Registrierungs- [auslöserbeispiel (Skripterstellung)](registration-trigger-example--scripting-.md), Beispiel für einen wöchentlichen Aufruf [(](weekly-trigger-example--scripting-.md)Skripterstellung), Beispiel für LOGON-Beispiel [(Skript](logon-trigger-example--scripting-.md)Erstellung) oder [Beispiel](boot-trigger-example--scripting-.md)für

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 






---
title: RegisteredTask-Objekt
description: Skripterstellungsobjekt, das die Methoden bereitstellt, die zum sofortigen Ausführen des Tasks, zum Abrufen aller ausgeführten Instanzen des Tasks, zum Abrufen oder Festlegen der Anmeldeinformationen zum Registrieren der Aufgabe verwendet werden, sowie der Eigenschaften, die den Task beschreiben.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- RegisteredTask-Objekt Taskplaner
- RegisteredTask-Objekt Taskplaner beschrieben
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90dc83c47b37343c41489ca2d7b3288f727086e769e83104b57ca5b6de13b2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681640"
---
# <a name="registeredtask-object"></a>RegisteredTask-Objekt

Skripterstellungsobjekt, das die Methoden bereitstellt, die zum sofortigen Ausführen des Tasks, zum Abrufen aller ausgeführten Instanzen des Tasks, zum Abrufen oder Festlegen der Anmeldeinformationen zum Registrieren der Aufgabe verwendet werden, sowie der Eigenschaften, die den Task beschreiben.

## <a name="members"></a>Member

Das **RegisteredTask-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **RegisteredTask-Objekt** verfügt über diese Methoden.



| Methode                                                                | Beschreibung                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Getinstances**](registeredtask-getinstances.md)                   | Gibt alle Instanzen der registrierten Aufgabe zurück, die derzeit ausgeführt werden.<br/>             |
| [**GetRunTimes**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | Ruft die Zeiten ab, zu denen die Ausführung des registrierten Tasks während eines angegebenen Zeitraums geplant ist.<br/> |
| [**GetSecurityDescriptor**](registeredtask-getsecuritydescriptor.md) | Ruft den Sicherheitsdeskriptor ab, der als Anmeldeinformationen für den registrierten Task verwendet wird.<br/>    |
| [**Ausführung**](registeredtask-run.md)                                     | Führt die registrierte Aufgabe sofort aus.<br/>                                                |
| [**RunEx**](registeredtask-runex.md)                                 | Führt die registrierte Aufgabe sofort mithilfe der angegebenen Flags und eines Sitzungsbezeichners aus.<br/> |
| [**SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md) | Legt den Sicherheitsdeskriptor fest, der als Anmeldeinformationen für die registrierte Aufgabe verwendet wird.<br/>    |
| [**Stoppen**](registeredtask-stop.md)                                   | Beendet die registrierte Aufgabe sofort.<br/>                                               |



 

### <a name="properties"></a>Eigenschaften

Das **RegisteredTask-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                   | Zugriffstyp           | Beschreibung                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**Definition**](registeredtask-definition.md)<br/>                 | Schreibgeschützt<br/>  | Ruft die Definition der Aufgabe ab.<br/>                                               |
| [**Aktiviert**](registeredtask-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, ob die registrierte Aufgabe aktiviert ist, oder legt diesen fest.<br/>  |
| [**LastRunTime**](registeredtask-lastruntime.md)<br/>               | Schreibgeschützt<br/>  | Ruft den Zeitpunkt der letzten Ausführung des registrierten Tasks ab.<br/>                                |
| [**LastTaskResult**](registeredtask-lasttaskresult.md)<br/>         | Schreibgeschützt<br/>  | Ruft die Ergebnisse ab, die bei der letzten Ausführung der registrierten Aufgabe zurückgegeben wurden.<br/> |
| [**Name**](registeredtask-name.md)<br/>                             | Schreibgeschützt<br/>  | Ruft den Namen der registrierten Aufgabe ab.<br/>                                          |
| [**NextRunTime**](registeredtask-nextruntime.md)<br/>               | Schreibgeschützt<br/>  | Ruft die Zeit ab, zu der die nächste geplante Ausführung des registrierten Tasks geplant ist.<br/>               |
| [**NumberOfMissedRuns**](registeredtask-numberofmissedruns.md)<br/> | Schreibgeschützt<br/>  | Ruft ab, wie oft der registrierte Task eine geplante Ausführung verpasst hat.<br/>       |
| [**Pfad**](registeredtask-path.md)<br/>                             | Schreibgeschützt<br/>  | Ruft den Pfad zum Gespeicherten der registrierten Aufgabe ab.<br/>                          |
| [**State**](registeredtask-state.md)<br/>                           | Schreibgeschützt<br/>  | Ruft den Betriebszustand des registrierten Tasks ab.<br/>                             |
| [**Xml**](registeredtask-xml.md)<br/>                               | Schreibgeschützt<br/>  | Ruft die XML-formatierten Registrierungsinformationen für den registrierten Task ab.<br/>       |



 

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Zeittriggerbeispiel (Skripterstellung)](time-trigger-example--scripting-.md) und [Anzeigen von Aufgabennamen und Zuständen (Skripterstellung).](displaying-task-names-and-state--scripting-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 






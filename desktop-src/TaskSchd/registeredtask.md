---
title: Registeredtask-Objekt
description: Skript Objekt, das die Methoden bereitstellt, die verwendet werden, um den Task sofort auszuführen, alle laufenden Instanzen der Aufgabe zu erhalten, die zum Registrieren der Aufgabe verwendeten Anmelde Informationen zu erhalten oder festzulegen, sowie die Eigenschaften, die den Task beschreiben.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Registeredtask-Objekt Taskplaner
- Registeredtask-Objekt Taskplaner, beschrieben
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
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740472"
---
# <a name="registeredtask-object"></a>Registeredtask-Objekt

Skript Objekt, das die Methoden bereitstellt, die verwendet werden, um den Task sofort auszuführen, alle laufenden Instanzen der Aufgabe zu erhalten, die zum Registrieren der Aufgabe verwendeten Anmelde Informationen zu erhalten oder festzulegen, sowie die Eigenschaften, die den Task beschreiben.

## <a name="members"></a>Member

Das **registeredtask** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **registeredtask** -Objekt verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Getinhaltungen**](registeredtask-getinstances.md)                   | Gibt alle Instanzen der registrierten Aufgabe zurück, die zurzeit ausgeführt werden.<br/>             |
| [**Getruntimes**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | Ruft die Zeiten ab, zu denen die Ausführung der registrierten Aufgabe innerhalb eines angegebenen Zeitraums geplant ist.<br/> |
| [**GetSecurityDescriptor**](registeredtask-getsecuritydescriptor.md) | Ruft die Sicherheits Beschreibung ab, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.<br/>    |
| [**Ausführen**](registeredtask-run.md)                                     | Führt die registrierte Aufgabe sofort aus.<br/>                                                |
| [**RunEx**](registeredtask-runex.md)                                 | Führt die registrierte Aufgabe sofort mit angegebenen Flags und einem Sitzungs Bezeichner aus.<br/> |
| [**SETSECURITYDESCRIPTOR**](registeredtask-setsecuritydescriptor.md) | Legt die Sicherheits Beschreibung fest, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.<br/>    |
| [**Stop**](registeredtask-stop.md)                                   | Beendet die registrierte Aufgabe sofort.<br/>                                               |



 

### <a name="properties"></a>Eigenschaften

Das **registeredtask** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                   | Zugriffstyp           | BESCHREIBUNG                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**Definition**](registeredtask-definition.md)<br/>                 | Schreibgeschützt<br/>  | Ruft die Definition der Aufgabe ab.<br/>                                               |
| [**Aktiviert**](registeredtask-enabled.md)<br/>                       | Lesen/Schreiben<br/> | Ruft einen booleschen Wert ab, der angibt, ob die registrierte Aufgabe aktiviert ist, oder legt ihn fest.<br/>  |
| [**Lastrauuntime**](registeredtask-lastruntime.md)<br/>               | Schreibgeschützt<br/>  | Ruft den Zeitpunkt ab, zu dem die registrierte Aufgabe zuletzt ausgeführt wurde.<br/>                                |
| [**Lasttaskresult**](registeredtask-lasttaskresult.md)<br/>         | Schreibgeschützt<br/>  | Ruft die Ergebnisse ab, die bei der letzten Durchführung der registrierten Aufgabe zurückgegeben wurden.<br/> |
| [**Name**](registeredtask-name.md)<br/>                             | Schreibgeschützt<br/>  | Ruft den Namen der registrierten Aufgabe ab.<br/>                                          |
| [**NextRunTime**](registeredtask-nextruntime.md)<br/>               | Schreibgeschützt<br/>  | Ruft den Zeitpunkt ab, zu dem die nächste Ausführung der registrierten Aufgabe geplant wird.<br/>               |
| [**Anzahl von Fehlern**](registeredtask-numberofmissedruns.md)<br/> | Schreibgeschützt<br/>  | Ruft ab, wie oft die registrierte Aufgabe einen geplanten Testlauf verpasst hat.<br/>       |
| [**ADS**](registeredtask-path.md)<br/>                             | Schreibgeschützt<br/>  | Ruft den Pfad ab, in dem die registrierte Aufgabe gespeichert wird.<br/>                          |
| [**State**](registeredtask-state.md)<br/>                           | Schreibgeschützt<br/>  | Ruft den Betriebszustand der registrierten Aufgabe ab.<br/>                             |
| [**Basi**](registeredtask-xml.md)<br/>                               | Schreibgeschützt<br/>  | Ruft die XML-formatierten Registrierungsinformationen für die registrierte Aufgabe ab.<br/>       |



 

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md) und [Anzeigen von Aufgaben Namen und-Zuständen (Skripterstellung)](displaying-task-names-and-state--scripting-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 






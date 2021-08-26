---
title: Taskplaner Scripting Objects
description: Die Skriptobjekte, die in den folgenden Themen beschrieben werden, bieten programmgesteuerten Zugriff auf die Funktionen, die im Taskplaner für Visual Basic- und Visual Basic verfügbar sind.
ms.assetid: 632bc9ae-b300-42ed-9d2c-f1d2d53d44fb
keywords:
- Taskplaner Taskplaner , Referenz, Skriptobjekte
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f42eac1c9e8904933cedba54d1b51e5cc63919279de93286bfa658be1f60b11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100110"
---
# <a name="task-scheduler-scripting-objects"></a>Taskplaner Scripting Objects

Die Skriptobjekte, die in den folgenden Themen beschrieben werden, bieten programmgesteuerten Zugriff auf die Funktionen, die im Taskplaner für Visual Basic- und Visual Basic verfügbar sind.


Die folgenden Objekte werden in Taskplaner 2.0 eingeführt.



| Object                                                         | BESCHREIBUNG                                                                                                                                                                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktion**](action.md)                                       | Stellt die allgemeinen Eigenschaften dar, die von allen Aktionsobjekten geerbt werden.                                                                                                                                                                              |
| [**ActionCollection**](actioncollection.md)                   | Enthält die aktionen, die von der Aufgabe ausgeführt werden.                                                                                                                                                                                                           |
| [**BootTrigger**](boottrigger.md)                             | Stellt einen Trigger dar, der eine Aufgabe startet, wenn das System gestartet wird.                                                                                                                                                                                    |
| [**ComHandlerAction**](comhandleraction.md)                   | Stellt eine Aktion dar, die einen Handler ausspricht.                                                                                                                                                                                                            |
| [**DailyTrigger**](dailytrigger.md)                           | Stellt einen Trigger dar, der eine Aufgabe basierend auf einem täglichen Zeitplan startet.                                                                                                                                                                                    |
| [**EmailAction**](emailaction.md)                             | Stellt eine Aktion dar, die eine E-Mail sendet.                                                                                                                                                                                                     |
| [**EventTrigger**](eventtrigger.md)                           | Stellt einen Trigger dar, der eine Aufgabe startet, wenn ein Systemereignis auftritt.                                                                                                                                                                                   |
| [**ExecAction**](execaction.md)                               | Stellt eine Aktion dar, die einen Befehlszeilenvorgang ausgeführt.                                                                                                                                                                                          |
| [**IdleSettings**](idlesettings.md)                           | Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer in einem Leerlaufzustand befindet.                                                                                                                                                            |
| [**IdleTrigger**](idletrigger.md)                             | Stellt einen Trigger dar, der eine Aufgabe startet, wenn eine Leerlaufbedingung auftritt.                                                                                                                                                                                |
| [**LogonTrigger**](logontrigger.md)                           | Stellt einen Trigger dar, der eine Aufgabe startet, wenn sich ein Benutzer anmeldet.                                                                                                                                                                                          |
| [**MonthlyDOWTrigger**](monthlydowtrigger.md)                 | Stellt einen Trigger dar, der eine Aufgabe nach einem monatlichen Wochentag startet.                                                                                                                                                                            |
| [**MonthlyTrigger**](monthlytrigger.md)                       | Stellt einen Trigger dar, der eine Aufgabe basierend auf einem monatlichen Zeitplan startet.                                                                                                                                                                                  |
| [**NetworkSettings**](networksettings.md)                     | Stellt die Einstellungen zur Verfügung, die Taskplaner Dienst verwendet, um ein Netzwerkprofil zu erhalten.                                                                                                                                                               |
| [**Prinzipal**](principal.md)                                 | Stellt die Sicherheitsanmeldeinformationen für einen Prinzipal zur                                                                                                                                                                                                    |
| [**RegisteredTask**](registeredtask.md)                       | Stellt die Methoden zur sofortigen Ausführung der Aufgabe, zum Erhalten aller ausgeführten Instanzen der Aufgabe, zum Erhalten oder Festlegen der Anmeldeinformationen, die zum Registrieren der Aufgabe verwendet werden, sowie der Eigenschaften, die die Aufgabe beschreiben, zurEntspricht.                                      |
| [**RegisteredTaskCollection**](registeredtaskcollection.md)   | Enthält alle aufgaben, die registriert sind.                                                                                                                                                                                                           |
| [**RegistrationInfo**](registrationinfo.md)                   | Stellt die administrativen Informationen zur Verfügung, die zum Beschreiben der Aufgabe verwendet werden können. Diese Informationen umfassen Details wie eine Beschreibung der Aufgabe, den Autor der Aufgabe, das Datum, an dem die Aufgabe registriert wurde, und die Sicherheitsbeschreibung der Aufgabe. |
| [**RegistrationTrigger**](registrationtrigger.md)             | Stellt einen Trigger dar, der eine Aufgabe startet, wenn der Task registriert wird.                                                                                                                                                                                  |
| [**Wiederholungspattern**](repetitionpattern.md)                 | Definiert, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.                                                                                                                                          |
| [**RunningTask**](runningtask.md)                             | Stellt die Methoden zum Erhalten von Informationen aus einer ausgeführten Aufgabe und zum Steuern dieser Aufgabe zur Verfügung.                                                                                                                                                                              |
| [**RunningTaskCollection**](runningtaskcollection.md)         | Wird zum Abrufen einer ausgeführten Aufgabe verwendet.                                                                                                                                                                                                                      |
| [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) | Wird zum Auslösen von Aufgaben für Konsolenverbinden oder -trennen, Remote verbinden oder trennen oder Benachrichtigungen zur Arbeitsstationssperre oder -entsperrung auslösen.                                                                                                                   |
| [**ShowMessageAction**](showmessageaction.md)                 | Stellt eine Aktion dar, die ein Meldungsfeld zeigt, wenn eine Aufgabe aktiviert wird.                                                                                                                                                                               |
| [**TaskDefinition**](taskdefinition.md)                       | Definiert alle Komponenten einer Aufgabe, z. B. die Aufgabeneinstellungen, Trigger, Aktionen und Registrierungsinformationen.                                                                                                                                     |
| [**TaskFolder**](taskfolder.md)                               | Stellt die Methoden zum Registrieren (Erstellen) von Aufgaben im Ordner, Entfernen von Tasks aus dem Ordner und Erstellen oder Entfernen von Unterordnern aus dem Ordner zur Verfügung.                                                                                           |
| [**TaskFolderCollection**](taskfoldercollection.md)           | Zählt die Anzahl der Ordner in der Auflistung und ruft einen angegebenen Ordner aus der Auflistung ab.                                                                                                                                                   |
| [**TaskNamedValuePair**](tasknamedvaluepair.md)               | Erstellt ein Name-Wert-Paar, in dem der Name dem Wert zugeordnet ist.                                                                                                                                                                             |
| [**TaskNamedValueCollection**](tasknamedvaluecollection.md)   | Enthält eine Auflistung von Name-Wert-Paaren des [**TaskNamedValuePair-Objekts.**](tasknamedvaluepair.md)                                                                                                                                                    |
| [**TaskService**](taskservice.md)                             | Ermöglicht den Zugriff auf den Taskplaner zum Verwalten registrierter Aufgaben.                                                                                                                                                                          |
| [**TaskSettings**](tasksettings.md)                           | Stellt die Einstellungen zur Verfügung, die Taskplaner den Dienst zum Ausführen der Aufgabe verwenden.                                                                                                                                                                      |
| [**TaskVariables**](taskvariables.md)                         | Definiert Taskvariablen, die als Parameter an Taskhandler und externe ausführbare Dateien übergeben werden können, die von Tasks gestartet werden.                                                                                                                         |
| [**TimeTrigger**](timetrigger.md)                             | Stellt einen Trigger dar, der eine Aufgabe startet, wenn der Trigger aktiviert wird.                                                                                                                                                                                |
| [**Trigger**](trigger.md)                                     | Stellt die allgemeinen Eigenschaften dar, die von allen Triggerobjekten geerbt werden.                                                                                                                                                                             |
| [**Triggercollection**](triggercollection.md)                 | Wird zum Hinzufügen, Entfernen aus und Abrufen der Trigger einer Aufgabe verwendet.                                                                                                                                                                                     |
| [**WeeklyTrigger**](weeklytrigger.md)                         | Stellt einen Trigger dar, der eine Aufgabe basierend auf einem wöchentlichen Zeitplan startet.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner Referenz](task-scheduler-reference.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





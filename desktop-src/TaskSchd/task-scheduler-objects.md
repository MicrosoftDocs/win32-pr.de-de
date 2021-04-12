---
title: Skript Objekte Taskplaner
description: Die Skript Objekte, die in den folgenden Themen beschrieben werden, ermöglichen den programmgesteuerten Zugriff auf die Funktionen, die in der Taskplaner für Visual Basic und Visual Basic Skript-Entwickler zur Verfügung stehen.
ms.assetid: 632bc9ae-b300-42ed-9d2c-f1d2d53d44fb
keywords:
- Taskplaner Taskplaner, Referenz, Skript Erstellungs Objekten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acf9d74ae2bf586941f3b93a6c2cbb3a84836144
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104213078"
---
# <a name="task-scheduler-scripting-objects"></a>Skript Objekte Taskplaner

Die Skript Objekte, die in den folgenden Themen beschrieben werden, ermöglichen den programmgesteuerten Zugriff auf die Funktionen, die in der Taskplaner für Visual Basic und Visual Basic Skript-Entwickler zur Verfügung stehen.


Die folgenden Objekte werden in Taskplaner 2,0 eingeführt.



| Object                                                         | BESCHREIBUNG                                                                                                                                                                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Hinspiel**](action.md)                                       | Stellt die allgemeinen Eigenschaften bereit, die von allen Aktions Objekten geerbt werden.                                                                                                                                                                              |
| [**ActionCollection**](actioncollection.md)                   | Enthält die Aktionen, die vom Task ausgeführt werden.                                                                                                                                                                                                           |
| [**Boottrigger**](boottrigger.md)                             | Stellt einen-Fehler dar, der einen Task startet, wenn das System gestartet wird.                                                                                                                                                                                    |
| [**Comhandleraction**](comhandleraction.md)                   | Stellt eine Aktion dar, die einen Handler auslöst.                                                                                                                                                                                                            |
| [**Dailylöst**](dailytrigger.md)                           | Stellt einen-Auslösers dar, der einen Task auf Grundlage eines täglichen Zeitplans startet.                                                                                                                                                                                    |
| [**Emailaction**](emailaction.md)                             | Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.                                                                                                                                                                                                     |
| [**EventTrigger**](eventtrigger.md)                           | Stellt einen-Fehler dar, der einen Task startet, wenn ein System Ereignis auftritt.                                                                                                                                                                                   |
| [**Execaction**](execaction.md)                               | Stellt eine Aktion dar, die einen Befehlszeilen Vorgang ausführt.                                                                                                                                                                                          |
| [**Idlesettings**](idlesettings.md)                           | Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.                                                                                                                                                            |
| [**Idle-Auslösung**](idletrigger.md)                             | Stellt einen-Fehler dar, der einen Task startet, wenn eine Leerlauf Bedingung auftritt.                                                                                                                                                                                |
| [**Logonauslöst**](logontrigger.md)                           | Stellt einen-auslöst dar, der einen Task startet, wenn sich ein Benutzer anmeldet.                                                                                                                                                                                          |
| [**Monthlydowlöst**](monthlydowtrigger.md)                 | Stellt einen-auslöst dar, der einen Task an einem monatlichen Wochentag startet.                                                                                                                                                                            |
| [**Monthly-auslöst**](monthlytrigger.md)                       | Stellt einen-auslöst dar, der einen Task auf der Grundlage eines monatlichen Zeitplans startet.                                                                                                                                                                                  |
| [**NetworkSettings**](networksettings.md)                     | Gibt die Einstellungen an, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.                                                                                                                                                               |
| [**Prinzipal**](principal.md)                                 | Stellt die Sicherheits Anmelde Informationen für einen Prinzipal bereit.                                                                                                                                                                                                    |
| [**Registeredtask**](registeredtask.md)                       | Stellt die Methoden bereit, die verwendet werden, um die Aufgabe sofort auszuführen, alle laufenden Instanzen der Aufgabe zu erhalten, die Anmelde Informationen, die zum Registrieren der Aufgabe verwendet werden, sowie die Eigenschaften, die den Task beschreiben, zu erhalten oder festzulegen.                                      |
| [**Registeredtaskcollection**](registeredtaskcollection.md)   | Enthält alle registrierten Tasks.                                                                                                                                                                                                           |
| [**RegistrationInfo**](registrationinfo.md)                   | Enthält Informationen zu den administrativen Informationen, die zum Beschreiben der Aufgabe verwendet werden können. Diese Informationen umfassen Details wie z. b. eine Beschreibung der Aufgabe, den Autor der Aufgabe, das Datum, an dem der Task registriert ist, und die Sicherheits Beschreibung des Tasks. |
| [**Registration-Auslösers**](registrationtrigger.md)             | Stellt einen-auslöst dar, der einen Task startet, wenn der Task registriert wird.                                                                                                                                                                                  |
| [**Repetitionpattern**](repetitionpattern.md)                 | Definiert, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird.                                                                                                                                          |
| [**Runningtask**](runningtask.md)                             | Stellt die Methoden bereit, mit denen Sie Informationen aus einer laufenden Aufgabe erhalten und steuern können.                                                                                                                                                                              |
| [**Runningtaskcollection**](runningtaskcollection.md)         | Wird verwendet, um eine laufende Aufgabe abzurufen.                                                                                                                                                                                                                      |
| [**Sessionstatechange-Auslösers**](sessionstatechangetrigger.md) | Wird verwendet, um Aufgaben für die Konsolen Verbindung oder die Verbindung, die Remote Verbindung oder die Verbindung zu trennen oder Benachrichtigungen für die Arbeitsstation zu sperren                                                                                                                   |
| [**Showmessageaction**](showmessageaction.md)                 | Stellt eine Aktion dar, die ein Meldungs Feld anzeigt, wenn ein Task aktiviert wird.                                                                                                                                                                               |
| [**Task Definition**](taskdefinition.md)                       | Definiert alle Komponenten einer Aufgabe, z. b. die Aufgaben Einstellungen, Trigger, Aktionen und Registrierungsinformationen.                                                                                                                                     |
| [**Task Folder**](taskfolder.md)                               | Stellt die Methoden bereit, die verwendet werden, um Aufgaben im Ordner zu registrieren (zu erstellen), Tasks aus dem Ordner zu entfernen und Unterordner aus dem Ordner zu erstellen oder zu entfernen.                                                                                           |
| [**Taskfoldercollection**](taskfoldercollection.md)           | Zählt die Anzahl der Ordner in der Sammlung und Ruft einen angegebenen Ordner aus der Auflistung ab.                                                                                                                                                   |
| [**Tasknamedvaluepair**](tasknamedvaluepair.md)               | Erstellt ein Name-Wert-Paar, in dem der Name dem Wert zugeordnet ist.                                                                                                                                                                             |
| [**Tasknamedvaluecollection**](tasknamedvaluecollection.md)   | Enthält eine Auflistung von [**tasknamedvaluepair**](tasknamedvaluepair.md) -Objektname-Wert-Paaren.                                                                                                                                                    |
| [**Task Service**](taskservice.md)                             | Bietet Zugriff auf den Taskplaner-Dienst zum Verwalten registrierter Tasks.                                                                                                                                                                          |
| [**Tasksettings**](tasksettings.md)                           | Gibt die Einstellungen an, die die Taskplaner-Dienste zum Ausführen der Aufgabe verwenden.                                                                                                                                                                      |
| [**TaskVariables**](taskvariables.md)                         | Definiert Task Variablen, die als Parameter an Task Handler und externe ausführbare Dateien, die von Aufgaben gestartet werden, übermittelt werden können.                                                                                                                         |
| [**TimeTrigger**](timetrigger.md)                             | Stellt einen-Auslösers dar, der einen Task startet, wenn der-ausgelöst wird.                                                                                                                                                                                |
| [**Trigger**](trigger.md)                                     | Stellt die allgemeinen Eigenschaften bereit, die von allen auslöserobjekten geerbt werden.                                                                                                                                                                             |
| [**TriggerCollection**](triggercollection.md)                 | Wird zum Hinzufügen, entfernen und Abrufen der Trigger einer Aufgabe verwendet.                                                                                                                                                                                     |
| [**Weeklyauslösers**](weeklytrigger.md)                         | Stellt einen-Auslösers dar, der einen Task auf der Grundlage eines wöchentlichen Zeitplans startet.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner Referenz](task-scheduler-reference.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





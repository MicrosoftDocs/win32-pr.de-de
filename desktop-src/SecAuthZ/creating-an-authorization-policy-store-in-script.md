---
description: Anweisungen zum Verwenden der Autorisierungs-Manager-API zum Erstellen eines Autorisierungs Richtlinien Speicher im Skript.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Erstellen eines Autorisierungs Richtlinien Speicher im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130656"
---
# <a name="creating-an-authorization-policy-store-in-script"></a>Erstellen eines Autorisierungs Richtlinien Speicher im Skript

Erstellen Sie eine Autorisierungs Richtlinie vor oder während der Installation einer Anwendung.

Wenn Sie die Autorisierungs-Manager-API verwenden, um eine Autorisierungs Richtlinie zu erstellen, befolgen Sie die Anweisungen in den folgenden Themen.



| Thema                                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen eines Autorisierungs Richtlinien-Speicher Objekts im Skript](creating-an-authorization-policy-store-object-in-script.md) | Ein Autorisierungs Richtlinien Speicher enthält Informationen über die Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen.                                                                                                                                       |
| [Erstellen eines Anwendungs Objekts im Skript](creating-an-application-object-in-script.md)                               | Für jede Anwendung, die einen Autorisierungs Richtlinien Speicher verwendet, müssen Sie ein [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekt erstellen und in einem Richtlinien Speicher speichern.                                                                                                |
| [Definieren von Vorgängen in Skripts](defining-operations-in-script.md)                                                     | Bei einem Vorgang handelt es sich um eine Funktion oder Methode einer Anwendung auf niedriger Ebene.                                                                                                                                                                                              |
| [Gruppieren von Vorgängen in Aufgaben in Skripts](grouping-operations-into-tasks-in-script.md)                               | Eine Aufgabe ist eine allgemeine Aktion, die Benutzer einer Anwendung ausführen müssen. Aufgaben bestehen aus Vorgängen, bei denen es sich um Low-Level-Funktionen und-Methoden der Anwendung handelt.                                                                                    |
| [Gruppieren von Aufgaben in Rollen in Skripts](grouping-tasks-into-roles-in-script.md)                                         | Eine Rolle stellt eine Kategorie von Benutzern und die Aufgaben dar, die diese Benutzer für die Ausführung autorisiert haben.                                                                                                                                                                     |
| [Definieren von Benutzergruppen in Skripts](defining-groups-of-users-in-script.md)                                           | Ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt stellt eine Gruppe von Benutzern dar. Rollen können dieser Gruppe von Benutzern gemeinsam zugewiesen werden. Ein **iazapplicationgroup** -Objekt kann auch andere **iazapplicationgroup** -Objekte als Member enthalten. |
| [Hinzufügen von Benutzern zu einer Anwendungs Gruppe im Skript](adding-users-to-an-application-group-in-script.md)                   | Eine Anwendungs Gruppe ist eine Gruppe von Benutzern und Benutzergruppen. Eine Anwendungs Gruppe kann andere Anwendungs Gruppen enthalten, sodass Gruppen von Benutzern gruppiert werden können. Eine Anwendungs Gruppe wird durch ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt dargestellt.    |



 

 

 




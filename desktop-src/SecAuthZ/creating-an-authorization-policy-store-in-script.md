---
description: Anweisungen für die Verwendung der Autorisierungs-Manager-API zum Erstellen eines Autorisierungsrichtlinienspeichers in Script.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Erstellen einer Autorisierungsrichtlinie Store in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cbe8bf5457f36cdb71577ae13c2cc226115d4c968436c84b72ca8e90a3446be9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782536"
---
# <a name="creating-an-authorization-policy-store-in-script"></a>Erstellen einer Autorisierungsrichtlinie Store in Skripts

Erstellen Sie vor oder während der Installation einer Anwendung eine Autorisierungsrichtlinie.

Wenn Sie die Autorisierungs-Manager-API zum Erstellen einer Autorisierungsrichtlinie verwenden, befolgen Sie die Anweisungen in den folgenden Themen.



| Thema                                                                                                                  | Beschreibung                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen einer Autorisierungsrichtlinie Store-Objekts im Skript](creating-an-authorization-policy-store-object-in-script.md) | Ein Autorisierungsrichtlinienspeicher enthält Informationen zur Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen.                                                                                                                                       |
| [Erstellen eines Anwendungsobjekts im Skript](creating-an-application-object-in-script.md)                               | Für jede Anwendung, die einen Autorisierungsrichtlinienspeicher verwendet, müssen Sie ein [**IAzApplication-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) erstellen und in einem Richtlinienspeicher speichern.                                                                                                |
| [Definieren von Vorgängen in Skripts](defining-operations-in-script.md)                                                     | Ein Vorgang ist eine Funktion oder Methode auf niedriger Ebene einer Anwendung.                                                                                                                                                                                              |
| [Gruppieren von Vorgängen in Tasks in Skripts](grouping-operations-into-tasks-in-script.md)                               | Eine Aufgabe ist eine übergeordnete Aktion, die Benutzer einer Anwendung ausführen müssen. Aufgaben bestehen aus Vorgängen, bei denen es sich um Funktionen und Methoden auf niedriger Ebene der Anwendung handelt.                                                                                    |
| [Gruppieren von Aufgaben in Rollen in Skripts](grouping-tasks-into-roles-in-script.md)                                         | Eine Rolle stellt eine Kategorie von Benutzern und die Aufgaben dar, für die diese Benutzer autorisiert sind.                                                                                                                                                                     |
| [Definieren von Benutzergruppen in Skripts](defining-groups-of-users-in-script.md)                                           | Ein [**IAzApplicationGroup-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) stellt eine Gruppe von Benutzern dar. Rollen können dann dieser Gruppe von Benutzern gemeinsam zugewiesen werden. Ein **IAzApplicationGroup-Objekt** kann auch andere **IAzApplicationGroup-Objekte** als Member enthalten. |
| [Hinzufügen von Benutzern zu einer Anwendungsgruppe im Skript](adding-users-to-an-application-group-in-script.md)                   | Eine Anwendungsgruppe ist eine Gruppe von Benutzern und Benutzergruppen. Eine Anwendungsgruppe kann andere Anwendungsgruppen enthalten, sodass Benutzergruppen geschachtelt werden können. Eine Anwendungsgruppe wird durch ein [**IAzApplicationGroup-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) dargestellt.    |



 

 

 




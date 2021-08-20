---
description: Anweisungen für die Verwendung der Autorisierungs-Manager-API zum Erstellen eines Autorisierungsrichtlinienspeichers in C++.
ms.assetid: a350f25a-7cda-4879-82d1-151a3da7d8ec
title: Erstellen einer Autorisierungsrichtlinie Store in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90eeb30fd1e66bc69760f8bf3d714419fe818dbda06c1b8e2eb059aeb579ca74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782526"
---
# <a name="creating-an-authorization-policy-store-in-c"></a>Erstellen einer Autorisierungsrichtlinie Store in C++

Erstellen Sie vor oder während der Installation einer Anwendung eine Autorisierungsrichtlinie.

Wenn Sie die Autorisierungs-Manager-API zum Erstellen einer Autorisierungsrichtlinie verwenden, befolgen Sie die Anweisungen in den folgenden Themen.



| Thema                                                                                                            | Beschreibung                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen einer Autorisierungsrichtlinie Store-Objekts in C++](creating-an-authorization-policy-store-object-in-c--.md) | Ein Autorisierungsrichtlinienspeicher enthält Informationen zur Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen. Die Informationen umfassen die Anwendungen, Vorgänge, Aufgaben, Benutzer und Benutzergruppen, die dem Speicher zugeordnet sind.              |
| [Erstellen eines Anwendungsobjekts in C++](creating-an-application-object-in-c--.md)                               | Ein Autorisierungsrichtlinienspeicher enthält Autorisierungsrichtlinieninformationen für eine oder mehrere Anwendungen. Für jede Anwendung, die diesen Richtlinienspeicher verwendet, müssen Sie ein [**IAzApplication-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) erstellen und in einem Richtlinienspeicher speichern. |
| [Definieren von Vorgängen in C++](defining-operations-in-c--.md)                                                     | Im Autorisierungs-Manager ist ein Vorgang eine Funktion oder Methode auf niedriger Ebene einer Anwendung.                                                                                                                                                               |
| [Gruppieren von Vorgängen in Aufgaben in C++](grouping-operations-into-tasks-in-c--.md)                               | Im Autorisierungs-Manager ist eine Aufgabe eine übergeordnete Aktion, die Benutzer einer Anwendung ausführen müssen. Aufgaben bestehen aus Vorgängen, bei denen es sich um Funktionen und Methoden auf niedriger Ebene der Anwendung handelt.                                                     |
| [Gruppieren von Aufgaben in Rollen in C++](grouping-tasks-into-roles-in-c--.md)                                         | Im Autorisierungs-Manager stellt eine Rolle eine Kategorie von Benutzern und die Aufgaben dar, für die diese Benutzer autorisiert sind.                                                                                                                                      |
| [Definieren von Benutzergruppen in C++](defining-groups-of-users-in-c--.md)                                           | Im Autorisierungs-Manager stellt ein [**IAzApplicationGroup-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) eine Gruppe von Benutzern dar. Rollen können dann dieser Gruppe von Benutzern gemeinsam zugewiesen werden.                                                                       |
| [Hinzufügen von Benutzern zu einer Anwendungsgruppe in C++](adding-users-to-an-application-group-in-c--.md)                   | Im Autorisierungs-Manager ist eine Anwendungsgruppe eine Gruppe von Benutzern und Benutzergruppen. Eine Anwendungsgruppe kann andere Anwendungsgruppen enthalten, sodass Benutzergruppen geschachtelt werden können.                                                                          |



 

 

 




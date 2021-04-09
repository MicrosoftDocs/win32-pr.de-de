---
description: Anweisungen zum Verwenden der Autorisierungs-Manager-API zum Erstellen eines Autorisierungs Richtlinien Stores in C++.
ms.assetid: a350f25a-7cda-4879-82d1-151a3da7d8ec
title: Erstellen eines Autorisierungs Richtlinien Speicher in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdff3ba26457510440c8d0e603bc993a4878281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130253"
---
# <a name="creating-an-authorization-policy-store-in-c"></a>Erstellen eines Autorisierungs Richtlinien Speicher in C++

Erstellen Sie eine Autorisierungs Richtlinie vor oder während der Installation einer Anwendung.

Wenn Sie die Autorisierungs-Manager-API verwenden, um eine Autorisierungs Richtlinie zu erstellen, befolgen Sie die Anweisungen in den folgenden Themen.



| Thema                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen eines Autorisierungs Richtlinien-Speicher Objekts in C++](creating-an-authorization-policy-store-object-in-c--.md) | Ein Autorisierungs Richtlinien Speicher enthält Informationen über die Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen. Zu diesen Informationen gehören die Anwendungen, Vorgänge, Tasks, Benutzer und Gruppen von Benutzern, die dem Speicher zugeordnet sind.              |
| [Erstellen eines Anwendungs Objekts in C++](creating-an-application-object-in-c--.md)                               | Ein Autorisierungs Richtlinien Speicher enthält Autorisierungs Richtlinien Informationen für eine oder mehrere Anwendungen. Für jede Anwendung, die diesen Richtlinien Speicher verwendet, müssen Sie ein [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekt erstellen und in einem Richtlinien Speicher speichern. |
| [Definieren von Vorgängen in C++](defining-operations-in-c--.md)                                                     | Im Autorisierungs-Manager handelt es sich bei einem Vorgang um eine Funktion oder Methode einer Anwendung auf niedriger Ebene.                                                                                                                                                               |
| [Gruppieren von Vorgängen in Aufgaben in C++](grouping-operations-into-tasks-in-c--.md)                               | Im Autorisierungs-Manager ist eine Aufgabe eine allgemeine Aktion, die Benutzer einer Anwendung ausführen müssen. Aufgaben bestehen aus Vorgängen, bei denen es sich um Low-Level-Funktionen und-Methoden der Anwendung handelt.                                                     |
| [Gruppieren von Aufgaben in Rollen in C++](grouping-tasks-into-roles-in-c--.md)                                         | Im Autorisierungs-Manager stellt eine Rolle eine Kategorie von Benutzern und die Aufgaben dar, die diese Benutzer für die Ausführung autorisiert haben.                                                                                                                                      |
| [Definieren von Benutzergruppen in C++](defining-groups-of-users-in-c--.md)                                           | Im Autorisierungs-Manager stellt ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt eine Gruppe von Benutzern dar. Rollen können dieser Gruppe von Benutzern gemeinsam zugewiesen werden.                                                                       |
| [Hinzufügen von Benutzern zu einer Anwendungs Gruppe in C++](adding-users-to-an-application-group-in-c--.md)                   | Im Autorisierungs-Manager ist eine Anwendungs Gruppe eine Gruppe von Benutzern und Benutzergruppen. Eine Anwendungs Gruppe kann andere Anwendungs Gruppen enthalten, sodass Gruppen von Benutzern gruppiert werden können.                                                                          |



 

 

 




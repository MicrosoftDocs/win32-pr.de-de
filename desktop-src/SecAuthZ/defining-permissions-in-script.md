---
description: Anweisungen zum Verwenden der Autorisierungs-Manager-API zum Definieren von Berechtigungen in Skripts durch Erstellen eines Autorisierungs Richtlinien Speicher.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Definieren von Berechtigungen in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e16f377ffa669da0b686ac28783e9a370efec94d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960328"
---
# <a name="defining-permissions-in-script"></a>Definieren von Berechtigungen in Skripts

Im Autorisierungs-Manager definieren Sie, welche Benutzer Zugriff auf welche Anwendungs Ressourcen haben, indem Sie einen Autorisierungs Richtlinien Speicher erstellen.

**So definieren Sie Zugriffsberechtigungen**

1.  Erstellen Sie den Speicher, in dem die Autorisierungs Richtlinie definiert ist:<dl>

[Erstellen eines Autorisierungs Richtlinien Speicher im Skript](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  Erstellen Sie im Autorisierungs Richtlinien Speicher einen Abschnitt für eine bestimmte Anwendung:<dl>

[Erstellen eines Anwendungs Objekts im Skript](creating-an-application-object-in-script.md)  
    </dl>
3.  Definieren von Vorgängen, die die Anwendung implementiert, um auf Ressourcen zuzugreifen und diese zu ändern<dl>

[Definieren von Vorgängen in Skripts](defining-operations-in-script.md)  
    </dl>
4.  Gruppieren von Vorgängen in Aufgaben auf hoher Ebene, die von Benutzern ausgeführt werden sollen:<dl>

[Gruppieren von Vorgängen in Aufgaben in Skripts](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  Definieren von Rollen, die aus Gruppen von Aufgaben bestehen:<dl>

[Gruppieren von Aufgaben in Rollen in Skripts](grouping-tasks-into-roles-in-script.md)  
    </dl>Ein Benutzer, der einer Rolle zugewiesen ist, verfügt über die Berechtigung zum Ausführen beliebiger Aufgaben, die dieser Rolle zugewiesen sind.
6.  Erstellen Sie Skripts, um den Zugriff auf Aufgaben zur Laufzeit zu qualifizieren:<dl>

[Qualifizieren des Zugriffs mit Geschäftslogik in Skripts](qualifying-access-with-business-logic-in-script.md)  
    </dl>Dieser Schritt ist optional.
7.  Definieren von Benutzergruppen:<dl>

[Definieren von Benutzergruppen in Skripts](defining-groups-of-users-in-script.md)  
    </dl>Diese Gruppen können dann Rollen zugewiesen werden, um zu bestimmen, welche Aufgaben Sie ausführen können.
8.  Benutzer zu Benutzergruppen hinzufügen:<dl>

[Hinzufügen von Benutzern zu einer Anwendungs Gruppe im Skript](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 




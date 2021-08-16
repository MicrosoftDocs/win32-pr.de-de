---
description: Anweisungen zum Verwenden der Autorisierungs-Manager-API zum Definieren von Berechtigungen in Skripts durch Erstellen eines Autorisierungsrichtlinienspeichers.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Definieren von Berechtigungen in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 772c55f453a68e3bf1a4933abc4beb7cf3d65380b3bcf5d2e2c4af2832173b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782101"
---
# <a name="defining-permissions-in-script"></a>Definieren von Berechtigungen in Skripts

Im Autorisierungs-Manager definieren Sie, welche Benutzer Zugriff auf welche Anwendungsressourcen haben, indem Sie einen Autorisierungsrichtlinienspeicher erstellen.

**So definieren Sie Zugriffsberechtigungen**

1.  Erstellen Sie den Speicher, in dem die Autorisierungsrichtlinie definiert ist:<dl>

[Erstellen einer Autorisierungsrichtlinie Store in Skripts](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  Erstellen Sie einen Abschnitt im Autorisierungsrichtlinienspeicher für eine bestimmte Anwendung:<dl>

[Erstellen eines Anwendungsobjekts im Skript](creating-an-application-object-in-script.md)  
    </dl>
3.  Definieren Sie Vorgänge, die die Anwendung implementiert, um auf Ressourcen zuzugreifen und diese zu ändern:<dl>

[Definieren von Vorgängen in Skripts](defining-operations-in-script.md)  
    </dl>
4.  Gruppieren Sie Vorgänge in übergeordnete Aufgaben, die Benutzer ausführen möchten:<dl>

[Gruppieren von Vorgängen in Tasks in Skripts](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  Definieren Sie Rollen, die aus Aufgabengruppen bestehen:<dl>

[Gruppieren von Aufgaben in Rollen in Skripts](grouping-tasks-into-roles-in-script.md)  
    </dl>Ein Benutzer, der einer Rolle zugewiesen ist, verfügt über die Berechtigung zum Ausführen von Aufgaben, die dieser Rolle zugewiesen sind.
6.  Erstellen Sie Skripts, um den Zugriff auf Aufgaben zur Laufzeit zu qualifizieren:<dl>

[Qualifizieren des Zugriffs mit Geschäftslogik in Skripts](qualifying-access-with-business-logic-in-script.md)  
    </dl>Dieser Schritt ist optional.
7.  Definieren von Benutzergruppen:<dl>

[Definieren von Benutzergruppen in Skripts](defining-groups-of-users-in-script.md)  
    </dl>Diese Gruppen können dann Rollen zugewiesen werden, um zu bestimmen, welche Aufgaben sie ausführen können.
8.  Hinzufügen von Benutzern zu Benutzergruppen:<dl>

[Hinzufügen von Benutzern zu einer Anwendungsgruppe im Skript](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 




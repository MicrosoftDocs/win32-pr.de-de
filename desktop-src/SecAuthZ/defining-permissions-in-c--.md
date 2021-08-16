---
description: Anweisungen zur Verwendung der Autorisierungs-Manager-API zum Definieren von Berechtigungen in C++ durch Erstellen eines Autorisierungsrichtlinienspeichers.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Definieren von Berechtigungen in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 008c82e74bcd4b4fec714e43c8beb7d8c7e908baaf569ee260559f64ba5bbc10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913773"
---
# <a name="defining-permissions-in-c"></a>Definieren von Berechtigungen in C++

Im Autorisierungs-Manager definieren Sie, welche Benutzer Zugriff auf welche Anwendungsressourcen haben, indem Sie einen Autorisierungsrichtlinienspeicher erstellen.

Informationen zum Definieren von Berechtigungen mit ACLs finden Sie unter [Definieren von Berechtigungen mit ACLs in C++.](defining-permissions-with-acls-in-c--.md)

**So definieren Sie Zugriffsberechtigungen**

1.  Erstellen Sie den Speicher, in dem die Autorisierungsrichtlinie definiert ist:<dl>

[Erstellen eines Autorisierungsrichtlinien-Store-Objekts in C++](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  Erstellen Sie einen Abschnitt im Autorisierungsrichtlinienspeicher für eine bestimmte Anwendung:<dl>

[Erstellen eines Anwendungsobjekts in C++](creating-an-application-object-in-c--.md)  
    </dl>
3.  Definieren Sie Vorgänge, die die Anwendung implementiert, um auf Ressourcen zu zugreifen und sie zu ändern:<dl>

[Definieren von Vorgängen in C++](defining-operations-in-c--.md)  
    </dl>
4.  Grupping von Vorgängen in tasks auf hoher Ebene, die Benutzer ausführen möchten:<dl>

[Gruppieren von Vorgängen in Tasks in C++](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  Definieren Sie Rollen, die aus Aufgabengruppen bestehen:<dl>

[Gruppieren von Aufgaben in Rollen in C++](grouping-tasks-into-roles-in-c--.md)  
    </dl>Ein Benutzer, der einer Rolle zugewiesen ist, verfügt über die Berechtigung zum Ausführen einer aufgabe, die dieser Rolle zugewiesen ist.
6.  Erstellen Sie Skripts, um den Zugriff auf Aufgaben zur Laufzeit zu qualifizieren:<dl>

[Qualifizieren des Zugriffs mit Geschäftslogik in C++](qualifying-access-with-business-logic-in-c--.md)  
    </dl>Dieser Schritt ist optional.
7.  Definieren von Benutzergruppen:<dl>

[Definieren von Benutzergruppen in C++](defining-groups-of-users-in-c--.md)  
    </dl>Diese Gruppen können dann Rollen zugewiesen werden, um zu bestimmen, welche Aufgaben sie ausführen können.
8.  Hinzufügen von Benutzern zu Benutzergruppen:<dl>

[Hinzufügen von Benutzern zu einer Anwendungsgruppe in C++](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 




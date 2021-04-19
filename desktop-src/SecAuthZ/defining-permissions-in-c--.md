---
description: Anweisungen zum Verwenden der Autorisierungs-Manager-API zum Definieren von Berechtigungen in C++ durch Erstellen eines Autorisierungs Richtlinien Speicher.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Definieren von Berechtigungen in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366518"
---
# <a name="defining-permissions-in-c"></a>Definieren von Berechtigungen in C++

Im Autorisierungs-Manager definieren Sie, welche Benutzer Zugriff auf welche Anwendungs Ressourcen haben, indem Sie einen Autorisierungs Richtlinien Speicher erstellen.

Informationen zum Definieren von Berechtigungen mit Zugriffs Steuerungs Listen finden Sie unter [Definieren von Berechtigungen mit ACLs in C++](defining-permissions-with-acls-in-c--.md).

**So definieren Sie Zugriffsberechtigungen**

1.  Erstellen Sie den Speicher, in dem die Autorisierungs Richtlinie definiert ist:<dl>

[Erstellen eines Autorisierungs Richtlinien-Speicher Objekts in C++](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  Erstellen Sie im Autorisierungs Richtlinien Speicher einen Abschnitt für eine bestimmte Anwendung:<dl>

[Erstellen eines Anwendungs Objekts in C++](creating-an-application-object-in-c--.md)  
    </dl>
3.  Definieren von Vorgängen, die die Anwendung implementiert, um auf Ressourcen zuzugreifen und diese zu ändern<dl>

[Definieren von Vorgängen in C++](defining-operations-in-c--.md)  
    </dl>
4.  Gruppieren von Vorgängen in Aufgaben auf hoher Ebene, die von Benutzern ausgeführt werden sollen:<dl>

[Gruppieren von Vorgängen in Aufgaben in C++](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  Definieren von Rollen, die aus Gruppen von Aufgaben bestehen:<dl>

[Gruppieren von Aufgaben in Rollen in C++](grouping-tasks-into-roles-in-c--.md)  
    </dl>Ein Benutzer, der einer Rolle zugewiesen ist, verfügt über die Berechtigung zum Ausführen beliebiger Aufgaben, die dieser Rolle zugewiesen sind.
6.  Erstellen Sie Skripts, um den Zugriff auf Aufgaben zur Laufzeit zu qualifizieren:<dl>

[Qualifizieren des Zugriffs mit Geschäftslogik in C++](qualifying-access-with-business-logic-in-c--.md)  
    </dl>Dieser Schritt ist optional.
7.  Definieren von Benutzergruppen:<dl>

[Definieren von Benutzergruppen in C++](defining-groups-of-users-in-c--.md)  
    </dl>Diese Gruppen können dann Rollen zugewiesen werden, um zu bestimmen, welche Aufgaben Sie ausführen können.
8.  Benutzer zu Benutzergruppen hinzufügen:<dl>

[Hinzufügen von Benutzern zu einer Anwendungs Gruppe in C++](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 




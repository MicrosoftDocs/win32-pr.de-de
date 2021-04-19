---
description: Verwenden der Autorisierungs-Manager-API, um den Zugriff auf Anwendungs Ressourcen zu steuern.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Verwenden der Autorisierung in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363625"
---
# <a name="using-authorization-in-c"></a>Verwenden der Autorisierung in C++

Sie können die Autorisierungs-Manager-API verwenden, um den Zugriff auf Anwendungs Ressourcen zu steuern.

Wenn Sie über eine vorhandene Zugriffs Steuerungslösung verfügen, die auf [*Zugriffs Steuerungs Listen (Access Control Lists*](/windows/desktop/SecGloss/a-gly) , ACLs) basiert, und Sie die Projekt Mappe nicht zur Verwendung des Autorisierungs-Managers umrechnen möchten, können Sie weiterhin ACLs zum Steuern des Zugriffs auf Ressourcen verwenden Informationen zum Steuern des Zugriffs auf Ressourcen mithilfe von ACLs finden Sie unter [Definieren von Berechtigungen mit ACLs in C++](defining-permissions-with-acls-in-c--.md), [Einrichten eines Client Kontexts aus einer SID in C++](establishing-a-client-context-from-a-sid-in-c--.md)und über [prüfen des Client Zugriffs mit ACLs in C++](verifying-client-access-with-acls-in-c--.md).

> [!Note]  
> Für große Unternehmen gibt es einen Kompromiss zwischen Verwaltungsaufwand und Leistung. Wenn die Anzahl der gesicherten Ressourcen und Benutzer zunimmt, wird die Verwaltung von ACLs komplizierter. Die Leistung wird nicht beeinträchtigt, da alle erforderlichen Informationen zu Zugriffsrechten an die gesicherten Ressourcen verteilt werden. Die Leistung des Autorisierungs-Managers wird durch die Skalierung beeinträchtigt.

 

Weitere Informationen zu anderen Autorisierungs Aufgaben finden Sie [unter unterstützen von Aufgaben für die Autorisierung in C++](supporting-tasks-for-authorization-in-c--.md).



| Thema                                                                                                                | BESCHREIBUNG                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Definieren von Berechtigungen in C++](defining-permissions-in-c--.md)                                                       | Definieren Sie, welche Benutzer auf welche Anwendungs Ressourcen zugreifen können, indem Sie einen Autorisierungs Richtlinien Speicher erstellen. |
| [Überprüfen des Client Zugriffs auf eine angeforderte Ressource in C++](verifying-client-access-to-a-requested-resource-in-c--.md) | Überprüfen Sie, ob der Client Zugriff auf einen oder mehrere Vorgänge hat.                                           |
| [Delegieren der definierenden Berechtigungen in C++](delegating-the-defining-of-permissions-in-c--.md)                   | Delegieren Sie die Verwaltung der Autorisierungs Richtlinien Speicher, die in Active Directory gespeichert werden.          |



 

 

 

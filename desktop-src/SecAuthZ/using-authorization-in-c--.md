---
description: Verwenden Sie die Autorisierungs-Manager-API, um den Zugriff auf Anwendungsressourcen zu steuern.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Verwenden der Autorisierung in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b948c138c24b0042d7f1f33fd95acceb18ab6afb9dfdcac7db2b61127fbc41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906770"
---
# <a name="using-authorization-in-c"></a>Verwenden der Autorisierung in C++

Sie können die Autorisierungs-Manager-API verwenden, um den Zugriff auf Anwendungsressourcen zu steuern.

Wenn Sie über eine vorhandene Zugriffssteuerungslösung verfügen, die auf Zugriffssteuerungslisten (Access [*Control*](/windows/desktop/SecGloss/a-gly) Lists, ACLs) basiert und vermeiden möchten, diese Lösung für die Verwendung des Autorisierungs-Managers zu konvertieren, können Sie weiterhin ACLs verwenden, um den Zugriff auf Ressourcen zu steuern. Informationen zum Steuern des Zugriffs auf Ressourcen mithilfe von ACLs finden Sie unter Definieren von Berechtigungen mit [ACLs in C++,](defining-permissions-with-acls-in-c--.md)Einrichten eines Clientkontexts über eine [SID in C++](establishing-a-client-context-from-a-sid-in-c--.md)und Überprüfen des Clientzugriffs mit [ACLs in C++.](verifying-client-access-with-acls-in-c--.md)

> [!Note]  
> Bei großen Unternehmen gibt es einen Abkniff zwischen Verwaltungsaufwand und Leistung. Mit zunehmender Anzahl geschützter Ressourcen und Benutzer wird die Verwaltung von ACLs komplizierter. Die Leistung wird nicht beeinträchtigt, da alle erforderlichen Informationen zu Zugriffsrechten an die gesicherten Ressourcen verteilt werden. Die Leistung des Autorisierungs-Managers wird durch die Skalierung beeinträchtigt.

 

Informationen zu anderen Autorisierungsaufgaben finden Sie unter [Unterstützende Aufgaben für die Autorisierung in C++.](supporting-tasks-for-authorization-in-c--.md)



| Thema                                                                                                                | BESCHREIBUNG                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Definieren von Berechtigungen in C++](defining-permissions-in-c--.md)                                                       | Legen Sie fest, welche Benutzer Zugriff auf welche Anwendungsressourcen haben, indem Sie einen Autorisierungsrichtlinienspeicher erstellen. |
| [Überprüfen des Clientzugriffs auf eine angeforderte Ressource in C++](verifying-client-access-to-a-requested-resource-in-c--.md) | Überprüfen Sie, ob der Client Zugriff auf einen oder mehrere Vorgänge hat.                                           |
| [Delegieren der Definition von Berechtigungen in C++](delegating-the-defining-of-permissions-in-c--.md)                   | Delegieren Sie die Verwaltung von Autorisierungsrichtlinienspeichern, die in Active Directory gespeichert sind.          |



 

 

 

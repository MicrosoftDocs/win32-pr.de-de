---
description: Jeder Dienst wird im Sicherheitskontext eines Benutzerkontos ausgeführt.
ms.assetid: a0e48918-6957-4288-a188-d65198b38c16
title: Dienst Benutzerkonten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c72f332b8eddbc5b5929718b6688f75e226e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868179"
---
# <a name="service-user-accounts"></a>Dienst Benutzerkonten

Jeder Dienst wird im Sicherheitskontext eines Benutzerkontos ausgeführt. Der Benutzername und das Kennwort eines Kontos werden bei der Installation des Diensts durch die Funktion " [**roateservice**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) " angegeben. Der Benutzername und das Kennwort können mithilfe der [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) -Funktion geändert werden. Mit der [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) -Funktion können Sie den Benutzernamen (aber nicht das Kennwort) abrufen, der einem Dienst Objekt zugeordnet ist. Der Dienststeuerungs-Manager (Service Control Manager, SCM) lädt das Benutzerprofil automatisch.

Wenn ein Dienst gestartet wird, meldet sich der SCM bei dem Konto an, das dem Dienst zugeordnet ist. Wenn die Anmeldung erfolgreich ist, erstellt das System ein Zugriffs Token und fügt es an den neuen Dienst Prozess an. Dieses Token identifiziert den Dienst Prozess in allen nachfolgenden Interaktionen mit Sicherungs fähigen Objekten (Objekte, denen eine Sicherheits Beschreibung zugeordnet ist). Wenn der Dienst z. b. versucht, ein Handle für eine Pipe zu öffnen, vergleicht das System das Zugriffs Token des Diensts mit der Sicherheits Beschreibung der Pipe, bevor der Zugriff gewährt wird.

Der SCM behält die Kenn Wörter der Dienst Benutzerkonten nicht bei. Wenn ein Kennwort abgelaufen ist, tritt bei der Anmeldung ein Fehler auf, und der Dienst kann nicht gestartet werden. Der Systemadministrator, der-Dienste Konten zuweist, kann Konten mit Kenn Wörtern erstellen, die nie ablaufen. Der Administrator kann auch Konten mit Kenn Wörtern verwalten, die ablaufen, indem ein [Dienst Konfigurationsprogramm](service-configuration-programs.md) verwendet wird, um die Kenn Wörter regelmäßig zu ändern.

Wenn ein Dienst einen anderen Dienst vor der Freigabe seiner Informationen erkennen muss, kann der zweite Dienst entweder das gleiche Konto wie der erste Dienst verwenden, oder er kann in einem Konto ausgeführt werden, das zu einem Alias gehört, der vom ersten Dienst erkannt wird. Dienste, die auf verteilte Weise über das Netzwerk ausgeführt werden müssen, sollten in Domänen weiten Konten ausgeführt werden.

Sie können eines der folgenden speziellen Konten angeben, anstatt ein Benutzerkonto für den Dienst anzugeben:

-   [LocalService](localservice-account.md)
-   [NetworkService](networkservice-account.md)
-   [LocalSystem](localsystem-account.md)

 

 




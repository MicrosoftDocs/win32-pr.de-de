---
description: Jeder Dienst wird im Sicherheitskontext eines Benutzerkontos ausgeführt.
ms.assetid: a0e48918-6957-4288-a188-d65198b38c16
title: Dienstbenutzerkonten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6053a4f870b2a49923d802f7cb5f2a45b786d63314d1010773c3e8f58627bec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888547"
---
# <a name="service-user-accounts"></a>Dienstbenutzerkonten

Jeder Dienst wird im Sicherheitskontext eines Benutzerkontos ausgeführt. Der Benutzername und das Kennwort eines Kontos werden von der [**CreateService-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) zum Zeitpunkt der Dienstinstallation angegeben. Der Benutzername und das Kennwort können mithilfe der [**ChangeServiceConfig-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) geändert werden. Sie können die [**QueryServiceConfig-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) verwenden, um den Benutzernamen (aber nicht das Kennwort) abzurufen, der einem Dienstobjekt zugeordnet ist. Der Dienststeuerungs-Manager (Service Control Manager, SCM) lädt automatisch das Benutzerprofil.

Beim Starten eines Diensts meldet sich der SCM bei dem Konto an, das dem Dienst zugeordnet ist. Wenn die Anmeldung erfolgreich ist, erstellt das System ein Zugriffstoken und fügt es an den neuen Dienstprozess an. Dieses Token identifiziert den Dienstprozess in allen nachfolgenden Interaktionen mit sicherungsfähigen Objekten (Objekten, denen eine Sicherheitsbeschreibung zugeordnet ist). Wenn der Dienst beispielsweise versucht, ein Handle für eine Pipe zu öffnen, vergleicht das System das Zugriffstoken des Diensts mit der Sicherheitsbeschreibung der Pipe, bevor der Zugriff gewährt wird.

Der SCM verwaltet die Kennwörter von Dienstbenutzerkonten nicht. Wenn ein Kennwort abgelaufen ist, schlägt die Anmeldung fehl, und der Dienst kann nicht gestartet werden. Der Systemadministrator, der Den Diensten Konten zuweist, kann Konten mit Kennwörtern erstellen, die nie ablaufen. Der Administrator kann auch Konten mit Kennwörtern verwalten, die ablaufen, indem er ein [Dienstkonfigurationsprogramm](service-configuration-programs.md) verwendet, um die Kennwörter regelmäßig zu ändern.

Wenn ein Dienst einen anderen Dienst vor der Freigabe seiner Informationen erkennen muss, kann der zweite Dienst entweder dasselbe Konto wie der erste Dienst verwenden oder in einem Konto ausgeführt werden, das zu einem Alias gehört, der vom ersten Dienst erkannt wird. Dienste, die verteilt über das Netzwerk ausgeführt werden müssen, sollten in domänenweiten Konten ausgeführt werden.

Sie können eines der folgenden speziellen Konten angeben, anstatt ein Benutzerkonto für den Dienst anzugeben:

-   [LocalService](localservice-account.md)
-   [NetworkService](networkservice-account.md)
-   [LocalSystem](localsystem-account.md)

 

 




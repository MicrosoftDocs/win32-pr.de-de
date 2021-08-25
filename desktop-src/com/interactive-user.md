---
title: Interaktiver Benutzer
description: Der interaktive Benutzer ist der Benutzer, der derzeit auf dem Computer angemeldet ist, auf dem der COM-Server ausgeführt wird.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d842a468634da0eba31b04317b66185b298fc5a2e44d3567f796dac52dbdc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992730"
---
# <a name="interactive-user"></a>Interaktiver Benutzer

Der *interaktive Benutzer* ist der Benutzer, der derzeit auf dem Computer angemeldet ist, auf dem der COM-Server ausgeführt wird. Wenn die Identität als interaktiver Benutzer festgelegt ist, verwenden alle Clients dieselbe Instanz des Servers, wenn der Server seine Klassen factory als mehrfach verwendet registriert. Wenn kein Benutzer angemeldet ist, wird der Server nicht ausgeführt. Wenn der Server über eine grafische Benutzeroberfläche (GUI) verfügt, die der Client sehen muss, sollten Sie einen interaktiven Benutzer für die Identität des Servers verwenden. Die Auswahl dieser Identität birgt jedoch einige Sicherheitsrisiken, da der Server unter der Identität des angemeldeten Benutzers ohne Wissen oder Zustimmung des angemeldeten Benutzers ausgeführt wird. Darüber hinaus kann eine Dienstanwendung keine Benutzeroberfläche anzeigen. Weitere Informationen finden Sie unter [Interactive Services](/windows/desktop/Services/interactive-services).

Wenn ein COM-Server für die Ausführung als interaktiver Benutzer konfiguriert ist, wird der Server in einer Terminaldienstumgebung in der interaktiven Sitzung gestartet, die der Benutzeridentität des Clients entspricht. Die Clientanwendung kann jedoch den Sitzungsmoniker verwenden, um auf ein Objekt zu verweisen, das vom Server in einer Sitzung bereitgestellt wird, die nicht mit der Clientidentität übereinstimmen. Wenn dies verwendet wird, kann die Clientanwendung eine beliebige Sitzung angeben. In diesem Fall wird der Server als der Benutzer ausgeführt, der die Sitzung besitzt, und nicht als der startende Benutzer. Die Standardzugriffsberechtigungen in diesem Szenario lassen nicht zu, dass der startde Benutzer Methoden auf dem Server aufruft. Die folgenden Sicherheitsrisiken bleiben jedoch bestehen:

-   Wenn der COM-Server Schnittstellen verfügbar macht, die nicht von COM gesteuert werden, z. B. TCP-Ports, Named Pipes, LPC-Ports, Abschnitte für gemeinsam genutzten Arbeitsspeicher, können diese vom startden Benutzer verwendet werden, um den Server zu beeinflussen. COM-Objekte, die so konfiguriert sind, dass sie als interaktiver Benutzer ausgeführt werden, sollten diese Angriffsfläche so weit wie möglich reduzieren.
-   COM-Objekte können ihre eigenen Zugriffsberechtigungen festlegen. Wenn das -Objekt Zugriffsberechtigungen entweder in seiner AppID-Registrierung oder durch Aufrufen von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)zum Zulassen des Startbenutzerzugriffs legt, kann der Benutzer den Server starten, um als anderer Benutzer ausgeführt zu werden, und dann auf das Objekt zugreifen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsidentität](application-identity.md)
</dt> <dt>

[Starten des Benutzers](launching-user.md)
</dt> <dt>

[Dienstidentität](service-identity.md)
</dt> <dt>

[Angegebener Benutzer](specified-user.md)
</dt> </dl>

 

 
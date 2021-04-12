---
description: Da eine COM+-Bibliotheks Anwendung von einem anderen Prozess gehostet wird, der möglicherweise über eigene Sicherheitseinstellungen verfügt, müssen für die Sicherheit von Bibliotheksanwendungen besondere Aspekte berücksichtigt werden.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Sicherheit der Bibliothek Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523419"
---
# <a name="library-application-security"></a>Sicherheit der Bibliothek Anwendungen

Da eine COM+-Bibliotheks Anwendung von einem anderen Prozess gehostet wird, der möglicherweise über eigene Sicherheitseinstellungen verfügt, müssen für die Sicherheit von Bibliotheksanwendungen besondere Aspekte berücksichtigt werden.

Die folgenden Einschränkungen gelten für die Anwendungssicherheit von Bibliotheken:

-   Bibliotheksanwendungen werden unter dem Client Prozess-Sicherheits Token und nicht unter ihrer eigenen Benutzeridentität ausgeführt. Sie haben nur so viele Berechtigungen wie der Client.
-   Bibliotheksanwendungen Steuern keine Sicherheit auf Prozessebene. Der Sicherheits Beschreibung für den Prozess werden keine Benutzer in Rollen hinzugefügt. Die einzige Möglichkeit für eine Bibliotheks Anwendung, eigene Zugriffs Überprüfungen durchzuführen, ist die Verwendung der Sicherheit auf Komponentenebene. (Siehe [Sicherheitsgrenzen](security-boundaries.md).)
-   Bibliotheksanwendungen können so konfiguriert werden, dass Sie entweder teilnehmen oder nicht an der Host Prozess Authentifizierung teilnehmen, indem Sie die Authentifizierung aktivieren oder deaktivieren. (Informationen hierzu finden Sie unter [Aktivieren der Authentifizierung für eine Bibliotheks Anwendung](enabling-authentication-for-a-library-application.md).)
-   Bibliotheksanwendungen können keine Identitätswechsel Ebene festlegen. Diese verwenden den Host Prozess.

## <a name="using-library-applications-to-limit-application-privilege"></a>Verwenden von Bibliotheksanwendungen zum Einschränken von Anwendungs Berechtigungen

In einigen Fällen möchten Sie möglicherweise eine Anwendung speziell als Bibliotheks Anwendung konfigurieren, damit Sie unter der Identität des Host Prozesses ausgeführt wird. Dadurch wird die Anwendung grundsätzlich eingeschränkt, sodass nur auf die Ressourcen zugegriffen werden kann, auf die der Client, der Host Prozess, zugreifen kann. Die Threads, auf denen die Bibliotheks Anwendungskomponenten ausgeführt werden, verwenden standardmäßig das-Prozess Token. Wenn Sie also Aufrufe außerhalb der Anwendung ausführen oder auf Ressourcen zugreifen, z. b. Dateien, die mit einer Sicherheits Beschreibung geschützt sind, werden Sie als Client angezeigt. Bei Anwendungen, die sensible Aufgaben ausführen, kann dies eine einfache Möglichkeit sein, den Umfang ihrer Aktionen zu steuern.

## <a name="effectively-securing-library-applications"></a>Effektive Sicherung von Bibliotheksanwendungen

Bei der Konfiguration der rollenbasierten Sicherheit und Authentifizierung für Bibliotheksanwendungen sind besondere Aspekte zu beachten, damit Sie erwartungsgemäß ausgeführt werden. Weitere Informationen finden Sie unter [Konfigurieren der Sicherheit für Bibliotheksanwendungen](configuring-security-for-library-applications.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Multi-Tier-Anwendungssicherheit](multi-tier-application-security.md)
</dt> <dt>

[Sicherheit für programmgesteuerte Komponenten](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[Verwenden der Richtlinie für Software Einschränkung in com+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 




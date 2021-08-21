---
description: Da eine COM+-Bibliotheksanwendung von einem anderen Prozess gehostet wird, der möglicherweise über eigene Sicherheitseinstellungen verfügt, muss die Sicherheit für Bibliotheksanwendungen besonders berücksichtigt werden.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Bibliotheksanwendungssicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9fa2d03f21707af42fa108cb9c4ecbce6d2a352ea03714961a0eef4f028119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813519"
---
# <a name="library-application-security"></a>Bibliotheksanwendungssicherheit

Da eine COM+-Bibliotheksanwendung von einem anderen Prozess gehostet wird, der möglicherweise über eigene Sicherheitseinstellungen verfügt, muss die Sicherheit für Bibliotheksanwendungen besonders berücksichtigt werden.

Die folgenden Einschränkungen gelten für die Sicherheit von Bibliotheksanwendungen:

-   Bibliotheksanwendungen werden nicht unter ihrer eigenen Benutzeridentität, sondern unter dem Clientprozesssicherheitstoken ausgeführt. Sie haben nur so viele Berechtigungen wie der Client.
-   Bibliotheksanwendungen steuern die Sicherheit auf Prozessebene nicht. Der Sicherheitsbeschreibung für den Prozess werden keine Benutzer in Rollen hinzugefügt. Die einzige Möglichkeit für eine Bibliotheksanwendung, eigene Zugriffsüberprüfungen durchzuführen, ist die Verwendung der Sicherheit auf Komponentenebene. (Siehe [Sicherheitsgrenzen](security-boundaries.md).)
-   Bibliotheksanwendungen können so konfiguriert werden, dass sie entweder an der Hostprozessauthentifizierung teilnehmen oder nicht, indem sie die Authentifizierung aktivieren oder deaktivieren. (Siehe [Aktivieren der Authentifizierung für eine Bibliotheksanwendung.)](enabling-authentication-for-a-library-application.md)
-   Bibliotheksanwendungen können keine Identitätswechselebene festlegen. sie verwenden die des Hostprozesses.

## <a name="using-library-applications-to-limit-application-privilege"></a>Verwenden von Bibliotheksanwendungen zum Einschränken von Anwendungsberechtigungen

In einigen Fällen können Sie eine Anwendung speziell als Bibliotheksanwendung konfigurieren, sodass sie unter der Identität des Hostingprozesses ausgeführt wird. Dies schränkt die Anwendung grundlegend ein, sodass sie nur auf die Ressourcen zugreifen kann, auf die ihr Client, der Hostprozess, zugreifen kann. Die Threads, auf denen die Bibliotheksanwendungskomponenten ausgeführt werden, verwenden standardmäßig das Prozesstoken. Daher werden sie, wenn sie Aufrufe außerhalb der Anwendung ausführen oder auf Ressourcen zugreifen, z. B. Dateien, die mit einer Sicherheitsbeschreibung geschützt werden, als Client angezeigt. Für Anwendungen, die sensible Aufgaben ausführen, kann dies eine einfache Möglichkeit sein, den Umfang ihrer Aktionen zu steuern.

## <a name="effectively-securing-library-applications"></a>Effektives Sichern von Bibliotheksanwendungen

Es gibt besondere Überlegungen beim Konfigurieren der rollenbasierten Sicherheit und Authentifizierung für Bibliotheksanwendungen, damit sie erwartungsgemäß funktionieren. Weitere Informationen finden Sie unter [Konfigurieren der Sicherheit für Bibliotheksanwendungen.](configuring-security-for-library-applications.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Clientidentitätswechsel und -delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Anwendungssicherheit mit mehreren Ebenen](multi-tier-application-security.md)
</dt> <dt>

[Programmgesteuerte Komponentensicherheit](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[Verwenden der Softwareeinschränkungsrichtlinie in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 




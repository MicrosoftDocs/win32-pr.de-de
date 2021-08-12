---
description: Role-Based-Sicherheitsverwaltung
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Role-Based-Sicherheitsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c72ed2f1fdd5eb0b650b991b776364bf982c774b3ffcaff1358ea2c3ed1ee4d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547072"
---
# <a name="role-based-security-administration"></a>Role-Based-Sicherheitsverwaltung

Rollenbasierte Sicherheit ist ein von COM+ bereitgestellter automatischer Dienst, mit dem Sie eine Zugriffssteuerungsrichtlinie für Ihre COM+-Anwendung administrativ erstellen und erzwingen können. Mit einem flexiblen und erweiterbaren Sicherheitskonfigurationsmodell bietet die rollenbasierte Sicherheit einen erheblichen Vorteil gegenüber der Erzwingung der gesamten Sicherheit innerhalb Ihrer Komponenten und bietet die folgenden Vorteile:

-   Sie können die Sicherheit mithilfe des Verwaltungstools Komponentendienste oder mithilfe der Verwaltungsfunktionen administrativer Art konfigurieren.
-   Sie müssen keine sicherheitsbezogene Logik in Ihre Komponenten schreiben, wenn der Rollenschutz auf Methodenebene ausreichend Zugriffssteuerung bietet.
-   Sie müssen die Sicherheit nicht in den Schnittstellen- oder Komponentenentwurf integrieren. Stattdessen können Sie die Sicherheit methodenweise festlegen.
-   Sie können sich auf die Struktur der Zu erzwingenden Sicherheitsrichtlinie konzentrieren, und über Rollen kann diese Richtlinie den Administratoren klar ausgedrückt werden, die Ihre Anwendung bereitstellen.
-   Sie können eine Sicherheitsrichtlinie problemlos ändern, um sie an sich ändernde Sicherheitsanforderungen für eine Anwendung anzupassen.
-   Sie können bei Bedarf präzisere Sicherheitsrichtlinien programmgesteuert erstellen, indem Sie die rollenbasierte Sicherheit als unterstützende Plattform verwenden.
-   Sie können die rollenbasierte Sicherheit nutzen, um eine detaillierte Überwachung zu durchführen, da Sie Sicherheitsinformationen des Aufrufers für eine gesamte Kette von Upstreamaufrufen abrufen können.

> [!Note]  
> Benutzer mit der Administratorrolle für die Systemanwendung müssen Mitglieder der lokalen Administratorgruppe sein. Ab Windows Server 2003 enthält die Authentifizierungsfunktion für die COM+-Systemanwendung außerdem den Wert EOAC \_ DISABLE \_ AAA. Dieser Wert, der AKTIVIERUNGSAKTIVATOR-Aktivierungen (AAA) deaktiviert, wird beim Starten der Systemanwendung im [**CoInitializeSecurity-Aufruf**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) verwendet. Wenn Sie die Authentifizierungsfunktion auf EOAC \_ DISABLE \_ AAA festlegen, kann eine Anwendung, die unter einem privilegierten Konto (z. B. LocalSystem) ausgeführt wird, verhindern, dass ihre Identität zum Starten nicht vertrauenswürdiger Komponenten verwendet wird.

 

In den folgenden Themen dieses Abschnitts finden Sie Informationen zur Funktionsweise der rollenbasierten Sicherheit und zu berücksichtigende Probleme beim Erstellen einer Sicherheitsrichtlinie für eine Anwendung:

-   [Verwenden von Rollen für die Clientautorisierung](using-roles-for-client-authorization.md)
-   [Effektives Entwerfen von Rollen](designing-roles-effectively.md)
-   [Sicherheitsgrenzen](security-boundaries.md)
-   [Kontextinformationen für Sicherheitsaufrufe](security-call-context-information.md)
-   [Sicherheitskontexteigenschaft](security-context-property.md)

Ausführliche Anleitungen zu den Schritten zum Konfigurieren der rollenbasierten Sicherheit für eine Anwendung finden Sie unter [Konfigurieren von Role-Based Security](configuring-role-based-security.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Clientidentitätswechsel und -delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Bibliotheksanwendungssicherheit](library-application-security.md)
</dt> <dt>

[Anwendungssicherheit mit mehreren Ebenen](multi-tier-application-security.md)
</dt> <dt>

[Programmgesteuerte Komponentensicherheit](programmatic-component-security.md)
</dt> <dt>

[Verwenden der Softwareeinschränkungsrichtlinie in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 

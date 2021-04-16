---
description: Role-Based Sicherheitsverwaltung
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Role-Based Sicherheitsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524040"
---
# <a name="role-based-security-administration"></a>Role-Based Sicherheitsverwaltung

Die rollenbasierte Sicherheit ist ein von com+ bereitgestellter automatischer Dienst, mit dem Sie eine Zugriffs Steuerungs Richtlinie für Ihre COM+-Anwendung administrativ erstellen und erzwingen können. Mit einem flexiblen und erweiterbaren Sicherheits Konfigurations Modell bietet die rollenbasierte Sicherheit einen erheblichen Vorteil gegenüber der Durchsetzung der gesamten Sicherheit in ihren Komponenten und bietet die folgenden Vorteile:

-   Sie können die Sicherheit administrativ konfigurieren, indem Sie entweder das Verwaltungs Programmkomponenten Dienste oder die Verwaltungsfunktionen verwenden.
-   Sie müssen keine sicherheitsbezogene Logik in Ihre Komponenten schreiben, wenn der Rollen Schutz auf Methoden Ebene Ihnen ausreichend Zugriffs Steuerung bereitstellt.
-   Sie müssen die Sicherheit nicht in eine Schnittstelle oder einen Komponenten Entwurf einbeziehen. Stattdessen können Sie die Sicherheit auf Methoden Basis festlegen.
-   Sie können sich auf die Struktur der Sicherheitsrichtlinie konzentrieren, die Sie erzwingen möchten, und überrollen kann diese Richtlinie den Administratoren, die Ihre Anwendung bereitstellen, eindeutig ausgedrückt werden.
-   Sie können eine Sicherheitsrichtlinie auf einfache Weise ändern, um sich an sich entwickelnde Sicherheitsanforderungen für eine Anwendung anzupassen.
-   Sie können bei Bedarf differenziertere Sicherheitsrichtlinien erstellen, wenn Sie die rollenbasierte Sicherheit als unterstützende Plattform verwenden möchten.
-   Sie können die rollenbasierte Sicherheit für eine ausführliche Überwachung nutzen, da Sie Aufrufer-Sicherheitsinformationen für eine ganze Kette von upstreamaufrufen abrufen können.

> [!Note]  
> Benutzer in der Administrator Rolle für die System Anwendung müssen Mitglieder der lokalen Administratoren Gruppe sein. Ab Windows Server 2003 enthält die Authentifizierungsfunktion für die com+-System Anwendung auch den Wert eoac- \_ deaktivierte \_ AAA. Dieser Wert, der Aktivierungen von Aktivierungen durch aktivierte Aktivierungen deaktiviert, wird beim Starten der System Anwendung im [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Befehl verwendet. Wenn Sie die Authentifizierungsfunktion auf eoac \_ deaktivieren, \_ kann eine Anwendung, die unter einem privilegierten Konto (z. b. LocalSystem) ausgeführt wird, verhindern, dass Ihre Identität verwendet wird, um nicht vertrauenswürdige Komponenten zu starten.

 

In den folgenden Themen dieses Abschnitts finden Sie Informationen zur Funktionsweise der rollenbasierten Sicherheit und zu berücksichtigende Aspekte bei der Verwendung, um eine Sicherheitsrichtlinie für eine Anwendung zu erstellen:

-   [Verwenden von Rollen für die Client Autorisierung](using-roles-for-client-authorization.md)
-   [Effektives Entwerfen von Rollen](designing-roles-effectively.md)
-   [Sicherheitsgrenzen](security-boundaries.md)
-   [Informationen zum Sicherheits Aufrufkontext](security-call-context-information.md)
-   [Sicherheitskontext Eigenschaft](security-context-property.md)

Ausführliche Beschreibungen der Schritte, die zum Konfigurieren der rollenbasierten Sicherheit für eine Anwendung erforderlich sind, finden Sie unter [Konfigurieren von Role-Based Sicherheit](configuring-role-based-security.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicherheit der Bibliothek Anwendungen](library-application-security.md)
</dt> <dt>

[Multi-Tier-Anwendungssicherheit](multi-tier-application-security.md)
</dt> <dt>

[Sicherheit für programmgesteuerte Komponenten](programmatic-component-security.md)
</dt> <dt>

[Verwenden der Richtlinie für Software Einschränkung in com+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 

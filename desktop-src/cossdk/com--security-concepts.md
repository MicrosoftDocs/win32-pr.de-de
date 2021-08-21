---
description: COM+ bietet mehrere Sicherheitsfeatures, mit denen Sie Ihre COM+-Anwendungen schützen können, von Diensten, die Sie administratorisch konfigurieren, bis hin zu APIs, die Sie im Code aufrufen können.
ms.assetid: 686fb391-d337-41b4-bb51-b70f27a0c300
title: COM+-Sicherheitskonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b93ac113cf4ff2b1c679936fd610c2d44f29689ff175930c6a67274002457d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047528"
---
# <a name="com-security-concepts"></a>COM+-Sicherheitskonzepte

COM+ bietet mehrere Sicherheitsfeatures, mit denen Sie Ihre COM+-Anwendungen schützen können, von Diensten, die Sie administratorisch konfigurieren, bis hin zu APIs, die Sie im Code aufrufen können.

Wenn möglich, ist es für COM+-Anwendungen besser, automatische Sicherheit zu verwenden, z. B. deklarative rollenbasierte Sicherheit und Authentifizierung, anstatt die Sicherheit innerhalb von Komponenten zu konfigurieren. Die Verwendung der automatischen Sicherheit erleichtert das Schreiben und Verwalten von Komponenten, vereinfacht das Entwerfen der Sicherheit für eine gesamte Anwendung und erleichtert, da sie verwaltungseist, die Sicherheitsrichtlinie einer Anwendung zu ändern. Diese automatischen Sicherheitsdienste ermöglichen es Ihnen, alle sicherheitsbezogenen Funktionen aus Ihren Komponenten heraus zu lassen. Wenn Sie die Dienste aktivieren und entsprechend konfigurieren können, verarbeitet COM+ die Details zum Erzwingen der von Ihnen angegebenen Sicherheitsrichtlinie.

Wenn die automatischen Sicherheitsdienste in COM+ jedoch nicht genau das tun, was Sie benötigen, können Sie sie erweitern, indem Sie auf der von COM+ bereitgestellten automatischen Sicherheitsplattform aufbaut. In Fällen, in denen Sie sich dafür entscheiden, die automatische Sicherheit nicht zu verwenden oder wenn Sie sie verwenden möchten, aber entsprechend den Sicherheitsanforderungen Ihrer Anwendung darauf aufbauen müssen, haben Sie die folgenden Optionen zum programmgesteuerten Konfigurieren der Sicherheit:

-   Programmgesteuerte rollenbasierte Sicherheit, z. B. Rollenüberprüfung, die verfügbar ist, wenn die rollenbasierte Sicherheit für Ihre Anwendung aktiviert ist.
-   Identitätswechsel: Wenn Sie die Identität eines Clients für den Zugriff auf eine geschützte Ressource verwenden möchten.
-   Überwachungsfeatures, die auf Kontextinformationen für Sicherheitsaufrufe basieren – auch verfügbar, wenn die rollenbasierte Sicherheit aktiviert ist.

Welche Mechanismen Sie verwenden, um eine bestimmte Anwendung zu schützen, hängt von den speziellen Anforderungen dieser Anwendung ab. Einige Sicherheitsoptionen können sich darauf auswirken, wie Sie Komponenten schreiben, und einige können sich erheblich auf den Entwurf der Anwendung auswirken. Bevor Sie Entscheidungen zur Implementierung einer Sicherheitsstrategie für eine Anwendung treffen, sollten Sie deren Sicherheitsanforderungen im Kontext des Gesamtentwurfs berücksichtigen – Leistungsanforderungen, Datenzugriff, physisches Design – und die am besten geeignete Kombination von Sicherheitsfeatures auswählen. Weitere Informationen zum Implementieren der programmgesteuerten Sicherheit finden Sie unter [Programmgesteuerte Komponentensicherheit.](programmatic-component-security.md)

Hier finden Sie kurze Beschreibungen von COM+-Sicherheitskategorien, -Features und -Problemen sowie Links zu Themen in diesem Abschnitt, die eine ausführliche Erläuterung der einzelnen wichtigen Bereiche bieten.

> [!Note]  
> Obwohl in diesem Abschnitt nicht erläutert, haben Komponenten in der Warteschlange auch bestimmte Probleme in Bezug darauf, welche Sicherheitsfeatures ihnen zur Verfügung stehen. Weitere Informationen finden Sie unter [Queued Components Security](queued-components-security.md) and Developing Queued Components (Sicherheit in Warteschlangenkomponenten und Entwickeln von Komponenten [in Warteschlangen).](developing-queued-components.md)

 

## <a name="role-based-security"></a>Rollenbasierte Sicherheit

Die rollenbasierte Sicherheit ist das zentrale Feature der COM+-Anwendungssicherheit. Mithilfe von Rollen können Sie eine Autorisierungsrichtlinie für eine Anwendung auf administrativer Ebene erstellen und (bei Bedarf bis zur Methodenebene) auswählen, welche Benutzer auf welche Ressourcen zugreifen können. Darüber hinaus stellen Rollen ein Framework zum Erzwingen der Sicherheitsüberprüfung im Code zur Verfügung, wenn Ihre Anwendung eine feiner abgrenzende Zugriffssteuerung erfordert.

Die rollenbasierte Sicherheit basiert auf einem allgemeinen Mechanismus, mit dem Sie Sicherheitsinformationen zu allen Upstreamaufrufern in der Kette der Aufrufe an Ihre Komponente abrufen können. Diese Einrichtung ist besonders nützlich, wenn Sie eine detaillierte Überwachung und Protokollierung wünschen. Eine Beschreibung der von COM+ bereitgestellten Überwachungsfunktionen finden Sie unter [Zugreifen auf Kontextinformationen für Sicherheitsaufrufe.](accessing-security-call-context-information.md)

Eine Beschreibung der probleme bei der rollenbasierten Sicherheit und Verwaltung, die Sie bei der Verwendung berücksichtigen sollten, finden Sie unter [Rollenbasierte Sicherheitsverwaltung.](role-based-security-administration.md)

## <a name="client-authentication"></a>Clientauthentifizierung

Bevor Sie Clients autorisieren können, um auf Ressourcen zugreifen zu können, müssen Sie sicher sein, dass sie die Person sind, die sie sind. Um diese Identitätsüberprüfung zu aktivieren, stellt COM+ Authentifizierungsdienste zur Verfügung. Obwohl diese Dienste tatsächlich auf einer grundlegenderen Ebene von COM und Microsoft Windows bereitgestellt werden, können Sie mit einer COM+-Anwendung den Authentifizierungsdienst einfach administrativer weise aktivieren, sodass er im Rahmen der Anwendung transparent funktioniert. Eine Beschreibung der Authentifizierungsdienste finden Sie unter [Clientauthentifizierung.](client-authentication.md)

## <a name="client-impersonation-and-delegation"></a>Client-Identitätswechsel und -delegierung

In einigen Fällen muss Ihre Anwendung die Arbeit im Auftrag eines Clients mithilfe der Identität des Clients durchführen, z. B. beim Zugriff auf eine Datenbank, die den ursprünglichen Client authentifiziert. Dies erfordert, dass Ihre Anwendung die Identität des Clients anfordert. COM+ bietet Funktionen zum Aktivieren verschiedener Ebenen des Identitätswechsels. Der Identitätswechsel wird administrativer Art konfiguriert, aber Sie müssen auch Unterstützung für den Identitätswechsel mit dem Code der Anwendungskomponenten bereitstellen. Eine Beschreibung des Identitätswechsels und probleme in Bezug auf die Verwendung finden Sie unter [Clientpersonation und Delegierung](client-impersonation-and-delegation.md).

## <a name="using-the-software-restriction-policy-in-com"></a>Verwenden der Softwareeinschränkungsrichtlinie in COM+

Eine Softwareeinschränkungsrichtlinie bietet eine Möglichkeit zum Ausführen von nicht vertrauenswürdigem und daher potenziell schädlichem Code in einer eingeschränkten Umgebung, damit die Berechtigungen des Benutzers nicht missbraucht werden können. Hierzu werden Dateien, die der Benutzer ausführen kann, Vertrauensebenen zugewiesen. Beispielsweise können bestimmte Systemdateien vollständig vertrauenswürdig sein und uneingeschränkten Zugriff auf die Berechtigungen des Benutzers erhalten, während eine Datei, die aus dem Internet heruntergeladen wurde, möglicherweise vollständig vertrauenswürdig ist und daher nur in einer eingeschränkten Umgebung ausgeführt werden darf, in der die Verwendung sicherheitssensibler Benutzerberechtigungen nicht zulässig ist.

Die systemweite Softwareeinschränkungsrichtlinie wird über das Lokale Sicherheitsrichtlinien-Verwaltungstool gesteuert, mit dem Administratoren Vertrauensebenen für einzelne Dateien konfigurieren können. Alle COM+-Serveranwendungen werden jedoch in der dllhost.exe ausgeführt. Daher bietet COM+ eine Möglichkeit, die Softwareeinschränkungsrichtlinie für jede Serveranwendung anzugeben, damit sie nicht von der Einschränkungsrichtlinie der dllhost.exe müssen. Eine Diskussion zur Verwendung der Softwareeinschränkungsrichtlinie in COM+ finden Sie unter [Verwenden der Softwareeinschränkungsrichtlinie in COM+.](using-the-software-restriction-policy-in-com-.md)

## <a name="library-application-security"></a>Sicherheit von Bibliotheksanwendung

Für Bibliotheksanwendungen gibt es besondere Sicherheitsüberlegungen. Da diese Anwendungen im Prozess des Clients ausgeführt werden, sind sie von der Sicherheit betroffen, die vom Hostingprozess erzwungen wird, während die Sicherheit auf Prozessebene nicht kontrolliert werden kann. Eine Beschreibung der Faktoren, die für Bibliotheksanwendungen zu berücksichtigen sind, finden Sie unter [Sicherheit von Bibliotheksanwendungen.](library-application-security.md)

## <a name="multi-tier-application-security"></a>Anwendungssicherheit mit mehreren Ebenen

COM+-Anwendungen sind in der Regel Anwendungen der mittleren Ebene. Das heißt, sie verschieben Informationen zwischen Clients und Back-End-Ressourcen wie Datenbanken. Es kann schwierig sein, zu bestimmen, wo und in welchem Grad Sicherheit erzwungen werden soll. Sicherheit umfasst grundsätzlich Leistungsrisiken. Einige der schwerwiegendsten davon treten auf, wenn Sie die Sicherheitsüberprüfung sowohl auf der Datenebene als auch auf der mittleren Ebene erzwingen müssen. Eine Erörterung der zu berücksichtigenden Probleme finden Sie unter [Anwendungssicherheit mit mehreren Ebenen.](multi-tier-application-security.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Client-Identitätswechsel und -delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[COM+-Sicherheitsaufgaben](com--security-tasks.md)
</dt> <dt>

[Sicherheit von Bibliotheksanwendung](library-application-security.md)
</dt> <dt>

[Anwendungssicherheit mit mehreren Ebenen](multi-tier-application-security.md)
</dt> <dt>

[Programmgesteuerte Komponentensicherheit](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[Verwenden der Softwareeinschränkungsrichtlinie in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 




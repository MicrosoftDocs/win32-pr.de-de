---
description: Com+ bietet verschiedene Sicherheitsfunktionen, die Sie zum Schutz Ihrer com+-Anwendungen verwenden können. Sie reichen von Diensten, die Sie administrativ für APIs konfigurieren, die Sie im Code aufrufen können.
ms.assetid: 686fb391-d337-41b4-bb51-b70f27a0c300
title: Com+-Sicherheitskonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca5126f4b715f84c2b8801c8ec1adc29b3cbb83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041508"
---
# <a name="com-security-concepts"></a>Com+-Sicherheitskonzepte

Com+ bietet verschiedene Sicherheitsfunktionen, die Sie zum Schutz Ihrer com+-Anwendungen verwenden können. Sie reichen von Diensten, die Sie administrativ für APIs konfigurieren, die Sie im Code aufrufen können.

Wenn möglich, ist es für COM+-Anwendungen besser, die automatische Sicherheit zu verwenden, wie z. b. deklarative rollenbasierte Sicherheit und Authentifizierung, anstatt die Sicherheit innerhalb von Komponenten zu konfigurieren. Die Verwendung der automatischen Sicherheit vereinfacht das Schreiben und Verwalten von Komponenten, das einfachere Entwerfen der Sicherheit für eine gesamte Anwendung, und da sie administrativ konfiguriert ist, ist es einfacher, die Sicherheitsrichtlinie einer Anwendung zu ändern. Diese automatischen Sicherheitsdienste ermöglichen es Ihnen, alle sicherheitsbezogenen Funktionen aus ihren Komponenten zu lassen. Wenn Sie die Dienste aktivieren und entsprechend konfigurieren können, behandelt com+ die Details der Durchsetzung der von Ihnen angegebenen Sicherheitsrichtlinie.

Wenn die automatischen Sicherheitsdienste in com+ jedoch nicht genau das tun, was Sie tun müssen, können Sie Sie erweitern und auf der von com+ bereitgestellten automatischen Sicherheitsplattform aufbauen. Wenn Sie sich dafür entscheiden, die automatische Sicherheit nicht zu verwenden, oder wenn Sie Sie verwenden möchten, aber entsprechend den Sicherheitsanforderungen Ihrer Anwendung aufbauen müssen, stehen Ihnen die folgenden Optionen zum programmgesteuerten Konfigurieren der Sicherheit zur Verfügung:

-   Programmgesteuerte rollenbasierte Sicherheit – beispielsweise die Rollen Überprüfung, die verfügbar ist, wenn rollenbasierte Sicherheit für Ihre Anwendung aktiviert ist.
-   Identitätswechsel – für den Fall, dass Sie die Identität eines Clients für den Zugriff auf eine geschützte Ressource verwenden möchten.
-   Überwachungsfunktionen auf der Grundlage von Kontextinformationen für den Sicherheitskontext – auch verfügbar, wenn rollenbasierte Sicherheit aktiviert ist.

Welche Mechanismen verwendet werden, um eine bestimmte Anwendung zu schützen, hängt von den speziellen Anforderungen dieser Anwendung ab. Einige Sicherheitsoptionen können sich auf die Art und Weise auswirken, wie Sie Komponenten schreiben, und einige können den Entwurf der Anwendung erheblich beeinflussen. Bevor Sie Entscheidungen darüber treffen, wie eine Sicherheitsstrategie für eine Anwendung implementiert werden kann, sollten Sie die Sicherheitsanforderungen im Zusammenhang mit dem allgemeinen Entwurf – Leistungsanforderungen, Datenzugriff, physikalischer Entwurf – berücksichtigen und die am besten geeignete Kombination aus Sicherheitsfunktionen auswählen. Weitere Informationen zum Implementieren der programmgesteuerten Sicherheit finden Sie Unterprogramm gesteuerte [Komponentensicherheit](programmatic-component-security.md).

Hier finden Sie eine kurze Beschreibung der com+-Sicherheitskategorien, Features und Probleme, die Links zu Themen in diesem Abschnitt enthalten, die eine ausführliche Erörterung der einzelnen wichtigen Bereiche bieten.

> [!Note]  
> Obwohl es in diesem Abschnitt nicht erläutert wird, haben Komponenten in der Warteschlange auch bestimmte Probleme im Zusammenhang mit den verfügbaren Sicherheitsfeatures. Weitere Informationen finden Sie unter Sicherheit in der [Warteschlange für Komponenten](queued-components-security.md) und entwickeln in der [Warteschlange befindliche Komponenten](developing-queued-components.md)

 

## <a name="role-based-security"></a>Rollenbasierte Sicherheit

Die rollenbasierte Sicherheit ist das zentrale Feature der com+-Anwendungssicherheit. Mithilfe von Rollen können Sie administrativ eine Autorisierungs Richtlinie für eine Anwendung erstellen, indem Sie (falls erforderlich) auswählen, welche Benutzer auf welche Ressourcen zugreifen können. Außerdem bieten Rollen ein Framework zum Erzwingen der Sicherheitsüberprüfung innerhalb von Code, wenn Ihre Anwendung eine präzisere Zugriffs Steuerung erfordert.

Die rollenbasierte Sicherheit basiert auf einem allgemeinen Mechanismus, mit dem Sie Sicherheitsinformationen zu allen upstreamaufrufern in der Kette von Aufrufen Ihrer Komponente abrufen können. Diese Funktion ist besonders nützlich, wenn Sie eine ausführliche Überwachung und Protokollierung durchführen möchten. Eine Beschreibung der von com+ bereitgestellten Überwachungsfunktionen finden Sie unter [zugreifen auf Kontextinformationen des Sicherheits Aufrufes](accessing-security-call-context-information.md).

Eine Beschreibung der rollenbasierten Sicherheits-und Verwaltungsprobleme, die Sie bei der Verwendung berücksichtigen sollten, finden Sie unter [rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md).

## <a name="client-authentication"></a>Clientauthentifizierung

Bevor Sie Clients autorisieren können, auf Ressourcen zuzugreifen, müssen Sie sicher sein, dass Sie die Benutzer sind, die Sie sagen. Um diese Identitätsüberprüfung zu aktivieren, stellt com+ Authentifizierungsdienste bereit. Wenngleich diese Dienste von com und Microsoft Windows auf einer grundlegendsten Ebene bereitgestellt werden, können Sie mit einer COM+-Anwendung einfach den Authentifizierungsdienst administrativ aktivieren, damit er im Hintergrund funktioniert, der für die Anwendung transparent ist. Eine Beschreibung der Authentifizierungsdienste finden Sie unter [Client Authentifizierung](client-authentication.md).

## <a name="client-impersonation-and-delegation"></a>Client Identitätswechsel und Delegierung

In einigen Fällen muss Ihre Anwendung im Auftrag eines Clients mit der Identität des Clients arbeiten – beispielsweise beim Zugriff auf eine Datenbank, in der der ursprüngliche Client authentifiziert wird. Dies erfordert, dass Ihre Anwendung die Identität des Clients annimmt. Com+ bietet Funktionen zum Aktivieren verschiedener Identitätswechsel Ebenen. Der Identitätswechsel wird administrativ konfiguriert, aber Sie müssen auch Unterstützung für den Identitätswechsel mit dem Code der Komponenten Ihrer Anwendung bereitstellen. Eine Beschreibung des Identitäts Wechsels und der zugehörigen Probleme finden Sie unter Client Identitätswechsel [und Delegierung](client-impersonation-and-delegation.md).

## <a name="using-the-software-restriction-policy-in-com"></a>Verwenden der Richtlinie für Software Einschränkung in com+

Eine Richtlinie für Software Einschränkung bietet eine Möglichkeit zum Ausführen von nicht vertrauenswürdigem und potenziell schädlichem Code in einer eingeschränkten Umgebung, damit die Benutzerberechtigungen nicht missbraucht werden können. Dies geschieht durch Zuweisen von Vertrauens Ebenen zu Dateien, die der Benutzer ausführen kann. Beispielsweise können bestimmte Systemdateien vollständig vertrauenswürdig sein und uneingeschränkten Zugriff auf die Berechtigungen des Benutzers erhalten, während eine Datei, die aus dem Internet heruntergeladen wurde, möglicherweise vollständig nicht vertrauenswürdig ist und daher nur in einer eingeschränkten Umgebung ausgeführt werden darf, in der es nicht zulässig ist, sicherheitsrelevante Benutzerberechtigungen zu verwenden.

Die systemweite Software Einschränkungs Richtlinie wird über das Verwaltungs Tool "lokale Sicherheitsrichtlinie" gesteuert, mit dem Administratoren Vertrauens Ebenen für einzelne Dateien konfigurieren können. Allerdings werden alle com+-Server Anwendungen in der dllhost.exe-Datei ausgeführt. Daher bietet com+ eine Möglichkeit, die Software Einschränkungs Richtlinie für jede Serveranwendung anzugeben, damit Sie nicht von der Einschränkungs Richtlinie der dllhost.exe Datei abhängen müssen. Eine Erläuterung zur Verwendung der Software Einschränkungs Richtlinie in com+ finden [Sie unter Verwenden der Software Einschränkungs Richtlinie in com+](using-the-software-restriction-policy-in-com-.md).

## <a name="library-application-security"></a>Sicherheit der Bibliothek Anwendungen

Bibliotheksanwendungen haben besondere Sicherheitsüberlegungen. Da diese Anwendungen im Client Prozess ausgeführt werden, sind Sie von der vom Hostingprozess erzwungenen Sicherheit betroffen, während die Sicherheit auf Prozessebene nicht gesteuert werden kann. Eine Beschreibung der Faktoren, die für Bibliotheksanwendungen zu berücksichtigen sind, finden Sie unter [Bibliothek Anwendungssicherheit](library-application-security.md).

## <a name="multi-tier-application-security"></a>Multi-Tier-Anwendungssicherheit

Com+-Anwendungen sind in der Regel Anwendungen der mittleren Ebene. Das heißt, dass Sie Informationen zwischen Clients und Back-End-Ressourcen, z. b. Datenbanken, verschieben. Schwierige Optionen können daran beteiligt sein, zu bestimmen, wo die Sicherheit erzwungen werden soll, und zu welchem Grad. Die Sicherheit ist von Natur aus mit Leistungseinbußen verbunden. Einige der schwerwiegendsten Komponenten treten auf, wenn Sie die Sicherheitsüberprüfung sowohl auf der Datenebene als auch auf der mittleren Ebene erzwingen müssen. Eine Erörterung der zu berücksichtigenden Probleme finden Sie unter [Multi-Tier Application Security](multi-tier-application-security.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Com+-Sicherheitsaufgaben](com--security-tasks.md)
</dt> <dt>

[Sicherheit der Bibliothek Anwendungen](library-application-security.md)
</dt> <dt>

[Multi-Tier-Anwendungssicherheit](multi-tier-application-security.md)
</dt> <dt>

[Sicherheit für programmgesteuerte Komponenten](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[Verwenden der Richtlinie für Software Einschränkung in com+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 




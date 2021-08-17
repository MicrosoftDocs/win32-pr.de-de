---
description: Unter bestimmten Umständen muss eine Serveranwendung eine Clientidentität für Ressourcen präsentieren, auf die sie im Auftrag des Clients zutritt. In der Regel wird dies dazu führen, dass Zugriffsüberprüfungen oder Authentifizierungen für die Clientidentität durchgeführt werden.
ms.assetid: fd75eb54-eefe-411f-a7aa-0bc8628f8778
title: Client-Identitätswechsel und -delegierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b0262f3d8dd6736d183fa76eb5d3f0946d50b2724e76bcea73843644aaefb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129372"
---
# <a name="client-impersonation-and-delegation"></a>Client-Identitätswechsel und -delegierung

Unter bestimmten Umständen muss eine Serveranwendung die Identität eines Clients für Ressourcen präsentieren, auf die er im Auftrag des Clients zutritt, um in der Regel Zugriffsüberprüfungen oder Authentifizierungen für die Identität des Clients durchzuführen. Bis zu einem gewissen Grad kann der Server unter der Identität des Clients agieren– eine Aktion, die als Identitätswechsel des Clients bezeichnet wird.

*Identitätswechsel ist* die Fähigkeit eines Threads, in einem anderen Sicherheitskontext als dem prozess, der den Thread besitzt, auszuführen. Der Serverthread verwendet ein Zugriffstoken, das die Anmeldeinformationen des Clients darstellt. Damit kann er auf Ressourcen zugreifen, auf die der Client zugreifen kann.

Durch die Verwendung des Identitätswechsels wird sichergestellt, dass der Server genau die Vom Client ausgeführten Daten ausführen kann. Der Zugriff auf Ressourcen kann entweder eingeschränkt oder erweitert werden, je nachdem, welche Berechtigungen der Client hat.

Sie können festlegen, dass ein Server beim Herstellen einer Verbindung mit einer Datenbank die Identität eines Clients an den Computer überträgt, damit die Datenbank den Client für sich selbst authentifizieren und autorisieren kann. Wenn Ihre Anwendung auf Dateien zutritt, die mit einem Sicherheitsdeskriptor geschützt sind, und um es dem Client zu ermöglichen, autorisierten Zugriff auf Informationen in diesen Dateien zu erhalten, kann die Anwendung die Identität des Clients vor dem Zugriff auf die Dateien imitieren.

## <a name="how-to-implement-impersonation"></a>Implementieren des Identitätswechsels

Der Identitätswechsel erfordert die Teilnahme von Client und Server (und in einigen Fällen von Systemadministratoren). Der Client muss seine Bereitschaft angeben, dem Server die Verwendung seiner Identität zu gestatten, und der Server muss die Identität des Clients programmgesteuert explizit annehmen. Weitere Informationen finden Sie in den Themen [Clientseitige Anforderungen](client-side-requirements-for-impersonation.md) für Identitätswechsel und Serverseitige Anforderungen [für Identitätswechsel.](server-side-requirements-for-impersonation.md)

## <a name="administrative-requirements-for-delegate-level-impersonation"></a>Administrative Anforderungen für Delegate-Level Identitätswechsel

Zur effektiven Verwendung der leistungsstärksten Form des Identitätswechsels, der Delegierung, bei der es sich um den Identitätswechsel von Clients über das Netzwerk handelt, müssen die Client- und Serverbenutzerkonten im Active Directory-Dienst ordnungsgemäß konfiguriert werden, um sie zu unterstützen (zusätzlich zur Clientgewährungs-Autorität zum Ausführen eines Identitätswechsels auf Delegatebene):

-   Die Serveridentität muss im Active Directory-Dienst als "Vertrauenswürdig für Delegierung" gekennzeichnet sein.
-   Die Clientidentität darf im Active Directory-Dienst nicht als "Konto ist vertraulich und kann nicht delegiert werden" gekennzeichnet werden.

Diese Konfigurationsfunktionen bieten dem Domänenadministrator ein hohes Maß an Kontrolle über die Delegierung, was angesichts des hohen Vertrauens (und damit des Sicherheitsrisikos) wünschenswert ist. Weitere Informationen zur Delegierung finden Sie unter [Delegierung und Identitätswechsel.](/windows/desktop/com/delegation-and-impersonation)

## <a name="cloaking"></a>Cloaking

Zusammen mit der Autorität, die ein Client einem Server über die Identitätswechselebene gewährt, bestimmt die Versenkungsfunktion des Servers größtenteils das Verhalten des Identitätswechsels. Das Verkleinern wirkt sich darauf aus, welche Identität tatsächlich vom Server präsentiert wird, wenn er Aufrufe im Namen des Clients sendet – seine eigene identität oder die des Clients. Weitere Informationen finden Sie unter [Cloaking](cloaking.md).

## <a name="performance-implications"></a>Folgen für die Leistung

Identitätswechsel können die Leistung und Skalierung erheblich beeinträchtigen. Im Allgemeinen ist es teurer, bei einem Aufruf die Identität eines Clients zu imitieren, als den Aufruf direkt zu machen. Im Folgenden finden Sie einige der zu berücksichtigenden Probleme:

-   Der Rechenaufwand für die Übergabe von Identitäten in komplizierten Mustern, insbesondere, wenn dynamische Verkleinerung aktiviert ist.
-   Die allgemeine Komplexität des Erzwingens redundanter Sicherheitsüberprüfungen an zahlreichen Stellen, nicht nur zentral auf der mittleren Ebene.
-   Ressourcen wie Datenbankverbindungen können beim Öffnen der Identität eines Clients nicht über mehrere Clients hinweg wiederverwendet werden– eine sehr große Sperre für die Skalierung.

Manchmal ist die einzige effektive Lösung für ein Problem die Verwendung des Identitätswechsels, aber diese Entscheidung sollte sorgfältig abgewogen werden. Eine weitere Erörterung dieser Probleme finden Sie unter [Anwendungssicherheit mit mehreren Ebenen.](multi-tier-application-security.md)

## <a name="queued-components"></a>Komponenten in der Warteschlange

[Komponenten in der Warteschlange](com--queued-components.md) unterstützen keinen Identitätswechsel. Wenn ein Client ein Objekt in der Warteschlange aufruft, erfolgt der Aufruf tatsächlich an die Aufzeichnung, die sie als Teil einer Nachricht an den Server verpackt. Der Listener liest dann die Nachricht aus der Warteschlange und übergibt sie an den Player, der die eigentliche Serverkomponente aufruft und denselben Methodenaufruf vorgibt. Wenn der Server den Aufruf empfängt, ist das ursprüngliche Clienttoken daher nicht per Identitätswechsel verfügbar. Die rollenbasierte Sicherheit gilt jedoch weiterhin, und die programmgesteuerte Sicherheit mithilfe der [**ISecurityCallContext-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) funktioniert. Weitere Informationen finden Sie unter [Queued Components Security](queued-components-security.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
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

 

 

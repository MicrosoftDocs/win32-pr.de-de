---
description: In einigen Fällen muss eine Serveranwendung eine Client Identität für Ressourcen bereitstellen, auf die Sie im Auftrag des Clients zugreift, in der Regel, um Zugriffs Überprüfungen oder Authentifizierung für die Client Identität auszuführen.
ms.assetid: fd75eb54-eefe-411f-a7aa-0bc8628f8778
title: Client Identitätswechsel und Delegierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7557dcde4cadf559dd8e116cf4e7bece4221aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342604"
---
# <a name="client-impersonation-and-delegation"></a>Client Identitätswechsel und Delegierung

In einigen Fällen muss eine Serveranwendung eine Client Identität für Ressourcen präsentieren, auf die Sie im Auftrag des Clients zugreift, in der Regel, um Zugriffs Überprüfungen oder Authentifizierung für die Identität des Clients durchzuführen. Der Server kann zu einem gewissen Grad unter der Identität des Clients agieren – eine Aktion, die als Identität des Clients angenommen wird.

Identitäts *Wechsel ist die* Fähigkeit eines Threads, in einem anderen Sicherheitskontext als dem Prozess auszuführen, der den Thread besitzt. Der Server Thread verwendet ein Zugriffs Token, das die Anmelde Informationen des Clients darstellt, und damit kann er auf Ressourcen zugreifen, auf die der Client zugreifen kann.

Durch die Verwendung des Identitäts Wechsels wird sichergestellt, dass der Server genau den Funktionsumfang des Clients erledigen kann. Der Zugriff auf Ressourcen kann entweder eingeschränkt oder erweitert werden, je nachdem, welche Berechtigung der Client hat.

Sie können festlegen, dass ein Server beim Herstellen einer Verbindung mit einer Datenbank die Identität eines Clients annimmt, damit die Datenbank den Client für sich selbst authentifizieren und autorisieren kann. Oder wenn Ihre Anwendung auf Dateien zugreift, die durch eine Sicherheits Beschreibung geschützt sind, und der Client autorisierten Zugriff auf Informationen in diesen Dateien erhalten soll, kann die Anwendung vor dem Zugriff auf die Dateien die Identität des Clients annehmen.

## <a name="how-to-implement-impersonation"></a>Implementieren des Identitäts Wechsels

Für den Identitätswechsel sind sowohl der Client als auch der Server erforderlich (in einigen Fällen auch Systemadministratoren). Der Client muss seine Bereitschaft angeben, die Identität des Servers zu gestatten, und der Server muss die Identität des Clients explizit übernehmen. Weitere Informationen finden Sie in den Themen [Client seitige Anforderungen für](client-side-requirements-for-impersonation.md) Identitätswechsel und [Server seitige Anforderungen für](server-side-requirements-for-impersonation.md)Identitätswechsel.

## <a name="administrative-requirements-for-delegate-level-impersonation"></a>Administrative Anforderungen für Delegate-Level Identitätswechsel

Um die leistungsfähigste Form des Identitäts Wechsels effektiv nutzen zu *können, müssen* die Client-und Server Benutzerkonten im Active Directory-Dienst ordnungsgemäß konfiguriert werden, um dies zu unterstützen (zusätzlich zur Client Zertifizierungsstelle zum Durchführen eines Identitäts Wechsels auf delegatebene):

-   Die Server Identität muss im Active Directory-Dienst als "vertrauenswürdig für die Delegierung" gekennzeichnet werden.
-   Die Client Identität darf nicht als "Konto ist vertraulich und kann nicht delegiert werden" im Active Directory-Dienst gekennzeichnet werden.

Mit diesen Konfigurations Features erhält der Domänen Administrator ein hohes Maß an Kontrolle über die Delegierung. Dies ist wünschenswert, da die Vertrauenswürdigkeit (und damit das Sicherheitsrisiko) berücksichtigt wird. Weitere Informationen zur Delegierung finden Sie unter [Delegierung und](/windows/desktop/com/delegation-and-impersonation)Identitätswechsel.

## <a name="cloaking"></a>Cloaking

Zusammen mit der Zertifizierungsstelle, die ein Client einem Server über die Identitätswechsel Ebene zuweist, bestimmt die tokenfähigkeit des Servers größtenteils, wie sich der Identitätswechsel verhält. Das Cloaking wirkt sich darauf aus, welche Identität vom Server tatsächlich angezeigt wird, wenn er Aufrufe im Auftrag des Clients durchführt – seinen eigenen oder den des Clients. Weitere Informationen finden Sie unter [Cloaking](cloaking.md).

## <a name="performance-implications"></a>Folgen für die Leistung

Der Identitätswechsel kann sich erheblich auf die Leistung und Skalierung auswirken. Es ist in der Regel günstiger, bei einem-Rückruf die Identität eines Clients anzunehmen, als den-Befehl direkt auszuführen. Im folgenden sind einige der zu berücksichtigenden Aspekte aufgeführt:

-   Der Rechenaufwand bei der Übergabe der Identität in komplizierten Mustern, insbesondere, wenn das dynamische Cloaking aktiviert ist.
-   Die allgemeine Komplexität der Erzwingung einer redundanten Sicherheitsüberprüfung an zahlreichen Stellen statt nur zentral in der mittleren Ebene.
-   Ressourcen, wie z. b. Datenbankverbindungen, die beim Öffnen des Identitäts Wechsels für einen Client nicht mehr verwendet werden können, können nicht über mehrere Clients hinweg wieder verwendet werden – ein sehr großer

Manchmal besteht die einzige wirksame Lösung für ein Problem darin, den Identitätswechsel zu verwenden, diese Entscheidung sollte jedoch sorgfältig abgewogen werden. Weitere Informationen zu diesen Problemen finden Sie unter [mehrstufige Anwendungssicherheit](multi-tier-application-security.md).

## <a name="queued-components"></a>Komponenten in der Warteschlange

In der [Warteschlange befindliche Komponenten](com--queued-components.md) unterstützen keinen Identitätswechsel. Wenn ein Client einen in die Warteschlange eingereihten Objekte aufruft, wird der-Befehl tatsächlich an die Aufzeichnung gerichtet, die ihn als Teil einer Nachricht an den Server verpackt. Der Listener liest die Nachricht dann aus der Warteschlange und übergibt sie an den Player, der die tatsächliche Serverkomponente aufruft und denselben Methodenaufruf ausführt. Wenn der Server den-Befehl empfängt, ist das ursprüngliche Client Token über den Identitätswechsel nicht verfügbar. Die rollenbasierte Sicherheit wird jedoch weiterhin angewendet, und die programmgesteuerte Sicherheit mithilfe der [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) -Schnittstelle funktioniert. Weitere Informationen finden Sie unter Sicherheit in der [Warteschlangen Sicherheit](queued-components-security.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
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

 

 

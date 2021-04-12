---
description: In vielen Szenarien ist die rollenbasierte Sicherheit ein sehr effektiver Mechanismus, aber es gibt Situationen, in denen Sie weniger effektiv ist.
ms.assetid: 6a1e6cf3-7a8c-4249-926d-675a54061adf
title: Effektives Entwerfen von Rollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a340cb2fc643a414ebf784a14e7b61a45bccd3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523248"
---
# <a name="designing-roles-effectively"></a>Effektives Entwerfen von Rollen

In vielen Szenarien ist die rollenbasierte Sicherheit ein sehr effektiver Mechanismus, aber es gibt Situationen, in denen Sie weniger effektiv ist. Berücksichtigen Sie bei der Entscheidung, wo und wie rollenbasierte Sicherheit auf eine bestimmte Anwendung angewendet werden soll, eine Reihe von Faktoren.

## <a name="user-and-data-characteristics-and-the-suitability-of-roles"></a>Benutzer-und Daten Merkmale und die Eignung von Rollen

Rollen funktionieren sehr gut, um Gruppen von Benutzern zu bezeichnen und auf dieser Grundlage die Aktionen zu filtern, die diese Benutzer ausführen können. Dies wird häufig in der Praxis durch das Erstellen von Rollen durchgeführt, die die Position eines Benutzers innerhalb einer Organisation widerspiegeln, z. –. die Rollen "Manager" und "Kassierer", "Administratoren" und "Leser", "Projekt ein Mitarbeiter" und "Projekt zwei Mitarbeiter". In solchen Fällen, in denen die Daten, auf die zugegriffen wird, relativ zu den Benutzern relativ generisch sind, können Rollen effizient verwendet werden, um Geschäftsregeln wie die folgenden zu erzwingen:

-   "Manager können jede beliebige Menge an Geld übertragen. Der Kassierer kann nur bis zu $10.000 übertragen. "

-   "Administratoren können beliebige Änderungen vornehmen. Alle anderen Personen können nur lesen. "

-   "Projekt ein Mitarbeiter kann auf eine bestimmte Datenbank zugreifen. Das ist nicht möglich. "

Abhängig davon, wie die Rollen die Organisationsstruktur eines Unternehmens modellieren, können Benutzer natürlich auf mehrere Rollen zugreifen.

Rollen funktionieren jedoch nicht sehr gut, wenn eine Entscheidung über den Sicherheits Zugriff auf die Merkmale eines bestimmten Daten Abschnitts trifft. Beispielsweise wäre es schwierig, Rollen zu verwenden, um komplizierte Benutzerdaten Beziehungen wie die folgenden widerzuspiegeln:

-   "Ein bestimmter Manager kann nur für Ihre Berichte auf Personaldaten zugreifen."

-   "Joe Consumer kann seinen Konto Saldo nachschlagen."

In solchen Fällen muss die Sicherheitsüberprüfung häufig in der Datenbank selbst durchgeführt werden, bei der es einfacher ist, die angeborenen Merkmale der Daten zu berücksichtigen, auf die zugegriffen wird. Dies bedeutet, dass Sie Identitäts *Wechsel verwenden müssen* , um die Client Identität an die Datenbank zu übergeben und die Datenbank überprüfen zu lassen. Dies kann die Leistung beeinträchtigen und den Anwendungs Entwurf beeinflussen – beispielsweise funktioniert das Verbindungspooling möglicherweise nicht, wenn eine Verbindung unter einer bestimmten Benutzeridentität geöffnet wird. Eine Erläuterung der betroffenen Probleme finden Sie unter [mehrstufige Anwendungssicherheit](multi-tier-application-security.md) und Client Identitätswechsel [und Delegierung](client-impersonation-and-delegation.md).

## <a name="complexity-and-scalability-of-a-role-based-authorization-policy"></a>Komplexität und Skalierbarkeit einer Role-Based Autorisierungs Richtlinie

Jede Sicherheitsrichtlinie, die Sie bereitstellen, ist nur so effektiv wie die Implementierung durch die Systemadministratoren, die Ihre Anwendung bereitstellen. Wenn Administratoren Fehler beim Zuweisen von Benutzern zu den richtigen Rollen gemäß Ihrer Sicherheitsrichtlinie leisten, funktioniert Ihre Richtlinie nicht wie vorgesehen. Probleme treten wahrscheinlich unter den folgenden Umständen auf:

-   Sie haben eine sehr komplizierte rollenbasierte Richtlinie erstellt, mit vielen Rollen und Benutzern, die zahlreichen Rollen zuordnet.
-   Sie erstellen Rollen mit mehrdeutigen Kriterien für die Benutzer, die zu Ihnen gehören sollen.
-   An dem Standort, an dem die Anwendung installiert ist, gibt es viele Benutzer, die sich häufig innerhalb der Organisation bewegen und sich in Bezug auf die von Ihnen erstellten Rollen ändern.
-   An dem Standort, an dem die Anwendung installiert ist, gibt es viele Administratoren mit einer Division von Zuständigkeiten, sodass ein Administrator, der mit den Sicherheitsanforderungen Ihrer Anwendung vertraut ist, nicht mit den großen Gruppen von Benutzern vertraut ist, die ihn verwenden müssen. Dies ist insbesondere dann von Bedeutung, wenn Benutzer innerhalb des Unternehmens wechseln – diese Informationen müssen gut kommuniziert werden.

Wenn die Anzahl der Rollen, die einer Anwendung zugewiesen sind, zunimmt, bedeutet dies, dass die Zeitspanne, die com+ für die Suche nach der Aufrufer-Mitgliedschaft in diesen Rollen aufwenden muss, mit einer wahrscheinlichen Beeinträchtigung der Leistung.

Um die Komplexität zu verwalten und diese Probleme zu mindern, können Sie die folgenden Richtlinien verwenden:

-   Wählen Sie Rollennamen aus, die selbst beschreibend sind. Legen Sie fest, wie möglich die Benutzer zu welchen Rollen gehören sollen.
-   Machen Sie Ihre rollenbasierte Richtlinie so einfach wie möglich (und nicht einfacher). Wählen Sie möglichst wenige Rollen aus, während Sie eine effektive Richtlinie beibehalten.
-   Dokumentieren Sie eindeutig die rollenbasierte Richtlinie, die Sie für Administratoren erstellen, unabhängig davon, ob die Rollen Mitgliedschaft offensichtlich ist (für Sie). Verwenden Sie insbesondere das Beschreibungsfeld, das für jede Rolle verfügbar ist, um die Absicht der Rolle zu beschreiben. Wenn Sie nicht in der Regel beschreiben können, wer in einigen Sätzen der Rolle angehören soll, ist dies wahrscheinlich zu kompliziert.
-   Legen Sie nachdrücklich fest, dass die Administratoren Ihrer Anwendung Rollen mit Benutzergruppen anstelle einzelner Benutzer auffüllen. Dies ist eine viel besser skalierbare Lösung. Es vereinfacht das Neuzuweisen oder Entfernen von Benutzern, wenn Sie sich innerhalb der Organisation bewegen, und isoliert Administratoren von einem gewissen Maß an Überwachung und Problemen bei der Kommunikation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheitsgrenzen](security-boundaries.md)
</dt> <dt>

[Informationen zum Sicherheits Aufrufkontext](security-call-context-information.md)
</dt> <dt>

[Sicherheitskontext Eigenschaft](security-context-property.md)
</dt> <dt>

[Verwenden von Rollen für die Client Autorisierung](using-roles-for-client-authorization.md)
</dt> </dl>

 

 




---
description: In vielen Szenarien ist die rollenbasierte Sicherheit ein sehr effektiver Mechanismus, aber es gibt Situationen, in denen sie weniger effektiv ist.
ms.assetid: 6a1e6cf3-7a8c-4249-926d-675a54061adf
title: Effektives Entwerfen von Rollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134b1caa68c06aef14a21963bb01ee4dfd12f43153ea917487598d76b0e36d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991120"
---
# <a name="designing-roles-effectively"></a>Effektives Entwerfen von Rollen

In vielen Szenarien ist die rollenbasierte Sicherheit ein sehr effektiver Mechanismus, aber es gibt Situationen, in denen sie weniger effektiv ist. Sie sollten eine Reihe von Faktoren berücksichtigen, wenn Sie entscheiden, wo und wie die rollenbasierte Sicherheit auf eine bestimmte Anwendung angewendet werden soll.

## <a name="user-and-data-characteristics-and-the-suitability-of-roles"></a>Benutzer- und Datenmerkmale und Eignung von Rollen

Rollen funktionieren sehr gut, um Benutzergruppen zu charakterisieren und auf dieser Grundlage zu filtern, welche Aktionen diese Benutzer ausführen können. Häufig erfolgt dies in der Praxis durch die Erstellung von Rollen, die den Platz eines Benutzers innerhalb einer Organisation widerspiegeln, z. B. die Rollen "Manager" und "Leser", "Administratoren" und "Leser", "Project Ein Mitarbeiter" und "Project zwei Mitarbeiter". In solchen Fällen, in denen die Daten, auf die zugegriffen wird, relativ zu den Benutzern relativ generisch sind, können Rollen effizient verwendet werden, um Geschäftsregeln wie die folgenden zu erzwingen:

-   "Manager können einen beliebigen Geldbetrag übertragen. Kassierer können nur bis zu 10.000 US-Dollar übertragen."

-   "Administratoren können alles ändern. Alle anderen Benutzer können nur lesen."

-   "Project Ein Mitarbeiter kann auf eine bestimmte Datenbank zugreifen. Niemand anderes kann dies tun."

Benutzer können auf natürliche Weise in mehrere Rollen fallen, je nachdem, wie die Rollen die Organisationsstruktur eines Unternehmens modellieren.

Rollen funktionieren jedoch nicht sehr gut, wenn eine Sicherheitszugriffsentscheidung auf den Merkmalen eines bestimmten Datenteils beruht. Beispielsweise wäre es schwierig, Rollen zu verwenden, um komplizierte Benutzerdatenbeziehungen wie die folgenden widerzuspiegeln:

-   "Eine bestimmte Managerin kann nur für ihre Berichte auf Mitarbeiterdaten zugreifen."

-   "Joe Consumer can look up his account balance." (Joe Consumer kann seinen Kontostand suchen.)

In solchen Fällen muss die Sicherheitsüberprüfung häufig in der Datenbank selbst durchgeführt werden, wo es einfacher ist, die merkmale der Daten zu berücksichtigen, auf die zugegriffen wird. Dies bedeutet, dass Sie den *Identitätswechsel* verwenden müssen, um die Clientidentität an die Datenbank zu übergeben und die Datenbank die Anforderung überprüfen zu lassen. Dies kann sich auf die Leistung auswirken und sich auf den Anwendungsentwurf auswirken. Verbindungspooling funktioniert beispielsweise möglicherweise nicht, wenn eine Verbindung unter einer bestimmten Benutzeridentität geöffnet wird. Eine Erläuterung der damit verbundenen Probleme finden Sie unter Anwendungssicherheit mit [mehreren Ebenen](multi-tier-application-security.md) und [Identitätswechsel und Delegierung](client-impersonation-and-delegation.md)von Clients.

## <a name="complexity-and-scalability-of-a-role-based-authorization-policy"></a>Komplexität und Skalierbarkeit einer Role-Based Autorisierungsrichtlinie

Jede von Ihnen eingerichtete Sicherheitsrichtlinie ist nur so effektiv wie die Implementierung durch die Systemadministratoren, die Ihre Anwendung bereitstellen. Wenn Administratoren Fehler beim Zuweisen von Benutzern zu den richtigen Rollen gemäß Ihrer Sicherheitsrichtlinie machen, funktioniert Ihre Richtlinie nicht wie vorgesehen. Probleme treten höchstwahrscheinlich unter den folgenden Umständen auf:

-   Sie haben eine sehr komplexe rollenbasierte Richtlinie erstellt, bei der viele Rollen und Benutzer zahlreichen Rollen zugeordnet sind.
-   Sie erstellen Rollen mit mehrdeutigen Kriterien dafür, wer zu ihnen gehören soll.
-   Es gibt viele Benutzer an dem Standort, an dem die Anwendung installiert ist, und Benutzer bewegen sich häufig innerhalb der Organisation und ändern sich in Bezug auf die rollen, die Sie erstellt haben.
-   An dem Standort, an dem die Anwendung installiert ist, gibt es viele Administratoren mit einer Aufteilung der Zuständigkeiten, sodass ein Administrator, der mit den Sicherheitsanforderungen Ihrer Anwendung vertraut ist, möglicherweise nicht mit den großen Benutzergruppen vertraut ist, die sie verwenden müssen. Dies ist besonders wichtig, wenn Benutzer innerhalb der Organisation verschoben werden. Diese Informationen müssen gut kommuniziert werden.

Mit zunehmender Anzahl von Rollen, die einer Anwendung zugewiesen sind, erhöht sich auch die Zeit, die COM+ mit der Suche nach der Aufrufermitgliedschaft in diesen Rollen verbringen muss, mit einer wahrscheinlichen Beeinträchtigung der Leistung.

Um die Komplexität zu verwalten und diese Probleme zu beheben, können Sie die folgenden Richtlinien verwenden:

-   Wählen Sie Rollennamen aus, die selbstdeskriptiv sind. Machen Sie so offensichtlich wie möglich, welche Benutzer zu welchen Rollen gehören sollen.
-   Gestalten Sie Ihre rollenbasierte Richtlinie so einfach wie möglich (und nicht einfacher). Wählen Sie so wenige Rollen wie sie können, und behalten Sie gleichzeitig eine effektive Richtlinie bei.
-   Dokumentieren Sie eindeutig die rollenbasierte Richtlinie, die Sie für Administratoren erstellen, unabhängig davon, ob die Rollenmitgliedschaft (für Sie) offensichtlich ist. Verwenden Sie insbesondere das für jede Rolle verfügbare Beschreibungsfeld, um die Absicht der Rolle zu beschreiben. Wenn Sie in einigen Sätzen nicht allgemein beschreiben können, wer der Rolle angehören soll, ist dies wahrscheinlich zu kompliziert.
-   Es wird dringend empfohlen, dass Administratoren Ihrer Anwendung Rollen mit Benutzergruppen statt mit einzelnen Benutzern auffüllen. Dies ist eine wesentlich skalierbare lösung. Dies erleichtert das erneute Zuweisen oder Entfernen von Benutzern, wenn sie innerhalb der Organisation verschoben werden, und schützt Administratoren vor einem bestimmten Maß an Überwachung und Kommunikationsproblemen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheitsgrenzen](security-boundaries.md)
</dt> <dt>

[Kontextinformationen für Sicherheitsaufrufe](security-call-context-information.md)
</dt> <dt>

[Sicherheitskontexteigenschaft](security-context-property.md)
</dt> <dt>

[Verwenden von Rollen für die Clientautorisierung](using-roles-for-client-authorization.md)
</dt> </dl>

 

 




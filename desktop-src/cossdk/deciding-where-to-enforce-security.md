---
description: Vor-und Nachteile sind inhärent beim Erzwingen der Sicherheit.
ms.assetid: f01573f3-aae6-400e-bdd9-6f34f4e262f6
title: Festlegen der Erzwingung der Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac994fb98d50a7e26f1b8142e77dc9ff771f6b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523259"
---
# <a name="deciding-where-to-enforce-security"></a>Festlegen der Erzwingung der Sicherheit

Vor-und Nachteile sind inhärent beim Erzwingen der Sicherheit. Eine Datenbank kann eine natürliche Stelle zum Platzieren von Sicherheitslogik sein, vorausgesetzt, dass diese Daten letztendlich das wichtigste sind, zu schützen. Allerdings hat dies erhebliche Auswirkungen auf die Leistung. Die Erzwingung der Sicherheit in der Datenbank kann sehr kostspielig sein, eine schlechte Skalierung und eine unflexible Skalierung

## <a name="enforcing-security-in-the-middle-tier"></a>Erzwingen der Sicherheit auf der mittleren Ebene

Die allgemeine Regel für skalierbare Anwendungen mit mehreren Ebenen mit com+ ist, dass Sie nach Möglichkeit eine detaillierte Sicherheit in der com+-Anwendung auf der mittleren Ebene erzwingen sollten. Auf diese Weise können Sie die von com+ bereitgestellten skalierbaren Dienste vollständig nutzen. Erzwingen Sie die Authentifizierung nur dann bei der Datenbank, wenn Sie dies unbedingt benötigen, und Wägen Sie die Auswirkungen der Leistung auf die Leistung ab.

Die optimale Situation besteht darin, Datenbanktabellen so zu sichern, dass die COM+-Anwendung unter ihrer eigenen Identität darauf zugreifen kann. Die Datenbank sollte nur die COM+-Anwendung authentifizieren und Ihr Vertrauen, um Clients, die auf Daten zugreifen werden, ordnungsgemäß zu authentifizieren und zu autorisieren. Diese Vorgehensweise bietet folgende Vorteile:

-   Sie ermöglicht das Verbindungspooling zwischen allen Clients, da die Verbindungen vollständig generisch sind.
-   Im allgemeinen optimiert Sie den Datenzugriff, häufig ein problematischer Knackpunkt beim Skalieren von Anwendungen.
-   Dadurch kann der logische mehr Aufwand für die Erzwingung der Sicherheit minimiert werden, insbesondere dann, wenn die deklarative rollenbasierte Sicherheit verwendet werden kann.
-   Dies kann eine hohe Flexibilität in einer Sicherheitsrichtlinie bereitstellen. Sie können es problemlos konfigurieren und neu konfigurieren, wie unter [rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)beschrieben.

Aber wie bereits erläutert, ist das [effektive Entwerfen von Rollen](designing-roles-effectively.md), während Rollen leicht und effektiv auf einige Benutzerdaten Beziehungen angewendet werden können, aber keine universelle Lösung für Entscheidungen zum Sicherheits Zugriff.

## <a name="enforcing-security-at-the-database"></a>Erzwingen der Sicherheit in der Datenbank

Trotz der bevorzugte Erzwingung der Sicherheit auf der mittleren Ebene gibt es eine Reihe von Gründen für die Durchsetzung der Sicherheit in der Datenbank, wie z. b.:

-   Sie haben keine Wahl, vielleicht aus Legacy Gründen oder vielleicht, weil die Entscheidung einfach nicht in Hand ist.
-   Der Zugriff auf die Datenbank erfolgt über eine Vielzahl von Anwendungen, und ihre Sicherheit kann nicht auf Grundlage einer einzelnen Anwendung konfiguriert werden.
-   Eine Datenbank kann als vorhersag barer Schutz erstellt werden. Wenn Sie Unternehmens wichtige Daten in einer Datenbank speichern, können Sie einen engen Wagen herum zeichnen und Steuern, wer Sie sehen kann.
-   Durch das Authentifizieren ursprünglicher Clients in der Datenbank wird eine ausführliche Protokollierung der Person ermöglicht, die in der Datenbank ausgeführt wurde.
-   Einige Daten sind an bestimmte Benutzer gebunden, und die Logik der Erstellung äußerst differenzierter Zugriffs Entscheidungen kann am effizientesten in der Datenbank selbst, nah an den Daten, ausgeführt werden.

Wenn Sie die Sicherheit der Datenbank und der com+-Anwendung gleichzeitig gestalten möchten, betreffen die meisten dieser Probleme die Merkmale der Daten selbst und deren Beziehung zu den Benutzern, die darauf zugreifen. Mit Daten, auf die von vorhersagbaren Kategorien von Benutzern zugegriffen werden kann, ist es effizient, den Zugriff auf der mittleren Ebene mithilfe von Rollen zu steuern. Mit Daten, die an sehr kleine Benutzer Klassen gebunden sind, müssen diese Beziehungen häufig mit den Daten selbst ausgedrückt werden. Daher müssen Sie eine gewisse Sicherheit in der Datenbank erzwingen.

### <a name="performance-implications-of-enforcing-security-at-the-database"></a>Leistungseinbußen beim Erzwingen der Sicherheit in der Datenbank

Wenn Sie Benutzer in der Datenbank authentifizieren oder autorisieren, muss die Benutzeridentität zur Unterstützung der Datenbank an die Datenbank weitergegeben werden. Wenn die Datenbank für die Anwendung der mittleren Ebene vertraut, ist es möglich, die Benutzer Sicherheitsinformationen in den Parametern zu übergeben. Andernfalls muss der Daten Bankwechsel unter der Identität des Benutzers erfolgen. Dies bedeutet, dass die Serveranwendung die Identität des Clients annehmen muss. Dies kann Auswirkungen auf die Leistung haben, z. b. die folgenden:

-   Das Annehmen der Identität des Clients kann viel langsamer sein als der direkte Anrufe unter der Anwendungs Identität. Weitere Details finden Sie unter [Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md).
-   Eine mit einer bestimmten Benutzeridentität erstellte Datenbankverbindung kann nicht in einem Pool zusammengefasst werden.
-   Wenn Sie Logik in der Datenbank selbst hinzufügen, besteht das Risiko, dass ein Skalierungs Engpass entsteht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Szenarien zum Sichern von Daten in Anwendungen mit mehreren Ebenen](basic-scenarios-for-securing-data-in-multi-tier-applications.md)
</dt> <dt>

[Multi-Tier-Anwendungssicherheit](multi-tier-application-security.md)
</dt> </dl>

 

 




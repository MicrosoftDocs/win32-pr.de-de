---
description: Mit der Erzwingen von Sicherheit sind Vor- und Abkniffe verbunden.
ms.assetid: f01573f3-aae6-400e-bdd9-6f34f4e262f6
title: Entscheidung, wo Die Sicherheit erzwungen werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c13bb81a74b329c662370f24db51559c9dd83f0c1c521ba70dfdcb8be1c813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128771"
---
# <a name="deciding-where-to-enforce-security"></a>Entscheidung, wo Die Sicherheit erzwungen werden soll

Mit der Erzwingen von Sicherheit sind Vor- und Abkniffe verbunden. Eine Datenbank kann ein natürlicher Ort sein, um Sicherheitslogik zu implementieren, da letztendlich diese Daten das Wichtigste sind, das geschützt werden muss. Dies hat jedoch erhebliche Auswirkungen auf die Leistung. Das Erzwingen der Sicherheit in der Datenbank kann sehr teuer, schlecht skaliert und unflexibel sein.

## <a name="enforcing-security-in-the-middle-tier"></a>Erzwingen der Sicherheit auf der mittleren Ebene

Die allgemeine Regel für skalierbare Anwendungen mit mehreren Ebenen mit COM+ ist, dass Sie nach Möglichkeit detaillierte Sicherheit in der COM+-Anwendung auf der mittleren Ebene erzwingen sollten. Auf diese Weise können Sie die skalierbaren Dienste von COM+ vollständig nutzen. Erzwingen Sie die Authentifizierung bei der Datenbank nur, wenn Dies unbedingt erforderlich ist, und wägen Sie die Auswirkungen auf die Leistung vollständig ab.

Die optimale Situation besteht in der Möglichkeit, Datenbanktabellen so zu sichern, dass die COM+-Anwendung unter ihrer eigenen Identität darauf zugreifen kann. Die Datenbank sollte lediglich die COM+-Anwendung authentifizieren und ihr vertrauen, um Clients, die auf Daten zugreifen, ordnungsgemäß zu authentifizieren und zu autorisieren. Die Vorteile dieses Ansatzes lauten wie folgt:

-   Es ermöglicht verbindungspooling zwischen allen Clients, da Verbindungen vollständig generisch sind.
-   Im Allgemeinen wird der Datenzugriff optimiert. Dies ist häufig ein problematischer Drosselungspunkt beim Skalieren von Anwendungen.
-   Dadurch kann der Logikaufwand für das Erzwingen der Sicherheit minimiert werden, insbesondere, wenn deklarative rollenbasierte Sicherheit verwendet werden kann.
-   Es kann eine große Flexibilität in einer Sicherheitsrichtlinie bieten. Sie können sie ganz einfach konfigurieren und neu konfigurieren, wie unter [Rollenbasierte Sicherheitsverwaltung beschrieben.](role-based-security-administration.md)

Wie unter Effektives Entwerfen von Rollen [erläutert,](designing-roles-effectively.md)können Rollen zwar einfach und effektiv auf einige Benutzer-Daten-Beziehungen angewendet werden, sind aber keine universelle Lösung für Entscheidungen zum Sicherheitszugriff.

## <a name="enforcing-security-at-the-database"></a>Erzwingen der Sicherheit in der Datenbank

Trotz der Bevorzugung der Erzwingung der Sicherheit auf der mittleren Ebene gibt es eine Reihe von Gründen, die Sicherheit für die Datenbank zu erzwingen, z. B.:

-   Sie haben keine Wahl, vielleicht aus legacy-Gründen oder weil die Entscheidung einfach nicht in Ihren Händen liegt.
-   Auf die Datenbank wird von einer Vielzahl von Anwendungen zugegriffen, und ihre Sicherheit kann nicht auf der Grundlage einer einzelnen Anwendung konfiguriert werden.
-   Eine Datenbank kann vorhersagbar geschützt werden. Wenn Sie unternehmenskritische Daten in einer Datenbank speichern, können Sie eine enge Schublade um sie herum ziehen und steuern, wer sie sehen kann.
-   Die Authentifizierung ursprünglicher Clients in der Datenbank ermöglicht eine detaillierte Protokollierung, wer was in der Datenbank getan hat.
-   Einige Daten sind von Natur aus an bestimmte Benutzer gebunden, und die Logik, äußerst fein abgrenzende Zugriffsentscheidungen zu treffen, kann in der Datenbank selbst, in der Nähe der Daten, am effektivsten ausgeführt werden.

Wenn Sie die Sicherheit der Datenbank und der COM+-Anwendung gemeinsam entwerfen möchten, beziehen sich die meisten dieser Probleme auf merkmale der Daten selbst und ihre Beziehung zu den Benutzern, die darauf zugreifen. Mit Daten, auf die von vorhersagbaren Benutzerkategorien zugegriffen werden kann, ist es effizient, den Zugriff auf der mittleren Ebene mithilfe von Rollen zu steuern. Bei Daten, die kompliziert an sehr kleine Benutzerklassen gebunden sind, müssen diese Beziehungen häufig mit den Daten selbst ausgedrückt werden. Daher müssen Sie sicherheitsmaßnahmen für die Datenbank erzwingen.

### <a name="performance-implications-of-enforcing-security-at-the-database"></a>Auswirkungen der Erzwingen der Sicherheit in der Datenbank auf die Leistung

Wenn Sie Benutzer in der Datenbank authentifizieren oder autorisieren, muss die Benutzeridentität zur Unterstützung an die Datenbank weitervergeben werden. Wenn die Datenbank der Anwendung der mittleren Ebene vertraut, ist es möglich, Benutzersicherheitsinformationen in Parametern zu übergeben. Andernfalls muss der Aufruf von an die Datenbank unter der Identität des Benutzers ausgeführt werden, was bedeutet, dass die Serveranwendung die Identität des Clients imitieren muss. Dies kann auswirkungen auf die Leistung haben, z. B.:

-   Der Identitätswechsel des Clients kann viel langsamer sein als der Aufruf direkt unter der Anwendungsidentität. Weitere Informationen finden Sie unter [Clientpersonation and Delegation](client-impersonation-and-delegation.md).
-   Eine Datenbankverbindung, die unter einer bestimmten Benutzeridentität hergestellt wird, kann nicht in einem Pool erstellt werden.
-   Durch das Hinzufügen von Logik in der Datenbank selbst besteht das Risiko, dass ein Skalierungsengpass verursacht wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Szenarien zum Sichern von Daten in Anwendungen mit mehreren Ebenen](basic-scenarios-for-securing-data-in-multi-tier-applications.md)
</dt> <dt>

[Anwendungssicherheit mit mehreren Ebenen](multi-tier-application-security.md)
</dt> </dl>

 

 




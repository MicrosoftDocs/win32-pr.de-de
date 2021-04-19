---
description: Multi-Tier-Anwendungssicherheit
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Multi-Tier-Anwendungssicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150f7894c7d11e832786e31ab028f9dbac35f6e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346226"
---
# <a name="multi-tier-application-security"></a>Multi-Tier-Anwendungssicherheit

Sie können Schwierigkeiten bei der Entscheidung treffen, wie die Sicherheit in einer auf mehreren Ebenen basierenden, komponentenbasierten Anwendung in der Datenbank zu erzwingen ist. Auf der mittleren Ebene? In den Komponenten? An einem anderen Ort? Überall? Wenn die Anzahl und Komplexität der Sicherheitsmechanismen zunimmt, wird die Leistung beeinträchtigt, und das Anwendungsverhalten wird weniger vorhersagbar. Dennoch müssen Sie sicherstellen, dass die Daten geschützt sind, dass Geschäftsregeln befolgt werden und dass eine beträchtliche Aktivität protokolliert wird und die Anwendung weiterhin für Clients funktioniert. Sie müssen sicher sein, dass jeder Client Pfad über die Anwendung korrekt ist und dass die vorhandenen Sicherheits Prüfpunkte ausreichen.

Die schwierigste Entscheidung besteht häufig darin, die Sicherheit in der Datenbank zu erzwingen. In der Vergangenheit handelt es sich hierbei um eine enge Sicherheit der Sicherheit, da Sie als ein Königreich wahrgenommen wird, das wirklich sicher sein muss, und Datenbankadministratoren sehr ungern eine andere Person als vertrauenswürdig einstufen, um die Sicherheit zu erzwingen. Die Erzwingung der Sicherheit in der Datenbank kann jedoch sehr kostspielig und schwer zu skalieren sein. Dies ist genau der Punkt, an dem Sie Anwendungen mit mehreren Ebenen erstellen.

Die allgemeine Regel für skalierbare Anwendungen mit mehreren Ebenen mit com+ ist, dass Sie nach Möglichkeit eine detaillierte Sicherheit in der com+-Anwendung auf der mittleren Ebene erzwingen sollten. Auf diese Weise können Sie die von com+ bereitgestellten skalierbaren Dienste vollständig nutzen. Authentifizieren Sie sich nur dann bei der Datenbank, wenn dies unbedingt erforderlich ist.

Eine Erörterung von Problemen bei der Entscheidung, wo Sicherheitsüberprüfungen durchgeführt werden sollen, finden Sie unter [entscheiden, wo die Sicherheit](deciding-where-to-enforce-security.md)erzwungen werden soll.

Eine Erläuterung einiger grundlegender Szenarien zum Sichern von Anwendungen mit mehreren Ebenen finden Sie unter [grundlegende Szenarien zum Sichern von Daten in Anwendungen mit mehreren Ebenen](basic-scenarios-for-securing-data-in-multi-tier-applications.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Client Identitätswechsel und Delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Sicherheit der Bibliothek Anwendungen](library-application-security.md)
</dt> <dt>

[Sicherheit für programmgesteuerte Komponenten](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[Verwenden der Richtlinie für Software Einschränkung in com+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 




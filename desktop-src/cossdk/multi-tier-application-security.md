---
description: Anwendungssicherheit mit mehreren Ebenen
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Anwendungssicherheit mit mehreren Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ba43970c2af5ff6c7abb733767b721091f6a3d3407178d5360e5f96db11d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070469"
---
# <a name="multi-tier-application-security"></a>Anwendungssicherheit mit mehreren Ebenen

Es kann schwierig sein, genau zu entscheiden, wo sicherheit in einer mehrschichtigen, komponentenbasierten Anwendung erzwungen werden soll: In der Datenbank? Auf der mittleren Ebene? In den Komponenten? Woanders? Überall? Mit zunehmender Anzahl und Komplexität von Sicherheitsmechanismen nimmt die Leistung ab, und das Anwendungsverhalten wird weniger vorhersagbar. Trotzdem müssen Sie sicherstellen, dass Daten geschützt sind, Geschäftsregeln eingehalten werden und wichtige Aktivitäten protokolliert werden, und Ihre Anwendung weiterhin wie vorgesehen für Clients funktioniert. Sie müssen sicher sein, dass jeder Clientpfad durch Ihre Anwendung korrekt ist und dass die eingerichteten Sicherheitsprüfpunkte ausreichen.

Die schwierigste Entscheidung ist häufig, ob die Sicherheit in der Datenbank erzwungen werden soll. In der Vergangenheit ist hier die Sicherheit am engsten, da sie als das einzige Königreich wahrgenommen wird, das wirklich sicher sein muss, und Datenbankadministratoren sind sehr vertrauenswürdig, jemand anderem zu vertrauen, um sicherheit für sie zu erzwingen. Die Erzwingung der Sicherheit in der Datenbank kann jedoch sehr teuer und schwierig zu skalieren sein. Dies ist genau der Punkt, an dem Anwendungen mit mehreren Ebenen überhaupt geschrieben werden.

Die allgemeine Regel für skalierbare Anwendungen mit mehreren Ebenen, die COM+ verwenden, ist, dass Sie nach Möglichkeit detaillierte Sicherheit in der COM+-Anwendung auf der mittleren Ebene erzwingen sollten. Auf diese Weise können Sie die skalierbaren Dienste von COM+ vollständig nutzen. Authentifizieren Sie sich nur dann bei der Datenbank, wenn Sie dies unbedingt benötigen, und wägen Sie die Auswirkungen auf die Leistung vollständig ab.

Eine Erläuterung der Zu berücksichtigenden Probleme bei der Entscheidung, wo Sicherheitsüberprüfungen durchgeführt werden sollen, finden Sie unter [Entscheidung, wo Sicherheit erzwungen werden soll.](deciding-where-to-enforce-security.md)

Eine Erläuterung einiger grundlegender Szenarien zum Sichern von Anwendungen mit mehreren Ebenen finden Sie unter Grundlegende Szenarien zum Schützen von Daten in Anwendungen mit [mehreren Ebenen.](basic-scenarios-for-securing-data-in-multi-tier-applications.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> <dt>

[Clientidentitätswechsel und -delegierung](client-impersonation-and-delegation.md)
</dt> <dt>

[Bibliotheksanwendungssicherheit](library-application-security.md)
</dt> <dt>

[Programmgesteuerte Komponentensicherheit](programmatic-component-security.md)
</dt> <dt>

[Rollenbasierte Sicherheitsverwaltung](role-based-security-administration.md)
</dt> <dt>

[Verwenden der Softwareeinschränkungsrichtlinie in COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 




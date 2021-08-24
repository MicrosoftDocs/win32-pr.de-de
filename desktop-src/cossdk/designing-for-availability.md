---
description: Verfügbarkeit ist die Fähigkeit einer Anwendung, Fehler in Serverressourcen zu tolerieren.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Entwerfen für Verfügbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f248b9ac9ed91788713e7ef02b4e7da0a2d7eb0c2070b1240e07dbce21b5895c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637660"
---
# <a name="designing-for-availability"></a>Entwerfen für Verfügbarkeit

Verfügbarkeit ist die Fähigkeit einer Anwendung, Fehler in Serverressourcen zu tolerieren. Dies bedeutet, dass der Client weiterhin über den Fehler bedient wird und im Idealfall für den Client transparent ist. Natürlich kann der Fehler entweder aus Hardware- oder Softwarequellen stammen, daher müssen Sie für beide Fälle entwickeln.

Die Verfügbarkeit kann durch die folgenden Faktoren beeinträchtigt werden:

-   Anwendungsmodell. Stellen Sie für höchste Verfügbarkeit sicher, dass die kritische Anwendungslogik mit dem [COM+-Transaktionsdienst](com--transactions.md) durchgeführt wird. Darüber hinaus kann die Verwendung eines Kompensationsmechanismus effektiv sein, um sicherzustellen, dass Ressourcen nach Ausfällen in einem fehlerfreien Zustand bleiben.
-   Clientmodell. Integrieren Sie die Logik "Bei Fehler wiederholen" in die Clientanwendung, und versuchen Sie, die Anwendung ordnungsgemäß zu beeinträchtigen, wenn Ressourcen oder Dienste nicht verfügbar sind. Verstehen Sie, was der Client von der Anwendung erwartet, und erstellen Sie einen Entwurf, der Alternativen zulässt, wenn ein Fehler auftritt.
-   Daten-/Statusverfügbarkeit. Verwenden Sie für konsistenten Zugriff auf persistente Daten Windows Clustering, um Failoverunterstützung bereitzustellen.
-   Dienstverfügbarkeit: Sie können den Netzwerklastenausgleich verwenden, um eingehende IP-Anforderungen über einen Servercluster hinweg auszugleichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen für die Bereitstellung](designing-for-deployment.md)
</dt> <dt>

[Entwerfen für Skalierbarkeit](designing-for-scalability.md)
</dt> <dt>

[Entwerfen für Die Sicherheit](designing-for-security.md)
</dt> </dl>

 

 




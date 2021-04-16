---
description: Verfügbarkeit ist die Fähigkeit einer Anwendung, Fehler in Server Ressourcen zu tolerieren.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Entwerfen für Verfügbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523547"
---
# <a name="designing-for-availability"></a>Entwerfen für Verfügbarkeit

Verfügbarkeit ist die Fähigkeit einer Anwendung, Fehler in Server Ressourcen zu tolerieren. Dies bedeutet, dass der Client weiterhin über den Fehler bedient wird und dass der Fehler im Idealfall für den Client transparent ist. Natürlich kann der Fehler entweder von Hardware-oder Software Quellen stammen, sodass Sie für beide Fälle entwickeln müssen.

Die Verfügbarkeit kann durch die folgenden Faktoren beeinträchtigt werden:

-   Anwendungsmodell. Stellen Sie sicher, dass die kritische Anwendungslogik mit dem [com+-Transaktions](com--transactions.md) Dienst ausgeführt wird, um die höchste Verfügbarkeit sicherzustellen. Außerdem kann die Verwendung eines Kompensierungs Mechanismus effektiv sein, um sicherzustellen, dass die Ressourcen nach Fehlern in einem fehlerfreien Zustand bleiben.
-   Client Modell. Integrieren Sie die Logik "Wiederholungs Versuche bei Fehler" in die Client Anwendung, und suchen Sie nach einer ordnungsgemäßen Verschlechterung der Anwendung, wenn Ressourcen oder Dienste nicht verfügbar sind. Verstehen Sie, was der Client von der Anwendung erwartet, und erstellen Sie einen Entwurf, der Alternativen ermöglicht, wenn ein Fehler auftritt.
-   Daten-/statusverfügbarkeit. Verwenden Sie zum konsistenten Zugriff auf persistente Daten die Windows-Cluster Unterstützung, um Failoverunterstützung bereitzustellen.
-   Dienst Verfügbarkeit. Sie können den Netzwerk Lastenausgleich für den Lastenausgleich eingehender IP-Anforderungen in einem Cluster von Servern verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen für die Bereitstellung](designing-for-deployment.md)
</dt> <dt>

[Entwerfen von Skalierbarkeit](designing-for-scalability.md)
</dt> <dt>

[Entwerfen für Sicherheit](designing-for-security.md)
</dt> </dl>

 

 




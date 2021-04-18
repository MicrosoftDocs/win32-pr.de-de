---
description: Fehler Isolation und FailFast-Richtlinie
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Fehler Isolation und FailFast-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523432"
---
# <a name="fault-isolation-and-failfast-policy"></a>Fehler Isolation und FailFast-Richtlinie

Com+ führt umfassende interne Integritäts-und Konsistenzprüfungen durch. Wenn com+ eine unerwartete interne Fehlerbedingung feststellt, wird der Prozess sofort beendet. Diese Richtlinie mit dem Namen " *FailFast*" vereinfacht die Fehler Aufnahme und führt zu zuverlässigeren und robusten Systemen.

Stellen Sie sich einen Fall vor, in dem com+ erkennt, dass eine der Datenstrukturen in einem beschädigten Zustand ist. An diesem Punkt sind sowohl die Ursache als auch die Größe der Beschädigung unbekannt, sodass com+ leider nicht erkennen kann, wie weit sich der Schaden verbreitet hat. Obwohl com+ sich in einem unbestimmten Zustand befindet, wird es jedoch nicht isoliert ausgeführt. Wie andere DLLs werden Sie in einer Prozessumgebung gehostet und teilen sich einen einzelnen Adressraum mit der ausführbaren Hauptprogramm Datei und vielen anderen DLLs. Daher geht com+ davon aus, dass der gesamte Prozess beschädigt wurde, und der Prozess wird sofort beendet, um zu verhindern, dass er potenziell beschädigte Informationen an andere Prozesse zuweist oder noch schlimmer ist, dass beschädigte Daten committet und dauerhaft gemacht werden können.

Die Weitergabe von Ausnahmen außerhalb eines Kontexts ist in com+ nicht zulässig. Wenn eine Ausnahme während der Ausführung innerhalb eines com+-Kontexts auftritt und die Anwendung die Ausnahme nicht abfängt, bevor Sie aus dem Kontext zurückkehrt, fängt com+ die Ausnahme ab und beendet den Prozess. Die Verwendung der FailFast-Richtlinie basiert in diesem Fall auf der Annahme, dass die Ausnahme den Prozess in einen unbestimmten Zustand versetzt hat. Es ist nicht sicher, die Verarbeitung fortzusetzen.

Als Entwickler oder Administrator sollten Sie das Ereignisanzeige-Anwendungsprotokoll überprüfen, um Details zu allen FailFast-Aktionen oder schwerwiegenden Anwendungsfehlern zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermitteln der Fehlerquelle](finding-the-source-of-an-error.md)
</dt> <dt>

[Ändern der Rückgabewerte durch com+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretieren von Fehler Codes](interpreting-error-codes.md)
</dt> <dt>

[Strategien für die Behandlung von Fehlern in com+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Problembehandlung](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 




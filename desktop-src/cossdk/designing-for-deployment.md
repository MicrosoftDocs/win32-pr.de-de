---
description: Entwerfen für die Bereitstellung
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Entwerfen für die Bereitstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a755132f1be35ecb6913b7690bce11e342fceb957e63607ee4e9b579bcc758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307300"
---
# <a name="designing-for-deployment"></a>Entwerfen für die Bereitstellung

Die Planung des Umfangs von COM+-Anwendungen ist eine wichtige Entwurfsaufgabe, die Sie frühzeitig berücksichtigen sollten. Verteilte Systeme, die mit COM+ ausgeführt werden sollen, sollten für die Bereitstellung mit der geringsten Menge an individueller Konfiguration und für die effizienteste Verwendung der einzelnen Prozesse konzipiert sein. Es gibt auch Techniken, die Sie verwenden können, um bei der Bereitstellung einer COM+-Anwendung eine optimale Leistung zu erzielen. (Weitere Informationen finden Sie unter [Bereitstellen für schnellere Kommunikation.)](deploying-for-faster-communication.md)

Wenn sie mit dem Component Services-Verwaltungstool angezeigt wird, wird jede COM+-Anwendung als Ordner angezeigt, in dem Komponentensätze logisch gruppiert werden. Während Sie einzelne Komponenten zwischen  com+-Anwendungskomponentenordnern verschieben können (d. h. von einer Anwendung in eine andere), können sich verschiedene Dienste, die auf COM+-Anwendungsebene festgelegt wurden, wie z.B. Sicherheit, unterscheiden. Diese Diensteinstellungen können sich auf die Portabilität auswirken.

## <a name="a-com-server-application-defines-a-process-boundary"></a>Eine COM+-Serveranwendung definiert eine Prozessgrenze.

Wenn Sie eine neue COM+-Serveranwendung erstellen, definieren Sie tatsächlich eine neue Prozessgrenze. (Beachten Sie die unten beschriebene Ausnahme für Bibliotheksanwendungen.) Dieser Prozess wird zur steuernden Anwendungsinstanz für die Komponenten, die in der COM+-Anwendung enthalten sind. Diese Komponenten werden alle prozessübergreifend in einer neuen Instanz des ausführbaren COM+-Programms ausgeführt, wenn ein Programm zum ersten Mal eine COM+-Anwendung aufruft. Dies bedeutet, dass alle Komponenten im **Komponentenordner** einer bestimmten COM+-Anwendung in einem einzigen Prozessbereich ausgeführt werden, der als DCOM-Server dient. Innerhalb der COM+-Anwendung verwaltet COM+ Arbeitsspeicher, Koordination mit dem Distributed Transaction Coordinator (DTC), Just-In-Time-Komponenteninstanzaktivierung, Absturzerkennung und -wiederherstellung sowie rollenbasierte Sicherheit.

## <a name="calling-across-com-application-boundaries"></a>Aufrufen über COM+-Anwendungsgrenzen hinweg

Da jede COM+-Anwendung normalerweise als separate ausführbare Datei implementiert wird, führt die Aufteilung einer verteilten Anwendung auf mehrere COM+-Anwendungen zu out-of-process-COM-Aufrufen, wenn Komponenten in einer COM+-Anwendung die Komponenten in einer anderen COM+-Anwendung aufrufen. Dies führt zu Leistungseinbußen aufgrund der zusätzlichen Belastung, die das Marshallen von COM-Parametern über Prozesse hinweg mit sich bringt.

> [!Note]  
> Diese Leistungseinbußen sind von Natur aus nicht falsch. Sie müssen sich nur bewusst sein, dass dies geschieht. Abhängig von der erforderlichen Antwortzeit, der Anzahl der Benutzer, die gleichzeitig Geschäftsdienste anfordern, und der zusätzlichen Startlast, die jede Komponente jeder COM+-Anwendung hinzufügt, stellen Sie möglicherweise fest, dass die durch anwendungsübergreifende Aufrufe bedingte Leistungssteigerung akzeptabel ist.

 

Eine Möglichkeit, die Leistungseinbußen durch Aufrufe über COM+-Anwendungsgrenzen hinweg zu beseitigen, besteht darin, eine bestimmte COM+-Anwendung als Bibliotheksanwendung zu markieren. Eine COM+-Bibliotheksanwendung wird im Prozess des Clients ausgeführt, der sie erstellt. Natürlich hat kein Leistungsgewinn keine Kosten. In diesem Fall umfasst der Vor- und Nachteile die Einschränkungen von COM+-Bibliotheksanwendungen. Obwohl eine Bibliotheksanwendung rollenbasierte Sicherheit verwenden kann, kann sie keine Komponenten in der Warteschlange oder den Remotezugriff unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bereitstellen für schnellere Kommunikation](deploying-for-faster-communication.md)
</dt> <dt>

[Entwerfen für Verfügbarkeit](designing-for-availability.md)
</dt> <dt>

[Entwerfen für Skalierbarkeit](designing-for-scalability.md)
</dt> <dt>

[Entwerfen für Die Sicherheit](designing-for-security.md)
</dt> </dl>

 

 




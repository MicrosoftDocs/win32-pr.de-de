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

Die Planung des Umfangs von COM+-Anwendungen ist eine wichtige Entwurfsaufgabe, die Sie frühzeitig in Betracht ziehen sollten. Verteilte Systeme, die mit COM+ ausgeführt werden sollen, sollten für die Bereitstellung mit der geringsten Anzahl einzelner Konfigurationen und für die effiziente Verwendung der einzelnen Prozesse konzipiert sein. Es gibt auch Techniken, die Sie verwenden können, um eine optimale Leistung bei der Bereitstellung einer COM+-Anwendung zu erzielen. (Weitere Informationen finden Sie unter [Bereitstellen für schnellere Kommunikation.)](deploying-for-faster-communication.md)

Wenn sie mit dem Verwaltungstool Komponentendienste angezeigt wird, wird jede COM+-Anwendung als Ordner angezeigt, in dem Komponentensätze logisch gruppiert werden. Sie können einzelne Komponenten zwischen  COM+-Anwendungskomponentenordnern verschieben (d. h. von einer Anwendung in eine andere), aber mehrere Dienste, die auf COM+-Anwendungsebene festgelegt sind, z. B. Sicherheit, können sich unterscheiden. Diese Diensteinstellungen können sich auf die Portabilität auswirken.

## <a name="a-com-server-application-defines-a-process-boundary"></a>Eine COM+-Serveranwendung definiert eine Prozessgrenze.

Wenn Sie eine neue COM+-Serveranwendung erstellen, definieren Sie tatsächlich eine neue Prozessgrenze. (Beachten Sie die unten erläuterte Ausnahme für Bibliotheksanwendungen.) Dieser Prozess wird zur steuernden Anwendungsinstanz für die Komponenten, die in der COM+-Anwendung enthalten sind. Alle diese Komponenten werden in einer neuen Instanz des ausführbaren COM+-Programms ausgeführt, wenn ein Programm zum ersten Mal eine COM+-Anwendung aufruft. Dies bedeutet, dass alle Komponenten innerhalb des Ordners **Components** einer bestimmten COM+-Anwendung in einem einzelnen Prozessbereich ausgeführt werden, der als DCOM-Server dient. Innerhalb der COM+-Anwendung verwaltet COM+ Arbeitsspeicher, Koordination mit dem Distributed Transaction Coordinator (DTC), Just-in-Time-Komponenteninstanzaktivierung, Absturzerkennung und -wiederherstellung sowie rollenbasierte Sicherheit.

## <a name="calling-across-com-application-boundaries"></a>Aufrufen über COM+-Anwendungsgrenzen hinweg

Da jede COM+-Anwendung normalerweise als separate ausführbare Datei implementiert wird, führt die Aufteilung einer verteilten Anwendung auf mehrere COM+-Anwendungen zu Out-of-Process-COM-Aufrufen, wenn Komponenten in einer COM+-Anwendung die Komponenten in einer anderen COM+-Anwendung aufrufen. Dies führt zu Leistungseinbußen aufgrund der zusätzlichen Belastung, die das prozessübergreifende Marshalling von COM-Parametern mit sich bringt.

> [!Note]  
> Es gibt grundsätzlich nichts Falsches, wenn diese Leistungssentität entstehen soll. Sie müssen sich lediglich darüber im Klaren sein, dass dies der Fall sein wird. Abhängig von der erforderlichen Antwortzeit, der Anzahl der Benutzer, die gleichzeitig Geschäftsdienste anfordern, und der zusätzlichen Startlast, die jede Komponente zu jeder COM+-Anwendung hinzufügt, stellen Sie möglicherweise fest, dass die Leistungssteigerung bei anwendungsübergreifenden Aufrufen akzeptabel ist.

 

Eine Möglichkeit, die leistungssentspricht, wenn Aufrufe über COM+-Anwendungsgrenzen hinweg verhindert werden, besteht in der Kennzeichnung einer bestimmten COM+-Anwendung als Bibliotheksanwendung. Eine COM+-Bibliotheksanwendung wird im Prozess des Clients ausgeführt, der sie erstellt. Natürlich hat kein Leistungsgewinn keine Kosten. In diesem Fall geht es um die Einschränkungen von COM+-Bibliotheksanwendungen. Während eine Bibliotheksanwendung rollenbasierte Sicherheit verwenden kann, unterstützt sie keine Komponenten in der Warteschlange oder den Remotezugriff.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bereitstellen für schnellere Kommunikation](deploying-for-faster-communication.md)
</dt> <dt>

[Entwerfen für Verfügbarkeit](designing-for-availability.md)
</dt> <dt>

[Entwerfen für Skalierbarkeit](designing-for-scalability.md)
</dt> <dt>

[Entwerfen aus Sicherheitsgründen](designing-for-security.md)
</dt> </dl>

 

 




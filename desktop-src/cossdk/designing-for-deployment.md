---
description: Entwerfen für die Bereitstellung
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Entwerfen für die Bereitstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483046"
---
# <a name="designing-for-deployment"></a>Entwerfen für die Bereitstellung

Die Planung des Umfangs der com+-Anwendungen ist eine wichtige Entwurfs Aufgabe, die Sie frühzeitig in Erwägung gezogen sollten. Verteilte Systeme, die mit com+ ausgeführt werden sollen, sollten für die Bereitstellung mit der geringsten Menge an einzelner Konfiguration und der optimalen Verwendung der einzelnen Prozesse konzipiert werden. Es gibt auch Techniken, die Sie verwenden können, mit denen Sie bei der Bereitstellung einer COM+-Anwendung eine optimale Leistung erzielen können. (Weitere Informationen finden Sie unter Bereitstellen [für schnellere Kommunikation](deploying-for-faster-communication.md).)

Wenn die COM+-Anwendung mit dem Verwaltungs Programmkomponenten Dienste angezeigt wird, wird Sie als Ordner angezeigt, in dem Gruppen von Komponenten logisch gruppiert sind. Während Sie einzelne Komponenten zwischen com+-Anwendungs **Komponenten** Ordnern (also von einer Anwendung in eine andere Anwendung) verschieben können, können sich mehrere auf der com+-Anwendungsebene festgelegte Dienste, wie z. b. die Sicherheit, unterscheiden. Diese Dienst Einstellungen können die Portabilität beeinflussen.

## <a name="a-com-server-application-defines-a-process-boundary"></a>Eine com+-Server Anwendung definiert eine Prozess Grenze.

Wenn Sie eine neue COM+-Serveranwendung erstellen, definieren Sie wirklich eine neue Prozess Grenze. (Beachten Sie die Ausnahme für Bibliotheksanwendungen, die unten erläutert werden.) Dieser Prozess wird zur steuernden Anwendungs Instanz für die Komponenten, die in der com+-Anwendung enthalten sind. Diese Komponenten werden alle Prozess Weise in einer neuen Instanz des ausführbaren com+-Programms ausgeführt, wenn ein Programm zum ersten Mal eine COM+-Anwendung aufruft. Dies bedeutet, dass alle Komponenten innerhalb eines **bestimmten Ordners der** com+-Anwendung in einem einzelnen Prozessbereich ausgeführt werden, der als DCOM-Server fungiert. In der com+-Anwendung verwaltet com+ den Arbeitsspeicher, die Koordination mit dem Distributed Transaction Coordinator (DTC), die Just-in-Time-Komponenten Instanzen Aktivierung, die Absturz Erkennung und-Wiederherstellung sowie die rollenbasierte Sicherheit.

## <a name="calling-across-com-application-boundaries"></a>Aufrufen über com+-Anwendungsgrenzen hinweg

Da jede com+-Anwendung normalerweise als separate ausführbare Datei implementiert ist, führt die Aufteilung einer verteilten Anwendung über mehrere COM+-Anwendungen zu Prozess externen com-aufrufen, wenn Komponenten in einer COM+-Anwendung die Komponenten in einer anderen COM+-Anwendung aufrufen. Dadurch wird die Leistungsminderung aufgrund der zusätzlichen Belastung durch das Marshalling von com-Parametern in Prozessen beeinträchtigt.

> [!Note]  
> Es gibt keinerlei falsche Probleme mit dieser Leistungs Einbuße. Sie müssen nur beachten, dass es passiert. Abhängig von der erforderlichen Antwortzeit, der Anzahl der Benutzer, die gleichzeitig Unternehmens Dienste anfordern, und der zusätzlichen Start Belastung, die jede Komponente zu den einzelnen com+-Anwendungen hinzufügt, können Sie feststellen, dass die Leistungseinbußen, die auf Anwendungsübergreifende Aufrufe zurückzuführen sind, akzeptabel sind.

 

Eine Möglichkeit, mit der die Leistungseinbußen beim Aufrufen von com+-Anwendungsgrenzen vermieden werden, besteht darin, eine bestimmte COM+-Anwendung als Bibliotheks Anwendung zu markieren. Eine COM+-Bibliotheks Anwendung wird im Prozess des Clients ausgeführt, von dem Sie erstellt wird. Natürlich hat keine Leistungssteigerung Kosten. In diesem Fall umfasst der Kompromiss die Einschränkungen der COM+-Bibliotheksanwendungen. Obwohl eine Bibliotheks Anwendung rollenbasierte Sicherheit verwenden kann, kann Sie in der Warteschlange befindliche Komponenten oder den Remote Zugriff nicht unterstützen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bereitstellen für schnellere Kommunikation](deploying-for-faster-communication.md)
</dt> <dt>

[Entwerfen für Verfügbarkeit](designing-for-availability.md)
</dt> <dt>

[Entwerfen von Skalierbarkeit](designing-for-scalability.md)
</dt> <dt>

[Entwerfen für Sicherheit](designing-for-security.md)
</dt> </dl>

 

 




---
description: Dieser Leitfaden identifiziert eine langsame Anwendung als Microsoft Windows-Anwendung mit eingeschränkter Leistung.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Erkennen langsamer Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369776"
---
# <a name="recognizing-slow-applications"></a>Erkennen langsamer Anwendungen

Dieser Leitfaden identifiziert eine *langsame* Anwendung als Microsoft Windows-Anwendung mit eingeschränkter Leistung. Eine langsame Anwendung weist eines oder mehrere der folgenden Symptome auf:

-   Die CPU-und Netzwerk Auslastung ist niedrig.

    Der Computer scheint auf etwas zu warten. Häufig wartet die Anwendung auf das Netzwerk.

-   Wenn Sie den Nagle-Algorithmus mithilfe der TCP \_ nodelay-Socketoption ausschalten, wird die Leistung gesteigert.

    Dies deutet auf andere Probleme hin und sollte nicht als Lösung betrachtet werden. Wenn Sie den Nagle-Algorithmus ausschalten, erhöht sich der Protokoll Mehraufwand. Verwenden Sie diese Methode nicht als Korrektur für die unterbrochenen Anwendungen – sondern nur als Anzeichen dafür, dass die Anwendung andere Aufgaben benötigt, um Leistungsprobleme zu beheben.

-   Die Anwendung stellt einen hohen mehr Aufwand dar.

    Um den Anwendungs Aufwand zu berechnen, legen Sie fest, wie viele Daten in den einzelnen Richtungen übertragen werden sollen. Verwenden Sie dann netstat, und fügen Sie (für Ethernet) 60 Bytes für jedes Paket und 500 Bytes für jede Verbindung hinzu. Der beste Aufwand, der für das Streaming über Ethernet zu erwarten ist, beträgt ungefähr 6%. Bei einer Modemverbindung liegt der beste Aufwand bei ungefähr 2%, da für einen PPP-Link die Header Komprimierung verwendet wird. Weitere Informationen finden Sie [unter Berechnen von Overhead mit netstat](calculating-overhead-with-netstat-2.md) .

-   Die Anwendungs Antwort wird verlangsamt, wenn die Verbindung über eine große RTT-Verbindung verfügt.

    Wenn die Anwendung die Bandbreite des Links nicht nähert, sollte eine große RTT nur wenig oder gar keine Auswirkung haben. Eine drastische Verlangsamung mit einem großen RTT ist ein deutliches Vorzeichen der serialisierten Verarbeitung und vieler kleiner Transaktionen.

Jede Anwendung sollte in einer Umgebung mit einem großen RTT getestet werden. Auf diese Weise werden die meisten Anwendungen angezeigt, die von schlechten Entwicklungsoptionen leiden. Diese Tests können in verschiedenen Umgebungen durchgeführt werden, einschließlich eines drahtlosen LAN-Netzwerks, eines Verbindungs Verzögerungs Simulators oder eines Satelliten Netzwerks.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsverhalten](application-behavior-2.md)
</dt> <dt>

[Hochleistungsfähige Windows Sockets-Anwendungen](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Nagle-Algorithmus](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 




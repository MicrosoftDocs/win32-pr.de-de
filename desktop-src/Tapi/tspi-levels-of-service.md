---
description: TAPI dividiert Kommunikationsdienste in Basic, ergänzend und erweitert. Weitere Informationen finden Sie unter TAPI-Dienst Ebenen.
ms.assetid: e2e6b113-b6b0-43a1-ac95-6e8e188a6120
title: TSPI-Dienst Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d829199bdcfce350d82f3c56cbbf9414fc46b35b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529210"
---
# <a name="tspi-levels-of-service"></a>TSPI-Dienst Ebenen

TAPI dividiert Kommunikationsdienste in Basic, ergänzend und erweitert. Weitere Informationen finden Sie [unter TAPI-Dienst Ebenen](./tapi-levels-of-service.md) .

Ein TSP ist erforderlich, um alle grundlegenden Telefoniefunktionen zu implementieren. Die [grundlegenden Telefoniefunktionen von TSPI](tspi-basic-telephony-functions.md) enthalten eine Zusammenfassung dieser Funktionen.

Ergänzende Telefoniefunktionen enthalten Features, die auf modernen PBXs, wie z. b. Hold, Transfer, Conference, Park usw., gefunden werden. Ein Dienstanbieter sollte einen ergänzenden Telefoniedienst nur dann bereitstellen, wenn er die genaue Bedeutung implementieren kann, wie er von TAPI definiert wurde. Andernfalls sollte die Funktion als erweiterter Telefoniedienst bereitgestellt werden. Alle ergänzenden Features sind optional. Ein Dienstanbieter gibt an, welche Dienste er durch Antworten auf Funktionen wie [**TSPI \_ linegetdevcaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) oder [**TSPI \_ linegetaddresscaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)unterstützt. Ein einzelner zusätzlicher Dienst kann aus mehreren Funktionsaufrufen und Nachrichten bestehen. Telefongeräte Dienste sind Teil der ergänzenden Telefonie.

Erweiterte Telefoniedienste ermöglichen es einem Anbieter, gerätespezifische Funktionen zu implementieren. Der Dienstanbieter muss die Erweiterungen mithilfe eines *Erweiterungs Bezeichners* eindeutig identifizieren. Anwendungen rufen und verwenden diesen eindeutigen Bezeichner, um zu bestimmen, welche Erweiterungen der Dienstanbieter unterstützt.

Die Erweiterungen können auf mehrere Hersteller angewendet werden. Spezielle Funktionen und Meldungen wie [**linedevspecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) und [**phonedevspecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) werden in TAPI bereitgestellt. Sie werden verwendet, um die Erweiterung des Funktions Satzes (im Gegensatz zu Enumerationen, Bitflags und Daten Strukturmembern) zuzulassen, die vom Dienstanbieter unterstützt werden. Die Parameter für jede Funktion werden auch vom Dienstanbieter definiert.

Ein Bezeichner wird einem Satz von Erweiterungen (vor der Verteilung) zugewiesen, nicht für jede einzelne Instanz einer Implementierung dieser Erweiterungen. Das Hilfsprogramm "extidgen" in TSPI generiert eindeutige Erweiterungs Bezeichner für Dienstanbieter. Dabei wird eine Ethernet-Adapter Adresse, eine Zufallszahl und die Tageszeit verwendet, um einen Bezeichner zu generieren. Daher ist es äußerst unwahrscheinlich, dass der resultierende Erweiterungs Bezeichner mit einem anderen Dienstanbieter in Konflikt steht. Daher ist es nicht erforderlich, dass Anbieter Erweiterungs-IDs registrieren.

Das Hilfsprogramm "extidgen" generiert keine Erweiterungs Bezeichner, es sei denn, auf dem Computer, auf dem es ausgeführt wird, wird auch NetBIOS oder andere Netzwerk Software ausgeführt.

 

 

---
description: TAPI unterteilt Kommunikationsdienste in Basic, Supplemental und Extended. Weitere Informationen finden Sie unter TAPI-Dienstebenen.
ms.assetid: e2e6b113-b6b0-43a1-ac95-6e8e188a6120
title: TSPI-Dienstebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c72f09f7a076364918815ba5fdb79591f6f5b12382ac2aa529e0859eec53f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012130"
---
# <a name="tspi-levels-of-service"></a>TSPI-Dienstebenen

TAPI unterteilt Kommunikationsdienste in Basic, Supplemental und Extended. Weitere Informationen [finden Sie unter TAPI-Dienstebenen.](./tapi-levels-of-service.md)

Ein TSP ist erforderlich, um alle grundlegenden Telefoniefunktionen zu implementieren. [TSPI Basic-Telefoniefunktionen](tspi-basic-telephony-functions.md) enthält eine Zusammenfassung dieser Funktionen.

Die ergänzende Telefonie umfasst Features, die auf modernen PBX-Dateien zu finden sind, z. B. Hold, Transfer, Conference, Park und so weiter. Ein Dienstanbieter sollte nur dann einen ergänzenden Telefoniedienst bereitstellen, wenn er die genaue Bedeutung gemäß DER TAPI implementieren kann. Falls nicht, sollte das Feature als erweiterter Telefoniedienst bereitgestellt werden. Alle ergänzenden Features sind optional. Ein Dienstanbieter gibt an, welche Dienste er durch Antworten auf Funktionen wie [**TSPI \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) oder [**TSPI \_ lineGetAddressCaps unterstützt.**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps) Ein einzelner ergänzender Dienst kann aus mehreren Funktionsaufrufen und Nachrichten bestehen. Telefon Gerätedienste sind Teil der ergänzenden Telefonie.

Erweiterte Telefoniedienste ermöglichen es einem Anbieter, gerätespezifische Funktionen zu implementieren. Der Dienstanbieter muss die Erweiterungen mithilfe eines *Erweiterungsbezeichners eindeutig identifizieren.* Anwendungen rufen diesen eindeutigen Bezeichner ab und verwenden diesen, um zu bestimmen, welche Erweiterungen der Dienstanbieter unterstützt.

Die Erweiterungen können für mehrere Hersteller gelten. Spezielle Funktionen und Meldungen wie [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) und [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) werden in TAPI bereitgestellt. Sie werden verwendet, um die Erweiterung der Vom Dienstanbieter unterstützten Funktionen zu ermöglichen (im Gegensatz zu Enumerationen, Bitflags und Datenstrukturmembern). Die Parameter für jede Funktion werden auch vom Dienstanbieter definiert.

Ein Bezeichner wird einem Satz von Erweiterungen (vor der Verteilung) zugewiesen, nicht jeder einzelnen Instanz einer Implementierung dieser Erweiterungen. Das EXTIDGEN-Hilfsprogramm in TSPI generiert eindeutige Erweiterungsbezeichner für Dienstanbieter. Es werden eine Ethernet-Adapteradresse, eine Zufallszahl und die Tageszeit zum Generieren eines Bezeichners verwendet. Daher ist es äußerst unwahrscheinlich, dass der resultierende Erweiterungsbezeichner mit anderen Dienstanbietern in Konflikt steht. Daher müssen Anbieter keine Erweiterungsbezeichner registrieren.

Das EXTIDGEN-Hilfsprogramm generiert keine Erweiterungsbezeichner, es sei denn, auf dem Computer, auf dem es ausgeführt wird, wird auch NetBIOS oder andere Netzwerksoftware ausgeführt.

 

 

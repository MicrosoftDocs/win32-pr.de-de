---
description: Erfahren Sie mehr über die TSPI-Versionierung. Im Laufe der Zeit können verschiedene Versionen von TAPI, Anwendungen und Dienstanbietern erstellt werden.
ms.assetid: 994fad0e-5958-4d93-8952-9db2bbe01f44
title: TSPI-Versionierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee1e1d77a33861c7943c8bda063432cd5f212971adae88ef8bdd1eb2c4f88a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117944307"
---
# <a name="tspi-versioning"></a>TSPI-Versionierung

Im Laufe der Zeit können verschiedene Versionen von TAPI, Anwendungen und Dienstanbietern erstellt werden. Diese neuen Versionen können neue Definitionen erstellen, z. B. für neue Features, neue Member in Datenstrukturen und neue Bitfelder. Versionsnummern sind daher erforderlich, um anzugeben, wie verschiedene Datenstrukturen interpretiert werden.

Um eine optimale Interoperabilität verschiedener Versionen von Anwendungen, Versionen von TAPI selbst und Versionen von Dienstanbietern verschiedener Anbieter zu ermöglichen, bietet Microsoft-Telefonie einen einfachen Mechanismus zur Versionsaushandlung für Anwendungen. Es gibt zwei verschiedene Versionen, die von TAPI und dem Telefoniedienstanbieter für jedes Liniengerät vereinbart werden müssen. Die erste ist die Versionsnummer für die SPI für die grundlegende und ergänzende Telefonie, die als *TSPI-Schnittstellenversion bezeichnet wird.* Die andere ist für anbieterspezifische Erweiterungen (sofern verfügbar) und wird als *Erweiterungsversion bezeichnet.* Das Format der Datenstrukturen und Datentypen, die von den grundlegenden und ergänzenden Features von TSPI verwendet werden, wird durch die TSPI-Version definiert, während die Erweiterungsversion das Format der Datenstrukturen bestimmt, die von den herstellerspezifischen Erweiterungen definiert werden.

Diese beiden Arten von Versionsaushandlung werden von zwei verschiedenen Prozeduren verarbeitet: [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) wird zum Aushandeln der TSPI-Schnittstellenversion verwendet, und [**TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) wird verwendet, um die Erweiterungsversion auszuhandeln. Die Erweiterungsversionsaushandlung kann übersprungen werden, wenn Erweiterungen nicht gewünscht sind. Wenn sich diese Bereichseingaben während der Aushandlung überlappen, muss der Dienstanbieter als Ergebnis der Aushandlung einen Wert innerhalb des überlappenden Teils des Bereichs zurückgeben. In der Regel sollte dies der höchste mögliche Wert sein. Wenn sich die Bereiche nicht überschneiden, sind die beiden Parteien inkompatibel, und die Funktion gibt einen Fehler zurück.

Die Ergebnisse einer Aushandlung geben lediglich an, dass der Dienstanbieter bereit ist, eine bestimmte Versionsnummer zu verwenden, aber den Dienstanbieter nicht dazu verpflichten. TapI kann z. B. neu aushandeln, um eine ideale Version zu bestimmen, nachdem eine mögliche Version ausgehandelt wurde. Die TSPI-Schnittstellenversion wird nur dann übertragen, wenn eine Zeile mitHILFE von [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) geöffnet wird, und bleibt erhalten, bis das Gerät geschlossen wird. Für die Erweiterungsversion wird ein Committed erfolgt, wenn die [**TSPI-Funktion \_ lineSelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion) aufgerufen wird, und bleibt erhalten, bis die Auswahl abgebrochen wird, indem die Erweiterungsversion 0 ausgewählt wird.

Die Auswahl der Erweiterungsversion kann oft vorkommen, auch wenn eine Erweiterungsversion in Kraft ist. Da für den Dienstanbieter ein Committed für die Erweiterungsversion gilt, wird der Bereich der unterstützten Versionen auf genau diese Erweiterungsversion eingeengt. Stellen Sie sich beispielsweise einen Dienstanbieter vor, der normalerweise mit den Erweiterungsversionen 1.0 bis 5.5 kompatibel ist. Wenn Version 3.0 in Kraft ist, während ein Aufrufer versucht, eine Version im Bereich von 1.0 bis 5.5 auszuhandeln, gibt die Aushandlung 3.0 zurück.

Da TAPI die Version aushandelt, können Sie ein Upgrade eines Dienstanbieters auf neue Versionen der Schnittstelle durchführen, ohne dass tapI ebenfalls aktualisiert werden muss. Auf ähnliche Weise kann TAPI aktualisiert werden, aber dennoch Ihren älteren Dienstanbieter verwenden.

 

 

---
description: Erfahren Sie mehr über die TSPI-Versionierung. Im Laufe der Zeit können verschiedene Versionen von TAPI, Anwendungen und Dienstanbietern erstellt werden.
ms.assetid: 994fad0e-5958-4d93-8952-9db2bbe01f44
title: TSPI-Versionierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0a0663a1fcc685df8643c634ec627f669aafe8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989235"
---
# <a name="tspi-versioning"></a>TSPI-Versionierung

Im Laufe der Zeit können verschiedene Versionen von TAPI, Anwendungen und Dienstanbietern erstellt werden. Diese neuen Versionen können neue Definitionen erstellen, z. B. für neue Features, neue Member in Datenstrukturen und neue Bitfelder. Versionsnummern sind daher erforderlich, um anzugeben, wie verschiedene Datenstrukturen interpretiert werden sollen.

Um eine optimale Interoperabilität verschiedener Versionen von Anwendungen, TAPI-Versionen selbst und Versionen von Dienstanbietern durch verschiedene Anbieter zu ermöglichen, bietet Microsoft Telefonie einen einfachen Mechanismus zur Versionsaushandlung für Anwendungen. Es gibt zwei verschiedene Versionen, die von TAPI und dem Telefoniedienstanbieter für jedes Liniengerät vereinbart werden müssen. Die erste ist die Versionsnummer für die Spi für die einfache und ergänzende Telefonie, die als *TSPI-Schnittstellenversion* bezeichnet wird. Das andere gilt für anbieterspezifische Erweiterungen, sofern vorhanden, und wird als *Erweiterungsversion* bezeichnet. Das Format der Datenstrukturen und Datentypen, die von den Basic- und Supplementary-Features von TSPI verwendet werden, wird durch die TSPI-Version definiert, während die Erweiterungsversion das Format von Datenstrukturen bestimmt, die von den herstellerspezifischen Erweiterungen definiert werden.

Diese beiden Arten der Versionsaushandlung werden von zwei verschiedenen Prozeduren verarbeitet: [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) wird verwendet, um die TSPI-Schnittstellenversion auszuhandeln, und [**TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) wird verwendet, um die Erweiterungsversion auszuhandeln. Die Erweiterungsversionsaushandlung kann übersprungen werden, wenn erweiterungen nicht gewünscht sind. Wenn sich diese Bereichseingaben während der Aushandlung überschneiden, muss der Dienstanbieter einen Wert innerhalb des überlappenden Teils des Bereichs als Ergebnis der Aushandlung zurückgeben. In der Regel sollte dies der höchste mögliche Wert sein. Wenn sich die Bereiche nicht überschneiden, sind die beiden Parteien inkompatibel, und die Funktion gibt einen Fehler zurück.

Die Ergebnisse einer Aushandlung deuten einfach darauf hin, dass der Dienstanbieter bereit ist, mit einer bestimmten Versionsnummer zu arbeiten, den Dienstanbieter jedoch nicht dazu zu committen. Beispielsweise kann TAPI neu aushandeln, um eine ideale Version zu bestimmen, nachdem eine mögliche Version ausgehandelt wurde. Für die TSPI-Schnittstellenversion wird nur ein Commit ausgeführt, wenn eine Zeile mit [**tspi \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) geöffnet wird und bis zum Schließen des Geräts überdauert wird. Für die Erweiterungsversion wird ein Commit ausgeführt, wenn die [**\_ TSPI-Funktion lineSelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion) aufgerufen wird, und bleibt erhalten, bis die Auswahl durch Auswahl der Erweiterungsversion 0 (null) abgebrochen wird.

Die Auswahl der Erweiterungsversion kann mehrmals erfolgen, auch wenn eine Erweiterungsversion wirksam ist. Da für den Dienstanbieter ein Commit auf die Erweiterungsversion ausgeführt wird, ist der Bereich der unterstützten Versionen auf genau diese Erweiterungsversion beschränkt. Betrachten Sie beispielsweise einen Dienstanbieter, der normalerweise mit den Erweiterungsversionen 1.0 bis 5.5 kompatibel ist. Wenn Version 3.0 in Kraft ist, während ein Aufrufer versucht, eine Version im Bereich von 1.0 bis 5.5 auszuhandeln, gibt die Aushandlung 3.0 zurück.

Da TAPI die Version aushandelt, können Sie ein Upgrade eines Dienstanbieters auf neue Versionen der Schnittstelle durchführen, ohne dass auch TAPI aktualisiert werden muss. Auf ähnliche Weise kann TAPI aktualisiert werden, aber trotzdem Ihren älteren Dienstanbieter verwenden.

 

 

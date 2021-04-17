---
description: Im Laufe der Zeit können verschiedene Versionen von TAPI, Anwendungen und Dienstanbietern erstellt werden.
ms.assetid: 994fad0e-5958-4d93-8952-9db2bbe01f44
title: TSPI-Versionsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe405a629ddc64f76535b33554509b1a6fca81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526813"
---
# <a name="tspi-versioning"></a>TSPI-Versionsverwaltung

Im Laufe der Zeit können verschiedene Versionen von TAPI, Anwendungen und Dienstanbietern erstellt werden. Diese neuen Versionen können neue Definitionen erstellen, z. b. für neue Features, neue Member in Datenstrukturen und neue Bitfelder. Daher sind Versionsnummern erforderlich, um anzugeben, wie verschiedene Datenstrukturen interpretiert werden sollen.

Um eine optimale Interoperabilität verschiedener Versionen von Anwendungen, Versionen von TAPI selbst und Versionen von Dienstanbietern durch verschiedene Lieferanten zu ermöglichen, bietet Microsoft Telefonie einen einfachen Versions Aushandlungs Mechanismus für Anwendungen. Es gibt zwei verschiedene Versionen, die von TAPI und dem Telefoniedienstanbieter für jedes Geräte Gerät vereinbart werden müssen. Der erste ist die Versionsnummer für den grundlegenden und ergänzenden telefonienspi, die als *TSPI-Schnittstellen Version* bezeichnet wird. Die andere gilt für anbieterspezifische Erweiterungen, sofern vorhanden, und wird als *Erweiterungs Version* bezeichnet. Das Format der Datenstrukturen und Datentypen, die von den grundlegenden und ergänzenden Features von TSPI verwendet werden, wird durch die TSPI-Version definiert, während die Erweiterungs Version das Format der Datenstrukturen bestimmt, die von den herstellerspezifischen Erweiterungen definiert werden.

Diese beiden Typen der Versions Aushandlung werden von zwei verschiedenen Prozeduren verarbeitet: [**TSPI \_ linenegotiatetspiversion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) wird zum Aushandeln der TSPI-Schnittstellen Version verwendet, und [**TSPI \_ linenegotiationextversion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) wird zum Aushandeln der Erweiterungs Version verwendet. Die Aushandlung der Erweiterungs Version kann übersprungen werden, wenn Erweiterungen nicht gewünscht werden. Wenn diese Bereiche während der Aushandlung eine Überschneidung haben, muss der Dienstanbieter einen Wert im überlappenden Bereich des Bereichs als Ergebnis der Aushandlung zurückgeben. In der Regel sollte dies der höchstmögliche Wert sein. Wenn sich die Bereiche nicht überlappen, sind die beiden Parteien nicht kompatibel, und die Funktion gibt einen Fehler zurück.

Die Ergebnisse einer Aushandlung geben lediglich an, dass der Dienstanbieter bereit ist, mit einer bestimmten Versionsnummer zu arbeiten, aber keinen Commit für den Dienstanbieter ausführen. Beispielsweise kann TAPI nach einer möglichen Version aushandeln, um eine ideale Version zu ermitteln. Für die TSPI-Schnittstellen Version wird nur dann ein Commit ausgeführt, wenn eine Zeile mit [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) geöffnet wird, bis das Gerät geschlossen wird. Für die Erweiterungs Version wird ein Commit ausgeführt, wenn die [**TSPI- \_ lineselectextversion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion) -Funktion aufgerufen wird, und bleibt erhalten, bis die Auswahl abgebrochen wird.

Die Auswahl der Erweiterungs Version kann mehrmals vorkommen, auch wenn eine Erweiterungs Version wirksam ist. Da der Dienstanbieter ein Commit für die Erweiterungs Version durchführt, schränkt sich der Bereich der unterstützten Versionen auf genau diese Erweiterungs Version ein. Stellen Sie sich beispielsweise einen Dienstanbieter vor, der normalerweise mit den Erweiterungs Versionen 1,0 bis 5,5 kompatibel ist. Wenn Version 3,0 wirksam ist, während ein Aufrufer versucht, eine Version im Bereich von 1,0 bis 5,5 auszuhandeln, gibt die Aushandlung 3,0 zurück.

Da TAPI die-Version aushandiert, können Sie einen Dienstanbieter auf neue Versionen der-Schnittstelle upgraden, ohne dass die TAPI ebenfalls aktualisiert werden muss. Auf ähnliche Weise kann TAPI aktualisiert werden, dennoch sollte trotzdem der ältere Dienstanbieter verwendet werden.

 

 

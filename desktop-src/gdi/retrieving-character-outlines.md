---
description: Sie können die getglyphumriss-Funktion verwenden, um die Kontur eines Symbols aus einer TrueType-Schriftart abzurufen.
ms.assetid: 9b255dfa-3c1d-4707-927d-a2d5f4117f6a
title: Abrufen von Zeichen umrissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 638193632d4992dfb53f29a3dfe66a858b3e1fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978313"
---
# <a name="retrieving-character-outlines"></a>Abrufen von Zeichen umrissen

Sie können die [getglyphumriss](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea) -Funktion verwenden, um die Kontur eines Symbols aus einer TrueType-Schriftart abzurufen. Die von der [**getglyphumriss**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) -Funktion zurückgegebene Symbol Gliederung ist für ein mit dem Raster eingegebenes Symbol. (Ein Raster eingebundenen Symbol wurde so geändert, dass das Bitmap-Bild so weit wie möglich dem ursprünglichen Entwurf des Symbols entspricht.) Wenn Ihre Anwendung eine unveränderte Symbol Gliederung erfordert, fordern Sie die Symbol Gliederung für ein Zeichen in einer Schriftart an, deren Größe gleich den EM-Einheiten der Schriftart ist. (Um eine Schriftart mit dieser Größe zu erstellen, legen Sie den **lfheight** -Member der [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur auf den negativen Wert des Werts des **ntmsizeem** -Members der [newtextmetric](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) -Struktur fest.)

[**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) gibt die Kontur als Bitmap oder als eine Reihe von Polylinien und Splines zurück. Wenn eine Anwendung eine Symbol Gliederung als eine Reihe von Polylinien und Splines abruft, werden die Informationen in einer [ttpolygonheader](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) -Struktur gefolgt von beliebig vielen [ttpolycurve](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) -Strukturen zurückgegeben, um das Symbol zu beschreiben. Alle Punkte werden als [pointfx](/windows/win32/api/wingdi/ns-wingdi-pointfx) -Strukturen zurückgegeben und stellen absolute Positionen dar, nicht Relative Verschiebungen. Der Startpunkt, der vom **pfxstart** -Member der [**ttpolygonheader**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) -Struktur angegeben wird, ist der Punkt, an dem die Kontur für eine Kontur beginnt. Die folgenden [**ttpolycurve**](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) -Strukturen können entweder Polylinie-Datensätze oder Spline-Datensätze sein.

Zum Rendering einer TrueType-Zeichen Gliederung müssen Sie sowohl die Polylinie-als auch die Spline-Datensätze verwenden. Das System kann sowohl Polylinien als auch Splines problemlos Rendering. Jeder Polylinie-und Spline-Datensatz enthält so viele sequenzielle Punkte wie möglich, um die Anzahl der zurückgegebenen Datensätze zu minimieren.

Der in der [**ttpolygonheader**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) -Struktur angegebene Ausgangspunkt ist immer in der Kontur des Symbols. Der angegebene Punkt dient sowohl als Start-als auch als Endpunkt für die Kontur.

Dieser Abschnitt enthält Informationen zu den folgenden Themen.

-   [Polyline-Datensätze](polyline-records.md)
-   [Spline-Datensätze](spline-records.md)

 

 

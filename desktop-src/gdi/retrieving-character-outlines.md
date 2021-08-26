---
description: Sie können die GetGlyphOutline-Funktion verwenden, um die Kontur eines Glyphens aus einer TrueType-Schriftart abzurufen.
ms.assetid: 9b255dfa-3c1d-4707-927d-a2d5f4117f6a
title: Abrufen von Zeichengliederungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3db9b9200f665088096fdecbffc12866668d093c0c4d5ddb4a1612153873e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092650"
---
# <a name="retrieving-character-outlines"></a>Abrufen von Zeichengliederungen

Sie können die [GetGlyphOutline-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea) verwenden, um die Kontur eines Glyphens aus einer TrueType-Schriftart abzurufen. Die von der [**GetGlyphOutline-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) zurückgegebene Glyphengliederung ist für ein an das Raster angepasstes Glyphen vorgesehen. (Ein an das Raster angepasstes Symbol wurde so geändert, dass sein Bitmapbild so genau wie möglich dem ursprünglichen Design des Symbols entspricht.) Wenn Ihre Anwendung eine unveränderte Glyphengliederung erfordert, fordern Sie die Glyphengliederung für ein Zeichen in einer Schriftart an, deren Größe gleich den Em-Einheiten der Schriftart ist. (Um eine Schriftart mit dieser Größe zu erstellen, legen Sie den **lfHeight-Member** der [LOGFONT-Struktur](/windows/win32/api/wingdi/ns-wingdi-logfonta) auf das Negative des Werts des **ntmSizeEM-Elements** der [NEWTEXTMETRIC-Struktur](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) fest.)

[**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) gibt die Kontur als Bitmap oder als Eine Reihe von Polylinien und Splines zurück. Wenn eine Anwendung eine Glyphengliederung als Eine Reihe von Polylinien und Splines abruft, werden die Informationen in einer [TTPOLYGONHEADER-Struktur](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) zurückgegeben, gefolgt von so [vielen TTPOLYCURVE-Strukturen,](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) wie zum Beschreiben des Glyphen erforderlich sind. Alle Punkte werden als [POINTFX-Strukturen](/windows/win32/api/wingdi/ns-wingdi-pointfx) zurückgegeben und stellen absolute Positionen dar, keine relativen Verschiebungen. Der vom **pfxStart-Member** der [**TTPOLYGONHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) angegebene Startpunkt ist der Punkt, an dem die Kontur für eine Kontur beginnt. Die [**folgenden TTPOLYCURVE-Strukturen**](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) können entweder Polyliniendatensätze oder Splinedatensätze sein.

Um eine TrueType-Zeichengliederung zu rendern, müssen Sie sowohl die Polylinien- als auch die Splinedatensätze verwenden. Das System kann sowohl Polylinien als auch Splines problemlos rendern. Jeder Polylinien- und Splinedatensatz enthält so viele sequenzielle Punkte wie möglich, um die Anzahl der zurückgegebenen Datensätze zu minimieren.

Der in der [**TTPOLYGONHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) angegebene Ausgangspunkt befindet sich immer in der Kontur des Glyphen. Der angegebene Punkt dient sowohl als Start- als auch als Endpunkt für die Kontur.

Dieser Abschnitt enthält Informationen zu den folgenden Themen.

-   [Polylinedatensätze](polyline-records.md)
-   [Splinedatensätze](spline-records.md)

 

 

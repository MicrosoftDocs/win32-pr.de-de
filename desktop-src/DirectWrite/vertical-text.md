---
title: Vertikaler Text
description: Ab dem Windows 8 verfügt DirectWrite über eine Reihe neuer APIs, mit denen Sie vertikalen Text in Ihren Apps verwenden können.
ms.assetid: F40A79AE-F7BF-4CAC-9480-1489CD212DA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa5e6626ae77e610c38bfb90def7cfe068db80f7f300f58a734969fb107a46a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632545"
---
# <a name="vertical-text"></a>Vertikaler Text

Ab dem Windows 8 verfügt [DirectWrite](direct-write-portal.md) über eine Reihe neuer APIs, mit denen Sie vertikalen Text in Ihren Apps verwenden können.

## <a name="drawing-vertical-text"></a>Zeichnen von vertikalem Text

Sie können vertikalen Text mit Direct2D zeichnen, indem Sie die [**DrawTextLayout-Methoden**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) verwenden. Um den Text vertikal zu zeichnen, übergeben Sie [**DWRITE \_ READING DIRECTION TOP TO \_ \_ \_ \_ BOTTOM**](/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction) an die [**IDWriteTextFormat::SetReadingDirection-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) und [**DWRITE FLOW DIRECTION RIGHT \_ \_ TO \_ \_ \_ LEFT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction) an die [**IDWriteTextFormatSetFlowDirection-Methode.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection) Anschließend können Sie ein vertikales [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) erstellen und zeichnen.

## <a name="analyzing-character-orientation"></a>Analysieren der Zeichenausrichtung

Jedes Zeichen hat eine bevorzugte Zeichenausrichtung oder die Richtung, in der das Zeichen in einem beliebigen Richtungslayout ausgerichtet werden soll. Beispielsweise werden beim herkömmlichen horizontalen Layout sowohl der lateinische als auch der chinesische Text vertikal ausgerichtet. Andererseits bleibt der chinesische Text in einem vertikalen Layout aufrecht, und der lateinische Text wird um 90 Grad gedreht. Dieser Unterschied bei der Ausrichtung wird hier im Beispiel gesehen.

![Ein Bild von englischem und chinesischem Text in horizontalen und vertikalen Layouts.](images/vertical-text.png)

Um die Ausrichtung des Texts zu bestimmen, müssen Sie die Schnittstellen [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) und [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) implementieren. Quelle und Senke nehmen die Glyphenläufe an und können überprüfen, ob sie vertikal ausgerichtet sind oder nicht.

Nachdem Sie Die Quelle und Senke implementiert haben, rufen Sie die [**AnalyzeVerticalGlyphOrientation-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) auf. In der Beispielbild gibt diese Funktion 3 Läufe zurück: "Englisch", "", und "Englisch".

## <a name="going-from-characters-to-glyphs"></a>Von Zeichen zu Glyphen

Nachdem Sie nun wissen, dass die Ausführung vertikale Glyphen enthält, müssen Sie Zugriff auf diese Glyphen erhalten. Im Beispiel gibt es bisher drei Läufe: eine mit vertikalen Glyphen und zwei ohne. Um von Zeichen zu Glyphen zu überwechseln, rufen Sie [**GetGlyphIndices auf.**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices) Diese Methode gibt die entsprechenden Glyphenindizes für die Zeichen im Beispiel zurück. Da die [**AnalyzeVerticalGlyphOrientation-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) eine Ausführung mit vertikalen Glyphen zurückgibt, müssen Sie [**GetVerticalGlyphVariants**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants)aufrufen, wodurch die vertikal ausgerichteten Glyphen-IDs statt der aktuellen Glyphen-IDs zurückgegeben werden.

## <a name="drawing-text-vertically"></a>Vertikales Zeichnen von Text

Schließlich müssen Sie den Text erstellen und zeichnen. Da Sie den Text vertikal zeichnen, müssen Sie weitere Informationen erhalten, damit der lateinische Text richtig gezeichnet wird. Wenn Sie den gesamten Text entlang der zentralen Baseline zeichnen, scheint der lateinische Text in der Mitte der Zeile zu gleiten. Sie benötigen Zugriff sowohl auf die zentrale als auch auf die romanische Baseline, um den Text richtig auszurichten. Verwenden Sie [**die IDWriteTextAnalyzer1::GetBaseline-Methode,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline) um die numerischen Werte der von Ihnen angegebenen Baselines zu erhalten. Sie können die romische Baseline von der zentralen Baseline subtrahieren, um den Offset zwischen den beiden zu erhalten.

Mit all diesen Informationen können Sie den Text auf dem Bildschirm zeichnen. Rufen Sie zunächst die [**GetGlyphOrientationTransform-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform) mit den Ergebnissen der [**Objekte IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) und [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) auf.

Wenn Sie [Direct2D](rendering-by-using-direct2d.md) verwenden, müssen Sie auch die Welttransformation auf dem Direct2D-Renderziel für vertikales Rendering festlegen.

Rufen Sie abschließend [**drawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) dreimal auf, einmal in jedem Textblock. Auf die beiden Textblöcke, die in Englischer Sprache sind, müssen Sie den Offset anwenden, den wir zwischen den beiden baselines von Roman und Central berechnet haben.

Nun wird der Text in Ihrer App vertikal mit der richtigen Glyphenausrichtung gezeichnet.

 

 
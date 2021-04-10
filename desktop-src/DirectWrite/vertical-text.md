---
title: Vertikaler Text
description: Ab Windows 8 verfügt DirectWrite über eine Reihe neuer APIs, mit denen Sie vertikalen Text in ihren Apps verwenden können.
ms.assetid: F40A79AE-F7BF-4CAC-9480-1489CD212DA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db8788a6be97a55911694942a930e17dc69976a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948785"
---
# <a name="vertical-text"></a>Vertikaler Text

Ab Windows 8 verfügt [DirectWrite](direct-write-portal.md) über eine Reihe neuer APIs, mit denen Sie vertikalen Text in ihren Apps verwenden können.

## <a name="drawing-vertical-text"></a>Zeichnen von vertikaler Text

Mithilfe der [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methoden können Sie vertikalen Text mit Direct2D zeichnen. Um den Text vertikal zu zeichnen, übergeben Sie die [**dwrite- \_ Lese \_ Richtung von \_ oben \_ nach \_ unten**](/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction) an die [**idschreitetextformat:: setreadingdirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) -Methode und die [**dwrite- \_ Fluss \_ Richtung von \_ rechts \_ nach \_ Links**](/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction) zur [**idschreitetextformatsetflowdirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection) -Methode. Anschließend können Sie ein vertikales [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt erstellen und zeichnen.

## <a name="analyzing-character-orientation"></a>Analysieren der Zeichen Ausrichtung

Jedes Zeichen hat eine bevorzugte Zeichen Ausrichtung oder die Richtung, in der das Zeichen in einem direktionalen Layout ausgerichtet werden soll. Beispielsweise werden im herkömmlichen horizontalen Layout sowohl der lateinische Text als auch der chinesische Text vertikal ausgerichtet. Andererseits bleibt der chinesische Text in einem vertikalen Layout nach oben, und der lateinische Text wird um 90 Grad gedreht. Dieser Unterschied bei der Ausrichtung ist im Beispiel hier dargestellt.

![ein Bild aus Englisch und Chinesisch in horizontalen und vertikalen Layouts.](images/vertical-text.png)

Um die Ausrichtung des Texts zu bestimmen, müssen Sie die [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) -und [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) -Schnittstelle implementieren. Die Quelle und die Senke nehmen das Symbol an und überprüfen, ob Sie vertikal ausgerichtet sind oder nicht.

Nachdem Sie die Quelle und die Senke implementiert haben, wird die Methode [**analyzeverticalglyphorientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) aufgerufen. Im Beispiel Bild gibt diese Funktion 3 Ausführungen zurück: "English", "中国" und "English".

## <a name="going-from-characters-to-glyphs"></a>Wechseln von Zeichen zu Glyphen

Nachdem Sie nun wissen, dass der Testlauf vertikale Symbole enthält, benötigen Sie Zugriff auf diese Glyphen. Im obigen Beispiel sind drei Ausführungen vorhanden: eine mit vertikalen Symbolen und zwei ohne. Um von Zeichen zu Glyphen zu wechseln, wird [**getglyphindices**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices)aufgerufen. Diese Methode gibt die entsprechenden Symbol Indizes für die Zeichen im Beispiel zurück. Da die [**analyzeverticalglyphorientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) -Methode einen Testlauf mit vertikalen Symbolen zurückgibt, müssen Sie [**getverticalglyphvarianten**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants)aufrufen, die die vertikal ausgerichteten Symbol-IDs anstelle der aktuellen Symbol-IDs zurückgibt.

## <a name="drawing-text-vertically"></a>Vertikaler Text wird gezeichnet

Schließlich müssen Sie den Text aufstellen und zeichnen. Da Sie den Text vertikal zeichnen, müssen Sie weitere Informationen erhalten, damit der lateinische Text ordnungsgemäß gezeichnet wird. Wenn Sie den gesamten Text entlang der zentralen Baseline zeichnen, wird der lateinische Text in der Mitte der Zeile angezeigt. Sie benötigen Zugriff auf die zentrale und die römische Baseline, um den Text ordnungsgemäß auszurichten. Verwenden Sie die [**IDWriteTextAnalyzer1:: getbaseline**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline) -Methode, um die numerischen Werte der von Ihnen angegebenen Basis Linien zu erhalten. Sie können die römische Baseline von der zentralen Baseline subtrahieren, um den Offset zwischen den beiden zu erhalten.

Mit all diesen Informationen können Sie den Text auf dem Bildschirm zeichnen. Aufrufen Sie zuerst die [**getglyphorientationtransform**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform) -Methode mit den Ergebnissen aus den [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) -und [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) -Objekten.

Wenn Sie [Direct2D](rendering-by-using-direct2d.md) verwenden, müssen Sie auch die Welt Transformation für das Direct2D-Renderziel für das vertikale Rendering festlegen.

Und schließlich wird [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) dreimal aufgerufen, einmal für jeden TextBlock. In den beiden Text Texten, die in englischer Sprache vorliegen, müssen Sie den Offset, den wir zwischen den Grundwerten "Roman" und "Central" berechnet haben, anwenden.

Nun wird der Text in der APP vertikal und mit der korrekten Symbol Ausrichtung gezeichnet.

 

 
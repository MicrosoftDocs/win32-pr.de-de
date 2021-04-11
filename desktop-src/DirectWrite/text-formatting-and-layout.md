---
title: Text Formatierung und Layout
description: DirectWrite stellt zwei Schnittstellen zum Formatieren von Text idschreitetextformat und idwrite tetextlayout bereit.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite, Textformatierung
- DirectWrite, Layout
- DirectWrite, idschreitetextformat-Schnittstelle
- DirectWrite, idschreitetextlayout-Schnittstelle
- Idschreitetextformat-Schnittstelle
- Idschreitetextlayout-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fcf884c15015af2645c32e217d3b4a6b433554
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209331"
---
# <a name="text-formatting-and-layout"></a>Text Formatierung und Layout

[DirectWrite](direct-write-portal.md) stellt zwei Schnittstellen zum Formatieren von Text bereit: [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). **Idwrite tetextformat** beschreibt nur das Format für Text und wird in Fällen verwendet, in denen eine ganze Zeichenfolge dieselbe Schriftgröße, denselben Stil, die gleiche Gewichtung usw. hat. Auf der anderen Seite kapselt **idbeschreib tetextlayout** sowohl eine Text Zeichenfolge als auch die Formatierung für angegebene Bereiche der Zeichenfolge. In diesem Dokument werden die einzelnen Schnittstellen und deren Verwendungsmöglichkeiten beschrieben. Weitere Informationen zur Erstellung und zu Methoden dieser Schnittstellen finden Sie auf den Referenzseiten [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Dieses Dokument enthält die folgenden Teile:

-   [Idschreitetextformat](#modifying-an-idwritetextformat)
    -   [Ändern eines idwrite-Textformat](#modifying-an-idwritetextformat)
-   [Idschreitetextlayout](#idwritetextlayout)
    -   [Formatieren eines Text Bereichs](#formatting-a-range-of-text)
    -   [Renderingoptionen](#rendering-options)

## <a name="idwritetextformat"></a>Idschreitetextformat

Ein [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt wird für Folgendes verwendet:

-   Beschreiben Sie das Format für eine ganze Zeichenfolge beim Rendern. Verwenden Sie zum renderingzeichen einer Zeichenfolge mit mehreren Formaten ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt.
-   Geben Sie beim Erstellen eines [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts das Standardtext Format an.

Zum Erstellen eines [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekts verwenden Sie die [**idschreitefactory::**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) -Methode für das Erstellen von Textformaten und geben die Schriftfamilie, die Schriftart Auflistung, die Schrift Breite, den Schrift Grad (in Dips) und den Gebiets Schema Namen an.

### <a name="modifying-an-idwritetextformat"></a>Ändern eines idwrite-Textformat

Wenn eine [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle erstellt wurde, können einige Werte nicht geändert werden: Schriftfamilie, Auflistung, Gewichtung und Größe sowie der Gebiets Schema Name. Um diese Werte zu ändern, muss ein neues **idschreitetextformat** -Objekt erstellt werden.

Mit [**idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) können Sie die oben aufgeführten Eigenschaften ändern, ohne einen Anding neu zu erstellen. Mit [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) können Sie Formatänderungen vornehmen, die für den gesamten Text gelten, z. b. die Textausrichtung. Wenn Sie die Formatierung auf bestimmte Zeichen Bereiche anwenden möchten, sollten Sie dazu ein **idwrite-Textlayout** verwenden.

[**Idwrite tetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) stellt Methoden zum Festlegen der Textausrichtung, der Fluss Richtung, des inkrementellen Tabstopps, des Zeilen Abstands, der Absatz Ausrichtung, der Kürzung und der Wort Umbruch bereit. Diese Eigenschaften können zu einem beliebigen Zeitpunkt nach der Erstellung des **idschreitetextformat** -Objekts geändert werden.

## <a name="idwritetextlayout"></a>Idschreitetextlayout

Die [**idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle stellt im Gegensatz zu [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)sowohl einen TextBlock als auch die zugeordnete Formatierung dar. **Idschreitetextformat** stellt anfängliche Formatierungsinformationen dar. Im folgenden Beispiel wird gezeigt, wie ein **idwrite-Textlayout** -Objekt mithilfe von [**idwrite tefactory:: up Text Layout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)erstellt wird.


```C++
// Create a text layout using the text format.
if (SUCCEEDED(hr))
{
    RECT rect;
    GetClientRect(hwnd_, &rect); 
    float width  = rect.right  / dpiScaleX_;
    float height = rect.bottom / dpiScaleY_;

    hr = pDWriteFactory_->CreateTextLayout(
        wszText_,      // The string to be laid out and formatted.
        cTextLength_,  // The length of the string.
        pTextFormat_,  // The text format to apply to the string (contains font information, etc).
        width,         // The width of the layout box.
        height,        // The height of the layout box.
        &pTextLayout_  // The IDWriteTextLayout interface pointer.
        );
}

```



Der Text in einem [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt kann nicht geändert werden, nachdem das Objekt erstellt wurde. Um den Text zu ändern, müssen Sie das vorhandene Objekt löschen und ein neues **idschreitetextlayout** -Objekt erstellen.

Sie können ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verwenden, um bestimmte Textbereiche zu formatieren. **Idwrite tetextlayout** bietet auch Methoden zum Ändern des Schrift Stils und der Gewichtung sowie zum Hinzufügen von OpenType-Schriftart Features und Treffer Tests. Weitere Informationen und eine umfassende Liste der Methoden finden Sie auf der Referenzseite zu [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

### <a name="formatting-a-range-of-text"></a>Formatieren eines Text Bereichs

[**Idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) stellt mehrere Methoden zum Formatieren von Textbereichen bereit. Jede dieser Methoden übernimmt eine [**dwrite- \_ Text \_ Bereichs**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) Struktur als Parameter, um die Anfangs Text Position innerhalb der Zeichenfolge und die Länge des zu formatierenden Bereichs anzugeben. Im folgenden Beispiel wird gezeigt, wie die Schrift Breite eines Text Bereichs auf "Bold" festgelegt wird.


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a>Renderingoptionen

Text mit Formatierungen, die nur von einem [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt beschrieben werden, kann mit [Direct2D](../direct2d/direct2d-portal.md)gerendert werden. es gibt jedoch noch einige weitere Optionen zum Rendern eines [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts.

Die durch ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt beschriebene Zeichenfolge kann mithilfe der folgenden Methoden gerendert werden.

1.  [Rendering mithilfe von Direct2D](rendering-by-using-direct2d.md).
2.  [Renderverwendung eines benutzerdefinierten textrenderers](how-to-implement-a-custom-text-renderer.md).
3.  [Rendering zu einer GDI-Oberfläche](render-to-a-gdi-surface.md).

 

 
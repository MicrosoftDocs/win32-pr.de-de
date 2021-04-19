---
title: Textformatierung und Layout
description: DirectWrite bietet zwei Schnittstellen zum Formatieren von Text IDWriteTextFormat und IDWriteTextLayout.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite,Textformatierung
- DirectWrite, Layout
- DirectWrite,IDWriteTextFormat-Schnittstelle
- DirectWrite,IDWriteTextLayout-Schnittstelle
- IDWriteTextFormat-Schnittstelle
- IDWriteTextLayout-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e5790742a3d3caf7f962a6b5e2b3111c626f28
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380754"
---
# <a name="text-formatting-and-layout"></a>Textformatierung und Layout

[DirectWrite](direct-write-portal.md) stellt zwei Schnittstellen zum Formatieren von Text bereit: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). **IDWriteTextFormat** beschreibt nur das Format für Text und wird in Fällen verwendet, in denen eine gesamte Zeichenfolge denselben Schriftgrad, Stil, dieselbe Gewichtung und so weiter haben soll. Andererseits kapselt **IDWriteTextLayout** sowohl eine Textzeichenfolge als auch die Formatierung für angegebene Bereiche der Zeichenfolge. In diesem Dokument werden die einzelnen Schnittstellen und deren Verwendung beschrieben. Weitere Informationen zur Erstellung und den Methoden dieser Schnittstellen finden Sie auf den Referenzseiten [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

Dieses Dokument enthält die folgenden Teile:

-   [Idwritetextformat](#modifying-an-idwritetextformat)
    -   [Ändern eines IDWriteTextFormat](#modifying-an-idwritetextformat)
-   [Idwritetextlayout](#idwritetextlayout)
    -   [Formatieren eines Textbereichs](#formatting-a-range-of-text)
    -   [Renderingoptionen](#rendering-options)

## <a name="idwritetextformat"></a>Idwritetextformat

Ein [**IDWriteTextFormat-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) wird für Dies verwendet:

-   Beschreiben des Formats für eine gesamte Zeichenfolge beim Rendern. Um eine Zeichenfolge mit mehreren Formaten zu rendern, verwenden Sie ein [**IDWriteTextLayout-Objekt.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
-   Geben Sie beim Erstellen eines [**IDWriteTextLayout-Objekts**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) das Standardtextformat an.

Um ein [**IDWriteTextFormat-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) zu erstellen, verwenden Sie die [**IDWriteFactory::CreateTextFormat-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) und geben die Schriftfamilie, die Schriftartauflistung, die Schriftbreite, den Schriftgrad (in DIPs) und den Gebietsschemanamen an.

### <a name="modifying-an-idwritetextformat"></a>Ändern eines IDWriteTextFormat

Nachdem eine [**IDWriteTextFormat-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) erstellt wurde, können einige Werte nicht mehr geändert werden: die Schriftfamilie, die Auflistung, die Gewichtung und die Größe sowie der Gebietsschemaname. Um diese Werte zu ändern, muss ein neues **IDWriteTextFormat-Objekt** erstellt werden.

[**MIT IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) können Sie die oben genannten Eigenschaften ändern, ohne etwas neu erstellen zu müssen. [**MIT IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) können Sie Formatänderungen vornehmen, die für den gesamten Text gelten, z. B. die Textausrichtung. Wenn Sie die Formatierung auf bestimmte Zeichenbereiche anwenden möchten, sollten Sie dazu ein **IDWriteTextLayout** verwenden.

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) stellt Methoden zum Festlegen der Textausrichtung, der Flussrichtung, der inkrementellen Tabstopps, des Zeilenabstands, der Absatzausrichtung, des Kürzens und des Zeilenumbruchs bereit. Diese Eigenschaften können nach der Erstellung des **IDWriteTextFormat-Objekts** jederzeit geändert werden.

## <a name="idwritetextlayout"></a>Idwritetextlayout

Die [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) stellt im Gegensatz zu [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)sowohl einen Textblock als auch die zugeordnete Formatierung dar. **IDWriteTextFormat** stellt Informationen zur anfänglichen Formatierung dar. Das folgende Beispiel zeigt, wie ein **IDWriteTextLayout-Objekt** mit [**idWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)erstellt wird.


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



Der Text in einem [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) kann nach der Erstellung des Objekts nicht mehr geändert werden. Um den Text zu ändern, müssen Sie das vorhandene Objekt löschen und ein neues **IDWriteTextLayout-Objekt** erstellen.

Sie können ein [**IDWriteTextLayout verwenden,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) um angegebene Textbereiche zu formatieren. **IDWriteTextLayout bietet** auch Methoden zum Ändern des Schriftschnitts und der Schriftgewichtung sowie zum Hinzufügen von OpenType-Schriftartfeatures und Treffertests. Weitere Informationen und eine vollständige Liste der Methoden finden Sie auf der [**Referenzseite zu IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

### <a name="formatting-a-range-of-text"></a>Formatieren eines Textbereichs

[**IDWriteTextLayout stellt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mehrere Methoden zum Formatieren von Textbereichen zur Verfügung. Jede dieser Methoden akzeptiert eine [**DWRITE \_ TEXT \_ RANGE-Struktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) als Parameter, um die Anfangstextposition innerhalb der Zeichenfolge und die Länge des zu formatierten Bereichs anzugeben. Das folgende Beispiel zeigt, wie die Schriftgrad eines Textbereichs fett festgelegt wird.


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a>Renderingoptionen

Text mit Formatierung, der nur von einem [**IDWriteTextFormat-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) beschrieben wird, kann mit [Direct2D](../direct2d/direct2d-portal.md)gerendert werden. Es gibt jedoch noch einige weitere Optionen zum Rendern eines [**IDWriteTextLayout-Objekts.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

Die von einem [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) beschriebene Zeichenfolge kann mit den unten angegebenen Methoden gerendert werden.

1.  [Rendern mithilfe von Direct2D](rendering-by-using-direct2d.md).
2.  [Rendern mithilfe eines benutzerdefinierten Textrenderers.](how-to-implement-a-custom-text-renderer.md)
3.  [Rendern sie auf einer GDI-Oberfläche.](render-to-a-gdi-surface.md)

 

 

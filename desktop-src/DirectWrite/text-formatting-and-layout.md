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
# <a name="text-formatting-and-layout"></a><span data-ttu-id="f562d-109">Text Formatierung und Layout</span><span class="sxs-lookup"><span data-stu-id="f562d-109">Text Formatting and Layout</span></span>

<span data-ttu-id="f562d-110">[DirectWrite](direct-write-portal.md) stellt zwei Schnittstellen zum Formatieren von Text bereit: [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="f562d-110">[DirectWrite](direct-write-portal.md) provides two interfaces for formatting text: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="f562d-111">**Idwrite tetextformat** beschreibt nur das Format für Text und wird in Fällen verwendet, in denen eine ganze Zeichenfolge dieselbe Schriftgröße, denselben Stil, die gleiche Gewichtung usw. hat.</span><span class="sxs-lookup"><span data-stu-id="f562d-111">**IDWriteTextFormat** describes only the format for text and is used in cases when an entire string is to be the same font size, style, weight and so on.</span></span> <span data-ttu-id="f562d-112">Auf der anderen Seite kapselt **idbeschreib tetextlayout** sowohl eine Text Zeichenfolge als auch die Formatierung für angegebene Bereiche der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f562d-112">On the other hand, **IDWriteTextLayout** encapsulates both a text string and the formatting for specified ranges of the string.</span></span> <span data-ttu-id="f562d-113">In diesem Dokument werden die einzelnen Schnittstellen und deren Verwendungsmöglichkeiten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f562d-113">This document describes each interface and their uses.</span></span> <span data-ttu-id="f562d-114">Weitere Informationen zur Erstellung und zu Methoden dieser Schnittstellen finden Sie auf den Referenzseiten [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="f562d-114">For more information about the creation and methods of these interfaces, see the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference pages.</span></span>

<span data-ttu-id="f562d-115">Dieses Dokument enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="f562d-115">This document contains the following parts:</span></span>

-   [<span data-ttu-id="f562d-116">Idschreitetextformat</span><span class="sxs-lookup"><span data-stu-id="f562d-116">IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
    -   [<span data-ttu-id="f562d-117">Ändern eines idwrite-Textformat</span><span class="sxs-lookup"><span data-stu-id="f562d-117">Modifying an IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
-   [<span data-ttu-id="f562d-118">Idschreitetextlayout</span><span class="sxs-lookup"><span data-stu-id="f562d-118">IDWriteTextLayout</span></span>](#idwritetextlayout)
    -   [<span data-ttu-id="f562d-119">Formatieren eines Text Bereichs</span><span class="sxs-lookup"><span data-stu-id="f562d-119">Formatting a range of text</span></span>](#formatting-a-range-of-text)
    -   [<span data-ttu-id="f562d-120">Renderingoptionen</span><span class="sxs-lookup"><span data-stu-id="f562d-120">Rendering Options</span></span>](#rendering-options)

## <a name="idwritetextformat"></a><span data-ttu-id="f562d-121">Idschreitetextformat</span><span class="sxs-lookup"><span data-stu-id="f562d-121">IDWriteTextFormat</span></span>

<span data-ttu-id="f562d-122">Ein [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt wird für Folgendes verwendet:</span><span class="sxs-lookup"><span data-stu-id="f562d-122">An [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object is used to:</span></span>

-   <span data-ttu-id="f562d-123">Beschreiben Sie das Format für eine ganze Zeichenfolge beim Rendern.</span><span class="sxs-lookup"><span data-stu-id="f562d-123">Describe the format for an entire string when rendering.</span></span> <span data-ttu-id="f562d-124">Verwenden Sie zum renderingzeichen einer Zeichenfolge mit mehreren Formaten ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f562d-124">To render a string with multiple formats, use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>
-   <span data-ttu-id="f562d-125">Geben Sie beim Erstellen eines [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts das Standardtext Format an.</span><span class="sxs-lookup"><span data-stu-id="f562d-125">Specify the default text format when creating an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="f562d-126">Zum Erstellen eines [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekts verwenden Sie die [**idschreitefactory::**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) -Methode für das Erstellen von Textformaten und geben die Schriftfamilie, die Schriftart Auflistung, die Schrift Breite, den Schrift Grad (in Dips) und den Gebiets Schema Namen an.</span><span class="sxs-lookup"><span data-stu-id="f562d-126">To create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, you use the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method and specify the font family, font collection, font weight, font size (in DIPs), locale name.</span></span>

### <a name="modifying-an-idwritetextformat"></a><span data-ttu-id="f562d-127">Ändern eines idwrite-Textformat</span><span class="sxs-lookup"><span data-stu-id="f562d-127">Modifying an IDWriteTextFormat</span></span>

<span data-ttu-id="f562d-128">Wenn eine [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle erstellt wurde, können einige Werte nicht geändert werden: Schriftfamilie, Auflistung, Gewichtung und Größe sowie der Gebiets Schema Name.</span><span class="sxs-lookup"><span data-stu-id="f562d-128">Once an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is created, some values cannot be changed: the font family, collection, weight, and size, as well the locale name.</span></span> <span data-ttu-id="f562d-129">Um diese Werte zu ändern, muss ein neues **idschreitetextformat** -Objekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f562d-129">To change these values, a new **IDWriteTextFormat** object must be created.</span></span>

<span data-ttu-id="f562d-130">Mit [**idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) können Sie die oben aufgeführten Eigenschaften ändern, ohne einen Anding neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f562d-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) enables you to change the properties above without recreating anthing.</span></span> <span data-ttu-id="f562d-131">Mit [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) können Sie Formatänderungen vornehmen, die für den gesamten Text gelten, z. b. die Textausrichtung.</span><span class="sxs-lookup"><span data-stu-id="f562d-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) enables you to make format changes that apply to the entire text, such as text alignment.</span></span> <span data-ttu-id="f562d-132">Wenn Sie die Formatierung auf bestimmte Zeichen Bereiche anwenden möchten, sollten Sie dazu ein **idwrite-Textlayout** verwenden.</span><span class="sxs-lookup"><span data-stu-id="f562d-132">If you want to apply formatting to specific character ranges, you should do so by using a **IDWriteTextLayout**.</span></span>

<span data-ttu-id="f562d-133">[**Idwrite tetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) stellt Methoden zum Festlegen der Textausrichtung, der Fluss Richtung, des inkrementellen Tabstopps, des Zeilen Abstands, der Absatz Ausrichtung, der Kürzung und der Wort Umbruch bereit.</span><span class="sxs-lookup"><span data-stu-id="f562d-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provides methods to set the text alignment, flow direction, incremental tab stop, line spacing, paragraph alignment, trimming, and word wrapping.</span></span> <span data-ttu-id="f562d-134">Diese Eigenschaften können zu einem beliebigen Zeitpunkt nach der Erstellung des **idschreitetextformat** -Objekts geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f562d-134">These properties can be changed at any time after the creation of the **IDWriteTextFormat** object.</span></span>

## <a name="idwritetextlayout"></a><span data-ttu-id="f562d-135">Idschreitetextlayout</span><span class="sxs-lookup"><span data-stu-id="f562d-135">IDWriteTextLayout</span></span>

<span data-ttu-id="f562d-136">Die [**idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle stellt im Gegensatz zu [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)sowohl einen TextBlock als auch die zugeordnete Formatierung dar.</span><span class="sxs-lookup"><span data-stu-id="f562d-136">The [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface, unlike [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), represents both a block of text and the associated formatting.</span></span> <span data-ttu-id="f562d-137">**Idschreitetextformat** stellt anfängliche Formatierungsinformationen dar.</span><span class="sxs-lookup"><span data-stu-id="f562d-137">**IDWriteTextFormat** represents initial formatting information.</span></span> <span data-ttu-id="f562d-138">Im folgenden Beispiel wird gezeigt, wie ein **idwrite-Textlayout** -Objekt mithilfe von [**idwrite tefactory:: up Text Layout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f562d-138">The following example shows how to create an **IDWriteTextLayout** object using [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span></span>


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



<span data-ttu-id="f562d-139">Der Text in einem [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt kann nicht geändert werden, nachdem das Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f562d-139">The text in an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object cannot be changed once the object is created.</span></span> <span data-ttu-id="f562d-140">Um den Text zu ändern, müssen Sie das vorhandene Objekt löschen und ein neues **idschreitetextlayout** -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="f562d-140">To change the text you must delete the existing object and create a new **IDWriteTextLayout** object.</span></span>

<span data-ttu-id="f562d-141">Sie können ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verwenden, um bestimmte Textbereiche zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="f562d-141">You can use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to format specified ranges of text.</span></span> <span data-ttu-id="f562d-142">**Idwrite tetextlayout** bietet auch Methoden zum Ändern des Schrift Stils und der Gewichtung sowie zum Hinzufügen von OpenType-Schriftart Features und Treffer Tests.</span><span class="sxs-lookup"><span data-stu-id="f562d-142">**IDWriteTextLayout** also provides methods for changing font style and weight, and adding OpenType font features and hit testing.</span></span> <span data-ttu-id="f562d-143">Weitere Informationen und eine umfassende Liste der Methoden finden Sie auf der Referenzseite zu [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="f562d-143">For more information and a complete list of methods see the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference page.</span></span>

### <a name="formatting-a-range-of-text"></a><span data-ttu-id="f562d-144">Formatieren eines Text Bereichs</span><span class="sxs-lookup"><span data-stu-id="f562d-144">Formatting a range of text</span></span>

<span data-ttu-id="f562d-145">[**Idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) stellt mehrere Methoden zum Formatieren von Textbereichen bereit.</span><span class="sxs-lookup"><span data-stu-id="f562d-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) provides several methods to format ranges of text.</span></span> <span data-ttu-id="f562d-146">Jede dieser Methoden übernimmt eine [**dwrite- \_ Text \_ Bereichs**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) Struktur als Parameter, um die Anfangs Text Position innerhalb der Zeichenfolge und die Länge des zu formatierenden Bereichs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f562d-146">Each of these methods takes a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) structure as a parameter to specify the starting text position within the string and the length of the range to format.</span></span> <span data-ttu-id="f562d-147">Im folgenden Beispiel wird gezeigt, wie die Schrift Breite eines Text Bereichs auf "Bold" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f562d-147">The following example shows how to set the font weight of a range of text to bold.</span></span>


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a><span data-ttu-id="f562d-148">Renderingoptionen</span><span class="sxs-lookup"><span data-stu-id="f562d-148">Rendering Options</span></span>

<span data-ttu-id="f562d-149">Text mit Formatierungen, die nur von einem [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt beschrieben werden, kann mit [Direct2D](../direct2d/direct2d-portal.md)gerendert werden. es gibt jedoch noch einige weitere Optionen zum Rendern eines [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f562d-149">Text with formatting described by only a [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="f562d-150">Die durch ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt beschriebene Zeichenfolge kann mithilfe der folgenden Methoden gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="f562d-150">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

1.  <span data-ttu-id="f562d-151">[Rendering mithilfe von Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="f562d-151">[Render using Direct2D](rendering-by-using-direct2d.md).</span></span>
2.  <span data-ttu-id="f562d-152">[Renderverwendung eines benutzerdefinierten textrenderers](how-to-implement-a-custom-text-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="f562d-152">[Render using a custom text renderer](how-to-implement-a-custom-text-renderer.md).</span></span>
3.  <span data-ttu-id="f562d-153">[Rendering zu einer GDI-Oberfläche](render-to-a-gdi-surface.md).</span><span class="sxs-lookup"><span data-stu-id="f562d-153">[Render to a GDI surface](render-to-a-gdi-surface.md).</span></span>

 

 
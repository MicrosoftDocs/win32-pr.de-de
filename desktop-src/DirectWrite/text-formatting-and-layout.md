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
# <a name="text-formatting-and-layout"></a><span data-ttu-id="37c27-109">Textformatierung und Layout</span><span class="sxs-lookup"><span data-stu-id="37c27-109">Text Formatting and Layout</span></span>

<span data-ttu-id="37c27-110">[DirectWrite](direct-write-portal.md) stellt zwei Schnittstellen zum Formatieren von Text bereit: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="37c27-110">[DirectWrite](direct-write-portal.md) provides two interfaces for formatting text: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="37c27-111">**IDWriteTextFormat** beschreibt nur das Format für Text und wird in Fällen verwendet, in denen eine gesamte Zeichenfolge denselben Schriftgrad, Stil, dieselbe Gewichtung und so weiter haben soll.</span><span class="sxs-lookup"><span data-stu-id="37c27-111">**IDWriteTextFormat** describes only the format for text and is used in cases when an entire string is to be the same font size, style, weight and so on.</span></span> <span data-ttu-id="37c27-112">Andererseits kapselt **IDWriteTextLayout** sowohl eine Textzeichenfolge als auch die Formatierung für angegebene Bereiche der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="37c27-112">On the other hand, **IDWriteTextLayout** encapsulates both a text string and the formatting for specified ranges of the string.</span></span> <span data-ttu-id="37c27-113">In diesem Dokument werden die einzelnen Schnittstellen und deren Verwendung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="37c27-113">This document describes each interface and their uses.</span></span> <span data-ttu-id="37c27-114">Weitere Informationen zur Erstellung und den Methoden dieser Schnittstellen finden Sie auf den Referenzseiten [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)</span><span class="sxs-lookup"><span data-stu-id="37c27-114">For more information about the creation and methods of these interfaces, see the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference pages.</span></span>

<span data-ttu-id="37c27-115">Dieses Dokument enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="37c27-115">This document contains the following parts:</span></span>

-   [<span data-ttu-id="37c27-116">Idwritetextformat</span><span class="sxs-lookup"><span data-stu-id="37c27-116">IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
    -   [<span data-ttu-id="37c27-117">Ändern eines IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="37c27-117">Modifying an IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
-   [<span data-ttu-id="37c27-118">Idwritetextlayout</span><span class="sxs-lookup"><span data-stu-id="37c27-118">IDWriteTextLayout</span></span>](#idwritetextlayout)
    -   [<span data-ttu-id="37c27-119">Formatieren eines Textbereichs</span><span class="sxs-lookup"><span data-stu-id="37c27-119">Formatting a range of text</span></span>](#formatting-a-range-of-text)
    -   [<span data-ttu-id="37c27-120">Renderingoptionen</span><span class="sxs-lookup"><span data-stu-id="37c27-120">Rendering Options</span></span>](#rendering-options)

## <a name="idwritetextformat"></a><span data-ttu-id="37c27-121">Idwritetextformat</span><span class="sxs-lookup"><span data-stu-id="37c27-121">IDWriteTextFormat</span></span>

<span data-ttu-id="37c27-122">Ein [**IDWriteTextFormat-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) wird für Dies verwendet:</span><span class="sxs-lookup"><span data-stu-id="37c27-122">An [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object is used to:</span></span>

-   <span data-ttu-id="37c27-123">Beschreiben des Formats für eine gesamte Zeichenfolge beim Rendern.</span><span class="sxs-lookup"><span data-stu-id="37c27-123">Describe the format for an entire string when rendering.</span></span> <span data-ttu-id="37c27-124">Um eine Zeichenfolge mit mehreren Formaten zu rendern, verwenden Sie ein [**IDWriteTextLayout-Objekt.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)</span><span class="sxs-lookup"><span data-stu-id="37c27-124">To render a string with multiple formats, use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>
-   <span data-ttu-id="37c27-125">Geben Sie beim Erstellen eines [**IDWriteTextLayout-Objekts**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) das Standardtextformat an.</span><span class="sxs-lookup"><span data-stu-id="37c27-125">Specify the default text format when creating an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="37c27-126">Um ein [**IDWriteTextFormat-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) zu erstellen, verwenden Sie die [**IDWriteFactory::CreateTextFormat-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) und geben die Schriftfamilie, die Schriftartauflistung, die Schriftbreite, den Schriftgrad (in DIPs) und den Gebietsschemanamen an.</span><span class="sxs-lookup"><span data-stu-id="37c27-126">To create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, you use the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method and specify the font family, font collection, font weight, font size (in DIPs), locale name.</span></span>

### <a name="modifying-an-idwritetextformat"></a><span data-ttu-id="37c27-127">Ändern eines IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="37c27-127">Modifying an IDWriteTextFormat</span></span>

<span data-ttu-id="37c27-128">Nachdem eine [**IDWriteTextFormat-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) erstellt wurde, können einige Werte nicht mehr geändert werden: die Schriftfamilie, die Auflistung, die Gewichtung und die Größe sowie der Gebietsschemaname.</span><span class="sxs-lookup"><span data-stu-id="37c27-128">Once an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is created, some values cannot be changed: the font family, collection, weight, and size, as well the locale name.</span></span> <span data-ttu-id="37c27-129">Um diese Werte zu ändern, muss ein neues **IDWriteTextFormat-Objekt** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="37c27-129">To change these values, a new **IDWriteTextFormat** object must be created.</span></span>

<span data-ttu-id="37c27-130">[**MIT IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) können Sie die oben genannten Eigenschaften ändern, ohne etwas neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="37c27-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) enables you to change the properties above without recreating anything.</span></span> <span data-ttu-id="37c27-131">[**MIT IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) können Sie Formatänderungen vornehmen, die für den gesamten Text gelten, z. B. die Textausrichtung.</span><span class="sxs-lookup"><span data-stu-id="37c27-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) enables you to make format changes that apply to the entire text, such as text alignment.</span></span> <span data-ttu-id="37c27-132">Wenn Sie die Formatierung auf bestimmte Zeichenbereiche anwenden möchten, sollten Sie dazu ein **IDWriteTextLayout** verwenden.</span><span class="sxs-lookup"><span data-stu-id="37c27-132">If you want to apply formatting to specific character ranges, you should do so by using a **IDWriteTextLayout**.</span></span>

<span data-ttu-id="37c27-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) stellt Methoden zum Festlegen der Textausrichtung, der Flussrichtung, der inkrementellen Tabstopps, des Zeilenabstands, der Absatzausrichtung, des Kürzens und des Zeilenumbruchs bereit.</span><span class="sxs-lookup"><span data-stu-id="37c27-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provides methods to set the text alignment, flow direction, incremental tab stop, line spacing, paragraph alignment, trimming, and word wrapping.</span></span> <span data-ttu-id="37c27-134">Diese Eigenschaften können nach der Erstellung des **IDWriteTextFormat-Objekts** jederzeit geändert werden.</span><span class="sxs-lookup"><span data-stu-id="37c27-134">These properties can be changed at any time after the creation of the **IDWriteTextFormat** object.</span></span>

## <a name="idwritetextlayout"></a><span data-ttu-id="37c27-135">Idwritetextlayout</span><span class="sxs-lookup"><span data-stu-id="37c27-135">IDWriteTextLayout</span></span>

<span data-ttu-id="37c27-136">Die [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) stellt im Gegensatz zu [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)sowohl einen Textblock als auch die zugeordnete Formatierung dar.</span><span class="sxs-lookup"><span data-stu-id="37c27-136">The [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface, unlike [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), represents both a block of text and the associated formatting.</span></span> <span data-ttu-id="37c27-137">**IDWriteTextFormat** stellt Informationen zur anfänglichen Formatierung dar.</span><span class="sxs-lookup"><span data-stu-id="37c27-137">**IDWriteTextFormat** represents initial formatting information.</span></span> <span data-ttu-id="37c27-138">Das folgende Beispiel zeigt, wie ein **IDWriteTextLayout-Objekt** mit [**idWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="37c27-138">The following example shows how to create an **IDWriteTextLayout** object using [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span></span>


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



<span data-ttu-id="37c27-139">Der Text in einem [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) kann nach der Erstellung des Objekts nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="37c27-139">The text in an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object cannot be changed once the object is created.</span></span> <span data-ttu-id="37c27-140">Um den Text zu ändern, müssen Sie das vorhandene Objekt löschen und ein neues **IDWriteTextLayout-Objekt** erstellen.</span><span class="sxs-lookup"><span data-stu-id="37c27-140">To change the text you must delete the existing object and create a new **IDWriteTextLayout** object.</span></span>

<span data-ttu-id="37c27-141">Sie können ein [**IDWriteTextLayout verwenden,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) um angegebene Textbereiche zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="37c27-141">You can use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to format specified ranges of text.</span></span> <span data-ttu-id="37c27-142">**IDWriteTextLayout bietet** auch Methoden zum Ändern des Schriftschnitts und der Schriftgewichtung sowie zum Hinzufügen von OpenType-Schriftartfeatures und Treffertests.</span><span class="sxs-lookup"><span data-stu-id="37c27-142">**IDWriteTextLayout** also provides methods for changing font style and weight, and adding OpenType font features and hit testing.</span></span> <span data-ttu-id="37c27-143">Weitere Informationen und eine vollständige Liste der Methoden finden Sie auf der [**Referenzseite zu IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)</span><span class="sxs-lookup"><span data-stu-id="37c27-143">For more information and a complete list of methods see the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference page.</span></span>

### <a name="formatting-a-range-of-text"></a><span data-ttu-id="37c27-144">Formatieren eines Textbereichs</span><span class="sxs-lookup"><span data-stu-id="37c27-144">Formatting a range of text</span></span>

<span data-ttu-id="37c27-145">[**IDWriteTextLayout stellt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mehrere Methoden zum Formatieren von Textbereichen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="37c27-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) provides several methods to format ranges of text.</span></span> <span data-ttu-id="37c27-146">Jede dieser Methoden akzeptiert eine [**DWRITE \_ TEXT \_ RANGE-Struktur**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) als Parameter, um die Anfangstextposition innerhalb der Zeichenfolge und die Länge des zu formatierten Bereichs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="37c27-146">Each of these methods takes a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) structure as a parameter to specify the starting text position within the string and the length of the range to format.</span></span> <span data-ttu-id="37c27-147">Das folgende Beispiel zeigt, wie die Schriftgrad eines Textbereichs fett festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="37c27-147">The following example shows how to set the font weight of a range of text to bold.</span></span>


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a><span data-ttu-id="37c27-148">Renderingoptionen</span><span class="sxs-lookup"><span data-stu-id="37c27-148">Rendering Options</span></span>

<span data-ttu-id="37c27-149">Text mit Formatierung, der nur von einem [**IDWriteTextFormat-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) beschrieben wird, kann mit [Direct2D](../direct2d/direct2d-portal.md)gerendert werden. Es gibt jedoch noch einige weitere Optionen zum Rendern eines [**IDWriteTextLayout-Objekts.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)</span><span class="sxs-lookup"><span data-stu-id="37c27-149">Text with formatting described by only a [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="37c27-150">Die von einem [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) beschriebene Zeichenfolge kann mit den unten angegebenen Methoden gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="37c27-150">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

1.  <span data-ttu-id="37c27-151">[Rendern mithilfe von Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="37c27-151">[Render using Direct2D](rendering-by-using-direct2d.md).</span></span>
2.  <span data-ttu-id="37c27-152">[Rendern mithilfe eines benutzerdefinierten Textrenderers.](how-to-implement-a-custom-text-renderer.md)</span><span class="sxs-lookup"><span data-stu-id="37c27-152">[Render using a custom text renderer](how-to-implement-a-custom-text-renderer.md).</span></span>
3.  <span data-ttu-id="37c27-153">[Rendern sie auf einer GDI-Oberfläche.](render-to-a-gdi-surface.md)</span><span class="sxs-lookup"><span data-stu-id="37c27-153">[Render to a GDI surface](render-to-a-gdi-surface.md).</span></span>

 

 

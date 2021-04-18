---
title: Tutorial für den Einstieg in DirectWrite
description: In diesem Dokument erfahren Sie, wie Sie mithilfe von DirectWrite und Direct2D einfachen Text erstellen, der ein einzelnes Format enthält, und dann Text mit mehreren Formaten.
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite, Tutorial
- Tutorial zu den ersten Schritten mit DirectWrite
- DirectWrite, Direct2D
- Direct2D
- DirectWrite, idschreitetextlayout-Schnittstelle
- Idschreitetextlayout-Schnittstelle
- DirectWrite, idschreitetypografie-Schnittstelle
- Idschreitetypografieschnittstelle
- DirectWrite, idschreitetextformat-Schnittstelle
- Idschreitetextformat-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315861"
---
# <a name="tutorial-getting-started-with-directwrite"></a><span data-ttu-id="4485d-113">Tutorial: Einstieg in DirectWrite</span><span class="sxs-lookup"><span data-stu-id="4485d-113">Tutorial: Getting Started with DirectWrite</span></span>

<span data-ttu-id="4485d-114">In diesem Dokument erfahren Sie, wie Sie mithilfe von [DirectWrite](direct-write-portal.md) und [Direct2D](rendering-by-using-direct2d.md) einfachen Text erstellen, der ein einzelnes Format enthält, und dann Text mit mehreren Formaten.</span><span class="sxs-lookup"><span data-stu-id="4485d-114">This document shows you how to use [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to create simple text that contains a single format, and then text that contains multiple formats.</span></span>

<span data-ttu-id="4485d-115">Dieses Tutorial enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="4485d-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="4485d-116">Quellcode</span><span class="sxs-lookup"><span data-stu-id="4485d-116">Source Code</span></span>](#source-code)
-   [<span data-ttu-id="4485d-117">Zeichnen von einfachem Text</span><span class="sxs-lookup"><span data-stu-id="4485d-117">Drawing Simple Text</span></span>](#drawing-simple-text)
    -   [<span data-ttu-id="4485d-118">Teil 1: Deklarieren von DirectWrite-und Direct2D-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4485d-118">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>](#part-1-declare-directwrite-and-direct2d-resources)
    -   [<span data-ttu-id="4485d-119">Teil 2: Erstellen von geräteunabhängigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4485d-119">Part 2: Create Device Independent Resources.</span></span>](#part-2-create-device-independent-resources)
    -   [<span data-ttu-id="4485d-120">Teil 3: Erstellen von Device-Dependent Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4485d-120">Part 3: Create Device-Dependent Resources.</span></span>](#part-3-create-device-dependent-resources)
    -   [<span data-ttu-id="4485d-121">Teil 4: Zeichnen von Text mithilfe der Direct2D DrawText-Methode.</span><span class="sxs-lookup"><span data-stu-id="4485d-121">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [<span data-ttu-id="4485d-122">Teil 5: Rendering der Fenster Inhalte mithilfe von Direct2D</span><span class="sxs-lookup"><span data-stu-id="4485d-122">Part 5: Render the Window Contents Using Direct2D</span></span>](#part-5-render-the-window-contents-using-direct2d)
-   [<span data-ttu-id="4485d-123">Zeichnen von Text mit mehreren Formaten.</span><span class="sxs-lookup"><span data-stu-id="4485d-123">Drawing Text with Multiple Formats.</span></span>](#drawing-text-with-multiple-formats)
    -   [<span data-ttu-id="4485d-124">Teil 1: Erstellen einer idschreitetextlayout-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4485d-124">Part 1: Create an IDWriteTextLayout Interface.</span></span>](#part-1-create-an-idwritetextlayout-interface)
    -   [<span data-ttu-id="4485d-125">Teil 2: Anwenden der Formatierung mit idbeschreib tetextlayout.</span><span class="sxs-lookup"><span data-stu-id="4485d-125">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>](#part-2-applying-formatting-with-idwritetextlayout)
    -   [<span data-ttu-id="4485d-126">Teil 3: Hinzufügen von typografischen Features mit idbeschreib tetypografie.</span><span class="sxs-lookup"><span data-stu-id="4485d-126">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>](#part-3-adding-typographic-features-with-idwritetypography)
    -   [<span data-ttu-id="4485d-127">Teil 4: Zeichnen von Text mithilfe der Direct2D drawtextlayout-Methode.</span><span class="sxs-lookup"><span data-stu-id="4485d-127">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a><span data-ttu-id="4485d-128">Quellcode</span><span class="sxs-lookup"><span data-stu-id="4485d-128">Source Code</span></span>

<span data-ttu-id="4485d-129">Der in dieser Übersicht angezeigte Quellcode stammt aus dem [DirectWrite-Hallo Welt Beispiel](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="4485d-129">The source code shown in this overview is taken from the [DirectWrite Hello World sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="4485d-130">Jeder Teil ist in einer separaten Klasse (SimpleText und multiformattedtext) implementiert und wird in einem separaten untergeordneten Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4485d-130">Each part is implemented in a separate class (SimpleText and MultiformattedText) and is displayed in a separate child window.</span></span> <span data-ttu-id="4485d-131">Jede Klasse stellt ein Microsoft Win32-Fenster dar.</span><span class="sxs-lookup"><span data-stu-id="4485d-131">Each class represents a Microsoft Win32 window.</span></span> <span data-ttu-id="4485d-132">Neben der *WndProc* -Methode enthält jede Klasse die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="4485d-132">In addition to the *WndProc* method, each class contains the following methods:</span></span>



| <span data-ttu-id="4485d-133">Funktion</span><span class="sxs-lookup"><span data-stu-id="4485d-133">Function</span></span>                              | <span data-ttu-id="4485d-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4485d-134">Description</span></span>                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4485d-135">**CreateDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="4485d-135">**CreateDeviceIndependentResources**</span></span>  | <span data-ttu-id="4485d-136">Erstellt Ressourcen, die Geräte unabhängig sind, sodass Sie überall wieder verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4485d-136">Creates resources that are device independent, so they can be reused anywhere.</span></span>                      |
| <span data-ttu-id="4485d-137">**Verwerfen von "Verwerfen von Ressourcen"**</span><span class="sxs-lookup"><span data-stu-id="4485d-137">**DiscardDeviceIndependentResources**</span></span> | <span data-ttu-id="4485d-138">Gibt die geräteunabhängigen Ressourcen frei, wenn Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="4485d-138">Releases the device-independent resources after they are no longer needed.</span></span>                          |
| <span data-ttu-id="4485d-139">**CreateDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="4485d-139">**CreateDeviceResources**</span></span>             | <span data-ttu-id="4485d-140">Erstellt Ressourcen, z. b. Pinsel und Renderziele, die an ein bestimmtes Gerät gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="4485d-140">Creates resources, such as brushes and render targets, that are tied to a particular device.</span></span>        |
| <span data-ttu-id="4485d-141">**Verwerfen von Datenquellen**</span><span class="sxs-lookup"><span data-stu-id="4485d-141">**DiscardDeviceResources**</span></span>            | <span data-ttu-id="4485d-142">Gibt die geräteabhängigen Ressourcen frei, wenn Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="4485d-142">Releases the device-dependent resources after they are no longer needed.</span></span>                            |
| <span data-ttu-id="4485d-143">**DrawD2DContent**</span><span class="sxs-lookup"><span data-stu-id="4485d-143">**DrawD2DContent**</span></span>                    | <span data-ttu-id="4485d-144">Verwendet [Direct2D](../direct2d/direct2d-portal.md) zum Rendering auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="4485d-144">Uses [Direct2D](../direct2d/direct2d-portal.md) to render to the screen.</span></span>                              |
| <span data-ttu-id="4485d-145">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="4485d-145">**DrawText**</span></span>                          | <span data-ttu-id="4485d-146">Zeichnet die Text Zeichenfolge mithilfe von [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="4485d-146">Draws the text string by using [Direct2D](../direct2d/direct2d-portal.md).</span></span>                            |
| <span data-ttu-id="4485d-147">**OnResize**</span><span class="sxs-lookup"><span data-stu-id="4485d-147">**OnResize**</span></span>                          | <span data-ttu-id="4485d-148">Ändert die Größe des [Direct2D](../direct2d/direct2d-portal.md) -Renderziels, wenn die Fenstergröße geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4485d-148">Resizes the [Direct2D](../direct2d/direct2d-portal.md) render target when the window size is changed.</span></span> |



 

<span data-ttu-id="4485d-149">Sie können das bereitgestellte Beispiel verwenden oder die folgenden Anweisungen befolgen, um [DirectWrite](direct-write-portal.md) und [Direct2D](rendering-by-using-direct2d.md) ihrer eigenen Win32-Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4485d-149">You can use the sample provided, or use the instructions that follow to add [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to your own Win32 application.</span></span> <span data-ttu-id="4485d-150">Weitere Informationen zum Beispiel und den zugehörigen Projektdateien finden Sie im [DirectWrite-HelloWorld-Beispiel](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="4485d-150">For more information about the sample and the associated project files, see the [DirectWriteHelloWorld sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="drawing-simple-text"></a><span data-ttu-id="4485d-151">Zeichnen von einfachem Text</span><span class="sxs-lookup"><span data-stu-id="4485d-151">Drawing Simple Text</span></span>

<span data-ttu-id="4485d-152">In diesem Abschnitt wird gezeigt, wie Sie mithilfe von [DirectWrite](direct-write-portal.md) und [Direct2D](../direct2d/direct2d-portal.md) einfachen Text mit einem einzelnen Format renderz, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4485d-152">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render simple text that has a single format, as shown in the following screen shot.</span></span>

![Screenshot von "Hello World using DirectWrite!"](images/simplecropped.png)

<span data-ttu-id="4485d-155">Zum Zeichnen von einfachem Text auf dem Bildschirm sind vier Komponenten erforderlich:</span><span class="sxs-lookup"><span data-stu-id="4485d-155">Drawing simple text to the screen requires four components:</span></span>

-   <span data-ttu-id="4485d-156">Eine Zeichenfolge, die dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4485d-156">A character string to render.</span></span>
-   <span data-ttu-id="4485d-157">Eine Instanz von [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="4485d-157">An instance of [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span>
-   <span data-ttu-id="4485d-158">Die Abmessungen des Bereichs, in dem der Text enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="4485d-158">The dimensions of the area to contain the text.</span></span>
-   <span data-ttu-id="4485d-159">Ein Objekt, das den Text erzeugen kann.</span><span class="sxs-lookup"><span data-stu-id="4485d-159">An object that can render the text.</span></span> <span data-ttu-id="4485d-160">In diesem Tutorial.</span><span class="sxs-lookup"><span data-stu-id="4485d-160">In this tutorial.</span></span> <span data-ttu-id="4485d-161">Sie verwenden ein [Direct2D](../direct2d/direct2d-portal.md) -Renderziel.</span><span class="sxs-lookup"><span data-stu-id="4485d-161">you use a [Direct2D](../direct2d/direct2d-portal.md) render target.</span></span>

<span data-ttu-id="4485d-162">Die [**idwrite Test Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle beschreibt den Schriftfamilien Namen, die Größe, die Gewichtung, den Stil und die Streckung, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen.</span><span class="sxs-lookup"><span data-stu-id="4485d-162">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface describes the font-family name, size, weight, style, and stretch used to format text, and it describes locale information.</span></span> <span data-ttu-id="4485d-163">**Idbeschreib tetextformat** definiert auch Methoden zum Festlegen und erhalten der folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4485d-163">**IDWriteTextFormat** also defines methods for setting and getting the following properties:</span></span>

-   <span data-ttu-id="4485d-164">Der Zeilenabstand.</span><span class="sxs-lookup"><span data-stu-id="4485d-164">The line spacing.</span></span>
-   <span data-ttu-id="4485d-165">Die Textausrichtung relativ zum linken und rechten Rand des layoutfelds.</span><span class="sxs-lookup"><span data-stu-id="4485d-165">The text alignment relative to the left and right edges of the layout box.</span></span>
-   <span data-ttu-id="4485d-166">Die Absatz Ausrichtung relativ zum oberen und unteren Rand des layoutfelds.</span><span class="sxs-lookup"><span data-stu-id="4485d-166">The paragraph alignment relative to the top and bottom of the layout box.</span></span>
-   <span data-ttu-id="4485d-167">Die Leserichtung.</span><span class="sxs-lookup"><span data-stu-id="4485d-167">The reading direction.</span></span>
-   <span data-ttu-id="4485d-168">Der Text, der die Granularität für Text beschneidet, der das layoutfeld überschreitet.</span><span class="sxs-lookup"><span data-stu-id="4485d-168">The text trimming granularity for text that overflows the layout box.</span></span>
-   <span data-ttu-id="4485d-169">Der inkrementelle Tabstopp.</span><span class="sxs-lookup"><span data-stu-id="4485d-169">The incremental tab stop.</span></span>
-   <span data-ttu-id="4485d-170">Die Absatz Fluss Richtung.</span><span class="sxs-lookup"><span data-stu-id="4485d-170">The paragraph flow direction.</span></span>

<span data-ttu-id="4485d-171">Die [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle ist zum Zeichnen von Text erforderlich, der beide in diesem Dokument beschriebenen Prozesse verwendet.</span><span class="sxs-lookup"><span data-stu-id="4485d-171">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is required for drawing text that uses both of the processes described in this document .</span></span>

<span data-ttu-id="4485d-172">Bevor Sie ein [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt oder ein anderes [DirectWrite](direct-write-portal.md) -Objekt erstellen können, benötigen Sie eine [**idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="4485d-172">Before you can create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, or any other [DirectWrite](direct-write-portal.md) object, you need an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) instance.</span></span> <span data-ttu-id="4485d-173">Sie verwenden eine **idwrite-Factory** , um **idschreitetextformat** -Instanzen und andere DirectWrite-Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4485d-173">You use an **IDWriteFactory** to create **IDWriteTextFormat** instances and other DirectWrite objects.</span></span> <span data-ttu-id="4485d-174">Verwenden Sie zum Abrufen einer Factory-Instanz die [**dschreitekreatefactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4485d-174">To obtain a factory instance, use the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function.</span></span>

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a><span data-ttu-id="4485d-175">Teil 1: Deklarieren von DirectWrite-und Direct2D-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4485d-175">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>

<span data-ttu-id="4485d-176">In diesem Teil deklarieren Sie die Objekte, die Sie später zum Erstellen und Anzeigen von Text als private Datenmember ihrer Klasse verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="4485d-176">In this part, you declare the objects that you will use later for creating and displaying text as private data members of your class.</span></span> <span data-ttu-id="4485d-177">Alle Schnittstellen, Funktionen und Datentypen für [DirectWrite](direct-write-portal.md) werden in der *dwrite. h* -Header Datei deklariert, und die für [Direct2D](../direct2d/direct2d-portal.md) sind in *d2d1. h deklariert.* Wenn Sie dies noch nicht getan haben, schließen Sie diese Header in Ihr Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="4485d-177">All of the interfaces, functions, and datatypes for [DirectWrite](direct-write-portal.md) are declared in the *dwrite.h* header file, and those for [Direct2D](../direct2d/direct2d-portal.md) are declared in the *d2d1.h*; if you haven't already done this, include these headers in your project.</span></span>

1.  <span data-ttu-id="4485d-178">Deklarieren Sie in der Klassen Header Datei (SimpleText. h) Zeiger auf die Schnittstellen [**idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) und [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) als private Member.</span><span class="sxs-lookup"><span data-stu-id="4485d-178">In your class header file (SimpleText.h), declare pointers to [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) and [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interfaces as private members.</span></span>
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  <span data-ttu-id="4485d-179">Deklarieren Sie Member, um die zu Rendering Ende Text Zeichenfolge und die Länge der Zeichenfolge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4485d-179">Declare members to hold the text string to render and the length of the string.</span></span>
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  <span data-ttu-id="4485d-180">Deklarieren Sie Zeiger auf [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)-, [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)-und [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Schnittstellen zum Rendern des Texts mit [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="4485d-180">Declare pointers to [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), and [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces for rendering the text with [Direct2D](../direct2d/direct2d-portal.md).</span></span>
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a><span data-ttu-id="4485d-181">Teil 2: Erstellen von geräteunabhängigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4485d-181">Part 2: Create Device Independent Resources.</span></span>

<span data-ttu-id="4485d-182">[Direct2D](rendering-by-using-direct2d.md) bietet zwei Arten von Ressourcen: Geräte abhängige Ressourcen und geräteunabhängige Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4485d-182">[Direct2D](rendering-by-using-direct2d.md) provides two types of resources: device-dependent resources and device-independent resources.</span></span> <span data-ttu-id="4485d-183">Geräte abhängige Ressourcen sind einem renderinggerät zugeordnet und funktionieren nicht mehr, wenn das Gerät entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4485d-183">Device-dependent resources are associated with a rendering device and no longer function if that device is removed.</span></span> <span data-ttu-id="4485d-184">Geräteunabhängige Ressourcen können auf der anderen Seite den Geltungsbereich ihrer Anwendung überdauern.</span><span class="sxs-lookup"><span data-stu-id="4485d-184">Device-independent resources, on the other hand, can last for the scope of your application.</span></span>

<span data-ttu-id="4485d-185">[DirectWrite](direct-write-portal.md) -Ressourcen sind Geräte unabhängig.</span><span class="sxs-lookup"><span data-stu-id="4485d-185">[DirectWrite](direct-write-portal.md) resources are device-independent.</span></span>

<span data-ttu-id="4485d-186">In diesem Abschnitt erstellen Sie die geräteunabhängigen Ressourcen, die von Ihrer Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4485d-186">In this section, you create the device-independent resources that are used by your application.</span></span> <span data-ttu-id="4485d-187">Diese Ressourcen müssen durch einen Aufrufder **releasemethode** der-Schnittstelle freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4485d-187">These resources must be freed with a call to the **Release** method of the interface.</span></span>

<span data-ttu-id="4485d-188">Einige der verwendeten Ressourcen müssen nur einmal erstellt werden und sind nicht an ein Gerät gebunden.</span><span class="sxs-lookup"><span data-stu-id="4485d-188">Some of the resources that are used have to be created only one time and are not tied to a device.</span></span> <span data-ttu-id="4485d-189">Die Initialisierung für diese Ressourcen wird in der *SimpleText:: createdeviceindependentresources* -Methode abgelegt, die beim Initialisieren der-Klasse aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4485d-189">The initialization for these resources is put in the *SimpleText::CreateDeviceIndependentResources* method, which is called when initializing the class.</span></span>

1.  <span data-ttu-id="4485d-190">Rufen Sie innerhalb der *SimpleText:: createdeviceindependentresources* -Methode in der Klassen Implementierungs Datei (SimpleText. cpp) die [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) -Funktion auf, um eine [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Schnittstelle zu erstellen, die die Stamm-factoryschnittstelle für alle [Direct2D](../direct2d/direct2d-portal.md) -Objekte ist.</span><span class="sxs-lookup"><span data-stu-id="4485d-190">Inside the *SimpleText::CreateDeviceIndependentResources* method in the class implementation file (SimpleText.cpp), call the [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) function to create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface, which is the root factory interface for all [Direct2D](../direct2d/direct2d-portal.md) objects.</span></span> <span data-ttu-id="4485d-191">Sie verwenden dieselbe Factory, um andere Direct2D-Ressourcen zu instanziieren.</span><span class="sxs-lookup"><span data-stu-id="4485d-191">You use the same factory to instantiate other Direct2D resources.</span></span>
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  <span data-ttu-id="4485d-192">Rufen Sie die [**dbeschreib tekreatefactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) -Funktion auf, um eine [**idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Schnittstelle zu erstellen, die die stammfactoringschnittstelle für alle [DirectWrite](direct-write-portal.md) -Objekte ist.</span><span class="sxs-lookup"><span data-stu-id="4485d-192">Call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function to create an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface, which is the root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span> <span data-ttu-id="4485d-193">Sie verwenden dieselbe Factory, um andere DirectWrite-Ressourcen zu instanziieren.</span><span class="sxs-lookup"><span data-stu-id="4485d-193">You use the same factory to instantiate other DirectWrite resources.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  <span data-ttu-id="4485d-194">Initialisieren Sie die Text Zeichenfolge, und speichern Sie Ihre Länge.</span><span class="sxs-lookup"><span data-stu-id="4485d-194">Initialize the text string and store its length.</span></span>

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  <span data-ttu-id="4485d-195">Erstellen Sie ein [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstellen Objekt, indem Sie die [**idschreitefactory::**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) -Methode zum Erstellen von Textformaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="4485d-195">Create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface object by using the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method.</span></span> <span data-ttu-id="4485d-196">Das **idwrite-Textformat** gibt die Schriftart, die Gewichtung, die Streckung, den Stil und das Gebiets Schema an, die zum renderingtext der Zeichenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4485d-196">The **IDWriteTextFormat** specifies the font, weight, stretch, style, and locale that will be used to render the text string.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  <span data-ttu-id="4485d-197">Zentrieren Sie den Text horizontal und vertikal, indem Sie die Methoden [**idschreitetextformat:: SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) und [**idschreitetextformat:: setparagraphalignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4485d-197">Center the text horizontally and vertically by calling the [**IDWriteTextFormat::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) and [**IDWriteTextFormat::SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) methods.</span></span>
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

<span data-ttu-id="4485d-198">In diesem Teil haben Sie die geräteunabhängigen Ressourcen initialisiert, die von Ihrer Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4485d-198">In this part, you initialized the device-independent resources that are used by your application.</span></span> <span data-ttu-id="4485d-199">Im nächsten Teil initialisieren Sie die geräteabhängigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4485d-199">In the next part, you initialize the device-dependent resources.</span></span>

### <a name="part-3-create-device-dependent-resources"></a><span data-ttu-id="4485d-200">Teil 3: Erstellen von Device-Dependent Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="4485d-200">Part 3: Create Device-Dependent Resources.</span></span>

<span data-ttu-id="4485d-201">In diesem Teil erstellen Sie eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -und eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Datei zum Rendern des Texts.</span><span class="sxs-lookup"><span data-stu-id="4485d-201">In this part, you create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) for rendering your text.</span></span>

<span data-ttu-id="4485d-202">Ein Renderziel ist ein Direct2D-Objekt, das Zeichnungs Ressourcen erstellt und Zeichnungs Befehle auf einem renderinggerät rendert.</span><span class="sxs-lookup"><span data-stu-id="4485d-202">A render target is a Direct2D object that creates drawing resources and renders drawing commands to a rendering device.</span></span> <span data-ttu-id="4485d-203">Ein [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) ist ein Renderziel, das in ein **HWND** gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="4485d-203">An [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) is a render target that renders to an **HWND**.</span></span>

<span data-ttu-id="4485d-204">Eine der Zeichnungs Ressourcen, die von einem Renderziel erstellt werden kann, ist ein Pinsel zum Zeichnen von umrissen, Füllungen und Text.</span><span class="sxs-lookup"><span data-stu-id="4485d-204">One of the drawing resources that a render target can create is a brush for painting outlines, fills, and text.</span></span> <span data-ttu-id="4485d-205">Ein [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) zeichnet mit einer voll Tonfarbe.</span><span class="sxs-lookup"><span data-stu-id="4485d-205">An [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints with a solid color.</span></span>

<span data-ttu-id="4485d-206">Die [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Schnittstelle und die [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Schnittstelle sind an ein renderinggerät gebunden, wenn Sie erstellt werden, und müssen freigegeben und neu erstellt werden, wenn das Gerät ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="4485d-206">Both the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces are bound to a rendering device when they are created and must be released and recreated if the device becomes invalid.</span></span>

1.  <span data-ttu-id="4485d-207">Überprüfen Sie in der SimpleText:: deatedeviceresources-Methode, ob der renderzielzeiger **null** ist.</span><span class="sxs-lookup"><span data-stu-id="4485d-207">Inside the SimpleText::CreateDeviceResources method, check whether the render target pointer is **NULL**.</span></span> <span data-ttu-id="4485d-208">Wenn dies der Fall ist, rufen Sie die Größe des Rendering-Bereichs ab, und erstellen Sie eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) dieser Größe.</span><span class="sxs-lookup"><span data-stu-id="4485d-208">If it is, retrieve the size of the render area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of that size.</span></span> <span data-ttu-id="4485d-209">Verwenden Sie **ID2D1HwndRenderTarget** , um eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4485d-209">Use the **ID2D1HwndRenderTarget** to create an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  <span data-ttu-id="4485d-210">Geben Sie in der SimpleText::D iscarddeviceresources-Methode sowohl den Pinsel als auch das Renderziel frei.</span><span class="sxs-lookup"><span data-stu-id="4485d-210">In the SimpleText::DiscardDeviceResources method, release both the brush and render target.</span></span>
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

<span data-ttu-id="4485d-211">Nachdem Sie nun ein Renderziel und einen Pinsel erstellt haben, können Sie diese verwenden, um den Text zu renderzielen.</span><span class="sxs-lookup"><span data-stu-id="4485d-211">Now that you have created a render target and a brush, you can use them to render your text.</span></span>

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a><span data-ttu-id="4485d-212">Teil 4: Zeichnen von Text mithilfe der Direct2D DrawText-Methode.</span><span class="sxs-lookup"><span data-stu-id="4485d-212">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>

1.  <span data-ttu-id="4485d-213">Definieren Sie in der SimpleText::D rawtext-Methode der Klasse den Bereich für das Text Layout, indem Sie die Dimensionen des Renderingbereichs abrufen, und erstellen Sie ein [Direct2D](../direct2d/direct2d-portal.md) -Rechteck, das die gleichen Dimensionen aufweist.</span><span class="sxs-lookup"><span data-stu-id="4485d-213">In the SimpleText::DrawText method of your class, define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="4485d-214">Verwenden Sie die [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -Methode und das [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt, um Text auf dem Bildschirm zu Rendering.</span><span class="sxs-lookup"><span data-stu-id="4485d-214">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="4485d-215">Die **ID2D1RenderTarget::D rawtext** -Methode übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="4485d-215">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="4485d-216">Eine zu Rendering-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4485d-216">A string to render.</span></span>
    -   <span data-ttu-id="4485d-217">Ein Zeiger auf eine [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4485d-217">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="4485d-218">Ein [Direct2D](../direct2d/direct2d-portal.md) -Layoutrechteck.</span><span class="sxs-lookup"><span data-stu-id="4485d-218">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="4485d-219">Ein Zeiger auf eine-Schnittstelle, die [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="4485d-219">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a><span data-ttu-id="4485d-220">Teil 5: Rendering der Fenster Inhalte mithilfe von Direct2D</span><span class="sxs-lookup"><span data-stu-id="4485d-220">Part 5: Render the Window Contents Using Direct2D</span></span>

<span data-ttu-id="4485d-221">Gehen Sie folgendermaßen vor, um den Inhalt des Fensters mithilfe von [Direct2D](../direct2d/direct2d-portal.md) zu Rendering, wenn eine Paint-Meldung empfangen wird:</span><span class="sxs-lookup"><span data-stu-id="4485d-221">To render the contents of the window by using [Direct2D](../direct2d/direct2d-portal.md) when a paint message is received, do the following:</span></span>

1.  <span data-ttu-id="4485d-222">Erstellen Sie die geräteabhängigen Ressourcen, indem Sie die SimpleText:: CreateDeviceResources-Methode aufrufen, die in Teil 3 implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="4485d-222">Create the device dependent resources by calling the SimpleText::CreateDeviceResources method implemented in Part 3.</span></span>
2.  <span data-ttu-id="4485d-223">Aufrufen der [**ID2D1HwndRenderTarget:: beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="4485d-223">Call the [**ID2D1HwndRenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method of the render target.</span></span>
3.  <span data-ttu-id="4485d-224">Löschen Sie das Renderziel durch Aufrufen der [**ID2D1HwndRenderTarget:: Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4485d-224">Clear the render target by calling the [**ID2D1HwndRenderTarget::Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) method.</span></span>
4.  <span data-ttu-id="4485d-225">Nennen Sie die in Teil 4 implementierte Methode SimpleText::D rawtext.</span><span class="sxs-lookup"><span data-stu-id="4485d-225">Call the SimpleText::DrawText method, implemented in Part 4.</span></span>
5.  <span data-ttu-id="4485d-226">Aufrufen der [**ID2D1HwndRenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="4485d-226">Call the [**ID2D1HwndRenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method of the render target.</span></span>
6.  <span data-ttu-id="4485d-227">Wenn dies erforderlich ist, verwerfen Sie die geräteabhängigen Ressourcen, damit Sie neu erstellt werden können, wenn das Fenster neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="4485d-227">If it is necessary, discard the device-dependent resources so that they can be recreated when the window is redrawn.</span></span>


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



<span data-ttu-id="4485d-228">Die SimpleText-Klasse wird in SimpleText. h und SimpleText. cpp implementiert.</span><span class="sxs-lookup"><span data-stu-id="4485d-228">The SimpleText class is implemented in SimpleText.h and SimpleText.cpp.</span></span>

## <a name="drawing-text-with-multiple-formats"></a><span data-ttu-id="4485d-229">Zeichnen von Text mit mehreren Formaten.</span><span class="sxs-lookup"><span data-stu-id="4485d-229">Drawing Text with Multiple Formats.</span></span>

<span data-ttu-id="4485d-230">In diesem Abschnitt wird gezeigt, wie Sie mithilfe von [DirectWrite](direct-write-portal.md) und [Direct2D](../direct2d/direct2d-portal.md) Text mit mehreren Formaten Renderen, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4485d-230">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render text with multiple formats, as shown in the following screen shot.</span></span>

![Screenshot von "Hello World using DirectWrite!" mit einigen Teilen in verschiedenen Formaten, Größen und Formaten](images/multiformattedcropped.png)

<span data-ttu-id="4485d-232">Der Code für diesen Abschnitt wird als multiformattedtext-Klasse im [dwrite-HelloWorld-Beispiel](/samples/browse/?redirectedfrom=MSDN-samples)implementiert.</span><span class="sxs-lookup"><span data-stu-id="4485d-232">The code for this section is implemented as the MultiformattedText class in the [DWriteHelloWorld Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="4485d-233">Es basiert auf den Schritten aus dem vorherigen Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="4485d-233">It is based on the steps from the previous section.</span></span>

<span data-ttu-id="4485d-234">Zum Erstellen von mehr formatiertem Text verwenden Sie die [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle zusätzlich zur [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle, die im vorherigen Abschnitt vorgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4485d-234">To create multi-formatted text, you use the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface in addition to the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface introduced in the previous section.</span></span> <span data-ttu-id="4485d-235">Die **idschreitetextlayout** -Schnittstelle beschreibt die Formatierung und das Layout eines Textblocks.</span><span class="sxs-lookup"><span data-stu-id="4485d-235">The **IDWriteTextLayout** interface describes the formatting and layout of a block of text.</span></span> <span data-ttu-id="4485d-236">Zusätzlich zur Standard Formatierung, die durch ein **idschreitetextformat** -Objekt angegeben wird, kann die Formatierung für bestimmte Textbereiche mithilfe von **idschreitetextlayout** geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4485d-236">In addition to default formatting specified by an **IDWriteTextFormat** object, the formatting for specific ranges of text can be changed by using **IDWriteTextLayout**.</span></span> <span data-ttu-id="4485d-237">Dazu zählen Schriftfamilien Name, Größe, Gewichtung, Stil, Streckung, durchgestrichen und Unterstreichung.</span><span class="sxs-lookup"><span data-stu-id="4485d-237">This includes font family name, size, weight, style, stretch, strikethrough, and underlining.</span></span>

<span data-ttu-id="4485d-238">[**Idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) bietet auch Treffer Testmethoden.</span><span class="sxs-lookup"><span data-stu-id="4485d-238">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) also provides hit-testing methods.</span></span> <span data-ttu-id="4485d-239">Die von diesen Methoden zurückgegebenen Treffer Testmetriken sind relativ zum layoutfeld, das angegeben wird, wenn das **idschreitetextlayout** -Schnittstellen Objekt mithilfe der Methode " [**kreatetextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) " der [**idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Schnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4485d-239">The hit-testing metrics returned by these methods are relative to the layout box specified when the **IDWriteTextLayout** interface object is created by using the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="4485d-240">Die [**idwrite-Typografie**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) -Schnittstelle wird verwendet, um optionale [OpenType](../intl/opentype-font-format.md) -Typografiefunktionen zu einem Text Layout hinzuzufügen, z. b. Schwung Schrift und alternative Stil Text Sätze.</span><span class="sxs-lookup"><span data-stu-id="4485d-240">The [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface is used to add optional [OpenType](../intl/opentype-font-format.md) typographic features to a text layout, such as swashes and alternative stylistic text sets.</span></span> <span data-ttu-id="4485d-241">Typografische Funktionen können einem bestimmten Textbereich in einem Text Layout hinzugefügt werden, indem die [**addfontfeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) -Methode der **idschreitetypografie** -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4485d-241">Typographic features can be added to a specific range of text within a text layout by calling the [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method of the **IDWriteTypography** interface.</span></span> <span data-ttu-id="4485d-242">Diese Methode empfängt eine [**dwrite- \_ Schriftart \_ Funktions**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) Struktur als Parameter, der die Enumerationskonstante des **dwrite- \_ Schriftart \_ Features \_** und einen **UInt32** Execution-Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="4485d-242">This method receives a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) structure as a parameter that contains a **DWRITE\_FONT\_FEATURE\_TAG** enumeration constant and a **UINT32** execution parameter.</span></span> <span data-ttu-id="4485d-243">Eine Liste der registrierten OpenType-Features finden Sie in der [OpenType-layouttagregistrierung](https://www.microsoft.com/typography/otspec/features_ae.htm) auf Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="4485d-243">A list of registered OpenType features can be found at the [OpenType Layout Tag Registry](https://www.microsoft.com/typography/otspec/features_ae.htm) on microsoft.com.</span></span> <span data-ttu-id="4485d-244">Informationen zu den entsprechenden DirectWrite-Enumerationskonstanten finden Sie unter **dwrite \_ Font \_ Feature \_ Tag**.</span><span class="sxs-lookup"><span data-stu-id="4485d-244">For the equivalent DirectWrite enumeration constants, see **DWRITE\_FONT\_FEATURE\_TAG**.</span></span>

### <a name="part-1-create-an-idwritetextlayout-interface"></a><span data-ttu-id="4485d-245">Teil 1: Erstellen einer idschreitetextlayout-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4485d-245">Part 1: Create an IDWriteTextLayout Interface.</span></span>

1.  <span data-ttu-id="4485d-246">Deklarieren Sie einen Zeiger auf eine [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle als Member der multiformattedtext-Klasse.</span><span class="sxs-lookup"><span data-stu-id="4485d-246">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the MultiformattedText class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="4485d-247">Erstellen Sie am Ende der multiformattedtext:: createdeviceindependentresources-Methode ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstellen Objekt, indem Sie die [**createtextlayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4485d-247">At the end of the MultiformattedText::CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span> <span data-ttu-id="4485d-248">Die **idwrite-Textlayout** -Schnittstelle stellt zusätzliche Formatierungsfunktionen bereit, z. b. die Möglichkeit, unterschiedliche Formate auf ausgewählte Teile von Text anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="4485d-248">The **IDWriteTextLayout** interface provides additional formatting features, such as the ability to apply different formats to selected portions of text.</span></span>
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

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a><span data-ttu-id="4485d-249">Teil 2: Anwenden der Formatierung mit idbeschreib tetextlayout.</span><span class="sxs-lookup"><span data-stu-id="4485d-249">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>

<span data-ttu-id="4485d-250">Die Formatierung, wie z. b. Schriftart Größe, Gewichtung und Unterstreichung, kann auf Teil Zeichenfolgen des Texts angewendet werden, der mithilfe der [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4485d-250">Formatting, such as the font size, weight, and underlining, can be applied to substrings of the text to be displayed by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

1.  <span data-ttu-id="4485d-251">Legen Sie den Schrift Grad für die Teil Zeichenfolge "di" von "DirectWrite" auf "100" fest, indem Sie einen [**dwrite- \_ Text \_ Bereich**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) deklarieren und die [**idschreitetextlayout:: SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4485d-251">Set the font size for the substring "Di" of "DirectWrite" to 100 by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) and calling the [**IDWriteTextLayout::SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) method.</span></span>
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  <span data-ttu-id="4485d-252">Unterstreichen Sie die Teil Zeichenfolge "DirectWrite", indem Sie die [**idwrite-Textlayout:: setstreicht**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4485d-252">Underline the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  <span data-ttu-id="4485d-253">Legen Sie die Schrift Breite für die Teil Zeichenfolge "DirectWrite" auf "Fett" fest, indem Sie die [**idschreitetextlayout:: SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4485d-253">Set the font weight to bold for the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) method.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a><span data-ttu-id="4485d-254">Teil 3: Hinzufügen von typografischen Features mit idbeschreib tetypografie.</span><span class="sxs-lookup"><span data-stu-id="4485d-254">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>

1.  <span data-ttu-id="4485d-255">Deklarieren und erstellen Sie ein [**idwrite-Typografie**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) -Schnittstellen Objekt, indem Sie die [**idschreitefactory:: createtypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4485d-255">Declare and create an [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface object by calling the [**IDWriteFactory::CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) method.</span></span>
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  <span data-ttu-id="4485d-256">Fügen Sie eine Schriftart Funktion hinzu, indem Sie ein [**dwrite- \_ Schriftart \_ Funktions**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) Objekt deklarieren, das die angegebene stilmenge 7 hat, und die [**idschreitetypo:: addfontfeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4485d-256">Add a font feature by declaring a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) object that has the stylistic set 7 specified and calling the [**IDWriteTypography::AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method.</span></span>
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  <span data-ttu-id="4485d-257">Legen Sie das Text Layout so fest, dass die Typografie für die gesamte Zeichenfolge verwendet wird, indem Sie eine [**dwrite- \_ Text \_ Bereichs**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) Variable deklarieren und die [**idwrite tetextlayout:: settypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) -Methode aufrufen und den Textbereich übergeben.</span><span class="sxs-lookup"><span data-stu-id="4485d-257">Set the text layout to use the typography over the whole string by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable and calling the [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) method and passing in the text range.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  <span data-ttu-id="4485d-258">Legen Sie die neue Breite und Höhe für das textlayoutobjekt in der multiformattedtext:: OnResize-Methode fest.</span><span class="sxs-lookup"><span data-stu-id="4485d-258">Set the new width and height for the text layout object in the MultiformattedText::OnResize method.</span></span>
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a><span data-ttu-id="4485d-259">Teil 4: Zeichnen von Text mithilfe der Direct2D drawtextlayout-Methode.</span><span class="sxs-lookup"><span data-stu-id="4485d-259">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>

<span data-ttu-id="4485d-260">Ändern Sie den Code in der multiformattedtext::D rawtext-Methode, um [**idschreitetextlayout::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)zu verwenden, um den Text mit den textlayouteinstellungen zu zeichnen, die vom [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4485d-260">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="4485d-261">Sie müssen eine [**D2D1 \_ Point \_ 2F**](../direct2d/d2d1-point-2f.md) -Variable und die Variable auf den oberen linken Punkt des Fensters festlegen.</span><span class="sxs-lookup"><span data-stu-id="4485d-261">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="4485d-262">Zeichnen Sie den Text auf dem Bildschirm, indem Sie die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode des [Direct2D](../direct2d/direct2d-portal.md) -Renderziels aufrufen und den [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Zeiger übergeben.</span><span class="sxs-lookup"><span data-stu-id="4485d-262">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

<span data-ttu-id="4485d-263">Die multiformattedtext-Klasse wird in multiformattedtext. h und multiformattedtext. cpp implementiert.</span><span class="sxs-lookup"><span data-stu-id="4485d-263">The MultiformattedText class is implemented in MultiformattedText.h and MultiformattedText.cpp.</span></span>

 

 
---
title: Interoperabilität mit GDI
description: DirectWrite bietet einen Migrationspfad von und einige Interoperabilität mit, dem GDI-Schriftart Modell sowie Schnittstellen zum Rendern von Text in eine Bitmap, die dann in einem Fenster gezeichnet werden kann.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- DirectWrite, GDI-Interoperation
- DirectWrite, Interoperabilität
- Interoperabilität
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039032"
---
# <a name="interoperating-with-gdi"></a><span data-ttu-id="d85a9-108">Interoperabilität mit GDI</span><span class="sxs-lookup"><span data-stu-id="d85a9-108">Interoperating with GDI</span></span>

<span data-ttu-id="d85a9-109">[DirectWrite](direct-write-portal.md) bietet einen Migrationspfad von und einige Interoperabilität mit, dem GDI-Schriftart Modell sowie Schnittstellen zum Rendern von Text in eine Bitmap, die dann in einem Fenster gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d85a9-109">[DirectWrite](direct-write-portal.md) provides a migration path from, and some interoperability with, GDI's font model, as well as interfaces for rendering text to a bitmap that can then be drawn on a window.</span></span>

<span data-ttu-id="d85a9-110">Diese Übersicht enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="d85a9-110">This overview contains the following parts:</span></span>

-   [<span data-ttu-id="d85a9-111">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="d85a9-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d85a9-112">Teil 1: idschreitegdiinterop</span><span class="sxs-lookup"><span data-stu-id="d85a9-112">Part 1: IDWriteGdiInterop</span></span>](#part-1-idwritegdiinterop)
-   [<span data-ttu-id="d85a9-113">Teil 2: Schriftart Objekte</span><span class="sxs-lookup"><span data-stu-id="d85a9-113">Part 2: Font Objects</span></span>](#part-2-font-objects)
-   [<span data-ttu-id="d85a9-114">Teil 3: Rendering</span><span class="sxs-lookup"><span data-stu-id="d85a9-114">Part 3: Rendering</span></span>](#part-3-rendering)

## <a name="introduction"></a><span data-ttu-id="d85a9-115">Einführung</span><span class="sxs-lookup"><span data-stu-id="d85a9-115">Introduction</span></span>

<span data-ttu-id="d85a9-116">[DirectWrite](direct-write-portal.md) bietet Methoden für die Typumwandlung zwischen der GDI-LOGFONT-Struktur und den DirectWrite-Schriftart Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="d85a9-116">[DirectWrite](direct-write-portal.md) provides methods for converting between GDI's LOGFONT structure and DirectWrite font interfaces.</span></span> <span data-ttu-id="d85a9-117">Dies ermöglicht es Ihnen, GDI für einige oder alle der Schriftart Enumeration und-Auswahl zu verwenden, während gleichzeitig die verbesserte Funktionalität und Leistung von DirectWrite genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="d85a9-117">This allows you to use GDI for some or all of the font enumeration and selection, while taking advantage of the improved functionality and performance of DirectWrite.</span></span> <span data-ttu-id="d85a9-118">DirectWrite verfügt auch über Schnittstellen zum Rendern in eine Bitmap, wenn Sie Text auf einer GDI-Oberfläche anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="d85a9-118">DirectWrite also has interfaces for rendering to a bitmap if you want to display text on a GDI surface.</span></span>

## <a name="part-1-idwritegdiinterop"></a><span data-ttu-id="d85a9-119">Teil 1: idschreitegdiinterop</span><span class="sxs-lookup"><span data-stu-id="d85a9-119">Part 1: IDWriteGdiInterop</span></span>

<span data-ttu-id="d85a9-120">Die [**idschreitegdiinterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) -Schnittstelle wird verwendet, um zwischen GDI-Schriftart Strukturen und [DirectWrite](direct-write-portal.md) -Schriftart Schnittstellen zu konvertieren und ein [**idwrite-bitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d85a9-120">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface is used to convert between GDI font structures and [DirectWrite](direct-write-portal.md) font interfaces, and also to create an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object.</span></span> <span data-ttu-id="d85a9-121">Zum Aufrufen eines **idschreitegdiinterop** -Objekts verwenden Sie die [**idschreitefactory:: getgdiinterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) -Methode, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d85a9-121">Get an **IDWriteGdiInterop** object by using the [**IDWriteFactory::GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) method, as shown in the following code.</span></span>


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a><span data-ttu-id="d85a9-122">Teil 2: Schriftart Objekte</span><span class="sxs-lookup"><span data-stu-id="d85a9-122">Part 2: Font Objects</span></span>

<span data-ttu-id="d85a9-123">GDI verwendet die LogFont-Struktur zum Speichern von Informationen über die Schriftart und den Text Stil.</span><span class="sxs-lookup"><span data-stu-id="d85a9-123">GDI uses the LOGFONT structure to store information about the font and style of text.</span></span> <span data-ttu-id="d85a9-124">Die [**idwrite-gdiinterop:: kreatefontfromlogfont**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) -Methode konvertiert eine LOGFONT-Struktur in ein [**idschreitefont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) -Objekt, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d85a9-124">The [**IDWriteGdiInterop::CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) method will convert a LOGFONT structure to an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object, as seen in the following code.</span></span>


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



<span data-ttu-id="d85a9-125">Allerdings werden von [**idwrite-Font**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) nicht alle Informationen in einer LogFont-Datei eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d85a9-125">However, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) does not encapsulate all of the same information that a LOGFONT does.</span></span> <span data-ttu-id="d85a9-126">Eine LOGFONT-Struktur enthält die Schriftgröße, die Gewichtung, den Stil, die Unterstreichung, das stricken, den Namen der Schriftart und einige andere Informationen.</span><span class="sxs-lookup"><span data-stu-id="d85a9-126">A LOGFONT structure contains the font size, weight, style, underline, strikeout, font face name, and some other information.</span></span> <span data-ttu-id="d85a9-127">**Idwrite-Font** -Objekte enthalten Informationen zu einer Schriftart und ihrer Gewichtung und Art, aber nicht zur Schriftart Größe, Unterstreichung usw.</span><span class="sxs-lookup"><span data-stu-id="d85a9-127">**IDWriteFont** objects contain information about a font and its weight and style, but not the font size, underline, and so on.</span></span> <span data-ttu-id="d85a9-128">Mit [DirectWrite](direct-write-portal.md)werden Formatierungs Informationselemente wie diese durch ein [**idwrite-Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt oder für bestimmte Textbereiche ein [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt gekapselt.</span><span class="sxs-lookup"><span data-stu-id="d85a9-128">With [DirectWrite](direct-write-portal.md), formatting information elements such as these are encapsulated by an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object or, for specific ranges of text, an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="d85a9-129">Sie haben die Möglichkeit, [**idschreibschriftart**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) mithilfe von [**idschreitegdiinterop:: convertfonttologfont**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)in eine LogFont-Datei zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="d85a9-129">You do have the option to convert a [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) to a LOGFONT by using the [**IDWriteGdiInterop::ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span></span>

## <a name="part-3-rendering"></a><span data-ttu-id="d85a9-130">Teil 3: Rendering</span><span class="sxs-lookup"><span data-stu-id="d85a9-130">Part 3: Rendering</span></span>

<span data-ttu-id="d85a9-131">Um DirectWrite-Text auf einer GDI-Oberfläche zu Renderen, verwenden Sie einen benutzerdefinierten TextRenderer.</span><span class="sxs-lookup"><span data-stu-id="d85a9-131">To render DirectWrite text to a GDI surface you use a custom text renderer.</span></span> <span data-ttu-id="d85a9-132">Weitere Informationen finden Sie im Thema [Rendering zu einer GDI-Oberfläche](render-to-a-gdi-surface.md) .</span><span class="sxs-lookup"><span data-stu-id="d85a9-132">See the [Render to a GDI Surface](render-to-a-gdi-surface.md) topic.</span></span>

 

 
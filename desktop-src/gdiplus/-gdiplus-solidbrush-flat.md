---
description: Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht. Diese flachen API-Funktionen werden von der SolidBrush C++-Klasse umschlossen.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: SolidBrush-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9feb2676c60b3f504315f75303aadb16a1cd1f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395555"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="ef5df-104">SolidBrush-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ef5df-104">SolidBrush Functions</span></span>

<span data-ttu-id="ef5df-105">Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="ef5df-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="ef5df-106">Die Funktionen in der flachen GDI+-API werden von einer Sammlung von etwa 40 C++-Klassen umschlossen.</span><span class="sxs-lookup"><span data-stu-id="ef5df-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="ef5df-107">Es wird empfohlen, die Funktionen in der flachen API nicht direkt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ef5df-107">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="ef5df-108">Wenn Sie GDI+ aufrufen, wird empfohlen, dies durch Aufrufen der Methoden und Funktionen zu tun, die von den C++-Wrappern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ef5df-108">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="ef5df-109">Microsoft Product Support Services bietet keine Unterstützung für Code, der die flache API direkt aufruft.</span><span class="sxs-lookup"><span data-stu-id="ef5df-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="ef5df-110">Weitere Informationen zur Verwendung dieser Wrappermethoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="ef5df-110">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="ef5df-111">Die folgenden flachen API-Funktionen werden von der [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++-Klasse umschlossen.</span><span class="sxs-lookup"><span data-stu-id="ef5df-111">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="ef5df-112">Pinselfunktionen und entsprechende Wrappermethoden</span><span class="sxs-lookup"><span data-stu-id="ef5df-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="ef5df-113">Flat-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef5df-113">Flat function</span></span>                                                                               | <span data-ttu-id="ef5df-114">Wrappermethode</span><span class="sxs-lookup"><span data-stu-id="ef5df-114">Wrapper method</span></span>                                                                                       | <span data-ttu-id="ef5df-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef5df-115">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef5df-116">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \* \* brush)**</span><span class="sxs-lookup"><span data-stu-id="ef5df-116">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="ef5df-117">[**SolidBrush::SolidBrush(IN const Color& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="ef5df-117">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="ef5df-118">Erstellt ein [**SolidBrush-Objekt**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basierend auf einer Farbe</span><span class="sxs-lookup"><span data-stu-id="ef5df-118">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="ef5df-119">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \* brush, ARGB color)**</span><span class="sxs-lookup"><span data-stu-id="ef5df-119">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="ef5df-120">**SolidBrush::SetColor(IN const Color& color)**</span><span class="sxs-lookup"><span data-stu-id="ef5df-120">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="ef5df-121">Legt die Farbe dieses Volltonpinsels fest.</span><span class="sxs-lookup"><span data-stu-id="ef5df-121">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="ef5df-122">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill-Pinsel, \* \* ARGB-Farbe)**</span><span class="sxs-lookup"><span data-stu-id="ef5df-122">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="ef5df-123">**SolidBrush::GetColor(OUT Color \* color) const**</span><span class="sxs-lookup"><span data-stu-id="ef5df-123">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="ef5df-124">Ruft die Farbe dieses Volltonpinsels ab.</span><span class="sxs-lookup"><span data-stu-id="ef5df-124">Gets the color of this solid brush</span></span>                                                      |



 

 

 

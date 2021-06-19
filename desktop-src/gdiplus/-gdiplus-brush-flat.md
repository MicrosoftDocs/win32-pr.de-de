---
description: Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht. Diese flachen API-Funktionen werden von der Brush C++-Klasse umschlossen.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Pinselfunktionen (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395085"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="b5c7f-104">Pinselfunktionen (GDI+)</span><span class="sxs-lookup"><span data-stu-id="b5c7f-104">Brush Functions (GDI+)</span></span>

<span data-ttu-id="b5c7f-105">Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="b5c7f-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="b5c7f-106">Die Funktionen in der flachen GDI+-API werden von einer Sammlung von etwa 40 C++-Klassen umschlossen.</span><span class="sxs-lookup"><span data-stu-id="b5c7f-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="b5c7f-107">Es wird empfohlen, die Funktionen in der flachen API nicht direkt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b5c7f-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="b5c7f-108">Wenn Sie GDI+ aufrufen, sollten Sie dazu die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b5c7f-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="b5c7f-109">Microsoft Product Support Services bietet keine Unterstützung für Code, der die flache API direkt aufruft.</span><span class="sxs-lookup"><span data-stu-id="b5c7f-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="b5c7f-110">Weitere Informationen zur Verwendung dieser Wrappermethoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="b5c7f-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="b5c7f-111">Die folgenden flachen API-Funktionen werden von der [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++-Klasse umschlossen.</span><span class="sxs-lookup"><span data-stu-id="b5c7f-111">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="b5c7f-112">Pinselfunktionen und entsprechende Wrappermethoden</span><span class="sxs-lookup"><span data-stu-id="b5c7f-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="b5c7f-113">Flat-Funktion</span><span class="sxs-lookup"><span data-stu-id="b5c7f-113">Flat function</span></span>                                                                        | <span data-ttu-id="b5c7f-114">Wrappermethode</span><span class="sxs-lookup"><span data-stu-id="b5c7f-114">Wrapper method</span></span>                                          | <span data-ttu-id="b5c7f-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5c7f-115">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c7f-116">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush-Pinsel, \* GpBrush \* \* cloneBrush)</span><span class="sxs-lookup"><span data-stu-id="b5c7f-116">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="b5c7f-117">**Brush::Clone**</span><span class="sxs-lookup"><span data-stu-id="b5c7f-117">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="b5c7f-118">Die [**Brush::Clone-Methode**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) erstellt ein neues [**Brush-Objekt,**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) das auf diesem Pinsel basiert.</span><span class="sxs-lookup"><span data-stu-id="b5c7f-118">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="b5c7f-119">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush-Pinsel) \*</span><span class="sxs-lookup"><span data-stu-id="b5c7f-119">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="b5c7f-120">virtual ~Brush()</span><span class="sxs-lookup"><span data-stu-id="b5c7f-120">virtual ~Brush()</span></span>                                        | <span data-ttu-id="b5c7f-121">Bereinigt die von einem [**Brush-Objekt**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) verwendeten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b5c7f-121">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="b5c7f-122">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush-Pinsel, \* \* GpBrushType-Typ)</span><span class="sxs-lookup"><span data-stu-id="b5c7f-122">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="b5c7f-123">**Brush::GetType**</span><span class="sxs-lookup"><span data-stu-id="b5c7f-123">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="b5c7f-124">Die [**Brush::GetType-Methode**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) ruft den Typ dieses Pinsels ab.</span><span class="sxs-lookup"><span data-stu-id="b5c7f-124">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 





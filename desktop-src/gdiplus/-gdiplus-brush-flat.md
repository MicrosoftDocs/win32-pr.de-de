---
description: Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Pinsel Funktionen (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490cc641312014987b2fb847979de640c28c47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345108"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="75696-103">Pinsel Funktionen (GDI+)</span><span class="sxs-lookup"><span data-stu-id="75696-103">Brush Functions (GDI+)</span></span>

<span data-ttu-id="75696-104">Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.</span><span class="sxs-lookup"><span data-stu-id="75696-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="75696-105">Die Funktionen in der flatapi GDI+ werden von einer Sammlung von ungefähr 40 C++-Klassen umschließt.</span><span class="sxs-lookup"><span data-stu-id="75696-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="75696-106">Es wird empfohlen, die Funktionen in der flatapi nicht direkt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="75696-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="75696-107">Wenn Sie GDI+ aufrufen, sollten Sie dies tun, indem Sie die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="75696-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="75696-108">Der Microsoft-Produktsupport bietet keine Unterstützung für Code, mit dem die flatapi direkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="75696-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="75696-109">Weitere Informationen zur Verwendung dieser Wrapper Methoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="75696-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="75696-110">Die folgenden flatapi-Funktionen werden von der [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++-Klasse umschließt.</span><span class="sxs-lookup"><span data-stu-id="75696-110">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="75696-111">Pinsel Funktionen und entsprechende Wrapper Methoden</span><span class="sxs-lookup"><span data-stu-id="75696-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="75696-112">Flat-Funktion</span><span class="sxs-lookup"><span data-stu-id="75696-112">Flat function</span></span>                                                                        | <span data-ttu-id="75696-113">Wrapper Methode</span><span class="sxs-lookup"><span data-stu-id="75696-113">Wrapper method</span></span>                                          | <span data-ttu-id="75696-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75696-114">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75696-115">Gpstatus wingdipapi gdipclonebrush (gpbrush-Pinsel \* , gpbrush \* \* cloneBrush)</span><span class="sxs-lookup"><span data-stu-id="75696-115">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="75696-116">**Pinsel:: Clone**</span><span class="sxs-lookup"><span data-stu-id="75696-116">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="75696-117">Die [**Brush:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) -Methode erstellt ein neues [**Pinsel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) Objekt auf Grundlage dieses Pinsels.</span><span class="sxs-lookup"><span data-stu-id="75696-117">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="75696-118">Gpstatus wingdipapi gdipdeletebrush (gpbrush-Pinsel \* )</span><span class="sxs-lookup"><span data-stu-id="75696-118">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="75696-119">virtuelles ~ Brush ()</span><span class="sxs-lookup"><span data-stu-id="75696-119">virtual ~Brush()</span></span>                                        | <span data-ttu-id="75696-120">Bereinigt die von einem [**Pinsel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) Objekt verwendeten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="75696-120">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="75696-121">Gpstatus wingdipapi gdipgetbrushtype (gpbrush-Pinsel \* , gpbrushtype- \* Typ)</span><span class="sxs-lookup"><span data-stu-id="75696-121">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="75696-122">**Brush:: GetType**</span><span class="sxs-lookup"><span data-stu-id="75696-122">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="75696-123">Mit der [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) -Methode wird der Typ dieses Pinsels abgerufen.</span><span class="sxs-lookup"><span data-stu-id="75696-123">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 





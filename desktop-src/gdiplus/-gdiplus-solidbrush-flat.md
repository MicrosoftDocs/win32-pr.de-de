---
description: Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: SolidBrush-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977545"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="161a0-103">SolidBrush-Funktionen</span><span class="sxs-lookup"><span data-stu-id="161a0-103">SolidBrush Functions</span></span>

<span data-ttu-id="161a0-104">Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.</span><span class="sxs-lookup"><span data-stu-id="161a0-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="161a0-105">Die Funktionen in der flatapi GDI+ werden von einer Sammlung von ungefähr 40 C++-Klassen umschließt.</span><span class="sxs-lookup"><span data-stu-id="161a0-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="161a0-106">Es wird empfohlen, die Funktionen in der flatapi nicht direkt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="161a0-106">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="161a0-107">Wenn Sie GDI+ aufrufen, empfiehlt es sich, dies zu tun, indem Sie die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="161a0-107">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="161a0-108">Der Microsoft-Produktsupport bietet keine Unterstützung für Code, mit dem die flatapi direkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="161a0-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="161a0-109">Weitere Informationen zur Verwendung dieser Wrapper Methoden finden Sie unter [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="161a0-109">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="161a0-110">Die folgenden flatapi-Funktionen werden von der [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++-Klasse umschließt.</span><span class="sxs-lookup"><span data-stu-id="161a0-110">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="161a0-111">Pinsel Funktionen und entsprechende Wrapper Methoden</span><span class="sxs-lookup"><span data-stu-id="161a0-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="161a0-112">Flat-Funktion</span><span class="sxs-lookup"><span data-stu-id="161a0-112">Flat function</span></span>                                                                               | <span data-ttu-id="161a0-113">Wrapper Methode</span><span class="sxs-lookup"><span data-stu-id="161a0-113">Wrapper method</span></span>                                                                                       | <span data-ttu-id="161a0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="161a0-114">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="161a0-115">**Gpstatus wingdipapi gdipkreatesolidfill (ARGB-Farbe, gpsolidfill- \* \* Pinsel)**</span><span class="sxs-lookup"><span data-stu-id="161a0-115">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="161a0-116">[**SolidBrush:: SolidBrush (in konstanten Farben& Farbe)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="161a0-116">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="161a0-117">Erstellt ein [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) -Objekt auf Grundlage einer Farbe.</span><span class="sxs-lookup"><span data-stu-id="161a0-117">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="161a0-118">**Gpstatus wingdipapi gdipsetsolidfillcolor (gpsolidfill- \* Pinsel, ARGB-Farbe)**</span><span class="sxs-lookup"><span data-stu-id="161a0-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="161a0-119">**SolidBrush:: setColor (in konstanten Farben& Farbe)**</span><span class="sxs-lookup"><span data-stu-id="161a0-119">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="161a0-120">Legt die Farbe dieses Pinsel-Pinsels fest.</span><span class="sxs-lookup"><span data-stu-id="161a0-120">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="161a0-121">**Gpstatus wingdipapi gdipgetsolidfillcolor (gpsolidfill- \* Pinsel, ARGB- \* Farbe)**</span><span class="sxs-lookup"><span data-stu-id="161a0-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="161a0-122">**SolidBrush:: GetColor (out Color \* Color) konstant**</span><span class="sxs-lookup"><span data-stu-id="161a0-122">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="161a0-123">Ruft die Farbe dieses Pinsel-Pinsels ab.</span><span class="sxs-lookup"><span data-stu-id="161a0-123">Gets the color of this solid brush</span></span>                                                      |



 

 

 

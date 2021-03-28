---
description: Der mit einem Domänen Controller verknüpfte Stift, Pinsel, Bitmap, Palette, Bereich und Pfad werden als Grafik Objekte bezeichnet. Die folgenden Attribute sind jedem dieser Objekte zugeordnet.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Grafikobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b80aadcb0988e7bd64910d04ecfbf6ec608845d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993983"
---
# <a name="graphic-objects"></a><span data-ttu-id="02030-104">Grafikobjekte</span><span class="sxs-lookup"><span data-stu-id="02030-104">Graphic Objects</span></span>

<span data-ttu-id="02030-105">Der mit einem Domänen Controller verknüpfte Stift, Pinsel, Bitmap, Palette, Bereich und Pfad werden als Grafik Objekte bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="02030-105">The pen, brush, bitmap, palette, region, and path associated with a DC are referred to as its graphic objects.</span></span> <span data-ttu-id="02030-106">Die folgenden Attribute sind jedem dieser Objekte zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="02030-106">The following attributes are associated with each of these objects.</span></span>



| <span data-ttu-id="02030-107">Grafik Objekt</span><span class="sxs-lookup"><span data-stu-id="02030-107">Graphic object</span></span> | <span data-ttu-id="02030-108">Zugeordnete Attribute</span><span class="sxs-lookup"><span data-stu-id="02030-108">Associated attributes</span></span>                                                               |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="02030-109">Bitmap</span><span class="sxs-lookup"><span data-stu-id="02030-109">Bitmap</span></span>         | <span data-ttu-id="02030-110">Größe in Bytes Dimensionen in Pixel; Farb Format; Komprimierungs Schema; Und so weiter.</span><span class="sxs-lookup"><span data-stu-id="02030-110">Size, in bytes; dimensions, in pixels; color-format; compression scheme; and so on.</span></span> |
| <span data-ttu-id="02030-111">Brush</span><span class="sxs-lookup"><span data-stu-id="02030-111">Brush</span></span>          | <span data-ttu-id="02030-112">Stil, Farbe, Muster und Ursprung.</span><span class="sxs-lookup"><span data-stu-id="02030-112">Style, color, pattern, and origin.</span></span>                                                  |
| <span data-ttu-id="02030-113">Palette</span><span class="sxs-lookup"><span data-stu-id="02030-113">Palette</span></span>        | <span data-ttu-id="02030-114">Farben und Größe (oder Anzahl von Farben).</span><span class="sxs-lookup"><span data-stu-id="02030-114">Colors and size (or number of colors).</span></span>                                              |
| <span data-ttu-id="02030-115">Schriftart</span><span class="sxs-lookup"><span data-stu-id="02030-115">Font</span></span>           | <span data-ttu-id="02030-116">Schriftart Name, Breite, Höhe, Gewichtung, Zeichensatz usw.</span><span class="sxs-lookup"><span data-stu-id="02030-116">Typeface name, width, height, weight, character set, and so on.</span></span>                     |
| <span data-ttu-id="02030-117">`Path`</span><span class="sxs-lookup"><span data-stu-id="02030-117">Path</span></span>           | <span data-ttu-id="02030-118">Gebildet.</span><span class="sxs-lookup"><span data-stu-id="02030-118">Shape.</span></span>                                                                              |
| <span data-ttu-id="02030-119">Stift</span><span class="sxs-lookup"><span data-stu-id="02030-119">Pen</span></span>            | <span data-ttu-id="02030-120">Stil, Breite und Farbe.</span><span class="sxs-lookup"><span data-stu-id="02030-120">Style, width, and color.</span></span>                                                            |
| <span data-ttu-id="02030-121">Region</span><span class="sxs-lookup"><span data-stu-id="02030-121">Region</span></span>         | <span data-ttu-id="02030-122">Speicherort und Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="02030-122">Location and dimensions.</span></span>                                                            |



 

<span data-ttu-id="02030-123">Wenn eine Anwendung einen DC erstellt, speichert das System automatisch eine Reihe von Standardobjekten darin (es gibt keine Standard Bitmap oder einen Standardpfad).</span><span class="sxs-lookup"><span data-stu-id="02030-123">When an application creates a DC, the system automatically stores a set of default objects in it (there is no default bitmap or path).</span></span> <span data-ttu-id="02030-124">Eine Anwendung kann die Attribute der Standardobjekte überprüfen, indem Sie die [**getcurrentobject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) -und [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) -Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="02030-124">An application can examine the attributes of the default objects by calling the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions.</span></span> <span data-ttu-id="02030-125">Die Anwendung kann diese Standardeinstellungen ändern, indem ein neues-Objekt erstellt und in den DC ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="02030-125">The application can change these defaults by creating a new object and selecting it into the DC.</span></span> <span data-ttu-id="02030-126">Ein Objekt wird durch Aufrufen der [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion in einem Domänen Controller ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="02030-126">An object is selected into a DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span>

<span data-ttu-id="02030-127">Eine Anwendung kann die aktuelle Pinsel Farbe mit [**setdcbrushcolor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)auf einen angegebenen Farbwert festlegen.</span><span class="sxs-lookup"><span data-stu-id="02030-127">An application can set the current brush color to a specified color value with [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span></span>

<span data-ttu-id="02030-128">Die [**getdcbrushcolor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) -Funktion gibt die DC-Pinsel Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="02030-128">The [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) function returns the DC brush color.</span></span> <span data-ttu-id="02030-129">Die Funktion [**setdcpencolor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) legt die Stift Farbe auf einen angegebenen Farbwert fest.</span><span class="sxs-lookup"><span data-stu-id="02030-129">The [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) function sets the pen color to a specified color value.</span></span> <span data-ttu-id="02030-130">Die [**getdcpencolor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) -Funktion gibt die DC-Stift Farbe zurück.</span><span class="sxs-lookup"><span data-stu-id="02030-130">The [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) function returns the DC pen color.</span></span>

 

 




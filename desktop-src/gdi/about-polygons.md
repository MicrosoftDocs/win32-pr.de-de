---
description: Ein Polygon ist eine gefüllte Form mit geraden Seiten.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: Informationen zu Polygonen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041981"
---
# <a name="about-polygons"></a><span data-ttu-id="18452-103">Informationen zu Polygonen</span><span class="sxs-lookup"><span data-stu-id="18452-103">About Polygons</span></span>

<span data-ttu-id="18452-104">Ein *Polygon* ist eine gefüllte Form mit geraden Seiten.</span><span class="sxs-lookup"><span data-stu-id="18452-104">A *polygon* is a filled shape with straight sides.</span></span> <span data-ttu-id="18452-105">Die Seiten eines Polygons werden mithilfe des aktuellen Stifts gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="18452-105">The sides of a polygon are drawn by using the current pen.</span></span> <span data-ttu-id="18452-106">Wenn das System ein Polygon füllt, verwendet es den aktuellen Pinsel und den aktuellen Polygon Füll Modus.</span><span class="sxs-lookup"><span data-stu-id="18452-106">When the system fills a polygon, it uses the current brush and the current polygon fill mode.</span></span> <span data-ttu-id="18452-107">Die zwei Füll Modi, Alternate (Standard) und die Auffüllung, bestimmen, ob Bereiche innerhalb eines komplexen Polygons ausgefüllt oder nicht gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="18452-107">The two fill modes, alternate (the default) and winding, determine whether regions within a complex polygon are filled or left unpainted.</span></span> <span data-ttu-id="18452-108">Eine Anwendung kann einen der beiden Modi auswählen, indem Sie die Funktion [**setpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) aufruft.</span><span class="sxs-lookup"><span data-stu-id="18452-108">An application can select either mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="18452-109">Weitere Informationen zu den Polygon Füll Modi finden Sie unter [Regionen](regions.md).</span><span class="sxs-lookup"><span data-stu-id="18452-109">For more information about polygon fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="18452-110">Die folgende Abbildung zeigt ein Polygon, das mit [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="18452-110">The following illustration shows a polygon drawn by using [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span></span>

![Abbildung eines Polygons in der Form eines fünf-Spitzen-Stern](images/csfsh-04.png)

<span data-ttu-id="18452-112">Zusätzlich zum Zeichnen eines einzelnen Polygone [**mithilfe eines Polygone**](/windows/win32/api/wingdi/nf-wingdi-polygon)kann eine Anwendung mehrere Polygone mithilfe der [**polypolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) -Funktion zeichnen.</span><span class="sxs-lookup"><span data-stu-id="18452-112">In addition to drawing a single polygon by using [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), an application can draw multiple polygons by using the [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) function.</span></span>

 

 

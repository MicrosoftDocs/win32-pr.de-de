---
description: Einige Anwendungen stellen Funktionen bereit, die die im Client Bereich gezeichneten Objekte Scheren.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Scherz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217047"
---
# <a name="shear"></a><span data-ttu-id="c8624-103">Scherz</span><span class="sxs-lookup"><span data-stu-id="c8624-103">Shear</span></span>

<span data-ttu-id="c8624-104">Einige Anwendungen stellen Funktionen bereit, die die im Client Bereich gezeichneten Objekte Scheren.</span><span class="sxs-lookup"><span data-stu-id="c8624-104">Some applications provide features that shear objects drawn in the client area.</span></span> <span data-ttu-id="c8624-105">Anwendungen, die die Scheren-Funktionen verwenden, verwenden die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion, um geeignete Werte in der Transformation für den Welt Raum auf den Seiten Raum festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c8624-105">Applications that use shear capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="c8624-106">Diese Funktion empfängt einen Zeiger auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur, die die entsprechenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="c8624-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="c8624-107">Die eM12-und eM21-Member von XForm geben die horizontalen bzw. vertikalen Proportionalitäts Konstanten an.</span><span class="sxs-lookup"><span data-stu-id="c8624-107">The eM12 and eM21 members of XFORM specify the horizontal and vertical proportionality constants, respectively.</span></span>

<span data-ttu-id="c8624-108">Es gibt zwei Komponenten der schof- *Transformation*.</span><span class="sxs-lookup"><span data-stu-id="c8624-108">There are two components of the *shear transformation*.</span></span> <span data-ttu-id="c8624-109">Der erste ändert die vertikalen Linien in einem-Objekt. die zweite ändert die horizontalen Linien.</span><span class="sxs-lookup"><span data-stu-id="c8624-109">The first alters the vertical lines in an object; the second alters the horizontal lines.</span></span> <span data-ttu-id="c8624-110">In der folgenden Abbildung wird ein Rechteck mit 20 x 20 Einheiten angezeigt, das beim Kopieren aus dem Welt Raum in den Seitenbereich horizontal geschliffen wurde.</span><span class="sxs-lookup"><span data-stu-id="c8624-110">The following illustration shows a 20-by-20-unit rectangle sheared horizontally when copied from world space to page space.</span></span>

![Darstellung eines Rechtecks im Raum der Welt und eines trapeziod im Seitenbereich](images/cstrn-13.png)

<span data-ttu-id="c8624-112">Eine horizontale Schraffurart kann durch den folgenden Algorithmus dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="c8624-112">A horizontal shear can be represented by the following algorithm:</span></span>

``` syntax
x' = x + (Sx * y) 
```

<span data-ttu-id="c8624-113">Dabei ist x die ursprüngliche x-Koordinate, SX ist die proportionationskonstante, und x ' ist das Ergebnis der scherungs Transformation.</span><span class="sxs-lookup"><span data-stu-id="c8624-113">where x is the original x-coordinate, Sx is the proportionality constant, and x' is the result of the shear transformation.</span></span>

<span data-ttu-id="c8624-114">Eine vertikale Schere kann durch den folgenden Algorithmus dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="c8624-114">A vertical shear can be represented by the following algorithm:</span></span>

``` syntax
y' = y + (Sy * x) 
```

<span data-ttu-id="c8624-115">bei y handelt es sich um die ursprüngliche y-Koordinate, sy ist die proportionationskonstante, und y ' ist das Ergebnis der schof-Transformation.</span><span class="sxs-lookup"><span data-stu-id="c8624-115">where y is the original y-coordinate, Sy is the proportionality constant, and y' is the result of the shear transformation.</span></span>

<span data-ttu-id="c8624-116">Die Transformationen mit horizontaler und vertikaler Schraffurart können mithilfe einer 2-x-2-Matrix zu einem einzelnen Vorgang kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="c8624-116">The horizontal-shear and vertical-shear transformations can be combined into a single operation using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

<span data-ttu-id="c8624-117">Die 2 x 2-Matrix, die die Schere erzeugt hat, enthält die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="c8624-117">The 2-by-2 matrix that produced the shear contains the following values:</span></span>

``` syntax
|1    1| 
|0    1| 
```

 

 




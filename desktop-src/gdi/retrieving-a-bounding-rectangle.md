---
description: Eine Anwendung ruft die Dimensionen des umgebenden Rechtecks eines Bereichs durch Aufrufen der getrgnbox-Funktion ab.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Abrufen eines umgebenden Rechtecks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214a3f2e8d4fcd81e7f03ecf6dddc72442e209b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754305"
---
# <a name="retrieving-a-bounding-rectangle"></a><span data-ttu-id="f28b8-103">Abrufen eines umgebenden Rechtecks</span><span class="sxs-lookup"><span data-stu-id="f28b8-103">Retrieving a Bounding Rectangle</span></span>

<span data-ttu-id="f28b8-104">Eine Anwendung ruft die Dimensionen des umgebenden Rechtecks eines Bereichs durch Aufrufen der [**getrgnbox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) -Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="f28b8-104">An application retrieves the dimensions of a region's bounding rectangle by calling the [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) function.</span></span> <span data-ttu-id="f28b8-105">Wenn die Region rechteckig ist, gibt **getrgnbox** die Dimensionen des Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="f28b8-105">If the region is rectangular, **GetRgnBox** returns the dimensions of the region.</span></span> <span data-ttu-id="f28b8-106">Wenn der Bereich elliptisch ist, gibt die-Funktion die Abmessungen des kleinsten Rechtecks zurück, das um die Ellipse gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f28b8-106">If the region is elliptical, the function returns the dimensions of the smallest rectangle that can be drawn around the ellipse.</span></span> <span data-ttu-id="f28b8-107">Die langen Seiten des Rechtecks weisen die gleiche Länge auf wie die Hauptachse der Ellipse, und die kurzen Seiten des Rechtecks entsprechen derselben Länge wie die Nebenachse der Ellipse.</span><span class="sxs-lookup"><span data-stu-id="f28b8-107">The long sides of the rectangle are the same length as the ellipse's major axis, and the short sides of the rectangle are the same length as the ellipse's minor axis.</span></span> <span data-ttu-id="f28b8-108">Wenn die Region polygonal ist, gibt **getrgnbox** die Dimensionen des kleinsten Rechtecks zurück, das um das gesamte Polygon gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f28b8-108">If the region is polygonal, **GetRgnBox** returns the dimensions of the smallest rectangle that can be drawn around the entire polygon.</span></span>

 

 




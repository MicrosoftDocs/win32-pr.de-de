---
description: Ein Rechteck ist ein vierseitiges Polygon, dessen Gegenseite parallel und gleich lang sind.
ms.assetid: 77d29981-032e-45ba-a06b-c9c992236803
title: Zeichen Rechtecke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c5908ff989f7534536b3a6e84bad2095c096e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863651"
---
# <a name="drawing-rectangles"></a><span data-ttu-id="50952-103">Zeichen Rechtecke</span><span class="sxs-lookup"><span data-stu-id="50952-103">Drawing Rectangles</span></span>

<span data-ttu-id="50952-104">Ein Rechteck ist ein vierseitiges Polygon, dessen Gegenseite parallel und gleich lang sind.</span><span class="sxs-lookup"><span data-stu-id="50952-104">A rectangle is a four-sided polygon whose opposing sides are parallel and equal in length.</span></span> <span data-ttu-id="50952-105">Obwohl eine Anwendung ein Rechteck durch Aufrufen der [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) Funktion zeichnen kann, um die Koordinaten der einzelnen Ecken anzugeben, bietet die [**Rechteck**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) Funktion eine einfachere Methode.</span><span class="sxs-lookup"><span data-stu-id="50952-105">Although an application can draw a rectangle by calling the [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) function, supplying the coordinates of each corner, the [**Rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) function provides a simpler method.</span></span> <span data-ttu-id="50952-106">Diese Funktion erfordert nur die Koordinaten für die obere linke Ecke und die unteren rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="50952-106">This function requires only the coordinates for the upper-left and the lower-right corners.</span></span> <span data-ttu-id="50952-107">Wenn eine Anwendung die [**Rechteck**](/windows/win32/api/wingdi/nf-wingdi-rectangle) Funktion aufruft, zeichnet das System das Rechteck mit Ausnahme der rechten und unteren Seite, wenn für den angegebenen Gerätekontext keine globale Transformation festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="50952-107">When an application calls the [**Rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) function, the system draws the rectangle, excluding the right and lower sides if no world transformation is set for the given device context.</span></span>

<span data-ttu-id="50952-108">Wenn eine globale Transformation mithilfe der Funktion [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) oder [**modifyworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) festgelegt wurde, enthält das System den rechten und unteren Rand.</span><span class="sxs-lookup"><span data-stu-id="50952-108">If a world transformation has been set by using the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower edges.</span></span>

<span data-ttu-id="50952-109">Zusätzlich zum Zeichnen eines herkömmlichen Rechtecks können Sie Rechtecke mit abgerundeten Ecken zeichnen.</span><span class="sxs-lookup"><span data-stu-id="50952-109">In addition to drawing a traditional rectangle, you can draw rectangles with rounded corners.</span></span> <span data-ttu-id="50952-110">Die [**roundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) -Funktion erfordert, dass die Anwendung die Koordinaten der unteren linken und oberen rechten Ecke sowie die Breite und Höhe der Ellipse bereitstellt, die zum Runden der einzelnen Ecken verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50952-110">The [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) function requires that the application supply the coordinates of the lower-left and upper-right corners, as well as the width and height of the ellipse used to round each corner.</span></span>

<span data-ttu-id="50952-111">Anwendungen können die folgenden Funktionen verwenden, um Rechtecke zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="50952-111">Applications can use the following functions to manipulate rectangles.</span></span>



| <span data-ttu-id="50952-112">Funktion</span><span class="sxs-lookup"><span data-stu-id="50952-112">Function</span></span>                         | <span data-ttu-id="50952-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50952-113">Description</span></span>                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="50952-114">**FillRect**</span><span class="sxs-lookup"><span data-stu-id="50952-114">**FillRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | <span data-ttu-id="50952-115">Zeichnet das Innere eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="50952-115">Repaints the interior of a rectangle.</span></span>                              |
| [<span data-ttu-id="50952-116">**FrameRect**</span><span class="sxs-lookup"><span data-stu-id="50952-116">**FrameRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-framerect)   | <span data-ttu-id="50952-117">Zeichnet die Seiten eines Rechtecks neu.</span><span class="sxs-lookup"><span data-stu-id="50952-117">Redraws the sides of a rectangle.</span></span>                                  |
| [<span data-ttu-id="50952-118">**Invertrect**</span><span class="sxs-lookup"><span data-stu-id="50952-118">**InvertRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-invertrect) | <span data-ttu-id="50952-119">Kehrt die Farben um, die innerhalb des Inneren eines Rechtecks angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="50952-119">Inverts the colors that appear within the interior of a rectangle.</span></span> |



 

 

 

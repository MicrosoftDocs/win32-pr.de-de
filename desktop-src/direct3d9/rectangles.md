---
description: Während der Direct3D-und Fenster Programmierung werden Objekte auf dem Bildschirm in Bezug auf Begrenzungs Rechtecke bezeichnet.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Rechtecke (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd74538e81482061452382de3123243c3dffe7a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123434"
---
# <a name="rectangles-direct3d-9"></a><span data-ttu-id="c8cbe-103">Rechtecke (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c8cbe-103">Rectangles (Direct3D 9)</span></span>

<span data-ttu-id="c8cbe-104">Während der Direct3D-und Fenster Programmierung werden Objekte auf dem Bildschirm in Bezug auf Begrenzungs Rechtecke bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c8cbe-104">Throughout Direct3D and Window programming, objects on the screen are referred to in terms of bounding rectangles.</span></span> <span data-ttu-id="c8cbe-105">Die Seiten eines umgebenden Rechtecks sind immer parallel zu den Seiten des Bildschirms. Daher kann das Rechteck durch zwei Punkte, die obere linke Ecke und die untere rechte Ecke beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c8cbe-105">The sides of a bounding rectangle are always parallel to the sides of the screen, so the rectangle can be described by two points, the upper-left corner and lower-right corner.</span></span> <span data-ttu-id="c8cbe-106">Die meisten Anwendungen verwenden die [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, um Informationen zu einem umgebenden Rechteck zu übertragen, das beim blisten auf den Bildschirm oder beim Ausführen der Treffer Erkennung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8cbe-106">Most applications use the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to carry information about a bounding rectangle to use when blitting to the screen or performing hit detection.</span></span>

<span data-ttu-id="c8cbe-107">In C++ hat die [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur die folgende Definition.</span><span class="sxs-lookup"><span data-stu-id="c8cbe-107">In C++, the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure has the following definition.</span></span>


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



<span data-ttu-id="c8cbe-108">Im vorherigen Beispiel sind die linken und oberen Elemente die x-und y-Koordinaten der linken oberen Ecke eines umgebenden Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="c8cbe-108">In the preceding example, the left and top members are the x- and y-coordinates of a bounding rectangle's upper-left corner.</span></span> <span data-ttu-id="c8cbe-109">Entsprechend bilden die Rechte und unteren Member die Koordinaten der unteren rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="c8cbe-109">Similarly, the right and bottom members make up the coordinates of the lower-right corner.</span></span> <span data-ttu-id="c8cbe-110">In der folgenden Abbildung wird gezeigt, wie diese Werte visualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="c8cbe-110">The following illustration shows how you can visualize these values.</span></span>

![Abbildung des Rechtecks, das durch die Werte Links, oben, rechts und unten begrenzt ist](images/rect.png)

<span data-ttu-id="c8cbe-112">Die Spalte mit Pixeln am rechten Rand und die Zeile der Pixel am unteren Rand sind nicht in der Rect enthalten.</span><span class="sxs-lookup"><span data-stu-id="c8cbe-112">The column of pixels at the right edge and the row of pixels at the bottom edge are not included in the RECT.</span></span> <span data-ttu-id="c8cbe-113">Wenn Sie z. b. ein Rect mit den Membern {10, 10, 138, 138} sperren, wird ein Objekt mit einer Breite und Höhe von 128 Pixel ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="c8cbe-113">For example, locking a RECT with members {10, 10, 138, 138} results in an object 128 pixels in width and height.</span></span>

<span data-ttu-id="c8cbe-114">Im Interesse der Effizienz, Konsistenz und Benutzerfreundlichkeit können alle Direct3D Presentation-Funktionen mit Rechtecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8cbe-114">In the interest of efficiency, consistency, and ease of use, all Direct3D presentation functions work with rectangles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8cbe-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c8cbe-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8cbe-116">Koordinatensysteme und Geometrie</span><span class="sxs-lookup"><span data-stu-id="c8cbe-116">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 

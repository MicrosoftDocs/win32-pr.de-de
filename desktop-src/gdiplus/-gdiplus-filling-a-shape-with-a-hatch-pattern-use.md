---
description: 'Ein Schraffurmuster wird aus zwei Farben erstellt: eine für den Hintergrund und eine für die Linien, die das Muster über den Hintergrund bilden.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Auffüllen einer Form mit einem Schraffurmuster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37f06c93a6ac66a4a6066874c99b88652a0819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988085"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a><span data-ttu-id="5c91a-103">Auffüllen einer Form mit einem Schraffurmuster</span><span class="sxs-lookup"><span data-stu-id="5c91a-103">Filling a Shape with a Hatch Pattern</span></span>

<span data-ttu-id="5c91a-104">Ein Schraffurmuster wird aus zwei Farben erstellt: eine für den Hintergrund und eine für die Linien, die das Muster über den Hintergrund bilden.</span><span class="sxs-lookup"><span data-stu-id="5c91a-104">A hatch pattern is made from two colors: one for the background and one for the lines that form the pattern over the background.</span></span> <span data-ttu-id="5c91a-105">Um eine geschlossene Form mit einem Schraffurmuster auszufüllen, verwenden Sie ein [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5c91a-105">To fill a closed shape with a hatch pattern, use a [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) object.</span></span> <span data-ttu-id="5c91a-106">Im folgenden Beispiel wird veranschaulicht, wie Sie eine Ellipse mit einem Schraffurmuster ausfüllen:</span><span class="sxs-lookup"><span data-stu-id="5c91a-106">The following example demonstrates how to fill an ellipse with a hatch pattern:</span></span>


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



<span data-ttu-id="5c91a-107">Die folgende Abbildung zeigt die gefüllte Ellipse.</span><span class="sxs-lookup"><span data-stu-id="5c91a-107">The following illustration shows the filled ellipse.</span></span>

![Abbildung einer Ellipse, die mit einem Schraffurmuster von horizontalen Linien über einem voll Bild Hintergrund gefüllt ist](images/hatch1.png)

<span data-ttu-id="5c91a-109">Der [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) -Konstruktor benötigt drei Argumente: die Schraffurart, die Farbe der schraffurzeile und die Farbe des Hintergrunds.</span><span class="sxs-lookup"><span data-stu-id="5c91a-109">The [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) constructor takes three arguments: the hatch style, the color of the hatch line, and the color of the background.</span></span> <span data-ttu-id="5c91a-110">Das schraffurargumentgument kann ein beliebiges Element der [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) -Enumeration sein.</span><span class="sxs-lookup"><span data-stu-id="5c91a-110">The hatch style argument can be any element of the [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) enumeration.</span></span> <span data-ttu-id="5c91a-111">In der **HatchStyle** -Enumeration sind mehr als 50 Elemente vorhanden. Einige dieser Elemente sind in der folgenden Liste aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="5c91a-111">There are more than fifty elements in the **HatchStyle** enumeration; a few of those elements are shown in the following list:</span></span>

-   <span data-ttu-id="5c91a-112">**HatchStyleHorizontal**</span><span class="sxs-lookup"><span data-stu-id="5c91a-112">**HatchStyleHorizontal**</span></span>
-   <span data-ttu-id="5c91a-113">**Hatchstylevertical**</span><span class="sxs-lookup"><span data-stu-id="5c91a-113">**HatchStyleVertical**</span></span>
-   <span data-ttu-id="5c91a-114">**Hatchstyleforwarddiagonal**</span><span class="sxs-lookup"><span data-stu-id="5c91a-114">**HatchStyleForwardDiagonal**</span></span>
-   <span data-ttu-id="5c91a-115">**Hatchstylebackwarddiagonal**</span><span class="sxs-lookup"><span data-stu-id="5c91a-115">**HatchStyleBackwardDiagonal**</span></span>
-   <span data-ttu-id="5c91a-116">**Hatchstylecross**</span><span class="sxs-lookup"><span data-stu-id="5c91a-116">**HatchStyleCross**</span></span>
-   <span data-ttu-id="5c91a-117">**Hatchstylediagonalcross**</span><span class="sxs-lookup"><span data-stu-id="5c91a-117">**HatchStyleDiagonalCross**</span></span>

 

 




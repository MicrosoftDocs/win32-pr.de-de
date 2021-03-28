---
description: Die meisten CAD-und Zeichnungs Anwendungen bieten Features, mit denen die vom Benutzer erstellte Ausgabe skaliert wird.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Skalierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980304"
---
# <a name="scaling"></a><span data-ttu-id="18b4b-103">Skalierung</span><span class="sxs-lookup"><span data-stu-id="18b4b-103">Scaling</span></span>

<span data-ttu-id="18b4b-104">Die meisten CAD-und Zeichnungs Anwendungen bieten Features, mit denen die vom Benutzer erstellte Ausgabe skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="18b4b-104">Most CAD and drawing applications provide features that scale output created by the user.</span></span> <span data-ttu-id="18b4b-105">Anwendungen, die Skalierungs-(oder Zoom-) Funktionen enthalten, setzen die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion ein, um die entsprechende Welt Raum-und Seiten Raum Transformation festzulegen.</span><span class="sxs-lookup"><span data-stu-id="18b4b-105">Applications that include scaling (or zoom) capabilities call the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="18b4b-106">Diese Funktion empfängt einen Zeiger auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur, die die entsprechenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="18b4b-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="18b4b-107">Die eM11-und eM22-Member von XForm geben die horizontalen bzw. vertikalen Skalierungs Komponenten an.</span><span class="sxs-lookup"><span data-stu-id="18b4b-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical scaling components, respectively.</span></span>

<span data-ttu-id="18b4b-108">Wenn die *Skalierung* erfolgt, werden die vertikalen und horizontalen Linien (oder Vektoren), die ein Objekt bilden, in Bezug auf die x-oder y-Achse gestreckt oder komprimiert.</span><span class="sxs-lookup"><span data-stu-id="18b4b-108">When *scaling* occurs, the vertical and horizontal lines (or vectors), that constitute an object, are stretched or compressed with respect to the x- or y-axis.</span></span> <span data-ttu-id="18b4b-109">In der folgenden Abbildung wird ein Rechteck mit einer Breite von 20 und 20 Einheiten dargestellt, das vertikal auf die ursprüngliche Höhe skaliert wird, wenn es aus dem weltweiten Koordinatenraum in den Seiten Koordinaten Bereich kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="18b4b-109">The following illustration shows a 20-by-20-unit rectangle scaled vertically to twice its original height when copied from world-coordinate space to page-coordinate space.</span></span>

![Darstellung eines kleinen Rechtecks im Raum der Welt und eines größeren Rechtecks im Seitenbereich](images/cstrn-10.png)

<span data-ttu-id="18b4b-111">In der obigen Abbildung sind die vertikalen Linien, die die Seite des ursprünglichen Rechtecks definieren, 20 Einheiten, während die vertikalen Linien, die die Seiten des skalierten Rechtecks definieren, 40 Einheiten messen.</span><span class="sxs-lookup"><span data-stu-id="18b4b-111">In the preceding illustration, the vertical lines that define the original rectangle's side measure 20 units, while the vertical lines that define the scaled rectangle's sides measure 40 units.</span></span>

<span data-ttu-id="18b4b-112">Die vertikale Skalierung kann durch den folgenden Algorithmus dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="18b4b-112">Vertical scaling can be represented by the following algorithm.</span></span>

``` syntax
y' = y * Dy 
```

<span data-ttu-id="18b4b-113">Dabei ist y ' die neue Länge, y ist die ursprüngliche Länge, und dy ist der vertikale Skalierungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="18b4b-113">Where y' is the new length, y is the original length, and Dy is the vertical scaling factor.</span></span>

<span data-ttu-id="18b4b-114">Die horizontale Skalierung kann durch den folgenden Algorithmus dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="18b4b-114">Horizontal scaling can be represented by the following algorithm.</span></span>

``` syntax
x' = x * Dx 
```

<span data-ttu-id="18b4b-115">Wobei x ' die neue Länge, x die ursprüngliche Länge und DX der Faktor für die horizontale Skalierung ist.</span><span class="sxs-lookup"><span data-stu-id="18b4b-115">Where x' is the new length, x is the original length, and Dx is the horizontal scaling factor.</span></span>

<span data-ttu-id="18b4b-116">Die vertikalen und horizontalen Skalierungs Transformationen können mithilfe einer 2-x-2-Matrix zu einem einzelnen Vorgang kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="18b4b-116">The vertical and horizontal scaling transformations can be combined into a single operation by using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

<span data-ttu-id="18b4b-117">Die 2 x 2-Matrix, die die Skalierungs Transformation erzeugt hat, enthält die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="18b4b-117">The 2-by-2 matrix that produced the scaling transformation contains the following values.</span></span>

``` syntax
|1    0| 
|0    2| 
```

 

 




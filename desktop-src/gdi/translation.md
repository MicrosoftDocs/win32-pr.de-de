---
description: Einige Anwendungen übersetzen (oder verschieben) Objekte, die im Client Bereich gezeichnet werden.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Sprachübersetzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988180"
---
# <a name="translation"></a><span data-ttu-id="95f9f-103">Sprachübersetzung</span><span class="sxs-lookup"><span data-stu-id="95f9f-103">Translation</span></span>

<span data-ttu-id="95f9f-104">Einige Anwendungen übersetzen (oder verschieben) Objekte, die im Client Bereich gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="95f9f-104">Some applications translate (or shift) objects drawn in the client area.</span></span> <span data-ttu-id="95f9f-105">durch Aufrufen der [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion zum Festlegen der entsprechenden Welt Raum-und Seiten Raum Transformation.</span><span class="sxs-lookup"><span data-stu-id="95f9f-105">by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="95f9f-106">Die setworldtransform-Funktion empfängt einen Zeiger auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur, die die entsprechenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="95f9f-106">The SetWorldTransform function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="95f9f-107">Die EDX-und Edy-Member von XForm geben die horizontalen bzw. vertikalen Übersetzungs Komponenten an.</span><span class="sxs-lookup"><span data-stu-id="95f9f-107">The eDx and eDy members of XFORM specify the horizontal and vertical translation components, respectively.</span></span>

<span data-ttu-id="95f9f-108">Wenn die *Übersetzung* auftritt, wird jeder Punkt in einem Objekt vertikal, horizontal oder beides um einen angegebenen Betrag verschoben.</span><span class="sxs-lookup"><span data-stu-id="95f9f-108">When *translation* occurs, each point in an object is shifted vertically, horizontally, or both, by a specified amount.</span></span> <span data-ttu-id="95f9f-109">Die folgende Abbildung zeigt ein Rechteck mit 20 x 20 Einheiten, das beim Kopieren aus der weltweiten Koordinaten Fläche in den Bereich der Seiten Koordinate nach rechts um 10 Einheiten übersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="95f9f-109">The following illustration shows a 20- by 20-unit rectangle that was translated to the right by 10 units when copied from world-coordinate space to page-coordinate space.</span></span>

![Darstellung eines Rechtecks an einer Position im Raum der Welt und an einer anderen Position im Seitenbereich](images/cstrn-09.png)

<span data-ttu-id="95f9f-111">In der obigen Abbildung ist die x-Koordinate der einzelnen Punkte im Rechteck 10 Einheiten größer als die ursprüngliche x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="95f9f-111">In the preceding illustration, the x-coordinate of each point in the rectangle is 10 units greater than the original x-coordinate.</span></span>

<span data-ttu-id="95f9f-112">Die horizontale Übersetzung kann durch den folgenden Algorithmus dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="95f9f-112">Horizontal translation can be represented by the following algorithm.</span></span>

``` syntax
x' = x + Dx 
```

<span data-ttu-id="95f9f-113">Where x ' ist die neue x-Koordinate, x ist die ursprüngliche x-Koordinate, und DX ist die horizontale Entfernung, die verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="95f9f-113">Where x' is the new x-coordinate, x is the original x-coordinate, and Dx is the horizontal distance moved.</span></span>

<span data-ttu-id="95f9f-114">Die vertikale Übersetzung kann durch den folgenden Algorithmus dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="95f9f-114">Vertical translation can be represented by the following algorithm.</span></span>

``` syntax
y' = y + Dy 
```

<span data-ttu-id="95f9f-115">Dabei ist y ' die neue y-Koordinate, y ist die ursprüngliche y-Koordinate, und dy ist der vertikale Abstand verschoben.</span><span class="sxs-lookup"><span data-stu-id="95f9f-115">Where y' is the new y-coordinate, y is the original y-coordinate, and Dy is the vertical distance moved.</span></span>

<span data-ttu-id="95f9f-116">Die horizontalen und vertikalen Übersetzungs Transformationen können mithilfe einer 3 x 3-Matrix zu einem einzelnen Vorgang kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="95f9f-116">The horizontal and vertical translation transformations can be combined into a single operation by using a 3-by-3 matrix.</span></span>

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

<span data-ttu-id="95f9f-117">(Die Regeln der Matrix Multiplikation geben an, dass die Anzahl der Zeilen in einer Matrix der Anzahl der Spalten im anderen entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="95f9f-117">(The rules of matrix multiplication state that the number of rows in one matrix must equal the number of columns in the other.</span></span> <span data-ttu-id="95f9f-118">Die Ganzzahl 1 in der Matrix \| x y 1 \| ist ein Platzhalter, der hinzugefügt wurde, um diese Anforderung zu erfüllen.)</span><span class="sxs-lookup"><span data-stu-id="95f9f-118">The integer 1 in the matrix \|x y 1\| is a placeholder that was added to meet this requirement.)</span></span>

<span data-ttu-id="95f9f-119">Die 3-x-3-Matrix, die die veranschaulichte Übersetzungs Transformation erzeugt hat, enthält die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="95f9f-119">The 3-by-3 matrix that produced the illustrated translation transformation contains the following values.</span></span>

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 




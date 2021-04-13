---
description: Einige Anwendungen stellen Funktionen bereit, die im Client Bereich gezeichnete Objekte widerspiegeln (oder Spiegeln).
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Spiegelung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978353"
---
# <a name="reflection"></a><span data-ttu-id="7d3e2-103">Spiegelung</span><span class="sxs-lookup"><span data-stu-id="7d3e2-103">Reflection</span></span>

<span data-ttu-id="7d3e2-104">Einige Anwendungen stellen Funktionen bereit, die im Client Bereich gezeichnete Objekte widerspiegeln (oder Spiegeln).</span><span class="sxs-lookup"><span data-stu-id="7d3e2-104">Some applications provide features that reflect (or mirror) objects drawn in the client area.</span></span> <span data-ttu-id="7d3e2-105">Anwendungen, die Reflektionsfunktionen enthalten, verwenden die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion, um die entsprechenden Werte in der Welt Raum Transformation auf die Seiten Raum Transformation festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7d3e2-105">Applications that contain reflection capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="7d3e2-106">Diese Funktion empfängt einen Zeiger auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur, die die entsprechenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="7d3e2-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="7d3e2-107">Die eM11-und eM22-Member von XForm geben die horizontalen bzw. vertikalen reflektionskomponenten an.</span><span class="sxs-lookup"><span data-stu-id="7d3e2-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical reflection components, respectively.</span></span>

<span data-ttu-id="7d3e2-108">Die *reflektionstransformation* erstellt ein Spiegelbild eines Objekts in Bezug auf die x-oder y-Achse.</span><span class="sxs-lookup"><span data-stu-id="7d3e2-108">The *reflection transformation* creates a mirror image of an object with respect to either the x- or y-axis.</span></span> <span data-ttu-id="7d3e2-109">Kurz gesagt, die Reflektion ist nur eine negative Skalierung.</span><span class="sxs-lookup"><span data-stu-id="7d3e2-109">In short, reflection is just negative scaling.</span></span> <span data-ttu-id="7d3e2-110">Um eine horizontale Reflektion zu schaffen, werden x-Koordinaten mit 1 multipliziert.</span><span class="sxs-lookup"><span data-stu-id="7d3e2-110">To produce a horizontal reflection, x-coordinates are multiplied by 1.</span></span> <span data-ttu-id="7d3e2-111">Um eine vertikale Reflektion zu schaffen, werden y-Koordinaten mit 1 multipliziert.</span><span class="sxs-lookup"><span data-stu-id="7d3e2-111">To produce a vertical reflection, y-coordinates are multiplied by 1.</span></span>

<span data-ttu-id="7d3e2-112">Die horizontale Reflektion kann durch den folgenden Algorithmus dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="7d3e2-112">Horizontal reflection can be represented by the following algorithm:</span></span>

``` syntax
x' = -x 
```

<span data-ttu-id="7d3e2-113">Dabei ist x die x-Koordinate, und x ' ist das Ergebnis der Reflektion.</span><span class="sxs-lookup"><span data-stu-id="7d3e2-113">where x is the x-coordinate and x' is the result of the reflection.</span></span>

<span data-ttu-id="7d3e2-114">Die 2 x 2-Matrix, die die horizontale Reflektion erzeugt hat, enthält die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="7d3e2-114">The 2-by-2 matrix that produced horizontal reflection contains the following values:</span></span>

``` syntax
|-1    0| 
|0     1| 
```

<span data-ttu-id="7d3e2-115">Die vertikale Reflektion kann durch den folgenden Algorithmus dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="7d3e2-115">Vertical reflection can be represented by the following algorithm:</span></span>

``` syntax
y' = -y 
```

<span data-ttu-id="7d3e2-116">Dabei ist y die y-Koordinate, und y ' ist das Ergebnis der Reflektion.</span><span class="sxs-lookup"><span data-stu-id="7d3e2-116">where y is the y-coordinate and y' is the result of the reflection.</span></span>

<span data-ttu-id="7d3e2-117">Die 2 x 2-Matrix, die die vertikale Reflektion erzeugt hat, enthält die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="7d3e2-117">The 2-by-2 matrix that produced vertical reflection contains the following values:</span></span>

``` syntax
|1    0| 
|0   -1| 
```

<span data-ttu-id="7d3e2-118">Die Vorgänge für die horizontale Reflektion und die vertikale Reflektion können mithilfe der folgenden 2-bis-2-Matrix in einem einzelnen Vorgang kombiniert werden:</span><span class="sxs-lookup"><span data-stu-id="7d3e2-118">The horizontal-reflection and vertical-reflection operations can be combined into a single operation by using the following 2-by-2 matrix:</span></span>

``` syntax
|-1    0| 
|0    -1| 
```

 

 




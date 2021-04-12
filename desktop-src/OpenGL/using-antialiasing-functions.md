---
title: Verwenden von Antialiasing-Funktionen
description: In der folgenden Tabelle sind die Iris GL-Antialiasing-Funktionen und ihre entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: d54990b6-5645-4389-82ca-7d7f0a7fd7e9
keywords:
- IRIS GL portieren, Antialiasing
- Portieren von IRIS GL, Antialiasing
- Portieren auf OpenGL von IRIS GL, Antialiasing
- OpenGL-Portierung von IRIS GL, Antialiasing
- Antialiasing (antialiasing)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896d02dec050c72e59762ff5ee139b0bd091d9a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206562"
---
# <a name="using-antialiasing-functions"></a><span data-ttu-id="72636-108">Verwenden von Antialiasing-Funktionen</span><span class="sxs-lookup"><span data-stu-id="72636-108">Using Antialiasing Functions</span></span>

<span data-ttu-id="72636-109">In der folgenden Tabelle sind die Iris GL-Antialiasing-Funktionen und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="72636-109">The following table lists IRIS GL antialiasing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="72636-110">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="72636-110">IRIS GL function</span></span> | <span data-ttu-id="72636-111">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="72636-111">OpenGL function</span></span>                                      | <span data-ttu-id="72636-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="72636-112">Meaning</span></span>                           |
|------------------|------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="72636-113">**PNP**</span><span class="sxs-lookup"><span data-stu-id="72636-113">**pntsmooth**</span></span>    | <span data-ttu-id="72636-114">[**glEnable**](glenable.md) (GL- \_ Punkt \_ glatt)</span><span class="sxs-lookup"><span data-stu-id="72636-114">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>   | <span data-ttu-id="72636-115">Ermöglicht das Antialiasing von Punkten.</span><span class="sxs-lookup"><span data-stu-id="72636-115">Enables antialiasing of points.</span></span>   |
| <span data-ttu-id="72636-116">**linesmuoth**</span><span class="sxs-lookup"><span data-stu-id="72636-116">**linesmooth**</span></span>   | <span data-ttu-id="72636-117">**glEnable**(GL- \_ Linie \_ glatt)</span><span class="sxs-lookup"><span data-stu-id="72636-117">**glEnable**( GL\_LINE\_SMOOTH )</span></span>                     | <span data-ttu-id="72636-118">Ermöglicht das Antialiasing von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="72636-118">Enables antialiasing of lines.</span></span>    |
| <span data-ttu-id="72636-119">**polysmooth**</span><span class="sxs-lookup"><span data-stu-id="72636-119">**polysmooth**</span></span>   | <span data-ttu-id="72636-120">[**glEnable**](glenable.md) (GL- \_ Polygon \_ glatt)</span><span class="sxs-lookup"><span data-stu-id="72636-120">[**glEnable**](glenable.md) ( GL\_POLYGON\_SMOOTH )</span></span> | <span data-ttu-id="72636-121">Ermöglicht das Antialiasing von Polygonen.</span><span class="sxs-lookup"><span data-stu-id="72636-121">Enables antialiasing of polygons.</span></span> |



 

<span data-ttu-id="72636-122">Verwenden Sie die entsprechenden [**gldeaktiviert**](gldisable.md) -Aufrufe, um das Antialiasing zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="72636-122">Use the equivalent [**glDisable**](gldisable.md) calls to turn off antialiasing.</span></span>

<span data-ttu-id="72636-123">In IRIS GL können Sie die Qualität des Antialiasing steuern, indem Sie Folgendes aufrufen:</span><span class="sxs-lookup"><span data-stu-id="72636-123">In IRIS GL, you can control the quality of the antialiasing by calling:</span></span>


```C++
linesmooth(SML_ON + SML_SMOOTHER);
```



<span data-ttu-id="72636-124">OpenGL bietet einen ähnlichen controluse- [**glhint**](glhint.md):</span><span class="sxs-lookup"><span data-stu-id="72636-124">OpenGL provides similar controluse [**glHint**](glhint.md):</span></span>


```C++
glHint(GL_POINT_SMOOTH_HINT, hintMode); 
glHint(GL_LINE_SMOOTH_HINT, hintMode); 
glHint(GL_POLYGON_SMOOTH_HINT, hintMode);
```



<span data-ttu-id="72636-125">Dabei ist *hintmode* einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="72636-125">where *hintMode* is one of the following:</span></span>

-   <span data-ttu-id="72636-126">GL \_ am schönsten (verwenden Sie die höchste Qualität der Glättung)</span><span class="sxs-lookup"><span data-stu-id="72636-126">GL\_NICEST (Use the highest quality smoothing.)</span></span>
-   <span data-ttu-id="72636-127">GL \_ schnellste (verwenden Sie die effizienteste Glättung)</span><span class="sxs-lookup"><span data-stu-id="72636-127">GL\_FASTEST (Use the most efficient smoothing.)</span></span>
-   <span data-ttu-id="72636-128">GL ist nicht \_ \_ wichtig</span><span class="sxs-lookup"><span data-stu-id="72636-128">GL\_DONT\_CARE</span></span>

<span data-ttu-id="72636-129">IRIS GL ermöglicht außerdem eine End-Korrektur durch Aufrufen von:</span><span class="sxs-lookup"><span data-stu-id="72636-129">IRIS GL also permits end-correction by calling:</span></span>


```C++
linesmooth(SML_ON +  SML_END_CORRECT);
```



<span data-ttu-id="72636-130">OpenGL ist für diese Funktion nicht gleichwertig.</span><span class="sxs-lookup"><span data-stu-id="72636-130">OpenGL has no equivalent for this function.</span></span>

 

 





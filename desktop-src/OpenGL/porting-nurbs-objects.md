---
title: Portieren von nursb-Objekten
description: Bei OpenGL werden nursb als Objekte behandelt, ähnlich der Art, wie viercs behandelt werden, indem Sie ein nursb-Objekt erstellen und dann angeben, wie es gerendert werden soll. In der folgenden Tabelle sind die OpenGL-Funktionen für die Verwaltung von nursb-Objekten aufgeführt.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- IRIS GL portieren, nursb-Objekte
- Portieren von IRIS GL, nursb-Objekten
- Portieren auf OpenGL von IRIS GL, nursb-Objekten
- OpenGL-Portierung von IRIS GL, nursb-Objekten
- Nursb-Objekte
- NURBS (Non-Uniform Rational B-Spline)
- Nicht einheitlicher rationaler B-Spline (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388484"
---
# <a name="porting-nurbs-objects"></a><span data-ttu-id="8cefb-111">Portieren von nursb-Objekten</span><span class="sxs-lookup"><span data-stu-id="8cefb-111">Porting NURBS Objects</span></span>

<span data-ttu-id="8cefb-112">Bei OpenGL werden nursb als Objekte behandelt, ähnlich der Art und Weise, wie viercs behandelt werden: Sie erstellen ein nursb-Objekt und geben dann an, wie es gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cefb-112">OpenGL treats NURBS as objects, similar to the way it treats quadrics: you create a NURBS object and then specify how it should be rendered.</span></span> <span data-ttu-id="8cefb-113">In der folgenden Tabelle sind die OpenGL-Funktionen für die Verwaltung von nursb-Objekten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cefb-113">The following table lists the OpenGL GLU functions for managing NURBS objects.</span></span>



| <span data-ttu-id="8cefb-114">OpenGL glu-Funktion</span><span class="sxs-lookup"><span data-stu-id="8cefb-114">OpenGL GLU function</span></span>                                      | <span data-ttu-id="8cefb-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8cefb-115">Meaning</span></span>                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8cefb-116">**glunewnurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="8cefb-116">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)       | <span data-ttu-id="8cefb-117">Erstellt ein neues nursb-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8cefb-117">Creates a new NURBS object.</span></span>                                    |
| [<span data-ttu-id="8cefb-118">**gludeletenurbsrenderer**</span><span class="sxs-lookup"><span data-stu-id="8cefb-118">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md) | <span data-ttu-id="8cefb-119">Löscht ein nursb-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8cefb-119">Deletes a NURBS object.</span></span>                                        |
| [<span data-ttu-id="8cefb-120">*glunurbscallback*</span><span class="sxs-lookup"><span data-stu-id="8cefb-120">*gluNurbsCallback*</span></span>](glunurbs.md)                       | <span data-ttu-id="8cefb-121">Verknüpft einen Rückruf mit einem nursb-Objekt für die Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="8cefb-121">Associates a callback with a NURBS object, for error handling.</span></span> |



 

<span data-ttu-id="8cefb-122">Beachten Sie bei der Portierung von IRIS GL nursb-Code in OpenGL die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="8cefb-122">When porting IRIS GL NURBS code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="8cefb-123">Nursb-Steuerungs Punkte sind Gleit Komma Zahlen und keine doppelte.</span><span class="sxs-lookup"><span data-stu-id="8cefb-123">NURBS control points are floats, not doubles.</span></span>
-   <span data-ttu-id="8cefb-124">Der Stride-Parameter wird in Gleit Komma Zahlen und nicht in Bytes gezählt.</span><span class="sxs-lookup"><span data-stu-id="8cefb-124">The stride parameter is counted in floats, not bytes.</span></span>
-   <span data-ttu-id="8cefb-125">Wenn Sie Beleuchtung verwenden und keine normale angeben, rufen Sie [**glEnable**](glenable.md) mit GL \_ Auto \_ Normal als Parameter auf, um normale automatisch zu generieren.</span><span class="sxs-lookup"><span data-stu-id="8cefb-125">If you're using lighting and you're not specifying normals, call [**glEnable**](glenable.md) with GL\_AUTO\_NORMAL as the parameter to generate normals automatically.</span></span>

<span data-ttu-id="8cefb-126">??</span><span class="sxs-lookup"><span data-stu-id="8cefb-126">??</span></span>

 

 





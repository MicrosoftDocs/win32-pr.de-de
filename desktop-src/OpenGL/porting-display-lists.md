---
title: Portieren von Anzeigelisten
description: Die OpenGL-Implementierung von Anzeigelisten ähnelt der Iris GL-Implementierung, mit zwei Ausnahmen in OpenGL können Sie anzeigen Listen nicht bearbeiten, nachdem Sie Sie erstellt haben, und Sie können keine Funktionen aus Anzeigelisten aufrufen.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- IRIS GL portieren, Anzeigen von Listen
- Portieren von IRIS GL, Anzeigen von Listen
- Portieren auf OpenGL von IRIS GL, Anzeigen von Listen
- OpenGL-Portierung von IRIS GL, Anzeigen von Listen
- Anzeigen von Listen, Portieren von IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309451"
---
# <a name="porting-display-lists"></a><span data-ttu-id="0e9dd-108">Portieren von Anzeigelisten</span><span class="sxs-lookup"><span data-stu-id="0e9dd-108">Porting Display Lists</span></span>

<span data-ttu-id="0e9dd-109">Die OpenGL-Implementierung von Anzeigelisten ähnelt der Iris GL-Implementierung mit zwei Ausnahmen: in OpenGL können Sie anzeigen Listen nicht bearbeiten, nachdem Sie Sie erstellt haben, und Sie können keine Funktionen aus Anzeigelisten aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0e9dd-109">The OpenGL implementation of display lists is similar to the IRIS GL implementation, with two exceptions: in OpenGL you can't edit display lists once you've created them and you can't call functions from within display lists.</span></span>

<span data-ttu-id="0e9dd-110">Da Sie Funktionen nicht innerhalb von Anzeigelisten bearbeiten oder aufrufen können, haben diese IRIS GL-Funktionen in OpenGL keine Entsprechung:</span><span class="sxs-lookup"><span data-stu-id="0e9dd-110">Because you can't edit or call functions from within display lists, these IRIS GL functions have no equivalent in OpenGL:</span></span>

-   <span data-ttu-id="0e9dd-111">**editobj**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-111">**editobj**</span></span>
-   <span data-ttu-id="0e9dd-112">**objdelete**, **objinsert** und **objreplace**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-112">**objdelete**, **objinsert**, and **objreplace**</span></span>
-   <span data-ttu-id="0e9dd-113">**maketag**, **Gentag**, **ISTAG** und **Delta Tag**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-113">**maketag**, **gentag**, **istag**, and **deltag**</span></span>
-   <span data-ttu-id="0e9dd-114">**callfunc**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-114">**callfunc**</span></span>

<span data-ttu-id="0e9dd-115">In IRIS GL verwenden Sie die Funktionen **makeobj** und **closeobj** , um Anzeigelisten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e9dd-115">In IRIS GL, you use the **makeobj** and **closeobj** functions to create display lists.</span></span> <span data-ttu-id="0e9dd-116">In OpenGL verwenden Sie " [**glnewlist**](glnewlist.md) " und " [**glendlist**](glendlist.md)".</span><span class="sxs-lookup"><span data-stu-id="0e9dd-116">In OpenGL, you use [**glNewList**](glnewlist.md) and [**glEndList**](glendlist.md).</span></span>

<span data-ttu-id="0e9dd-117">In der folgenden Tabelle sind die Funktionen der Iris GL-Anzeigeliste mit den entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0e9dd-117">The following table lists the IRIS GL display list functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="0e9dd-118">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="0e9dd-118">IRIS GL function</span></span> | <span data-ttu-id="0e9dd-119">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="0e9dd-119">OpenGL function</span></span>                                                      | <span data-ttu-id="0e9dd-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0e9dd-120">Meaning</span></span>                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0e9dd-121">**makeobj**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-121">**makeobj**</span></span>      | <span data-ttu-id="0e9dd-122">**glnewlist**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-122">**glNewList**</span></span>                                                        | <span data-ttu-id="0e9dd-123">Erstellt eine neue Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="0e9dd-123">Creates a new display list.</span></span>                                   |
| <span data-ttu-id="0e9dd-124">**closeobj**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-124">**closeobj**</span></span>     | <span data-ttu-id="0e9dd-125">**glendlist**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-125">**glEndList**</span></span>                                                        | <span data-ttu-id="0e9dd-126">Signalisiert das Ende der Anzeigeliste.</span><span class="sxs-lookup"><span data-stu-id="0e9dd-126">Signals end of display list.</span></span>                                  |
| <span data-ttu-id="0e9dd-127">**czuweisung**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-127">**callobj**</span></span>      | <span data-ttu-id="0e9dd-128">[**glCallList**](glcalllist.md), [ **glcalllists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="0e9dd-128">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="0e9dd-129">Führt die Anzeigeliste oder Listen aus.</span><span class="sxs-lookup"><span data-stu-id="0e9dd-129">Executes display list or lists.</span></span>                               |
| <span data-ttu-id="0e9dd-130">**isobj**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-130">**isobj**</span></span>        | [<span data-ttu-id="0e9dd-131">**glislist**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-131">**glIsList**</span></span>](glislist.md)                                         | <span data-ttu-id="0e9dd-132">Testet, ob die Anzeigeliste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0e9dd-132">Tests for display list existence.</span></span>                             |
| <span data-ttu-id="0e9dd-133">**Delta-**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-133">**delobj**</span></span>       | [<span data-ttu-id="0e9dd-134">**gldelta etelists**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-134">**glDeleteLists**</span></span>](gldeletelists.md)                               | <span data-ttu-id="0e9dd-135">Löscht eine zusammenhängende Gruppe von Anzeigelisten.</span><span class="sxs-lookup"><span data-stu-id="0e9dd-135">Deletes contiguous group of display lists.</span></span>                    |
| <span data-ttu-id="0e9dd-136">**genobj**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-136">**genobj**</span></span>       | [<span data-ttu-id="0e9dd-137">**glgenlists**</span><span class="sxs-lookup"><span data-stu-id="0e9dd-137">**glGenLists**</span></span>](glgenlists.md)                                     | <span data-ttu-id="0e9dd-138">Generiert die angegebene Anzahl von zusammenhängenden leeren Anzeigelisten.</span><span class="sxs-lookup"><span data-stu-id="0e9dd-138">Generates the given number of contiguous empty display lists.</span></span> |



 

<span data-ttu-id="0e9dd-139">Dieses Thema enthält Informationen zu den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="0e9dd-139">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="0e9dd-140">Portieren der BBOX2-Funktion</span><span class="sxs-lookup"><span data-stu-id="0e9dd-140">Porting the bbox2 Function</span></span>](porting-the-bbox2-function.md)
-   [<span data-ttu-id="0e9dd-141">Portieren von bearbeiteten anzeigen Listen</span><span class="sxs-lookup"><span data-stu-id="0e9dd-141">Porting Edited Display Lists</span></span>](porting-edited-display-lists.md)
-   [<span data-ttu-id="0e9dd-142">Einen Beispielport einer Anzeigeliste</span><span class="sxs-lookup"><span data-stu-id="0e9dd-142">A Sample Port of a Display List</span></span>](a-sample-port-of-a-display-list.md)

 

 





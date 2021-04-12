---
title: Portieren von Linien
description: Das Portieren von IRIS GL-Code, der Linien zeichnet, ist recht unkompliziert. Beachten Sie jedoch die Unterschiede in der Art und Weise, wie OpenGL Stipeln. In der folgenden Tabelle sind IRIS GL-Funktionen für Zeichnungslinien und ihre entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- IRIS GL Porting, Lines
- Portieren von IRIS GL, Lines
- Portieren auf OpenGL von IRIS GL, Lines
- OpenGL-Portierung von IRIS GL, Zeilen
- Zeichnungsfunktionen, Zeilen
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207150"
---
# <a name="porting-lines"></a><span data-ttu-id="ef70e-110">Portieren von Linien</span><span class="sxs-lookup"><span data-stu-id="ef70e-110">Porting Lines</span></span>

<span data-ttu-id="ef70e-111">Das Portieren von IRIS GL-Code, der Linien zeichnet, ist recht unkompliziert. Beachten Sie jedoch die Unterschiede in der Art und Weise, wie OpenGL Stipeln.</span><span class="sxs-lookup"><span data-stu-id="ef70e-111">Porting IRIS GL code that draws lines is fairly straightforward, though you should note the differences in the way OpenGL stipples.</span></span> <span data-ttu-id="ef70e-112">In der folgenden Tabelle sind IRIS GL-Funktionen für Zeichnungslinien und ihre entsprechenden OpenGL-Funktionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef70e-112">The following table lists IRIS GL functions for drawing lines and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="ef70e-113">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef70e-113">IRIS GL function</span></span>                               | <span data-ttu-id="ef70e-114">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef70e-114">OpenGL function</span></span>                                                                                         | <span data-ttu-id="ef70e-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ef70e-115">Meaning</span></span>                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef70e-116">**bgnclosedline**,**endclosedline**</span><span class="sxs-lookup"><span data-stu-id="ef70e-116">**bgnclosedline**,**endclosedline**</span></span><br/> | <span data-ttu-id="ef70e-117">[**glBegin**](glbegin.md) (GL- \_ Zeilen \_ Schleife)[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="ef70e-117">[**glBegin**](glbegin.md) ( GL\_LINE\_LOOP )[**glEnd**](glend.md)</span></span><br/>                          | <span data-ttu-id="ef70e-118">Zeichnet eine geschlossene Zeile.</span><span class="sxs-lookup"><span data-stu-id="ef70e-118">Draws a closed line.</span></span>                                                                                                                         |
| <span data-ttu-id="ef70e-119">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="ef70e-119">**bgnline**</span></span>                                    | <span data-ttu-id="ef70e-120">[**glBegin**](glbegin.md) (GL- \_ Zeilen \_ Streifen)</span><span class="sxs-lookup"><span data-stu-id="ef70e-120">[**glBegin**](glbegin.md) ( GL\_LINE\_STRIP )</span></span>                                                          | <span data-ttu-id="ef70e-121">Zeichnet Liniensegmente.</span><span class="sxs-lookup"><span data-stu-id="ef70e-121">Draws line segments.</span></span>                                                                                                                         |
| <span data-ttu-id="ef70e-122">**LineWidth**</span><span class="sxs-lookup"><span data-stu-id="ef70e-122">**linewidth**</span></span>                                  | [<span data-ttu-id="ef70e-123">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="ef70e-123">**glLineWidth**</span></span>](gllinewidth.md)                                                                      | <span data-ttu-id="ef70e-124">Legt die Linienbreite fest.</span><span class="sxs-lookup"><span data-stu-id="ef70e-124">Sets line width.</span></span>                                                                                                                             |
| <span data-ttu-id="ef70e-125">**getlwidth**</span><span class="sxs-lookup"><span data-stu-id="ef70e-125">**getlwidth**</span></span>                                  | <span data-ttu-id="ef70e-126">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL- \_ Linienstärke \_ )</span><span class="sxs-lookup"><span data-stu-id="ef70e-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_WIDTH )</span></span>            | <span data-ttu-id="ef70e-127">Gibt die aktuelle Linienbreite zurück.</span><span class="sxs-lookup"><span data-stu-id="ef70e-127">Returns current line width.</span></span>                                                                                                                  |
| <span data-ttu-id="ef70e-128">**deflinestyle**,**SetLineStyle**</span><span class="sxs-lookup"><span data-stu-id="ef70e-128">**deflinestyle**,**setlinestyle**</span></span><br/>   | [<span data-ttu-id="ef70e-129">**gllinestippel**</span><span class="sxs-lookup"><span data-stu-id="ef70e-129">**glLineStipple**</span></span>](gllinestipple.md)                                                                  | <span data-ttu-id="ef70e-130">Gibt ein Zeilen stippingmuster an.</span><span class="sxs-lookup"><span data-stu-id="ef70e-130">Specifies a line stipple pattern.</span></span>                                                                                                            |
| <span data-ttu-id="ef70e-131">**lsrepeat**</span><span class="sxs-lookup"><span data-stu-id="ef70e-131">**lsrepeat**</span></span>                                   | <span data-ttu-id="ef70e-132">Faktor Argument von **gllinestippel**</span><span class="sxs-lookup"><span data-stu-id="ef70e-132">factor argument of **glLineStipple**</span></span>                                                                    | <span data-ttu-id="ef70e-133">Legt einen Wiederholungs Faktor für den Linienstil fest.</span><span class="sxs-lookup"><span data-stu-id="ef70e-133">Sets a repeat factor for the line style.</span></span>                                                                                                     |
| <span data-ttu-id="ef70e-134">**getlstyle**</span><span class="sxs-lookup"><span data-stu-id="ef70e-134">**getlstyle**</span></span>                                  | <span data-ttu-id="ef70e-135">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL- \_ Zeilen \_ stippingmuster \_ )</span><span class="sxs-lookup"><span data-stu-id="ef70e-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_PATTERN )</span></span> | <span data-ttu-id="ef70e-136">Gibt ein Zeilen stippingmuster zurück.</span><span class="sxs-lookup"><span data-stu-id="ef70e-136">Returns line stipple pattern.</span></span>                                                                                                                |
| <span data-ttu-id="ef70e-137">**getlsrepeat**</span><span class="sxs-lookup"><span data-stu-id="ef70e-137">**getlsrepeat**</span></span>                                | <span data-ttu-id="ef70e-138">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL- \_ Zeilen- \_ Stippel \_ wiederholen)</span><span class="sxs-lookup"><span data-stu-id="ef70e-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_REPEAT )</span></span>  | <span data-ttu-id="ef70e-139">Gibt den Wiederholungs Faktor zurück.</span><span class="sxs-lookup"><span data-stu-id="ef70e-139">Returns repeat factor.</span></span>                                                                                                                       |
| <span data-ttu-id="ef70e-140">**linesmuoth**, **glä-Linie**</span><span class="sxs-lookup"><span data-stu-id="ef70e-140">**linesmooth**, **smoothline**</span></span>                 | <span data-ttu-id="ef70e-141">[**glEnable**](glenable.md) (GL- \_ Linie \_ glatt)</span><span class="sxs-lookup"><span data-stu-id="ef70e-141">[**glEnable**](glenable.md) ( GL\_LINE\_SMOOTH )</span></span>                                                       | <span data-ttu-id="ef70e-142">Schaltet ein Zeilen-Antialiasing (Weitere Informationen zum Antialiasing finden Sie unter [Portieren von Antialiasing-Funktionen](porting-antialiasing-functions.md).)</span><span class="sxs-lookup"><span data-stu-id="ef70e-142">Turns on line antialiasing (For more information on antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="ef70e-143">OpenGL verwendet keine Tabellen für Zeilen Stipeln; Es wird nur ein Zeilen stippingmuster verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ef70e-143">OpenGL doesn't use tables for line stipples; it maintains only one line-stipple pattern.</span></span> <span data-ttu-id="ef70e-144">Sie können mit [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md) zwischen verschiedenen Stippel Mustern wechseln.</span><span class="sxs-lookup"><span data-stu-id="ef70e-144">You can use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to switch between different stipple patterns.</span></span>

<span data-ttu-id="ef70e-145">Ältere Zeilen Stil Funktionen von IRIS gl (z. b. **Draw**, **lsbackup**, **getlsbackup** usw.) werden von OpenGL nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef70e-145">Older IRIS GL line style functions (such as **draw**, **lsbackup**, **getlsbackup**, and so on) are not supported by OpenGL.</span></span>

<span data-ttu-id="ef70e-146">Weitere Informationen zum Zeichnen von Zeilen mit Antialiasing finden Sie unter [Portieren von Antialiasing-Funktionen](porting-antialiasing-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ef70e-146">For information on drawing antialiased lines, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).</span></span>

<span data-ttu-id="ef70e-147">??</span><span class="sxs-lookup"><span data-stu-id="ef70e-147">??</span></span>

 

 






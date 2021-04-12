---
title: Portieren von Schattierungs Modellen
description: Wie IRIS GL ermöglicht OpenGL den Wechsel zwischen Smooth (Gouraud) Schattierung und flacher Schattierung. In der folgenden Tabelle werden die Funktionen zum Schattieren und Dithering von IRIS GL sowie die entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- IRIS GL portieren, Schattierung
- Portieren von IRIS GL, Schattierung
- Portieren auf OpenGL von IRIS GL, Schattierung
- OpenGL-Portierung von IRIS GL, Schattierung
- Smooth-Schattierung
- Gouraud-Schattierung
- flatschattierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310543"
---
# <a name="porting-shading-models"></a><span data-ttu-id="6e364-111">Portieren von Schattierungs Modellen</span><span class="sxs-lookup"><span data-stu-id="6e364-111">Porting Shading Models</span></span>

<span data-ttu-id="6e364-112">Wie IRIS GL ermöglicht OpenGL den Wechsel zwischen Smooth (Gouraud) Schattierung und flacher Schattierung.</span><span class="sxs-lookup"><span data-stu-id="6e364-112">Like IRIS GL, OpenGL lets you switch between smooth (Gouraud) shading and flat shading.</span></span> <span data-ttu-id="6e364-113">In der folgenden Tabelle werden die Funktionen zum Schattieren und Dithering von IRIS GL sowie die entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6e364-113">The following table lists the IRIS GL shading and dithering functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="6e364-114">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="6e364-114">IRIS GL function</span></span>                                   | <span data-ttu-id="6e364-115">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="6e364-115">OpenGL function</span></span>                                                                                    | <span data-ttu-id="6e364-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6e364-116">Meaning</span></span>                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="6e364-117">**shademodel**(flach)</span><span class="sxs-lookup"><span data-stu-id="6e364-117">**shademodel**(FLAT)</span></span>                               | <span data-ttu-id="6e364-118">[**glshademodel**](glshademodel.md) (GL \_ Flat)</span><span class="sxs-lookup"><span data-stu-id="6e364-118">[**glShadeModel**](glshademodel.md) ( GL\_FLAT )</span></span>                                                  | <span data-ttu-id="6e364-119">Führt eine flache Schattierung durch.</span><span class="sxs-lookup"><span data-stu-id="6e364-119">Does flat shading.</span></span>           |
| <span data-ttu-id="6e364-120">**shademodel**(Gouraud)</span><span class="sxs-lookup"><span data-stu-id="6e364-120">**shademodel**(GOURAUD)</span></span>                            | <span data-ttu-id="6e364-121">**glshademodel**(GL \_ Smooth)</span><span class="sxs-lookup"><span data-stu-id="6e364-121">**glShadeModel**( GL\_SMOOTH )</span></span>                                                                     | <span data-ttu-id="6e364-122">Führt eine Smooth-Schattierung durch.</span><span class="sxs-lookup"><span data-stu-id="6e364-122">Does smooth shading.</span></span>         |
| <span data-ttu-id="6e364-123">**ge-m**</span><span class="sxs-lookup"><span data-stu-id="6e364-123">**getsm**</span></span>                                          | <span data-ttu-id="6e364-124">[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL- \_ Schattierung- \_ Modell)</span><span class="sxs-lookup"><span data-stu-id="6e364-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SHADE\_MODEL )</span></span>      | <span data-ttu-id="6e364-125">Gibt das aktuelle Farbton Modell zurück.</span><span class="sxs-lookup"><span data-stu-id="6e364-125">Returns current shade model.</span></span> |
| <span data-ttu-id="6e364-126">**Dithering**(dt \_ on) **Dithering**(dt \_ Off)</span><span class="sxs-lookup"><span data-stu-id="6e364-126">**dither**(DT\_ON) **dither**(DT\_OFF)</span></span> <br/> | <span data-ttu-id="6e364-127">[**glEnable**](glenable.md) (GL \_ Dither)[**gldeaktiviert**](gldisable.md)(GL \_ Dither)</span><span class="sxs-lookup"><span data-stu-id="6e364-127">[**glEnable**](glenable.md) ( GL\_DITHER )[**glDisable**](gldisable.md)( GL\_DITHER )</span></span><br/> | <span data-ttu-id="6e364-128">Schaltet die Dithering ein/aus.</span><span class="sxs-lookup"><span data-stu-id="6e364-128">Turns dithering on/off.</span></span>      |



 

<span data-ttu-id="6e364-129">??</span><span class="sxs-lookup"><span data-stu-id="6e364-129">??</span></span>

 

 






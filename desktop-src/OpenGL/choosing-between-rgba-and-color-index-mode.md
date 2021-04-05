---
title: Auswählen zwischen RGBA und Color-Index Modus
description: Verwenden Sie im Allgemeinen den RGBA-Modus für Ihre OpenGL-Anwendungen. Sie bietet mehr Flexibilität als der Farb Index Modus für Effekte wie Schattierung, Beleuchtung, Farbzuordnung, Nebel, Antialiasing und Vermischung.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL unter Windows, RGBA-Modus
- OpenGL unter Windows, Farb Index Modus
- RGBA-Modus OpenGL
- Farb Index Modus OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710422"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a><span data-ttu-id="ea2a8-107">Auswählen zwischen RGBA und Color-Index Modus</span><span class="sxs-lookup"><span data-stu-id="ea2a8-107">Choosing Between RGBA and Color-Index Mode</span></span>

<span data-ttu-id="ea2a8-108">Verwenden Sie im Allgemeinen den RGBA-Modus für Ihre OpenGL-Anwendungen. Sie bietet mehr Flexibilität als der Farb Index Modus für Effekte wie Schattierung, Beleuchtung, Farbzuordnung, Nebel, Antialiasing und Vermischung.</span><span class="sxs-lookup"><span data-stu-id="ea2a8-108">In general, use the RGBA mode for your OpenGL applications; it provides more flexibility than the color-index mode for effects such as shading, lighting, color mapping, fog, antialiasing, and blending.</span></span>

<span data-ttu-id="ea2a8-109">In den folgenden Fällen sollten Sie den Farb Index Modus verwenden:</span><span class="sxs-lookup"><span data-stu-id="ea2a8-109">Consider using the color-index mode in the following cases:</span></span>

-   <span data-ttu-id="ea2a8-110">Wenn eine begrenzte Anzahl von bitflächen verfügbar ist, der Farb Index Modus kann weniger grobe Schattierung als der RGBA-Modus bewirken.</span><span class="sxs-lookup"><span data-stu-id="ea2a8-110">If you have a limited number of bitplanes available; the color-index mode can produce less-coarse shading than the RGBA mode.</span></span>
-   <span data-ttu-id="ea2a8-111">Wenn Sie sich keine Gedanken über die Verwendung von "Real"-Farben machen möchten, Beispielsweise können Sie verschiedene Farben in einer Topographic-Karte verwenden, um relative Erweiterungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ea2a8-111">If you are not concerned about using "real" colors; for example, using several colors in a topographic map to designate relative elevations.</span></span>
-   <span data-ttu-id="ea2a8-112">Wenn Sie eine vorhandene Anwendung portieren, die den Farb Index Modus ausgiebig verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea2a8-112">When you're porting an existing application that uses color-index mode extensively.</span></span>
-   <span data-ttu-id="ea2a8-113">Wenn Sie die Farb Zuordnungs Animation und-Effekte in der Anwendung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="ea2a8-113">When you want to use color-map animation and effects in your application.</span></span> <span data-ttu-id="ea2a8-114">(Dies ist auf echt Farben Geräten nicht möglich.)</span><span class="sxs-lookup"><span data-stu-id="ea2a8-114">(This is not possible on true-color devices.)</span></span>

 

 





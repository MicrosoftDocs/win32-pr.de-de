---
description: Ein Pfad ist eine Sequenz von Grafik primitiven (Linien, Rechtecke, Kurven, Text usw.), die als einzelne Einheit manipuliert und gezeichnet werden können. Ein Pfad kann in Abbildungen aufgeteilt werden, die entweder geöffnet oder geschlossen sind. Eine Abbildung kann mehrere primitive enthalten.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Erstellen und Zeichnen von Pfaden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe5f1528e58e3df19afbc83bb6acfdc2a6fca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994303"
---
# <a name="constructing-and-drawing-paths"></a><span data-ttu-id="db005-105">Erstellen und Zeichnen von Pfaden</span><span class="sxs-lookup"><span data-stu-id="db005-105">Constructing and Drawing Paths</span></span>

<span data-ttu-id="db005-106">Ein Pfad ist eine Sequenz von Grafik primitiven (Linien, Rechtecke, Kurven, Text usw.), die als einzelne Einheit manipuliert und gezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="db005-106">A path is a sequence of graphics primitives (lines, rectangles, curves, text, and the like) that can be manipulated and drawn as a single unit.</span></span> <span data-ttu-id="db005-107">Ein Pfad kann in *Abbildungen* aufgeteilt werden, die entweder geöffnet oder geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="db005-107">A path can be divided into *figures* that are either open or closed.</span></span> <span data-ttu-id="db005-108">Eine Abbildung kann mehrere primitive enthalten.</span><span class="sxs-lookup"><span data-stu-id="db005-108">A figure can contain several primitives.</span></span>

<span data-ttu-id="db005-109">Sie können einen Pfad zeichnen, indem Sie die Grafik [**::D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) -Methode der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse aufrufen, und Sie können einen Pfad auffüllen, indem Sie die [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) -Methode der **Grafik** Klasse aufrufen.</span><span class="sxs-lookup"><span data-stu-id="db005-109">You can draw a path by calling the [**Graphics::DrawPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, and you can fill a path by calling the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method of the **Graphics** class.</span></span>

<span data-ttu-id="db005-110">In den folgenden Themen werden Pfade ausführlicher behandelt:</span><span class="sxs-lookup"><span data-stu-id="db005-110">The following topics cover paths in more detail:</span></span>

-   [<span data-ttu-id="db005-111">Erstellen von Abbildungen Figuren aus Linien, Kurven und Formen</span><span class="sxs-lookup"><span data-stu-id="db005-111">Creating Figures from Lines, Curves, and Shapes</span></span>](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [<span data-ttu-id="db005-112">Auffüllen offener Abbildungen</span><span class="sxs-lookup"><span data-stu-id="db005-112">Filling Open Figures</span></span>](-gdiplus-filling-open-figures-use.md)

 

 




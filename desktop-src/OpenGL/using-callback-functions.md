---
title: Verwenden von Rückruf Funktionen
description: Die glu-Rückruf Funktionen "glubeginpolygon", "glutess Vertex", "glunextcontour" und "gluendpolygon" ähneln den OpenGL-Polygon Funktionen.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- OpenGL-Hilfsprogramm (GLU), Rückruf Funktionen
- GLU (OpenGL-Hilfsprogramm), Rückruf Funktionen
- OpenGL-Hilfsprogramm (GLU), Mosaik
- GLU (OpenGL-Hilfsprogramm), Mosaik
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a826d9416f94304762be2e840a3b6fea9ba458ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855819"
---
# <a name="using-callback-functions"></a><span data-ttu-id="d7ebf-107">Verwenden von Rückruf Funktionen</span><span class="sxs-lookup"><span data-stu-id="d7ebf-107">Using Callback Functions</span></span>

<span data-ttu-id="d7ebf-108">Die glu-Rückruf Funktionen " [**glubeginpolygon**](glubeginpolygon.md)", " [**glutess Vertex**](glutessvertex.md)", " [**glunextcontour**](glunextcontour.md)" und " [**gluendpolygon**](gluendpolygon.md)" ähneln den OpenGL-Polygon Funktionen.</span><span class="sxs-lookup"><span data-stu-id="d7ebf-108">The GLU callback functions, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), are similar to the OpenGL polygon functions.</span></span>

<span data-ttu-id="d7ebf-109">In der Regel speichern Sie die Daten für die Dreiecke, Dreiecksnetze und Dreiecks Lüfter in benutzerdefinierten Datenstrukturen oder in OpenGL-Anzeigelisten.</span><span class="sxs-lookup"><span data-stu-id="d7ebf-109">They typically save the data for the triangles, triangle meshes, and triangle fans in user-defined data structures or in OpenGL display lists.</span></span> <span data-ttu-id="d7ebf-110">Um die Polygone zu rendieren, durchläuft anderer Code die Datenstrukturen oder ruft die Anzeigelisten auf.</span><span class="sxs-lookup"><span data-stu-id="d7ebf-110">To render the polygons, other code traverses the data structures or calls the display lists.</span></span> <span data-ttu-id="d7ebf-111">Obwohl die Rückruf Funktionen OpenGL-Funktionen aufrufen können, um Polygone direkt anzuzeigen, wird dies in der Regel nicht durchgeführt, da das Mosaik Rechenressourcen intensiv sein kann.</span><span class="sxs-lookup"><span data-stu-id="d7ebf-111">Although the callback functions could call OpenGL functions to display polygons directly, this is usually not done, as tessellation can be computationally resource-intensive.</span></span> <span data-ttu-id="d7ebf-112">Es empfiehlt sich, die Daten zu speichern, wenn Sie die Möglichkeit haben, Sie erneut anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d7ebf-112">It's a good idea to save the data if there is any chance that you want to display it again.</span></span> <span data-ttu-id="d7ebf-113">Es ist garantiert, dass die glu-Mosaik Funktionen keine neuen Scheitel Punkte zurückgeben, sodass keine interpolung von Scheitel Punkten, Texturkoordinaten oder Farben erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d7ebf-113">The GLU tessellation functions are guaranteed never to return any new vertices, so interpolation of vertices, texture coordinates, or colors is never required.</span></span>

 

 





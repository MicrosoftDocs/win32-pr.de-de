---
title: Verwenden von Evaluatoren
description: Verwenden von Evaluatoren
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, Evaluators
- Evaluatoren OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309643"
---
# <a name="using-evaluators"></a><span data-ttu-id="4a7e9-105">Verwenden von Evaluatoren</span><span class="sxs-lookup"><span data-stu-id="4a7e9-105">Using Evaluators</span></span>

<span data-ttu-id="4a7e9-106">Mit den OpenGL-Auswertungsfunktionen können Sie eine polynomale Zuordnung verwenden, um Vertices, normale, Texturkoordinaten und Farben zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="4a7e9-106">The OpenGL evaluator functions allow you to use a polynomial mapping to produce vertices, normals, texture coordinates, and colors.</span></span> <span data-ttu-id="4a7e9-107">Diese berechneten Werte werden dann an die Verarbeitungs Pipeline weitergegeben, als würden Sie direkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="4a7e9-107">These calculated values are then passed on to the processing pipeline as if they had been directly specified.</span></span> <span data-ttu-id="4a7e9-108">Die auswerterfunktionen sind auch die Grundlage für die NURBS-Funktionen (Non-Uniform Rational B-Spline), mit denen Sie Kurven und Oberflächen definieren können, wie unter [OpenGL Utility Library](opengl-utility-library.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a7e9-108">The evaluator functions are also the basis for the NURBS (Non-Uniform Rational B-Spline) functions, which allow you to define curves and surfaces, as described under [OpenGL Utility library](opengl-utility-library.md).</span></span>

<span data-ttu-id="4a7e9-109">Der erste Schritt bei der Verwendung von auswergratoren besteht darin, die entsprechende eindimensionale oder zweidimensionale polynomenzuordnung mithilfe von " [**glmap \***](glmap1.md)" zu definieren.</span><span class="sxs-lookup"><span data-stu-id="4a7e9-109">The first step in using evaluators is to define the appropriate one- or two-dimensional polynomial mapping using [**glMap\***](glmap1.md).</span></span> <span data-ttu-id="4a7e9-110">Sie können dann die Domänen Werte für diese Zuordnung auf zwei Arten angeben und auswerten:</span><span class="sxs-lookup"><span data-stu-id="4a7e9-110">You can then specify and evaluate the domain values for this map in one of two ways:</span></span>

-   <span data-ttu-id="4a7e9-111">Definieren Sie eine Reihe von gleichmäßig zugeordneten Domänen Werten, die mithilfe von [**glmapgrid**](glmapgrid-functions.md) zugeordnet werden sollen, und evaluieren Sie dann eine rechteckige Teilmenge dieses Rasters mit [**glevalmesh**](glevalmesh-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4a7e9-111">Define a series of evenly spaced domain values to be mapped using [**glMapGrid**](glmapgrid-functions.md) and then evaluate a rectangular subset of that grid with [**glEvalMesh**](glevalmesh-functions.md).</span></span> <span data-ttu-id="4a7e9-112">Ein einzelner Punkt des Rasters kann mithilfe von [**glevalpoint**](glevalpoint.md)ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="4a7e9-112">A single point of the grid can be evaluated using [**glEvalPoint**](glevalpoint.md).</span></span>
-   <span data-ttu-id="4a7e9-113">Geben Sie einen gewünschten Domänen Wert explizit als Argument an, das die Zuordnungen mit diesem Wert auswertet.</span><span class="sxs-lookup"><span data-stu-id="4a7e9-113">Explicitly specify a desired domain value as an argument, which evaluates the maps at that value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a7e9-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a7e9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a7e9-115">Evaluatorreferenz</span><span class="sxs-lookup"><span data-stu-id="4a7e9-115">Evaluators Reference</span></span>](evaluators-reference.md)
</dt> </dl>

 

 





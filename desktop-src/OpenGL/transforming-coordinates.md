---
title: Transformieren von Koordinaten
description: Die OpenGL Utility Library (GLU) stellt mehrere häufig verwendete Matrix Transformations Funktionen bereit.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- OpenGL-Hilfsprogramm (GLU), Matrix Transformations Funktionen
- GLU (OpenGL-Hilfsprogramm), Matrix Transformations Funktionen
- Matrix Transformations Funktionen OpenGL
- OpenGL-Hilfsprogramm (GLU), Transformieren von Koordinaten
- GLU (OpenGL-Hilfsprogramm), Transformieren von Koordinaten
- Transformieren von Koordinaten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713937"
---
# <a name="transforming-coordinates"></a><span data-ttu-id="5abc6-109">Transformieren von Koordinaten</span><span class="sxs-lookup"><span data-stu-id="5abc6-109">Transforming Coordinates</span></span>

<span data-ttu-id="5abc6-110">Die OpenGL Utility Library (GLU) stellt mehrere häufig verwendete Matrix Transformations Funktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5abc6-110">The OpenGL Utility library (GLU) provides several commonly used matrix transformation functions.</span></span> <span data-ttu-id="5abc6-111">Sie können einen zweidimensionalen orthografischen Anzeigebereich mit [**gluOrtho2D**](gluortho2d.md), ein Standardmäßiges perspektivisches Ansichts Volume mithilfe von " [**gluperspective**](gluperspective.md)" oder ein Ansichts Volume einrichten, das auf einem angegebenen Punkt mit " [**glulookat**](glulookat.md)" zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="5abc6-111">You can set up a two-dimensional orthographic viewing region with [**gluOrtho2D**](gluortho2d.md), a standard perspective view volume using [**gluPerspective**](gluperspective.md), or a view volume that is centered on a specified eyepoint with [**gluLookAt**](glulookat.md).</span></span> <span data-ttu-id="5abc6-112">Jede dieser Funktionen erstellt die gewünschte Matrix und wendet sie mit [**glmultmatrix**](glmultmatrix.md)auf die aktuelle Matrix an.</span><span class="sxs-lookup"><span data-stu-id="5abc6-112">Each of these functions creates the desired matrix and applies it to the current matrix using [**glMultMatrix**](glmultmatrix.md).</span></span>

<span data-ttu-id="5abc6-113">Die Funktion " [**glupickmatrix**](glupickmatrix.md) " vereinfacht die Auswahl einer Auswahl Matrix, indem eine Matrix erstellt wird, die das Zeichnen auf einen kleinen Bereich des Viewports einschränkt.</span><span class="sxs-lookup"><span data-stu-id="5abc6-113">The [**gluPickMatrix**](glupickmatrix.md) function simplifies selection of a picking matrix by creating a matrix that restricts drawing to a small region of the viewport.</span></span> <span data-ttu-id="5abc6-114">Wenn Sie die Szene nach dem Anwenden dieser Matrix im Auswahlmodus erneut Renderen, werden alle Objekte, die in der Nähe des Cursors gezeichnet werden, ausgewählt, und die Informationen zu Ihnen werden im Auswahl Puffer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5abc6-114">If you re-render the scene in selection mode after this matrix has been applied, all objects that would be drawn near the cursor will be selected, and information about them will be stored in the selection buffer.</span></span> <span data-ttu-id="5abc6-115">Weitere Informationen zum Auswahlmodus finden Sie unter "Auswahl und Feedback durchführen" Auswahl [und Feedback](performing-selection-and-feedback.md).</span><span class="sxs-lookup"><span data-stu-id="5abc6-115">For more information about selection mode, see "Performing Selection and Feedback" [Performing Selection and Feedback](performing-selection-and-feedback.md).</span></span>

<span data-ttu-id="5abc6-116">Um zu ermitteln, an welcher Stelle im Fenster ein Objekt gezeichnet wird, verwenden Sie " [**gluproject**](gluproject.md)", das die angegebenen Objekt Koordinaten " *objX*", " *objy*" und " *objz* " mithilfe von *modelmatrix*, *projmatrix* und *Viewport* in Fenster Koordinaten konvertiert.</span><span class="sxs-lookup"><span data-stu-id="5abc6-116">To determine where in the window an object is being drawn, use [**gluProject**](gluproject.md), which converts the specified object coordinates *objx*, *objy*, and *objz* into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="5abc6-117">Das Ergebnis wird in *Winx*, *Winy* und *Winz* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5abc6-117">The result is stored in *winx*, *winy*, and *winz*.</span></span> <span data-ttu-id="5abc6-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert "GL \_ true".</span><span class="sxs-lookup"><span data-stu-id="5abc6-118">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="5abc6-119">Wenn die Funktion fehlschlägt, ist der Rückgabewert "GL \_ false".</span><span class="sxs-lookup"><span data-stu-id="5abc6-119">If the function fails, the return value is GL\_FALSE.</span></span>

<span data-ttu-id="5abc6-120">Die Funktion " [**gluunproject**](gluunproject.md) " führt die umgekehrte Konvertierung durch: Sie transformiert die angegebenen Fenster Koordinaten *Winx*, *Winy* und *Winz* in Objekt Koordinaten mithilfe von *modelmatrix*, *projmatrix* und *Viewport*.</span><span class="sxs-lookup"><span data-stu-id="5abc6-120">The [**gluUnProject**](gluunproject.md) function performs the inverse conversion: it transforms the specified window coordinates *winx*, *winy*, and *winz* into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="5abc6-121">Das Ergebnis wird in *objX*, *objy* und *objz* gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5abc6-121">The result is stored in *objx*, *objy*, and *objz*.</span></span> <span data-ttu-id="5abc6-122">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert "GL \_ true".</span><span class="sxs-lookup"><span data-stu-id="5abc6-122">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="5abc6-123">Wenn die Funktion fehlschlägt, ist der Rückgabewert "GL \_ false".</span><span class="sxs-lookup"><span data-stu-id="5abc6-123">If the function fails, the return value is GL\_FALSE.</span></span>

 

 





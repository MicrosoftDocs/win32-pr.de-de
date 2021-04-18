---
title: Verwalten von Modi und Ausführung
description: Verwalten von Modi und Ausführung
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427e04b856c79c9adfdfebf4061f7e96f09db835
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340820"
---
# <a name="managing-modes-and-execution"></a><span data-ttu-id="59d88-104">Verwalten von Modi und Ausführung</span><span class="sxs-lookup"><span data-stu-id="59d88-104">Managing Modes and Execution</span></span>

<span data-ttu-id="59d88-105">Die Auswirkung vieler OpenGL-Funktionen hängt davon ab, ob ein bestimmter Modus wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="59d88-105">The effect of many OpenGL functions depends on whether a particular mode is in effect.</span></span> <span data-ttu-id="59d88-106">Die Funktionen " [**glEnable**](glenable.md) " und " [**gldeaktivieren**](gldisable.md) " legen solche Modi fest. " [**glisenabled**](glisenabled.md) " bestimmt, ob ein bestimmter Modus festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="59d88-106">The [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions set such modes; [**glIsEnabled**](glisenabled.md) determines whether a particular mode is set.</span></span>

<span data-ttu-id="59d88-107">Sie können die Ausführung von zuvor ausgestellten OpenGL-Funktionen mit [**glfinish**](glfinish.md)steuern, wodurch alle Funktionen beendet werden, oder [**glflush**](glflush.md), wodurch sichergestellt wird, dass alle diese Funktionen innerhalb einer begrenzten Zeit abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="59d88-107">You can control the execution of previously issued OpenGL functions with [**glFinish**](glfinish.md), which forces all such functions to finish, or [**glFlush**](glflush.md), which ensures that all such functions will be completed in a finite time.</span></span>

<span data-ttu-id="59d88-108">In einer bestimmten Implementierung von OpenGL können Sie möglicherweise bestimmte Verhalten mit Hinweisen mithilfe von [**glhint**](glhint.md)steuern.</span><span class="sxs-lookup"><span data-stu-id="59d88-108">In a particular implementation of OpenGL, you may be able to control certain behaviors with hints by using [**glHint**](glhint.md).</span></span> <span data-ttu-id="59d88-109">Solche Verhalten sind die Qualität der Farb-und Texturkoordinaten interpolung. die Genauigkeit von Nebel Berechnungen; und die Stichproben Qualität von Antialiasing Punkten, Linien oder Polygonen.</span><span class="sxs-lookup"><span data-stu-id="59d88-109">Such behaviors are the quality of color and texture coordinate interpolation; the accuracy of fog calculations; and the sampling quality of antialiased points, lines, or polygons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59d88-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59d88-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59d88-111">Modi und Ausführungs Verweis</span><span class="sxs-lookup"><span data-stu-id="59d88-111">Modes and Execution Reference</span></span>](modes-and-execution-reference.md)
</dt> </dl>

 

 





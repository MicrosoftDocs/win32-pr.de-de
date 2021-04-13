---
title: Portieren von Code im msingle-Modus
description: OpenGL hat keine Entsprechung für den msingle-, Single Matrix-Modus.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- IRIS GL Porting, msingle Mode
- Portieren von IRIS GL, msingle Mode
- Portieren auf OpenGL von IRIS GL, msingle Mode
- OpenGL-Portierung von IRIS GL, msingle Mode
- Msingle-Modus
- IRIS GL portieren, Einzel Matrix Modus
- Portieren von IRIS GL, Einzel Matrix Modus
- Portieren auf OpenGL von IRIS GL, Single Matrix Mode
- OpenGL-Portierung von IRIS GL, Einzel Matrix Modus
- Einzel Matrix Modus
- Double-Matrix-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8c62f93fa8e027dd1c91ca0bd40bc8e6ffaf9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388486"
---
# <a name="porting-msingle-mode-code"></a><span data-ttu-id="3ef05-114">Portieren von Code im msingle-Modus</span><span class="sxs-lookup"><span data-stu-id="3ef05-114">Porting MSINGLE Mode Code</span></span>

<span data-ttu-id="3ef05-115">OpenGL hat keine Entsprechung für den **msingle**-, Single Matrix-Modus.</span><span class="sxs-lookup"><span data-stu-id="3ef05-115">OpenGL has no equivalent for **MSINGLE**, single-matrix mode.</span></span> <span data-ttu-id="3ef05-116">Obwohl die Verwendung dieses Modus davon abgeraten hat, ist dies der Standardwert für Iris GL.</span><span class="sxs-lookup"><span data-stu-id="3ef05-116">Though use of this mode has been discouraged, it is the default for IRIS GL.</span></span> <span data-ttu-id="3ef05-117">Wenn Ihr IRIS GL-Programm den Einzel Matrix Modus verwendet, müssen Sie es so umschreiben, dass nur der Double-Matrix-Modus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ef05-117">If your IRIS GL program uses the single-matrix mode, you need to rewrite it to use double-matrix mode only.</span></span> <span data-ttu-id="3ef05-118">OpenGL befindet sich immer im Double-Matrix-Modus und ist anfänglich im GL \_ Modelview-Modus.</span><span class="sxs-lookup"><span data-stu-id="3ef05-118">OpenGL is always in double-matrix mode, and is initially in GL\_MODELVIEW mode.</span></span>

<span data-ttu-id="3ef05-119">Der größte IRIS GL-Code im msingle-Modus sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="3ef05-119">Most IRIS GL code in MSINGLE mode looks like this:</span></span>

``` syntax
projectionmatrix();
```

<span data-ttu-id="3ef05-120">Dabei ist *ProjectionMatrix* einer der folgenden **: Ortho**, **ortho2**, **Perspective** oder **Window**.</span><span class="sxs-lookup"><span data-stu-id="3ef05-120">where *projectionmatrix* is one of: **ortho**, **ortho2**, **perspective**, or **window**.</span></span> <span data-ttu-id="3ef05-121">Um auf OpenGL zu portieren, ersetzen Sie die " **msingle** -Mode *ProjectionMatrix* "-Funktion durch:</span><span class="sxs-lookup"><span data-stu-id="3ef05-121">To port to OpenGL, replace the **MSINGLE** -mode *projectionmatrix* function with:</span></span>


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 





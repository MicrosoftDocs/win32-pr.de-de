---
title: Portieren der BBOX2-Funktion
description: Es gibt keine OpenGL-Entsprechung für die Iris GL BBOX2-Funktion.
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- IRIS GL Porting, BBOX2-Funktion
- Portieren von IRIS GL, BBOX2-Funktion
- Portieren auf OpenGL von IRIS GL, BBOX2-Funktion
- OpenGL-Portierung von IRIS GL, BBOX2-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21060b8a11ccd6c44297c8b533bca98d79cc00f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712498"
---
# <a name="porting-the-bbox2-function"></a><span data-ttu-id="97898-107">Portieren der BBOX2-Funktion</span><span class="sxs-lookup"><span data-stu-id="97898-107">Porting the bbox2 Function</span></span>

<span data-ttu-id="97898-108">Es gibt keine OpenGL-Entsprechung für die Iris GL **BBOX2** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="97898-108">There is no OpenGL equivalent for the IRIS GL **bbox2** function.</span></span>

<span data-ttu-id="97898-109">**So portieren Sie Code, der BBOX2-Funktionen enthält**</span><span class="sxs-lookup"><span data-stu-id="97898-109">**To port code that contains bbox2 functions**</span></span>

1.  <span data-ttu-id="97898-110">Erstellen Sie eine neue (OpenGL) Anzeigeliste, die alle Elemente in der entsprechenden IRIS GL-Anzeigeliste enthält, mit Ausnahme des Aufrufes **BBOX2**.</span><span class="sxs-lookup"><span data-stu-id="97898-110">Create a new (OpenGL) display list that contains everything in the equivalent IRIS GL display list except the call to **bbox2**.</span></span>
2.  <span data-ttu-id="97898-111">Verwenden Sie den entsprechenden Windows-Code, um ein Rechteck mit der gleichen Größe wie das IRIS GL- **bFeld** zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="97898-111">Use appropriate Windows code to draw a rectangle the same size as the IRIS GL **bbox**.</span></span>

 

 





---
title: Erweiterte Drehung
description: In diesem Abschnitt wird erläutert, wie ein Objekt basierend auf dem Ort, an dem der Benutzer die Drehung bearbeitet, gedreht wird.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Windows-Fingereingabe, Drehung
- Windows-Fingereingabe, erweiterte Drehung
- Windows-Fingereingabe, Manipulationen
- Manipulationen, Drehung
- Manipulationen, erweiterte Drehung
- Rotation, erweitert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a84679f4189d28941262cda2585887b0932c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947433"
---
# <a name="advanced-rotation"></a><span data-ttu-id="498d6-109">Erweiterte Drehung</span><span class="sxs-lookup"><span data-stu-id="498d6-109">Advanced Rotation</span></span>

<span data-ttu-id="498d6-110">In diesem Abschnitt wird erläutert, wie ein Objekt basierend auf dem Ort, an dem der Benutzer die Drehung bearbeitet, gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="498d6-110">This section explains how to rotate an object based on where the user is performing the rotation manipulation.</span></span>

<span data-ttu-id="498d6-111">In der folgenden Abbildung werden zwei verschiedene Möglichkeiten veranschaulicht, wie ein Objekt gedreht werden kann.</span><span class="sxs-lookup"><span data-stu-id="498d6-111">The following image illustrates two different ways that an object can be rotated.</span></span>

![die Abbildung zeigt zwei Arten von Einzel fingerdrehung: um den Mittelpunkt oder um den Rand, wobei der Rand sowohl Drehung als auch Übersetzung umfasst.](images/rotation.png)

<span data-ttu-id="498d6-113">In Beispiel A wird das Objekt um den Mittelpunkt des Objekts manipuliert.</span><span class="sxs-lookup"><span data-stu-id="498d6-113">In example A, the object is manipulated around the center point of the object.</span></span> <span data-ttu-id="498d6-114">In Beispiel B wird das Objekt um den Mittelpunkt der Bearbeitung gedreht.</span><span class="sxs-lookup"><span data-stu-id="498d6-114">In example B, the object is rotated around the center point of the manipulation.</span></span> <span data-ttu-id="498d6-115">Zur Unterstützung von Manipulationen um einen anderen Punkt als den Mittelpunkt des Objekts muss eine verbundbearbeitung durchgeführt werden, die sowohl Drehung als auch Übersetzung ausführt.</span><span class="sxs-lookup"><span data-stu-id="498d6-115">To support manipulation around a point other than the center point of the object, you must perform a compound manipulation that performs both rotation and translation.</span></span> <span data-ttu-id="498d6-116">Der folgende Code zeigt, wie diese Manipulation ausgeführt und berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="498d6-116">The following code shows how this manipulation is performed and calculated.</span></span>


```C++
RotateVector(FLOAT *vector, FLOAT *tVector, FLOAT fAngle) {
    FLOAT fAngleRads = fAngle / 180.0f * 3.14159f;
    FLOAT fSin = sin(fAngleRads);
    FLOAT fCos = cos(fAngleRads);

    FLOAT fNewX = (vector[0]*fCos) - (vector[1]*fSin);
    FLOAT fNewY = (vector[0]*fSin) + (vector[1]*fCos);

    tVector[0] = fNewX;
    tVector[1] = fNewY;
}
     
```



## <a name="related-topics"></a><span data-ttu-id="498d6-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="498d6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="498d6-118">Erweiterte Manipulationen</span><span class="sxs-lookup"><span data-stu-id="498d6-118">Advanced Manipulations</span></span>](advanced-manipulations.md)
</dt> <dt>

[<span data-ttu-id="498d6-119">Manipulationen</span><span class="sxs-lookup"><span data-stu-id="498d6-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 





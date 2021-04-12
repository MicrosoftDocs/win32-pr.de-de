---
title: Erweiterte Erweiterung
description: Erweiterte Erweiterung
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Windows-Fingereingabe, Erweiterung
- Windows-Fingereingabe, erweiterte Erweiterung
- Windows-Fingereingabe, Manipulationen
- Manipulationen, Erweiterung
- Manipulationen, erweiterte Erweiterung
- Erweiterung, erweitert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81a3a395da053b7d0e8f79a115a2489f3e63190
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206325"
---
# <a name="advanced-expansion"></a><span data-ttu-id="4db4e-109">Erweiterte Erweiterung</span><span class="sxs-lookup"><span data-stu-id="4db4e-109">Advanced Expansion</span></span>

<span data-ttu-id="4db4e-110">Die folgende Abbildung zeigt zwei Möglichkeiten, wie ein Objekt erweitert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4db4e-110">The following illustration shows two ways that an object can be expanded.</span></span>

![die Abbildung zeigt eine einfache Erweiterung um den Mittelpunkt eines Objekts und eine erweiterte Erweiterung um den Mittelpunkt der Bearbeitung.](images/expansion.png)

<span data-ttu-id="4db4e-112">In Beispiel A, dem einfachen Erweiterungs Beispiel, wird das-Objekt um seinen Mittelpunkt erweitert.</span><span class="sxs-lookup"><span data-stu-id="4db4e-112">In example A, the simple expansion example, the object is expanded around its center point.</span></span> <span data-ttu-id="4db4e-113">In Beispiel B wird das Objekt um den Mittelpunkt der Bearbeitung erweitert.</span><span class="sxs-lookup"><span data-stu-id="4db4e-113">In example B, the object is expanded around the center point of the manipulation.</span></span> <span data-ttu-id="4db4e-114">Um dies zu ermöglichen, müssen Sie das Objekt übersetzen, während es erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="4db4e-114">To enable this, you must translate the object while it is being expanded.</span></span> <span data-ttu-id="4db4e-115">Die Menge, die Sie das Objekt übersetzen, entspricht der Entfernung vom Mittelpunkt des Objekts bis zum Mittelpunkt der Bewegung.</span><span class="sxs-lookup"><span data-stu-id="4db4e-115">The amount that you will translate the object is the same as the distance from the center of the object to the center point of the gesture.</span></span> <span data-ttu-id="4db4e-116">Intuitiv ist es so, als ob Sie das Objekt vom Mittelpunkt der Erweiterungs Geste erweitern und es dann verschieben, damit es sich immer noch in der gleichen Mitte wie die anfängliche Position befindet.</span><span class="sxs-lookup"><span data-stu-id="4db4e-116">Intuitively, it is as though you are expanding the object from the center point of your expansion gesture and then moving it so that it is still at the same center as its initial position.</span></span> <span data-ttu-id="4db4e-117">Der folgende Code zeigt eine Möglichkeit, wie dieses Konzept angewendet werden kann, um die Erweiterung um einen Mittelpunkt zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4db4e-117">The following code shows one way that this concept can be applied to enable expansion around a center point.</span></span>


```C++
    if(m_fFactor != 1.0f)
    {
        // We represent our vectors as an array.
        // x: vx[0], y: vx[1]

        FLOAT v1[2];
        v1[0] = this->get_CenterX() - fOffset[0];
        v1[1] = this->get_CenterY() - fOffset[1];

        FLOAT v2[2];
        v2[0] = v1[0] * m_fFactor;
        v2[1] = v1[1] * m_fFactor;
        
        m_fdX += v2[0] - v1[0];
        m_fdY += v2[1] - v1[1];
    }
   
```



## <a name="related-topics"></a><span data-ttu-id="4db4e-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4db4e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4db4e-119">Manipulationen</span><span class="sxs-lookup"><span data-stu-id="4db4e-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 





---
title: Erweiterte Übersetzung
description: Erweiterte Übersetzung
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Windows-Fingereingabe, Übersetzung
- Windows-Fingereingabe, erweiterte Übersetzung
- Windows-Fingereingabe, Manipulationen
- Manipulationen, Übersetzung
- Manipulationen, erweiterte Übersetzung
- Verschiebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc383c71e1f1417d30b64db18aa627039602b942
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855503"
---
# <a name="advanced-translation"></a><span data-ttu-id="5b966-109">Erweiterte Übersetzung</span><span class="sxs-lookup"><span data-stu-id="5b966-109">Advanced Translation</span></span>

<span data-ttu-id="5b966-110">Die folgende Abbildung zeigt zwei Interpretationen der Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="5b966-110">The following illustration shows two interpretations of translation.</span></span>

![Abbildung, die zuerst die einfache Übersetzung anzeigt, bei der ein Objekt ohne Drehung verschoben wird, und dann die erweiterte Übersetzung anzeigt, die das Verschieben mit Drehung einschließt](images/translation.png)

<span data-ttu-id="5b966-112">In Beispiel A, dem Beispiel für die einfache Übersetzung, wird das Objekt ohne Drehung verschoben.</span><span class="sxs-lookup"><span data-stu-id="5b966-112">In example A, the simple translation example, the object is moved without rotation.</span></span> <span data-ttu-id="5b966-113">In Beispiel B wird das Objekt während der Übersetzung gedreht, je nachdem, wo sich der Objekt Kontaktpunkt befindet.</span><span class="sxs-lookup"><span data-stu-id="5b966-113">In example B, the object is rotated during the translation, depending on where the object contact point is.</span></span> <span data-ttu-id="5b966-114">Wenn Sie die Drehung mit einem Finger wie in [Einzel Finger Drehung](single-finger-rotation.md)beschrieben aktivieren, können Sie die komplexe Übersetzung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5b966-114">If you enable single-finger rotation as described in [Single-Finger Rotation](single-finger-rotation.md), you can enable complex translation.</span></span> <span data-ttu-id="5b966-115">Das folgende Diagramm zeigt die verschiedenen Komponenten der Einzel Finger Drehung, wenn Sie die Übersetzung durchführen.</span><span class="sxs-lookup"><span data-stu-id="5b966-115">The following diagram shows the various components of single-finger rotation when you are performing translation.</span></span>

![die Abbildung zeigt die Komponenten der Einzel Finger Drehung: pivotpointx, pivotpointy und pivotradius.](images/translation-complex-components.png)

<span data-ttu-id="5b966-117">Beim Verschieben des Objekts wird der RADIUS neu berechnet, und der Pivotpunkt wird verschoben.</span><span class="sxs-lookup"><span data-stu-id="5b966-117">As the object is moved, the radius is recalculated and the pivot point is moved.</span></span>

<span data-ttu-id="5b966-118">Der folgende Code zeigt eine Möglichkeit, wie Sie dies in einer Implementierung von [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) durchführen können, die eine komplexe Übersetzung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5b966-118">The following code shows one way that you can do this in an implementation of [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) that enables complex translation.</span></span>


```C++
    //Apply transformation based on rotationDelta (in radians)
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    // Set values for one finger rotations
    FLOAT fPivotRadius = (FLOAT)(m_dObj->get_Width() + m_dObj->get_Height())/8.0f;
    FLOAT fPivotPtX = m_dObj->get_CenterX();
    FLOAT fPivotPtY = m_dObj->get_CenterY();
        
    m_manip->put_PivotPointX(fPivotPtX);
    m_manip->put_PivotPointY(fPivotPtY);
    m_manip->put_PivotRadius(fPivotRadius);       
   
```



> [!Note]  
> <span data-ttu-id="5b966-119">Objekt Transformationen treten auf, bevor die pivotpunkte und der Radius berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="5b966-119">Object transformations occur before the pivot points and radius are calculated.</span></span> <span data-ttu-id="5b966-120">Auf diese Weise wird das Objekt ordnungsgemäß verschoben, wenn der Benutzer während des Verschiebens eine Erweiterung des Objekts ausführt.</span><span class="sxs-lookup"><span data-stu-id="5b966-120">In this manner the object will move correctly if the user performs expansion on the object while it is moving.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5b966-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b966-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b966-122">Manipulationen</span><span class="sxs-lookup"><span data-stu-id="5b966-122">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 





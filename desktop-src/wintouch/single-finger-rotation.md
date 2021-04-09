---
title: Single-Finger Drehung
description: In diesem Abschnitt wird erläutert, wie ein Objekt mithilfe eines pivotpunkts gedreht wird.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows-Fingereingabe, Drehung
- Windows-Fingereingabe, Manipulationen
- Windows Touch, Einzel Finger Drehung
- Windows-Fingereingabe, pivotpunktdrehung
- Manipulationen, Drehung
- Drehung, pivotpunkte
- Drehung, Einzel Finger
- Gesten, Einzel Finger Drehung
- Rotation mit einem Finger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d74263f502749e2aaf942c4bbec5aa0a284e76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855739"
---
# <a name="single-finger-rotation"></a><span data-ttu-id="72267-112">Single-Finger Drehung</span><span class="sxs-lookup"><span data-stu-id="72267-112">Single-Finger Rotation</span></span>

<span data-ttu-id="72267-113">In diesem Abschnitt wird erläutert, wie ein Objekt mithilfe eines pivotpunkts gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="72267-113">This section explains how to rotate an object using a pivot point.</span></span>

<span data-ttu-id="72267-114">In der folgenden Abbildung wird die Rotation mit einem Finger veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="72267-114">The following image illustrates single-finger rotation.</span></span>

![Abbildung mit zwei Arten von Einzel fingerdrehung: um das Zentrum oder um den Rand herum](images/sfrotation.png)

<span data-ttu-id="72267-116">In Beispiel A wird das Objekt um den Mittelpunkt des Objekts mit der Drehungs Bewegung gedreht.</span><span class="sxs-lookup"><span data-stu-id="72267-116">In example A, the object is rotated around the center point of the object by using the rotation gesture.</span></span> <span data-ttu-id="72267-117">In Beispiel B wird das Objekt gedreht, indem ein einzelner Finger um den Rand des Objekts bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="72267-117">In example B, the object is rotated by moving a single finger around the edge of the object.</span></span> <span data-ttu-id="72267-118">Der Manipulations Prozessor ermöglicht diese Rotation mithilfe von Pivotpunkt-und Pivot-RADIUS-Werten.</span><span class="sxs-lookup"><span data-stu-id="72267-118">The manipulation processor enables this rotation by using pivot point and pivot radius values.</span></span> <span data-ttu-id="72267-119">In der folgenden Abbildung werden die Komponenten der Einzel Finger Drehung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="72267-119">The following image illustrates the components of single-finger rotation.</span></span>

![die Abbildung zeigt die Komponenten der Einzel Finger Drehung: pivotpointx, pivotpointy und pivotradius.](images/sfrotation-components.png)

<span data-ttu-id="72267-121">Nachdem Sie die Werte [**pivotpointx**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**pivotpointy**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)und [**pivotradius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) festgelegt haben, enthalten nachfolgende Übersetzungs Meldungen die Drehung.</span><span class="sxs-lookup"><span data-stu-id="72267-121">After you set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy), and [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) values, subsequent translation messages will incorporate rotation.</span></span> <span data-ttu-id="72267-122">Je größer der pivotradius ist, desto größer ist die Änderung in x und y, um das Objekt zu drehen.</span><span class="sxs-lookup"><span data-stu-id="72267-122">The larger the pivot radius, the greater the change in x and y must be to rotate the object.</span></span> <span data-ttu-id="72267-123">Der folgende Code zeigt, wie diese Werte im Bearbeitungs Prozessor festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="72267-123">The following code shows how these values could be set in the manipulation processor.</span></span>


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // Set the pivot point to the object's center and then set the radius 
    // to the distance from the center to the edge of the object.
    m_pManip->put_PivotPointX(m_objectRef->xPos);
    m_pManip->put_PivotPointY(m_objectRef->yPos);
    
    float fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->get_Width()/2, 2) + pow(m_dObj->get_Height()/2, 2)))*0.4f;
    
    m_pManip->put_PivotRadius(fPivotRadius);
  

    return S_OK;
}    
     
```



<span data-ttu-id="72267-124">Im vorherigen Beispiel wird der Abstand zum Rand des Objekts (auf 40 Prozent skaliert) als pivotradius verwendet.</span><span class="sxs-lookup"><span data-stu-id="72267-124">In the previous example, the distance to the edge of the object (scaled to 40 percent) is used as the pivot radius.</span></span> <span data-ttu-id="72267-125">Da die Objektgröße berücksichtigt wird, ist diese Berechnung für jedes Objekt Delta gültig.</span><span class="sxs-lookup"><span data-stu-id="72267-125">Because the object size is taken into consideration, this calculation is valid for every object delta.</span></span> <span data-ttu-id="72267-126">Beim Skalieren des Objekts wächst der pivotradius.</span><span class="sxs-lookup"><span data-stu-id="72267-126">As the object scales, the pivot radius grows.</span></span> <span data-ttu-id="72267-127">Dieser Wert und die x-und y-Werte des-Objekts werden an den Manipulations Prozessor übermittelt, um das Objekt um den Pivotpunkt zu drehen.</span><span class="sxs-lookup"><span data-stu-id="72267-127">This value and the object's center x and y values are passed to the manipulation processor to rotate the object around the pivot point.</span></span>

> [!Note]  
> <span data-ttu-id="72267-128">Der [**pivotradius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) -Wert darf niemals zwischen 0,0 und 1,0 liegen.</span><span class="sxs-lookup"><span data-stu-id="72267-128">The [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) value should never be between 0.0 and 1.0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="72267-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72267-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72267-130">Manipulationen</span><span class="sxs-lookup"><span data-stu-id="72267-130">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> <dt>

[<span data-ttu-id="72267-131">**Pivotradius**</span><span class="sxs-lookup"><span data-stu-id="72267-131">**PivotRadius**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[<span data-ttu-id="72267-132">**Pivotpointx**</span><span class="sxs-lookup"><span data-stu-id="72267-132">**PivotPointX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[<span data-ttu-id="72267-133">**Pivotpointy**</span><span class="sxs-lookup"><span data-stu-id="72267-133">**PivotPointY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 





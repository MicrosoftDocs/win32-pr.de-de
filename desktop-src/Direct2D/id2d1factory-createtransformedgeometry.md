---
title: ID2D1Factory-Methode für die Methode "kreatetransformedgeometry" (D2d1. h)
description: Transformiert die angegebene Geometrie und speichert das Ergebnis als ID2D1TransformedGeometry-Objekt.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- Methoden der Methode "Direct2D"
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5da3b548c3118209c915714e03fe9e4061c77e96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360335"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a><span data-ttu-id="178da-104">ID2D1Factory:: kreatetransformedgeometry-Methoden</span><span class="sxs-lookup"><span data-stu-id="178da-104">ID2D1Factory::CreateTransformedGeometry methods</span></span>

<span data-ttu-id="178da-105">Transformiert die angegebene Geometrie und speichert das Ergebnis als [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="178da-105">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="178da-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="178da-106">Overload list</span></span>



| <span data-ttu-id="178da-107">Methode</span><span class="sxs-lookup"><span data-stu-id="178da-107">Method</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="178da-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="178da-108">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="178da-109">[**ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F \* , ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="178da-109">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F\*,ID2D1TransformedGeometry\*\*)**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span></span> | <span data-ttu-id="178da-110">Transformiert die angegebene Geometrie und speichert das Ergebnis als [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="178da-110">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |
| <span data-ttu-id="178da-111">[**ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F&, ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span><span class="sxs-lookup"><span data-stu-id="178da-111">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F&,ID2D1TransformedGeometry\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span></span>  | <span data-ttu-id="178da-112">Transformiert die angegebene Geometrie und speichert das Ergebnis als [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="178da-112">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="178da-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="178da-113">Remarks</span></span>

<span data-ttu-id="178da-114">Wie andere Ressourcen erbt eine transformierte Geometrie den Ressourcenbereich und die Threading Richtlinie der Factory, von der Sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="178da-114">Like other resources, a transformed geometry inherits the resource space and threading policy of the factory that created it.</span></span> <span data-ttu-id="178da-115">Dieses Objekt ist unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="178da-115">This object is immutable.</span></span>

<span data-ttu-id="178da-116">Beim Übertragen einer transformierten Geometrie mit der [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -Methode wird die Strichbreite von der auf die Geometrie angewendeten Transformation nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="178da-116">When stroking a transformed geometry with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method, the stroke width is not affected by the transform applied to the geometry.</span></span> <span data-ttu-id="178da-117">Die Strichbreite wird nur von der Welt Transformation beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="178da-117">The stroke width is only affected by the world transform.</span></span>

## <a name="examples"></a><span data-ttu-id="178da-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="178da-118">Examples</span></span>

<span data-ttu-id="178da-119">Im folgenden Beispiel wird ein [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))erstellt und dann gezeichnet, ohne es zu transformieren.</span><span class="sxs-lookup"><span data-stu-id="178da-119">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), then draws it without transforming it.</span></span> <span data-ttu-id="178da-120">Sie erzeugt die in der folgenden Abbildung gezeigte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="178da-120">It produces the output shown in the following illustration.</span></span>

![Abbildung eines Rechtecks](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



<span data-ttu-id="178da-122">Im nächsten Beispiel wird das Renderziel verwendet, um die Geometrie um den Faktor 3 zu skalieren, und dann gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="178da-122">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="178da-123">Die folgende Abbildung zeigt das Ergebnis des Zeichnens des Rechtecks ohne die Transformation und mit der Transformation. Gibt an, dass der Strich nach der Transformation dicker ist, auch wenn die Strichstärke 1 ist.</span><span class="sxs-lookup"><span data-stu-id="178da-123">The following illustration shows the result of drawing the rectangle without the transform and with the transform; notices that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![Darstellung eines kleineren Rechtecks innerhalb eines größeren Rechtecks mit einem dickeren Strich](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="178da-125">Im nächsten Beispiel wird die Methode " **kreatetransformedgeometry** " verwendet, um die Geometrie mit dem Faktor 3 zu skalieren, und dann gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="178da-125">The next example uses the **CreateTransformedGeometry** method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="178da-126">Sie erzeugt die in der folgenden Abbildung gezeigte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="178da-126">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="178da-127">Beachten Sie, dass, obwohl das Rechteck größer ist, der Strich nicht vergrößert wurde.</span><span class="sxs-lookup"><span data-stu-id="178da-127">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![Abbildung eines kleineren Rechtecks innerhalb eines größeren Rechtecks mit dem gleichen Strich](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a><span data-ttu-id="178da-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="178da-129">Requirements</span></span>



| <span data-ttu-id="178da-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="178da-130">Requirement</span></span> | <span data-ttu-id="178da-131">Wert</span><span class="sxs-lookup"><span data-stu-id="178da-131">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="178da-132">Header</span><span class="sxs-lookup"><span data-stu-id="178da-132">Header</span></span><br/>  | <dl> <span data-ttu-id="178da-133"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="178da-133"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="178da-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="178da-134">Library</span></span><br/> | <dl> <span data-ttu-id="178da-135"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="178da-135"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="178da-136">DLL</span><span class="sxs-lookup"><span data-stu-id="178da-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="178da-137"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="178da-137"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="178da-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="178da-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="178da-139">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="178da-139">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

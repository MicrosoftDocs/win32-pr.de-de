---
title: ID2D1RenderTarget setTransform-Methoden
description: Wendet die angegebene Transformation auf das Renderziel an und ersetzt dabei die vorhandene Transformation. Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- SetTransform-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 8310bf9e5c97beb3ea3cf3b2a9a513f606079a18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362166"
---
# <a name="id2d1rendertargetsettransform-methods"></a><span data-ttu-id="2c7be-105">ID2D1RenderTarget:: setTransform-Methoden</span><span class="sxs-lookup"><span data-stu-id="2c7be-105">ID2D1RenderTarget::SetTransform methods</span></span>

<span data-ttu-id="2c7be-106">Wendet die angegebene Transformation auf das Renderziel an und ersetzt dabei die vorhandene Transformation.</span><span class="sxs-lookup"><span data-stu-id="2c7be-106">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="2c7be-107">Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.</span><span class="sxs-lookup"><span data-stu-id="2c7be-107">All subsequent drawing operations occur in the transformed space.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2c7be-108">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="2c7be-108">Overload list</span></span>



| <span data-ttu-id="2c7be-109">Methode</span><span class="sxs-lookup"><span data-stu-id="2c7be-109">Method</span></span>                                                                                              | <span data-ttu-id="2c7be-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c7be-110">Description</span></span>                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7be-111">[**SetTransform (D2D1 \_ Matrix \_ 3x2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="2c7be-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="2c7be-112">Wendet die angegebene Transformation auf das Renderziel an und ersetzt dabei die vorhandene Transformation.</span><span class="sxs-lookup"><span data-stu-id="2c7be-112">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="2c7be-113">Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.</span><span class="sxs-lookup"><span data-stu-id="2c7be-113">All subsequent drawing operations occur in the transformed space.</span></span> <br/> |
| <span data-ttu-id="2c7be-114">[**SetTransform (D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="2c7be-114">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="2c7be-115">Wendet die angegebene Transformation auf das Renderziel an und ersetzt dabei die vorhandene Transformation.</span><span class="sxs-lookup"><span data-stu-id="2c7be-115">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="2c7be-116">Alle nachfolgenden Zeichnungsvorgänge erfolgen im transformierten Raum.</span><span class="sxs-lookup"><span data-stu-id="2c7be-116">All subsequent drawing operations occur in the transformed space.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="2c7be-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c7be-117">Examples</span></span>

<span data-ttu-id="2c7be-118">Im folgenden Beispiel wird die **setTransform** -Methode verwendet, um eine Drehung auf das Renderziel anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="2c7be-118">The following example uses the **SetTransform** method to apply a rotation to the render target.</span></span> <span data-ttu-id="2c7be-119">Das komplette Beispiel finden Sie unter Gewusst [wie: Drehen eines Objekts](how-to-rotate.md).</span><span class="sxs-lookup"><span data-stu-id="2c7be-119">For the complete example, see [How to Rotate an Object](how-to-rotate.md).</span></span>


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



<span data-ttu-id="2c7be-120">Weitere Beispiele, die zeigen, wie Sie ein Renderziel transformieren, finden Sie unter [Skalieren eines Objekts](how-to-scale.md), Vorgehens [Weise beim Verzerren eines](how-to-skew.md)Objekts und [Übersetzen eines Objekts](how-to-translate.md).</span><span class="sxs-lookup"><span data-stu-id="2c7be-120">For additional examples showing how to transform a render target, see [How to Scale an Object](how-to-scale.md), [How to Skew an Object](how-to-skew.md), and [How to Translate an Object](how-to-translate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c7be-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c7be-121">Requirements</span></span>



| <span data-ttu-id="2c7be-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c7be-122">Requirement</span></span> | <span data-ttu-id="2c7be-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2c7be-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7be-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2c7be-124">Library</span></span><br/> | <dl> <span data-ttu-id="2c7be-125"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c7be-125"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="2c7be-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2c7be-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c7be-127"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c7be-127"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c7be-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c7be-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c7be-129">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="2c7be-129">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="2c7be-130">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="2c7be-130">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="2c7be-131">Drehen eines Objekts</span><span class="sxs-lookup"><span data-stu-id="2c7be-131">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="2c7be-132">Skalieren eines Objekts</span><span class="sxs-lookup"><span data-stu-id="2c7be-132">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="2c7be-133">Vorgehensweise beim Verzerren eines Objekts</span><span class="sxs-lookup"><span data-stu-id="2c7be-133">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="2c7be-134">Übersetzen eines Objekts</span><span class="sxs-lookup"><span data-stu-id="2c7be-134">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="2c7be-135">Anwenden mehrerer Transformationen auf ein Objekt</span><span class="sxs-lookup"><span data-stu-id="2c7be-135">How to Apply Multiple Transforms to an Object</span></span>](how-to-apply-multiple-transforms.md)
</dt> </dl>

 


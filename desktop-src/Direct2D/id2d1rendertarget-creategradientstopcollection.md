---
title: ID2D1RenderTarget CreateGradientStopCollection-Methoden (D2d1 \_ 1.h)
description: Erstellt eine ID2D1GradientStopCollection aus dem angegebenen Array von D2D1 \_ GRADIENT \_ STOP-Strukturen.
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- CreateGradientStopCollection-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: f099c1c71015ca433299843d388085103571d31d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549415"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a><span data-ttu-id="0d4f7-104">ID2D1RenderTarget::CreateGradientStopCollection-Methoden</span><span class="sxs-lookup"><span data-stu-id="0d4f7-104">ID2D1RenderTarget::CreateGradientStopCollection methods</span></span>

<span data-ttu-id="0d4f7-105">Erstellt eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) aus dem angegebenen Array von [**D2D1 \_ GRADIENT \_ STOP-Strukturen.**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)</span><span class="sxs-lookup"><span data-stu-id="0d4f7-105">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) structures.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0d4f7-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="0d4f7-106">Overload list</span></span>



| <span data-ttu-id="0d4f7-107">Methode</span><span class="sxs-lookup"><span data-stu-id="0d4f7-107">Method</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="0d4f7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d4f7-108">Description</span></span>                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d4f7-109">**CreateGradientStopCollection(D2D1 \_ GRADIENT \_ STOP \* ,D2D1 \_ GAMMA,D2D1 \_ EXTEND \_ MODE,ID2D1GradientStopCollection \* \* )**</span><span class="sxs-lookup"><span data-stu-id="0d4f7-109">**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,D2D1\_GAMMA,D2D1\_EXTEND\_MODE,ID2D1GradientStopCollection\*\*)**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) | <span data-ttu-id="0d4f7-110">Erstellt eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) aus den angegebenen Farbverlaufsstopps, farbinterpolation gamma und dem Extend-Modus.</span><span class="sxs-lookup"><span data-stu-id="0d4f7-110">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops, color interpolation gamma, and extend mode.</span></span> <br/>                                                              |
| [<span data-ttu-id="0d4f7-111">**CreateGradientStopCollection(D2D1 \_ GRADIENT \_ STOP \* ,ID2D1GradientStopCollection \* \* )**</span><span class="sxs-lookup"><span data-stu-id="0d4f7-111">**CreateGradientStopCollection(D2D1\_GRADIENT\_STOP\*,ID2D1GradientStopCollection\*\*)**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)                                                            | <span data-ttu-id="0d4f7-112">Erstellt eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) aus den angegebenen Farbverlaufsstopps, die das Gamma der [**D2D1 \_ GAMMA \_ 2 2-Farbinterpolation \_**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) und den Klammererweiterungsmodus verwenden.</span><span class="sxs-lookup"><span data-stu-id="0d4f7-112">Creates an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from the specified gradient stops that uses the [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) color interpolation gamma and the clamp extend mode.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="0d4f7-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d4f7-113">Examples</span></span>

<span data-ttu-id="0d4f7-114">Im folgenden Beispiel wird ein Array von Farbverlaufsstopps erstellt und dann verwendet, um eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d4f7-114">The following example creates an array of gradient stops, then uses them to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



<span data-ttu-id="0d4f7-115">Im nächsten Codebeispiel wird [**id2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) verwendet, um eine [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d4f7-115">The next code example uses the [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to create an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span>


```C++
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}
```



## <a name="requirements"></a><span data-ttu-id="0d4f7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d4f7-116">Requirements</span></span>



| <span data-ttu-id="0d4f7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d4f7-117">Requirement</span></span> | <span data-ttu-id="0d4f7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0d4f7-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4f7-119">Header</span><span class="sxs-lookup"><span data-stu-id="0d4f7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0d4f7-120"><dt>D2d1 \_ 1.h (einschließlich D2d1.h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d4f7-120"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="0d4f7-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0d4f7-121">Library</span></span><br/> | <dl> <span data-ttu-id="0d4f7-122"><dt>D2d1.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d4f7-122"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0d4f7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0d4f7-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d4f7-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d4f7-124"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="0d4f7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d4f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d4f7-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="0d4f7-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="0d4f7-127">**D2D1 \_ GRADIENT \_ STOP**</span><span class="sxs-lookup"><span data-stu-id="0d4f7-127">**D2D1\_GRADIENT\_STOP**</span></span>](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[<span data-ttu-id="0d4f7-128">Erstellen eines linearen Farbverlaufspinsels</span><span class="sxs-lookup"><span data-stu-id="0d4f7-128">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="0d4f7-129">Erstellen eines Pinsels mit radialen Farbverläufen</span><span class="sxs-lookup"><span data-stu-id="0d4f7-129">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="0d4f7-130">Übersicht über Pinsel</span><span class="sxs-lookup"><span data-stu-id="0d4f7-130">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>
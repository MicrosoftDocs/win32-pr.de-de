---
title: ID2D1Factory-Methoden für die Methode "deestrokestyle"
description: Erstellt eine ID2D1StrokeStyle, die die Start Abdeckung, das Bindestrich Muster und andere Features eines Strichs beschreibt.
ms.assetid: cc7bd68b-a6eb-4d05-b331-032ce80f375c
keywords:
- Methoden für "kreatestrokestyle" Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 09a578cafe6795bbf742d9dac114365d6e850586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372749"
---
# <a name="id2d1factorycreatestrokestyle-methods"></a><span data-ttu-id="c472b-104">ID2D1Factory:: kreatestrokestyle-Methoden</span><span class="sxs-lookup"><span data-stu-id="c472b-104">ID2D1Factory::CreateStrokeStyle methods</span></span>

<span data-ttu-id="c472b-105">Erstellt eine [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) , die die Start Abdeckung, das Bindestrich Muster und andere Features eines Strichs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c472b-105">Creates an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) that describes start cap, dash pattern, and other features of a stroke.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c472b-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="c472b-106">Overload list</span></span>



| <span data-ttu-id="c472b-107">Methode</span><span class="sxs-lookup"><span data-stu-id="c472b-107">Method</span></span>                                                                                                                                                                                                  | <span data-ttu-id="c472b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c472b-108">Description</span></span>                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c472b-109">[**Kreatestrokestyle (Eigenschaften des D2D1- \_ Strich \_ Stils \_&, float \* , uint, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties__constfloat_uint32_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="c472b-109">[**CreateStrokeStyle(D2D1\_STROKE\_STYLE\_PROPERTIES&, FLOAT\*, UINT, ID2D1StrokeStyle\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties__constfloat_uint32_id2d1strokestyle))</span></span>  | <span data-ttu-id="c472b-110">Erstellt eine [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) , die die Start Abdeckung, das Bindestrich Muster und andere Features eines Strichs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c472b-110">Creates an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) that describes start cap, dash pattern, and other features of a stroke.</span></span><br/> |
| <span data-ttu-id="c472b-111">[**Kreatestrokestyle (Eigenschaften des D2D1- \_ Strich \_ Stils \_ \* , float \* , uint, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties_constfloat_uint32_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="c472b-111">[**CreateStrokeStyle(D2D1\_STROKE\_STYLE\_PROPERTIES\*, FLOAT\*, UINT, ID2D1StrokeStyle\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties_constfloat_uint32_id2d1strokestyle))</span></span> | <span data-ttu-id="c472b-112">Erstellt eine [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) , die die Start Abdeckung, das Bindestrich Muster und andere Features eines Strichs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c472b-112">Creates an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) that describes start cap, dash pattern, and other features of a stroke.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="c472b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c472b-113">Examples</span></span>

<span data-ttu-id="c472b-114">Im folgenden Beispiel wird ein Strich erstellt, der ein benutzerdefiniertes Bindestrich Muster verwendet.</span><span class="sxs-lookup"><span data-stu-id="c472b-114">The following example creates a stroke that uses a custom dash pattern.</span></span>


```C++
// Dash array for dashStyle D2D1_DASH_STYLE_CUSTOM
float dashes[] = {1.0f, 2.0f, 2.0f, 3.0f, 2.0f, 2.0f};

// Stroke Style with Dash Style -- Custom
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateStrokeStyle(
        D2D1::StrokeStyleProperties(
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_ROUND,
            D2D1_LINE_JOIN_MITER,
            10.0f,
            D2D1_DASH_STYLE_CUSTOM,
            0.0f),
        dashes,
        ARRAYSIZE(dashes),
        &m_pStrokeStyleCustomOffsetZero
        );
}
```



<span data-ttu-id="c472b-115">Im nächsten Beispiel wird der Strich Stil verwendet, um eine Linie zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="c472b-115">The next example uses the stroke style when drawing a line.</span></span>


```C++
m_pRenderTarget->DrawLine(
    D2D1::Point2F(0, 310),
    D2D1::Point2F(200, 310),
    m_pCornflowerBlueBrush,
    10.0f,
    m_pStrokeStyleCustomOffsetZero
    );
```



## <a name="requirements"></a><span data-ttu-id="c472b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c472b-116">Requirements</span></span>



| <span data-ttu-id="c472b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c472b-117">Requirement</span></span> | <span data-ttu-id="c472b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c472b-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c472b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c472b-119">Library</span></span><br/> | <dl> <span data-ttu-id="c472b-120"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c472b-120"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="c472b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c472b-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="c472b-122"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c472b-122"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c472b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c472b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c472b-124">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="c472b-124">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 


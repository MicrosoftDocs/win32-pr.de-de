---
title: ID2D1Factory-Methode für die Methode "Methode" (D2d1. h)
description: Erstellt ein ID2D1EllipseGeometry-.
ms.assetid: 4c03bb0b-74fe-456a-aa26-5449d758c0ea
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
ms.openlocfilehash: ca991732b9a80fd93e3df3c2b72493f5195ea0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367681"
---
# <a name="id2d1factorycreateellipsegeometry-methods"></a><span data-ttu-id="2d5e7-104">ID2D1Factory:: kreateellipcgeometry-Methoden</span><span class="sxs-lookup"><span data-stu-id="2d5e7-104">ID2D1Factory::CreateEllipseGeometry methods</span></span>

<span data-ttu-id="2d5e7-105">Erstellt ein [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)-.</span><span class="sxs-lookup"><span data-stu-id="2d5e7-105">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span>

### <a name="overload-list"></a><span data-ttu-id="2d5e7-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="2d5e7-106">Overload list</span></span>



| <span data-ttu-id="2d5e7-107">Methode</span><span class="sxs-lookup"><span data-stu-id="2d5e7-107">Method</span></span>                                                                                                                                                      | <span data-ttu-id="2d5e7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d5e7-108">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="2d5e7-109">[**"Kreateellipsegeometry" (D2D1 \_ Ellipse&, ID2D1EllipseGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry))</span><span class="sxs-lookup"><span data-stu-id="2d5e7-109">[**CreateEllipseGeometry(D2D1\_ELLIPSE&,ID2D1EllipseGeometry\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry))</span></span>  | <span data-ttu-id="2d5e7-110">Erstellt ein [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)-.</span><span class="sxs-lookup"><span data-stu-id="2d5e7-110">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span> <br/> |
| <span data-ttu-id="2d5e7-111">[**"Kreateellipsegeometry" (D2D1 \_ Ellipse \* , ID2D1EllipseGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371265(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2d5e7-111">[**CreateEllipseGeometry(D2D1\_ELLIPSE\*,ID2D1EllipseGeometry\*\*)**](/previous-versions/windows/desktop/legacy/dd371265(v=vs.85))</span></span> | <span data-ttu-id="2d5e7-112">Erstellt ein [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)-.</span><span class="sxs-lookup"><span data-stu-id="2d5e7-112">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="2d5e7-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d5e7-113">Examples</span></span>

<span data-ttu-id="2d5e7-114">Im folgenden werden zwei [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) -Objekte erstellt und mit den verschiedenen Modi zum Kombinieren von Geometrie kombiniert.</span><span class="sxs-lookup"><span data-stu-id="2d5e7-114">The following creates two [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects and combines them using the different geometry combine modes.</span></span>


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr = S_OK;
    ID2D1GeometrySink *pGeometrySink = NULL;

    // Create the first ellipse geometry to merge.
    const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
        D2D1::Point2F(75.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        circle1,
        &m_pCircleGeometry1
        );

    if (SUCCEEDED(hr))
    {
        // Create the second ellipse geometry to merge.
        const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
            D2D1::Point2F(125.0f, 75.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
    }


    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryUnion->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_UNION,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_INTERSECT to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryIntersect);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryIntersect->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_INTERSECT,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_XOR to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryXOR);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryXOR->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_XOR,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_EXCLUDE to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryExclude);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryExclude->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_EXCLUDE,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    return hr;
}
```



<span data-ttu-id="2d5e7-115">Mit diesem Code wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="2d5e7-115">This code produces the output shown in the following illustration.</span></span>

![Abbildung von zwei Ellipsen kombiniert mithilfe von vier Geometry-Kombi Modi (Union, Intersect, XOR und Exclude)](images/combine-modes.png)

## <a name="requirements"></a><span data-ttu-id="2d5e7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d5e7-117">Requirements</span></span>



| <span data-ttu-id="2d5e7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d5e7-118">Requirement</span></span> | <span data-ttu-id="2d5e7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2d5e7-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5e7-120">Header</span><span class="sxs-lookup"><span data-stu-id="2d5e7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2d5e7-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d5e7-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d5e7-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2d5e7-122">Library</span></span><br/> | <dl> <span data-ttu-id="2d5e7-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d5e7-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="2d5e7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2d5e7-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="2d5e7-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d5e7-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d5e7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d5e7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d5e7-127">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="2d5e7-127">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

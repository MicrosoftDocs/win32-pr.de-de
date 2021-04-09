---
title: Kombinieren von Geometrien
description: Zeigt, wie zwei Geometrien mithilfe von Direct2D kombiniert werden.
ms.assetid: c5413e59-ae73-4797-b4ad-3a78ad700634
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8332421c62f49b60bb2186118ac7f741922fdc7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039316"
---
# <a name="how-to-combine-geometries"></a><span data-ttu-id="48898-103">Kombinieren von Geometrien</span><span class="sxs-lookup"><span data-stu-id="48898-103">How to Combine Geometries</span></span>

<span data-ttu-id="48898-104">In diesem Thema wird beschrieben, wie zwei Geometrien kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="48898-104">This topic describes how to combine two geometries.</span></span> <span data-ttu-id="48898-105">Direct2D unterstützt vier Modi zum Kombinieren von Geometrien: Union, Intersect, XOR und Exclude.</span><span class="sxs-lookup"><span data-stu-id="48898-105">Direct2D supports four modes for combining geometries: Union, Intersect, XOR, and Exclude.</span></span> <span data-ttu-id="48898-106">Diese Modi werden im Enumeration-Typ [**D2D1- \_ \_ kombinierungsmodus**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) angegeben.</span><span class="sxs-lookup"><span data-stu-id="48898-106">These modes are specified in the [**D2D1\_COMBINE\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) enum type.</span></span>

<span data-ttu-id="48898-107">**So kombinieren Sie zwei Geometrien mithilfe eines der vier Modi**</span><span class="sxs-lookup"><span data-stu-id="48898-107">**To combine two geometries by using any of the four modes**</span></span>

1.  <span data-ttu-id="48898-108">Deklarieren Sie eine Pfad Geometrie: eine Variable vom Typ [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) , in der das Ergebnis der Geometrie Kombination gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="48898-108">Declare a path geometry: a variable of type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) that will store the result of geometry combination.</span></span>
2.  <span data-ttu-id="48898-109">Deklarieren Sie eine Geometry-Senke: eine Variable vom Typ [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) , in der die Pfad Geometrie gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="48898-109">Declare a geometry sink: a variable of type [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) that will store the path geometry.</span></span>
3.  <span data-ttu-id="48898-110">Erstellen Sie den Pfad Geometry-Objekt, indem Sie die [**ID2D1Factory:: createpathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="48898-110">Create the path geometry object by calling the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method.</span></span>
4.  <span data-ttu-id="48898-111">Öffnen Sie das Geometry-senktobjekt durch Aufrufen der [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) -Methode.</span><span class="sxs-lookup"><span data-stu-id="48898-111">Open the geometry sink object by calling the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>
5.  <span data-ttu-id="48898-112">Verwenden Sie einen der vier Modi, um die beiden Geometrien zu kombinieren, indem Sie die [**ID2D1EllipseGeometry:: combinewithgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="48898-112">Use one of the four modes to combine the two geometries by calling the [**ID2D1EllipseGeometry::CombineWithGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) method.</span></span>
6.  <span data-ttu-id="48898-113">Schließen Sie das Objekt "Geometry Sink".</span><span class="sxs-lookup"><span data-stu-id="48898-113">Close the geometry sink object.</span></span>

<span data-ttu-id="48898-114">Der folgende Code deklariert die Variablen des Typs [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) und **ID2D1GeometrySink**.</span><span class="sxs-lookup"><span data-stu-id="48898-114">The following code declares the variables of type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and **ID2D1GeometrySink**.</span></span>


```C++
    ID2D1PathGeometry *m_pPathGeometryUnion;
    ID2D1PathGeometry *m_pPathGeometryIntersect;
    ID2D1PathGeometry *m_pPathGeometryXOR;
    ID2D1PathGeometry *m_pPathGeometryExclude;
```



<span data-ttu-id="48898-115">Der folgende Code verwendet jeden der vier Modi, um die beiden [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) -Objekte zu kombinieren, und führt die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="48898-115">The following code uses each of the four modes to combine the two [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects and performs the following actions:</span></span>

-   <span data-ttu-id="48898-116">Erstellt zwei Ellipsen, m \_ spellipmingeometryone und m \_ spellipmingeometrytwo.</span><span class="sxs-lookup"><span data-stu-id="48898-116">Creates two ellipses, m\_spEllipseGeometryOne and m\_spEllipseGeometryTwo.</span></span>
-   <span data-ttu-id="48898-117">Erstellt ein Pfad Geometrie Objekt.</span><span class="sxs-lookup"><span data-stu-id="48898-117">Creates a path geometry object.</span></span>
-   <span data-ttu-id="48898-118">Öffnet ein Geometry-senkobjekt.</span><span class="sxs-lookup"><span data-stu-id="48898-118">Opens a geometry sink object.</span></span>
-   <span data-ttu-id="48898-119">Kombiniert die beiden Ellipsen.</span><span class="sxs-lookup"><span data-stu-id="48898-119">Combines the two ellipses.</span></span>
-   <span data-ttu-id="48898-120">Schließt das Geometry-senkobjekt.</span><span class="sxs-lookup"><span data-stu-id="48898-120">Closes the geometry sink object.</span></span>


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



<span data-ttu-id="48898-121">Mit diesem Code wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="48898-121">This code produces the output shown in the following illustration.</span></span>

![Darstellung zweier Geometrien und vier Modi für die Kombination der Geometrien (Union, Schnittmenge, XOR und Exclude)](images/combine-modes.png)

## <a name="related-topics"></a><span data-ttu-id="48898-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48898-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48898-124">**D2D1 \_ \_ kombinierungsmodus**</span><span class="sxs-lookup"><span data-stu-id="48898-124">**D2D1\_COMBINE\_MODE**</span></span>](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode)
</dt> <dt>

[<span data-ttu-id="48898-125">**ID2D1EllipseGeometry**</span><span class="sxs-lookup"><span data-stu-id="48898-125">**ID2D1EllipseGeometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)
</dt> <dt>

[<span data-ttu-id="48898-126">**ID2D1PathGeometry**</span><span class="sxs-lookup"><span data-stu-id="48898-126">**ID2D1PathGeometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)
</dt> <dt>

<span data-ttu-id="48898-127">**ID2D1GeometrySink**</span><span class="sxs-lookup"><span data-stu-id="48898-127">**ID2D1GeometrySink**</span></span>
</dt> </dl>

 

 
---
title: Abrufen von Geometriedaten durch Erweiterung von ID2D1SimplifiedGeometrySink
description: Zeigt, wie Geometriedaten durch Erweiterung der ID2D1SimplifiedGeometrySink-Schnittstelle abgerufen werden.
ms.assetid: c6777b11-6d4e-409e-9c30-da1e060c9aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba3670eb8d0152cc1dae8fbcc164bd8a6167630
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039411"
---
# <a name="how-to-retrieve-geometry-data-by-extending-id2d1simplifiedgeometrysink"></a><span data-ttu-id="cca7e-103">Abrufen von Geometriedaten durch Erweiterung von ID2D1SimplifiedGeometrySink</span><span class="sxs-lookup"><span data-stu-id="cca7e-103">How to Retrieve Geometry Data by Extending ID2D1SimplifiedGeometrySink</span></span>

<span data-ttu-id="cca7e-104">Obwohl ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekt unveränderlich ist, gibt es Fälle, in denen Sie die Geometriedaten in einem Pfad Geometrie Objekt bearbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="cca7e-104">While an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object is immutable, there are cases where you need to manipulate the geometry data in a path geometry object.</span></span> <span data-ttu-id="cca7e-105">Direct2D ermöglicht Ihnen dies, indem Sie eine erweiterbare Schnittstelle mit dem Namen " [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cca7e-105">Direct2D enables you to do so by providing an extendable interface named [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span> <span data-ttu-id="cca7e-106">In diesem Thema wird beschrieben, wie Sie diese Schnittstelle zum Abrufen der Geometriedaten aus einem Pfad Geometrie Objekt erweitern können.</span><span class="sxs-lookup"><span data-stu-id="cca7e-106">For concept illustration, this topic describes how to extend this interface to retrieve the geometry data from a path geometry object.</span></span>

<span data-ttu-id="cca7e-107">**So erweitern Sie die ID2D1SimplifiedGeometrySink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cca7e-107">**To Extend the ID2D1SimplifiedGeometrySink interface**</span></span>

1.  <span data-ttu-id="cca7e-108">Implementieren Sie eine Klasse, die von [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)erbt.</span><span class="sxs-lookup"><span data-stu-id="cca7e-108">Implement a class that inherits from [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span>
2.  <span data-ttu-id="cca7e-109">Erstellen Sie eine Instanz dieser Klasse, und übergeben Sie Sie an [**ID2D1Geometry:: Simple**](id2d1geometry-simplify.md).</span><span class="sxs-lookup"><span data-stu-id="cca7e-109">Create an instance of that class and pass it to [**ID2D1Geometry::Simplify**](id2d1geometry-simplify.md).</span></span>

<span data-ttu-id="cca7e-110">Im folgenden Codebeispiel wird gezeigt, wie eine Klasse namens "spezizedsink" implementiert wird, die von der [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) -Schnittstelle erbt.</span><span class="sxs-lookup"><span data-stu-id="cca7e-110">The following code example shows how to implement a class named SpecializedSink that inherits from the [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) interface.</span></span> <span data-ttu-id="cca7e-111">Zur Vereinfachung der Konzept Abbildung werden die Geometriedaten von der erweiterten **AddLines** -Methode abgerufen und im Konsolenfenster angezeigt. Sie können diese Methode anpassen, um Ihre spezifischen Datenanforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="cca7e-111">For the simplicity of concept illustration, the extended **AddLines** method retrieves the geometry data and then displays it on the console window; you can customize this method to meet your specific data needs.</span></span>


```C++
class SpecializedSink : public ID2D1SimplifiedGeometrySink
{
    public:
        SpecializedSink()
            : m_cRef(1)
        {
        }

        STDMETHOD_(ULONG, AddRef)(THIS)
        {
            return InterlockedIncrement(reinterpret_cast<LONG volatile *>(&m_cRef));
        }

        STDMETHOD_(ULONG, Release)(THIS)
        {
            ULONG cRef = static_cast<ULONG>(
            InterlockedDecrement(reinterpret_cast<LONG volatile *>(&m_cRef)));

            if(0 == cRef)
            {
                delete this;
            }

            return cRef;
        }

        STDMETHOD(QueryInterface)(THIS_ REFIID iid, void** ppvObject)
        {
            HRESULT hr = S_OK;

            if (__uuidof(IUnknown) == iid)
            {
                *ppvObject = static_cast<IUnknown*>(this);
                AddRef();
            }
            else if (__uuidof(ID2D1SimplifiedGeometrySink) == iid)
            {
                *ppvObject = static_cast<ID2D1SimplifiedGeometrySink*>(this);
                AddRef();
            }
            else
            {
                *ppvObject = NULL;
                hr = E_NOINTERFACE;
            }

            return hr;
        }

        STDMETHOD_(void, AddBeziers)(const D2D1_BEZIER_SEGMENT * /*beziers*/,
                                     UINT /*beziersCount*/)
        {
            // Customize this method to meet your specific data needs.
        }

        STDMETHOD_(void, AddLines)(const D2D1_POINT_2F *points, UINT pointsCount)
        {
            // Customize this method to meet your specific data needs.
            printf("\n\nRetrieving geometry data from a derived ID2D1SimplifiedGeometrySink object:\n");
            for (UINT i = 0; i < pointsCount; ++i)
            {
                printf("%.0f, %.0f\n", points[i].x, points[i].y);
            }
        }

        STDMETHOD_(void, BeginFigure)(D2D1_POINT_2F startPoint,
                                      D2D1_FIGURE_BEGIN figureBegin)
        {
        }

        STDMETHOD_(void, EndFigure)(D2D1_FIGURE_END figureEnd)
        {
        }

        STDMETHOD_(void, SetFillMode)(D2D1_FILL_MODE fillMode)
        {
        }

        STDMETHOD_(void, SetSegmentFlags)(D2D1_PATH_SEGMENT vertexFlags)
        {
        }

        STDMETHOD(Close)()
        {
            return S_OK;
        }

    private:
        UINT m_cRef;
};
```



<span data-ttu-id="cca7e-112">Im Beispiel wird dann ein Satz von Daten (182, 209), (211, 251), (251, 226), (392, 360) und (101, 360) verwendet, um eine aufgefüllte Pfad Geometrie (**m \_ pgeometry**) zu erstellen, in der Daten abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="cca7e-112">The example then uses a set of data (182, 209), (211, 251), (251, 226), (392, 360), and (101, 360) to create a populated path geometry (**m\_pGeometry**) where data can be retrieved.</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pGeometry);
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;

    hr = m_pGeometry->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

        pSink->BeginFigure(
            D2D1::Point2F(101,360),
            D2D1_FIGURE_BEGIN_FILLED
            );
        D2D1_POINT_2F points[5] = {
           D2D1::Point2F(182,209),
           D2D1::Point2F(211,251),
           D2D1::Point2F(251,226),
           D2D1::Point2F(392,360),
           D2D1::Point2F(101,360),
           };

        printf("Adding the following geometry data to an ID2D1GeometrySink object:\n");
        printf("182, 209\n");
        printf("211, 251\n");
        printf("251, 226\n");
        printf("392, 360\n");
        printf("101, 360\n");

        pSink->AddLines(points, ARRAYSIZE(points));
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
        pSink->Release();
```



<span data-ttu-id="cca7e-113">Zum Schluss erstellt das Beispiel ein spezizedsink-Objekt und ruft dann die [**ID2D1Geometry:: Simple**](id2d1geometry-simplify.md) -Methode auf, wobei das spezialisizedsink-Objekt und der [**D2D1 \_ Geometry- \_ \_ Option \_ Lines**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_simplification_option) -Parameter übergeben werden, was dazu führt, dass alle Kurven in Liniensegmente vereinfacht werden.</span><span class="sxs-lookup"><span data-stu-id="cca7e-113">Finally, the example creates a SpecializedSink object, and then calls the [**ID2D1Geometry::Simplify**](id2d1geometry-simplify.md) method, passing in the SpecializedSink object and the [**D2D1\_GEOMETRY\_SIMPLIFICATION\_OPTION\_LINES**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_simplification_option) parameter, which causes any curves to be flattened into line segments.</span></span>


```C++
        SpecializedSink *pSpecializedSink = NULL;

        if (SUCCEEDED(hr))
        {
            pSpecializedSink = new SpecializedSink();
            if (!pSpecializedSink)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        if (SUCCEEDED(hr))
        {
            hr = m_pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES, // This causes any curves to be flattened into line segments.
                    NULL, // world transform
                    pSpecializedSink
                    );


            if (SUCCEEDED(hr))
            {
                hr = pSpecializedSink->Close();
            }

            pSpecializedSink->Release();
        }
```



<span data-ttu-id="cca7e-114">Das Programm erstellt Ausgaben, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="cca7e-114">The program creates outputs as shown in the following screen shot.</span></span>

![Screenshot eines Konsolenfensters mit Ausgabe zum Hinzufügen und Abrufen von Geometriedaten](images/specializedgeometrysink.png)

## <a name="related-topics"></a><span data-ttu-id="cca7e-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cca7e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cca7e-117">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="cca7e-117">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 
---
title: Abrufen von Geometriedaten durch Erweitern von ID2D1SimplifiedGeometrySink
description: Zeigt, wie Geometriedaten durch Erweitern der ID2D1SimplifiedGeometrySink-Schnittstelle abgerufen werden.
ms.assetid: c6777b11-6d4e-409e-9c30-da1e060c9aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9cd7e3f5e01b77c07e0082d3460b718a4363cf88288859b715369a94ca09bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003429"
---
# <a name="how-to-retrieve-geometry-data-by-extending-id2d1simplifiedgeometrysink"></a>Abrufen von Geometriedaten durch Erweitern von ID2D1SimplifiedGeometrySink

Während ein [**ID2D1Geometry-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) unveränderlich ist, gibt es Fälle, in denen Sie die Geometriedaten in einem geometry-Pfadobjekt bearbeiten müssen. Direct2D ermöglicht Ihnen dies, indem Sie eine erweiterbare Schnittstelle namens [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)bereitstellen. Zur Veranschaulichung des Konzepts wird in diesem Thema beschrieben, wie diese Schnittstelle erweitert wird, um die Geometriedaten aus einem geometry-Pfadobjekt abzurufen.

**So erweitern Sie die ID2D1SimplifiedGeometrySink-Schnittstelle**

1.  Implementieren Sie eine Klasse, die von [**ID2D1SimplifiedGeometrySink erbt.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)
2.  Erstellen Sie eine Instanz dieser Klasse, und übergeben Sie sie an [**ID2D1Geometry::Simplify**](id2d1geometry-simplify.md).

Das folgende Codebeispiel zeigt, wie Sie eine Klasse namens SpecializedSink implementieren, die von der [**ID2D1SimplifiedGeometrySink-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) erbt. Zur Vereinfachung der Konzeptdarstellung ruft die erweiterte **AddLines-Methode** die Geometriedaten ab und zeigt sie dann im Konsolenfenster an. Sie können diese Methode an Ihre spezifischen Datenanforderungen anpassen.


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



Im Beispiel wird dann ein Satz von Daten (182, 209), (211, 251), (251, 226), (392, 360) und (101, 360) verwendet, um eine aufgefüllte Pfadgeometrie **(m \_ pGeometry)** zu erstellen, in der Daten abgerufen werden können.


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



Schließlich erstellt das Beispiel ein SpecializedSink-Objekt und ruft dann die [**ID2D1Geometry::Simplify-Methode**](id2d1geometry-simplify.md) auf, wobei das SpecializedSink-Objekt und der [**Parameter D2D1 \_ GEOMETRY \_ SIMPLIFY OPTION \_ \_ LINES**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_simplification_option) übergeben werden, wodurch alle Kurven in Liniensegmente vereinfacht werden.


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



Das Programm erstellt Ausgaben wie im folgenden Screenshot gezeigt.

![Screenshot eines Konsolenfensters mit Ausgabe zum Hinzufügen und Abrufen von Geometriedaten](images/specializedgeometrysink.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 
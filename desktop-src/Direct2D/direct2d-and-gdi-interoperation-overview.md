---
title: Übersicht über die Direct2D-und GDI-Interoperabilität
description: Beschreibt die gemeinsame Verwendung von Direct2D und GDI.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D, GDI-Interoperation
- Direct2D, Interoperabilität
- Interoperabilität, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- Interoperabilität, Graphics Device Interface (GDI)
- Direct3D, Interoperabilität
- Direct3D, Direct2D Interoperation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991d94b4460e9130b3353be38d5f749511434eb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729664"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a>Übersicht über die Direct2D-und GDI-Interoperabilität

In diesem Thema wird die gemeinsame Verwendung von Direct2D und [GDI](/windows/desktop/gdi/windows-gdi) beschrieben. Es gibt zwei Möglichkeiten, Direct2D mit GDI zu kombinieren: Sie können GDI-Inhalte in ein Direct2D GDI-kompatibles Renderziel schreiben, oder Sie können Direct2D-Inhalte in einen [GDI-Gerätekontext (DC)](/windows/desktop/gdi/device-contexts)schreiben.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Zeichnen von Direct2D-Inhalt in einen GDI-Gerätekontext](#draw-direct2d-content-to-a-gdi-device-context)
-   [ID2D1DCRenderTargets, GDI-Transformationen und von rechts nach links geschriebene sprach Builds von Windows](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [Ziehen Sie GDI-Inhalte in ein Direct2D-GDI-Compatible Renderziel.](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Diese Übersicht setzt voraus, dass Sie mit grundlegenden Direct2D-Zeichnungs Vorgängen vertraut sind. Ein Tutorial finden Sie unter [Direct2D Quick Start](direct2d-quickstart.md). Außerdem wird davon ausgegangen, dass Sie mit GDI-Zeichnungs Vorgängen vertraut sind.

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a>Zeichnen von Direct2D-Inhalt in einen GDI-Gerätekontext

Um Direct2D-Inhalte zu einem GDI-DC zu zeichnen, verwenden Sie ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)-Objekt. Wenn Sie ein DC-Renderziel erstellen möchten, verwenden Sie die [**ID2D1Factory::**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) -Methode. Diese Methode nimmt zwei Parameter an.

Der erste Parameter, eine [**D2D1 \_ - \_ Renderziel- \_ Eigenschafts**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) Struktur, gibt Rendering-, Remoting-, dpi-, Pixel-und Verwendungs Informationen an. Um das DC-Renderziel für die Zusammenarbeit mit GDI zu aktivieren, legen Sie das DXGI-Format auf [DXGI- \_ Format \_ B8G8R8A8 \_ unorm](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) und den Alpha-Modus auf [**D2D1 \_ alpha \_ Modus \_ vorab multipliziert**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) bzw. **D2D1 \_ alpha \_ Mode \_ Ignore** fest.

Der zweite Parameter ist die Adresse des Zeigers, der den DC-renderzielverweis empfängt.

Der folgende Code erstellt ein DC-Renderziel.


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



Im vorangehenden Code ist *m \_ pD2DFactory* ein Zeiger auf [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), und *m \_ pdcrt* ist ein Zeiger auf ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).

Bevor Sie das Rendering mit dem DC-Renderziel durchführen können, müssen Sie die [**binddc**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) -Methode verwenden, um Sie einem GDI-DC zuzuordnen. Dies geschieht jedes Mal, wenn Sie einen anderen Domänen Controller verwenden oder die Größe des Bereichs, den Sie ändern möchten.

Die [**binddc**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) -Methode erfordert zwei Parameter: *hdc* und *psubrect*. Der *hdc* -Parameter stellt ein Handle für den Gerätekontext bereit, der die Ausgabe des Renderziels empfängt. Der *psubrect* -Parameter ist ein Rechteck, das den Teil des Geräte Kontexts beschreibt, in dem der Inhalt gerendert wird. Das DC-Renderziel aktualisiert seine Größe entsprechend dem von *psubrect* beschriebenen Gerätekontext Bereich, wenn die Größe geändert werden soll.

Mit dem folgenden Code wird ein DC an ein DC-Renderziel gebunden.


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



Nachdem Sie das DC-Renderziel mit einem DC verknüpft haben, können Sie es zum Zeichnen verwenden. Der folgende Code zeichnet Direct2D-und GDI-Inhalte mithilfe eines DC.


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



Mit diesem Code werden Ausgaben erzeugt, wie in der folgenden Abbildung gezeigt (es wurden Legenden aufgerufen, um den Unterschied zwischen dem Direct2D-und dem GDI-Rendering hervorzuheben).

![Abbildung von zwei Kreis Diagrammen, die mit Direct2D und GDI gerendert werden](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a>ID2D1DCRenderTargets, GDI-Transformationen und von rechts nach links geschriebene sprach Builds von Windows

Wenn Sie ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)-Objekt verwenden, wird Direct2D-Inhalt in eine interne Bitmap gerendert, und anschließend wird die Bitmap mit GDI auf dem DC gerendert.

GDI kann eine GDI-Transformation (über die [**setworldtransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) -Methode) oder andere Auswirkungen auf denselben DC anwenden, der vom Renderziel verwendet wird. in diesem Fall transformiert GDI die von Direct2D erstellte Bitmap. Die Verwendung einer GDI-Transformation zum Transformieren des Direct2D-Inhalts hat die Möglichkeit, die visuelle Qualität der Ausgabe zu beeinträchtigen, da Sie eine Bitmap transformieren, bei der das Antialiasing und die unter Pixel Positionierung bereits berechnet wurden.

Nehmen Sie beispielsweise an, Sie verwenden das Renderziel, um eine Szene zu zeichnen, die Antialiasing-Geometrien und Text enthält. Wenn Sie eine GDI-Transformation verwenden, um eine Skalierungs Transformation auf den DC anzuwenden und die Szene so zu skalieren, dass Sie zehnmal größer ist, sehen Sie die pixelisierung und die verzweigten Kanten. (Wenn Sie jedoch eine ähnliche Transformation mithilfe von Direct2D angewendet haben, wird die visuelle Qualität der Szene nicht beeinträchtigt.)

In einigen Fällen ist es möglicherweise nicht offensichtlich, dass GDI zusätzliche Verarbeitungsvorgänge ausführt, die die Qualität des Direct2D-Inhalts beeinträchtigen können. Beispielsweise kann der Inhalt, der von einem [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) gerendert wird, bei einem Windows-Build von rechts nach links (RTL) horizontal invertiert werden, wenn er von GDI in das Ziel kopiert wird. Ob der Inhalt tatsächlich invertiert wird, hängt von den aktuellen Einstellungen des DC ab.

Abhängig vom Typ des gerenderten Inhalts empfiehlt es sich, die Inversion zu verhindern. Wenn der Direct2D-Inhalt Klartext enthält, wird die Qualität des Texts von dieser Inversion herabgestuft.

Sie können das Verhalten von RTL-Rendering mithilfe der [**setLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) -GDI-Funktion steuern. Um die Spiegelung zu verhindern, müssen Sie die **setLayout** -GDI-Funktion aufrufen und das **Layout \_ bitmaporientationbeibehaltenes** als einzigen Wert für den zweiten Parameter angeben (kombinieren Sie ihn nicht mit **Layout \_ RTL**), wie im folgenden Beispiel gezeigt:


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a>Ziehen Sie GDI-Inhalte in ein Direct2D-GDI-Compatible Renderziel.

Im vorherigen Abschnitt wird beschrieben, wie Sie Direct2D-Inhalte in einen GDI-DC schreiben. Sie können GDI-Inhalte auch in ein Direct2D GDI-kompatibles Renderziel schreiben. Diese Vorgehensweise ist nützlich für Anwendungen, die in erster Linie mit Direct2D Rendering, aber über ein Erweiterbarkeits Modell oder andere Legacy Inhalte verfügen, die die Fähigkeit zum Rendering mit GDI erfordern.

Wenn Sie GDI-Inhalte in einem Direct2D GDI-kompatiblen Renderziel Renderziel, verwenden Sie ein [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)-Objekt, das Zugriff auf einen Gerätekontext bietet, der GDI-Draw-Aufrufe akzeptieren kann. Anders als bei anderen Schnittstellen wird ein **ID2D1GdiInteropRenderTarget** -Objekt nicht direkt erstellt. Verwenden Sie stattdessen die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode einer vorhandenen renderzielinstanz. Dies wird im folgenden Code veranschaulicht:


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



Im vorangehenden Code ist *m \_ pD2DFactory* ein Zeiger auf [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), und *m \_ pgdirt* ist ein Zeiger auf ein [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).

Beachten Sie, dass das Flag [**D2D1 \_ Rendering \_ Target \_ Usage \_ GDI \_ Compatible**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) angegeben wird, wenn das HWND-GDI-kompatible Renderziel erstellt wird. Wenn ein Pixel Format erforderlich ist, verwenden Sie das [DXGI- \_ Format \_ B8G8R8A8 \_ unorm](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Wenn ein Alpha-Modus erforderlich ist, verwenden Sie den [**D2D1- \_ Alpha Modus, der \_ \_ vorab multipliziert**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ist, oder den **D2D1 \_ alpha \_ \_**-Modus

Beachten Sie, dass die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode immer erfolgreich ist. Um zu testen, ob die Methoden der [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) -Schnittstelle für ein bestimmtes Renderziel funktionieren, erstellen Sie eine [**D2D1- \_ \_ Renderziel \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) Eigenschaft, die GDI-Kompatibilität und das entsprechende Pixel Format angibt, und rufen Sie dann die [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) -Methode des Renderziels auf, um zu überprüfen, ob das Renderziel GDI

Im folgenden Beispiel wird gezeigt, wie ein Kreis Diagramm (GDI-Inhalt) in das HWND-GDI-kompatible Renderziel gezeichnet wird.


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



Der Code gibt Diagramme aus, wie in der folgenden Abbildung gezeigt, mit aufrufen, um den Unterschied bei der renderingqualität hervorzuheben. Das Rechte Kreis Diagramm (GDI-Inhalt) hat eine niedrigere renderingqualität als das linke Kreis Diagramm (Direct2D Content). Dies liegt daran, dass Direct2D mit Antialiasing rendern kann.

![Abbildung von zwei Zirkel Diagrammen, die in einem Direct2D GDI-kompatiblen Renderziel gerendert werden](images/gdicontentind2d.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Factory:: kreatedcrendertarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[**D2D1 \_ \_ Renderziel \_ Eigenschaften**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[GDI-Geräte Kontexte](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[GDI SDK](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 
---
title: Übersicht über die Interoperabilität von Direct2D und GDI
description: Beschreibt, wie Direct2D und GDI zusammen verwendet werden.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D,GDI-Interoperation
- Direct2D, Interoperabilität
- Interoperabilität,Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- Interoperabilität, Graphics Device Interface (GDI)
- Direct3D, Interoperabilität
- Direct3D,Direct2D-Interoperation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a1f3be132aba742eb1df4b8a893dad245f851a0
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631562"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a>Übersicht über die Interoperabilität von Direct2D und GDI

In diesem Thema wird beschrieben, wie Direct2D und [GDI](/windows/desktop/gdi/windows-gdi) zusammen verwendet werden. Es gibt zwei Möglichkeiten, Direct2D mit GDI zu kombinieren: Sie können GDI-Inhalt in ein Direct2D GDI-kompatibles Renderziel schreiben oder Direct2D-Inhalt in einen [GDI-Gerätekontext (DC)](/windows/desktop/gdi/device-contexts)schreiben.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Zeichnen von Direct2D-Inhalten in einen GDI-Gerätekontext](#draw-direct2d-content-to-a-gdi-device-context)
-   [ID2D1DCRenderTargets, GDI-Transformationen und Sprachbuilds von rechts nach links von Windows](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [Zeichnen von GDI-Inhalten in ein Direct2D-GDI-Compatible-Renderziel](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

In dieser Übersicht wird davon ausgegangen, dass Sie mit grundlegenden Direct2D-Zeichnungsvorgängen vertraut sind. Ein Tutorial finden Sie im [Direct2D-Schnellstart.](direct2d-quickstart.md) Außerdem wird davon ausgegangen, dass Sie mit GDI-Zeichnungsvorgängen vertraut sind.

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a>Zeichnen von Direct2D-Inhalten in einen GDI-Gerätekontext

Um Direct2D-Inhalt auf einen GDI-DC zu zeichnen, verwenden Sie eine [**ID2D1DCRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) Um ein DC-Renderziel zu erstellen, verwenden Sie die [**ID2D1Factory::CreateDCRenderTarget-Methode.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) Diese Methode nimmt zwei Parameter an.

Der erste Parameter, eine [**D2D1 \_ RENDER \_ TARGET \_ PROPERTIES-Struktur,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) gibt Rendering-, Remoting-, DPI-, Pixelformat- und Nutzungsinformationen an. Damit das DC-Renderziel mit GDI funktioniert, legen Sie das DXGI-Format auf [DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) und den Alphamodus auf [**D2D1 \_ ALPHA MODE \_ \_ PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) oder **D2D1 \_ ALPHA MODE \_ \_ IGNORE** fest.

Der zweite Parameter ist die Adresse des Zeigers, der den DC-Renderzielverweis empfängt.

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



Im vorangehenden Code ist *m \_ pD2DFactory* ein Zeiger auf eine [**ID2D1Factory,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)und *m \_ pDCRT* ist ein Zeiger auf eine [**ID2D1DCRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)

Bevor Sie mit dem DC-Renderziel rendern können, müssen Sie dessen [**BindDC-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) verwenden, um es einem GDI-DC zuzuordnen. Dies geschieht jedes Mal, wenn Sie einen anderen Domänencontroller verwenden, oder die Größe des Bereichs, den Sie zeichnen möchten, ändert sich.

Die [**BindDC-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) verwendet zwei Parameter: *hDC* und *pSubRect.* Der *hDC-Parameter* stellt ein Handle für den Gerätekontext bereit, der die Ausgabe des Renderziels empfängt. Der *pSubRect-Parameter* ist ein Rechteck, das den Teil des Gerätekontexts beschreibt, in den Inhalt gerendert wird. Das DC-Renderziel aktualisiert seine Größe entsprechend dem von *pSubRect* beschriebenen Gerätekontextbereich, falls die Größe geändert wird.

Der folgende Code bindet einen DC an ein DC-Renderziel.


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col  />
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



Nachdem Sie das DC-Renderziel einem DC zugeordnet haben, können Sie es zum Zeichnen verwenden. Der folgende Code zeichnet Direct2D- und GDI-Inhalte mithilfe eines Domänencontrollers.


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



Dieser Code erzeugt Ausgaben, wie in der folgenden Abbildung dargestellt (Aufrufe wurden hinzugefügt, um den Unterschied zwischen Direct2D- und GDI-Rendering hervorzuheben).

![Abbildung von zwei Kreisdiagrammen, die mit direct2d und gdi gerendert werden](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a>ID2D1DCRenderTargets, GDI-Transformationen und Sprachbuilds von rechts nach links von Windows

Wenn Sie ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)verwenden, rendert es Direct2D-Inhalt in einer internen Bitmap und rendert die Bitmap dann mit GDI auf dem DC.

GDI kann eine GDI-Transformation (über die [**SetWorldTransform-Methode)**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) oder einen anderen Effekt auf denselben Domänencontroller anwenden, der vom Renderziel verwendet wird. In diesem Fall transformiert GDI die von Direct2D erzeugte Bitmap. Die Verwendung einer GDI-Transformation zum Transformieren des Direct2D-Inhalts kann die visuelle Qualität der Ausgabe beeinträchtigen, da Sie eine Bitmap transformieren, für die Antialiasing und Subpixelpositionierung bereits berechnet wurden.

Angenommen, Sie verwenden das Renderziel, um eine Szene zu zeichnen, die antialiasierte Geometrien und Text enthält. Wenn Sie eine GDI-Transformation verwenden, um eine Skalierungstransformation auf den DC anzuwenden und die Szene so zu skalieren, dass sie zehnmal größer ist, werden Pixelisierung und verzweigte Kanten angezeigt. (Wenn Sie jedoch eine ähnliche Transformation mit Direct2D angewendet haben, würde die visuelle Qualität der Szene nicht beeinträchtigt.)

In einigen Fällen ist es möglicherweise nicht offensichtlich, dass GDI eine zusätzliche Verarbeitung durchführt, die die Qualität des Direct2D-Inhalts beeinträchtigen kann. Beispielsweise kann bei einem RTL-Build (Right-to-Left) von Windows inhalt, der von einem [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) gerendert wird, horizontal umgekehrt werden, wenn GDI ihn in das Ziel kopiert. Ob der Inhalt tatsächlich invertiert wird, hängt von den aktuellen Einstellungen des Domänencontrollers ab.

Je nach Art des gerenderten Inhalts möchten Sie möglicherweise die Umkehrung verhindern. Wenn der Direct2D-Inhalt ClearType-Text enthält, beeinträchtigt diese Umkehrung die Qualität des Texts.

Sie können das RTL-Renderingverhalten mithilfe der [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) GDI-Funktion steuern. Um die Spiegelung zu verhindern, rufen Sie die **SetLayout** GDI-Funktion auf, und geben Sie **LAYOUT \_ BITMAPORIENTATIONPRESERVED** als einzigen Wert für den zweiten Parameter an (kombinieren Sie ihn nicht mit **LAYOUT \_ RTL),** wie im folgenden Beispiel gezeigt:


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a>Zeichnen von GDI-Inhalten in ein Direct2D-GDI-Compatible-Renderziel

Im vorherigen Abschnitt wird beschrieben, wie Direct2D-Inhalte in einen GDI-DC geschrieben werden. Sie können GDI-Inhalte auch in ein Direct2D-GDI-kompatibles Renderziel schreiben. Dieser Ansatz ist nützlich für Anwendungen, die hauptsächlich mit Direct2D gerendert werden, aber über ein Erweiterbarkeitsmodell oder andere Legacyinhalte verfügen, die die Möglichkeit zum Rendern mit GDI erfordern.

Verwenden Sie zum Rendern von GDI-Inhalten in einem Direct2D GDI-kompatiblen Renderziel eine [**ID2D1GdiInteropRenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)die Zugriff auf einen Gerätekontext bietet, der GDI-Zeichnen-Aufrufe akzeptieren kann. Im Gegensatz zu anderen Schnittstellen wird ein **ID2D1GdiInteropRenderTarget-Objekt** nicht direkt erstellt. Verwenden Sie stattdessen die [**QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) einer vorhandenen Renderzielinstanz. Dies wird im folgenden Code veranschaulicht:


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



Im vorangehenden Code ist *m \_ pD2DFactory* ein Zeiger auf eine [**ID2D1Factory,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)und *m \_ pGDIRT* ist ein Zeiger auf eine [**ID2D1GdiInteropRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)

Beachten Sie, dass das Flag [**D2D1 \_ RENDER TARGET USAGE \_ \_ \_ GDI \_ COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) beim Erstellen des Hwnd GDI-kompatiblen Renderziels angegeben wird. Wenn ein Pixelformat erforderlich ist, verwenden Sie [DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Wenn ein Alphamodus erforderlich ist, verwenden Sie [**D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) oder **D2D1 \_ ALPHA MODE \_ \_ IGNORE**.

Beachten Sie, dass die [**QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) immer erfolgreich ist. Um zu testen, ob die Methoden der [**ID2D1GdiInteropRenderTarget-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) für ein bestimmtes Renderziel funktionieren, erstellen Sie eine [**D2D1-RENDERZIELEIGENSCHAFTEN, \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) die GDI-Kompatibilität und das entsprechende Pixelformat angibt, und rufen Sie dann die [**IsSupported-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) des Renderziels auf, um festzustellen, ob das Renderziel GDI-kompatibel ist.

Das folgende Beispiel zeigt, wie ein Kreisdiagramm (GDI-Inhalt) auf das Hwnd-GDI-kompatible Renderziel gezeichnet wird.


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



Der Code gibt Diagramme wie in der folgenden Abbildung gezeigt mit Aufrufen aus, um den Unterschied bei der Renderingqualität hervorzuheben. Das rechte Kreisdiagramm (GDI-Inhalt) hat eine niedrigere Renderingqualität als das linke Kreisdiagramm (Direct2D-Inhalt). Dies liegt daran, dass Direct2D mit Antialiasing gerendert werden kann.

![Abbildung von zwei Kreisdiagrammen, die in einem gdi-kompatiblen Direct2d-Renderziel gerendert werden](images/gdicontentind2d.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[**D2D1– \_ \_ \_ RENDERZIELEIGENSCHAFTEN**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[GDI-Gerätekontexte](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[GDI SDK](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 

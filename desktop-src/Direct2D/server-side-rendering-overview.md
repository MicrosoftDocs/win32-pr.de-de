---
title: Verwenden von Direct2D für Server-Side Rendering
description: Beschreibt die Verwendung von Direct2D für serverseitiges Rendering.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, serverseitiges Rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65991d2437939ce7f1d218022e0c3c57649405a18e2c1b9d073635b5b37d1a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917217"
---
# <a name="using-direct2d-for-server-side-rendering"></a>Verwenden von Direct2D für Server-Side Rendering

Direct2D eignet sich gut für Grafikanwendungen, die serverseitiges Rendering auf dem Windows erfordern. In dieser Übersicht werden die Grundlagen der Verwendung von Direct2D für serverseitiges Rendering beschrieben. Sie enthält die folgenden Abschnitte:

-   [Anforderungen für Server-Side Rendering](#requirements-for-server-side-rendering)
-   [Optionen für verfügbare APIs](#options-for-available-apis)
    -   [Gdi](#gdi)
    -   [GDI+](#gdi)
    -   [Direct2D](#using-direct2d-for-server-side-rendering)
-   [Verwenden von Direct2D für Server-Side Rendering](#how-to-use-direct2d-for-server-side-rendering)
    -   [Softwarerendering](#software-rendering)
    -   [Multithreading](#multithreading)
    -   [Generieren einer Bitmapdatei](#generating-a-bitmap-file)
-   [Zusammenfassung](#conclusion)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements-for-server-side-rendering"></a>Anforderungen für Server-Side Rendering

Das folgende Szenario ist ein typisches Szenario für einen Diagrammserver: Diagramme und Grafiken werden auf einem Server gerendert und als Bitmaps als Reaktion auf Webanforderungen bereitgestellt. Der Server kann mit einer Low-End-Grafikkarte oder gar keiner Grafikkarte ausgestattet sein.

Dieses Szenario zeigt drei Anwendungsanforderungen. Erstens muss die Anwendung mehrere gleichzeitige Anforderungen effizient verarbeiten, insbesondere auf Servern mit mehreren Kernen. Zweitens muss die Anwendung Softwarerendering verwenden, wenn sie auf Servern mit einer Low-End-Grafikkarte oder ohne Grafikkarte ausgeführt wird. Schließlich muss die Anwendung als Dienst in Sitzung 0 ausgeführt werden, damit kein Benutzer angemeldet sein muss. Weitere Informationen zu Sitzung 0 finden Sie unter Auswirkung der Isolation von Sitzung 0 auf Dienste und Treiber [in Windows.](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx)

## <a name="options-for-available-apis"></a>Optionen für verfügbare APIs

Es gibt drei Optionen für serverseitiges Rendering: GDI, GDI+ und Direct2D. Wie GDI und GDI+ ist Direct2D eine native 2D-Rendering-API, die Anwendungen mehr Kontrolle über die Verwendung von Grafikgeräten bietet. Darüber hinaus unterstützt Direct2D eindeutig eine Singlethread-Factory und eine Multithread-Factory. In den folgenden Abschnitten wird jede API in Bezug auf Zeichnungsqualitäten und serverseitiges Multithreadrendering verglichen.

### <a name="gdi"></a>GDI

Im Gegensatz zu Direct2D und GDI+ unterstützt GDI keine hochwertigen Zeichnungsfeatures. GDI unterstützt z. B. keine Antialiasing für die Erstellung reibungsloser Linien und bietet nur eingeschränkte Unterstützung für Transparenz. Basierend auf den Grafikleistungstestergebnissen auf Windows 7 und Windows Server 2008 R2 wird Direct2D effizienter skaliert als GDI, trotz der Neugestaltung von Sperren in GDI. Weitere Informationen zu diesen Testergebnissen finden Sie unter [Engineering Windows 7 Graphics Performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).

Darüber hinaus sind Anwendungen, die GDI verwenden, auf 10240 GDI-Handles pro Prozess und 65536 GDI-Handles pro Sitzung beschränkt. Der Grund dafür ist, dass Windows intern ein 16-Bit-WORD verwendet, um den Index der Handles für jede Sitzung zu speichern.

### <a name="gdi"></a>GDI+

Obwohl GDI+ Antialiasing und Alphablending für hochwertiges Zeichnen unterstützt, besteht das Hauptproblem von GDI+ für Serverszenarien in der Nichtunterstützung der Ausführung in Sitzung 0. Da Sitzung 0 nur nicht interaktive Funktionen unterstützt, erhalten Funktionen, die direkt oder indirekt mit Anzeigegeräten interagieren, Fehler. Zu den spezifischen Beispielen für Funktionen gehören nicht nur solche, die mit Anzeigegeräten zu tun haben, sondern auch solche, die indirekt mit Gerätetreibern zu tun haben.

Ähnlich wie GDI wird GDI+ durch seinen Sperrmechanismus eingeschränkt. Die Sperrmechanismen in GDI+ sind in Windows 7 und Windows Server 2008 R2 identisch wie in früheren Versionen.

### <a name="direct2d"></a>Direct2D

Direct2D ist eine hardwarebeschleunigte 2D-Grafik-API im Unmittelbarmodus mit Hardwarebeschleunung, die leistungsstarkes und hochwertiges Rendering ermöglicht. Sie bietet eine Singlethread- und Multithread-Factory sowie die lineare Skalierung des kursorientierten Softwarerenderings.

Zu diesem Grund definiert Direct2D eine Stamm-Factoryschnittstelle. In der Regel kann ein in einer Factory erstelltes Objekt nur mit anderen Objekten verwendet werden, die aus derselben Factory erstellt wurden. Der Aufrufer kann beim Erstellen entweder eine Singlethread-Factory oder eine Multithread-Factory anfordern. Wenn eine Singlethread-Factory angefordert wird, erfolgt keine Sperrung von Threads. Wenn der Aufrufer eine Multithread-Factory an fordert, wird immer dann eine factoryweite Threadsperre verwendet, wenn ein Aufruf in Direct2D erfolgt.

Darüber hinaus ist die Sperrung von Threads in Direct2D präziser als in GDI und GDI+, sodass die Erhöhung der Anzahl von Threads nur minimale Auswirkungen auf die Leistung hat.

## <a name="how-to-use-direct2d-for-server-side-rendering"></a>Verwenden von Direct2D für Server-Side Rendering

In den folgenden Abschnitten wird beschrieben, wie Sie Softwarerendering verwenden, wie Sie eine Singlethread- und Multithread-Factory optimal verwenden und eine komplexe Zeichnung in einer Datei zeichnen und speichern.

### <a name="software-rendering"></a>Softwarerendering

Serverseitige Anwendungen verwenden Softwarerendering, indem [sie das RENDERziel IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) erstellen, bei dem der Renderzieltyp entweder auf D2D1 RENDER TARGET TYPE SOFTWARE oder \_ \_ \_ \_ D2D1 RENDER TARGET TYPE DEFAULT festgelegt \_ \_ \_ \_ ist. Weitere Informationen zu [IWICBitmap-Renderzielen](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) finden Sie unter der [**ID2D1Factory::CreateWicBitmapRenderTarget-Methode.**](id2d1factory-createwicbitmaprendertarget.md) Weitere Informationen zu den Renderzieltypen finden Sie unter [**D2D1 \_ RENDER \_ TARGET \_ TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).

### <a name="multithreading"></a>Multithreading

Wenn Sie wissen, wie Factorys erstellt und gemeinsam verwendet werden und Ziele threadübergreifend gerendert werden, kann dies die Leistung einer Anwendung erheblich beeinträchtigen. Die folgenden drei Abbildungen zeigen drei verschiedene Ansätze. Der optimale Ansatz ist in Abbildung 3 dargestellt.

![Direct2d-Multithreadingdiagramm mit einem einzelnen Renderziel.](images/server-side-rendering-1.png)

In Abbildung 1 verwenden verschiedene Threads dieselbe Factory und dasselbe Renderziel. Dieser Ansatz kann zu unvorhersehbaren Ergebnissen führen, wenn mehrere Threads gleichzeitig den Zustand des freigegebenen Renderziels ändern, z. B. das gleichzeitige Festlegen der Transformationsmatrix. Da die interne Sperre in Direct2D keine freigegebene Ressource synchronisiert, z. B. Renderziele, kann dieser Ansatz dazu führen, dass der [**BeginDraw-Aufruf**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) in Thread 1 fehlschlägt, da der **BeginDraw-Aufruf** in Thread 2 bereits das freigegebene Renderziel verwendet.

![Direct2d-Multithreadingdiagramm mit mehreren Renderzielen.](images/server-side-rendering-2.png)

Um die unvorhersehbaren Ergebnisse in Abbildung 1 zu vermeiden, zeigt Abbildung 2 eine Multithread-Factory mit jedem Thread mit einem eigenen Renderziel. Dieser Ansatz funktioniert, funktioniert aber effektiv als Singlethreadanwendung. Der Grund dafür ist, dass die factoryweite Sperre nur auf die Zeichnungsvorgangsebene angewendet wird und daher alle Zeichnungsaufrufe in derselben Factory serialisiert werden. Daher wird Thread 1 blockiert, wenn versucht wird, einen Zeichnungsaufruf zu erhalten, während Thread 2 gerade einen weiteren Zeichnungsaufruf ausgeführt.

![Direct2d-Multithreadingdiagramm mit mehreren Factorys und mehreren Renderzielen.](images/server-side-rendering-3.png)

Abbildung 3 zeigt den optimalen Ansatz, bei dem eine Singlethread-Factory und ein Singlethread-Renderziel verwendet werden. Da bei Verwendung einer Singlethread-Factory keine Sperren ausgeführt werden, können Zeichnungsvorgänge in jedem Thread gleichzeitig ausgeführt werden, um eine optimale Leistung zu erzielen.

### <a name="generating-a-bitmap-file"></a>Generieren einer Bitmapdatei

Um eine Bitmapdatei mithilfe von Softwarerendering zu generieren, verwenden Sie ein [IWICBitmap-Renderziel.](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) Verwenden Sie [einen IWICStream,](/windows/win32/api/wincodec/nn-wincodec-iwicstream) um die Bitmap in eine Datei zu schreiben. Verwenden [Sie IWICBitmapFrameEncode,](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) um die Bitmap in ein angegebenes Bildformat zu codieren. Das folgende Codebeispiel zeigt, wie Sie das folgende Bild zeichnen und in einer Datei speichern.

![Beispielausgabebild.](images/saveasimagefile-sample.png)

In diesem Codebeispiel werden zunächst eine [IWICBitmap und](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) ein [IWICBitmap-Renderziel](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) erstellt. Anschließend wird eine Zeichnung mit Text, eine Pfadgeometrie, die ein Stundenglas darstellt, und ein transformiertes Stundenglas in eine WIC-Bitmap gerendert. Anschließend wird [IWICStream::InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) verwendet, um die Bitmap in einer Datei zu speichern. Wenn Ihre Anwendung die Bitmap im Arbeitsspeicher speichern muss, verwenden Sie [stattdessen IWICStream::InitializeFromMemory.](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) Schließlich wird [IWICBitmapFrameEncode verwendet,](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) um die Bitmap zu codieren.


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a>Zusammenfassung

Wie oben zu sehen, ist die Verwendung von Direct2D für serverseitiges Rendering einfach und unkompliziert. Darüber hinaus bietet es qualitativ hochwertiges und hochgradig parallelisierbares Rendering, das in Umgebungen mit geringen Berechtigungen des Servers ausgeführt werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 
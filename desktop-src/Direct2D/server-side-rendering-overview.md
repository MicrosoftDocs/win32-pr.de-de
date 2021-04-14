---
title: Verwenden von Direct2D zum Server-Side Rendering
description: Beschreibt die Verwendung von Direct2D für serverseitiges Rendering.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, serverseitiges Rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390438"
---
# <a name="using-direct2d-for-server-side-rendering"></a>Verwenden von Direct2D zum Server-Side Rendering

Direct2D eignet sich gut für Grafikanwendungen, die serverseitiges Rendering auf Windows Server erfordern. In dieser Übersicht werden die Grundlagen der Verwendung von Direct2D für serverseitiges Rendering beschrieben. Sie enthält die folgenden Abschnitte:

-   [Anforderungen für Server-Side Rendering](#requirements-for-server-side-rendering)
-   [Optionen für verfügbare APIs](#options-for-available-apis)
    -   [GDI](#gdi)
    -   [GDI+](#gdi)
    -   [Direct2D](#using-direct2d-for-server-side-rendering)
-   [Verwenden von Direct2D zum Server-Side Rendering](#how-to-use-direct2d-for-server-side-rendering)
    -   [Software Rendering](#software-rendering)
    -   [Multithreading](#multithreading)
    -   [Erstellen einer Bitmapdatei](#generating-a-bitmap-file)
-   [Zusammenfassung](#conclusion)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements-for-server-side-rendering"></a>Anforderungen für Server-Side Rendering

Im folgenden finden Sie ein typisches Szenario für einen Diagramm Server: Diagramme und Grafiken werden auf einem Server gerendert und als Bitmaps in Reaktion auf Webanforderungen übermittelt. Der Server ist möglicherweise mit einer Low-End-Grafikkarte oder einer Grafikkarte ausgestattet.

In diesem Szenario werden drei Anwendungsanforderungen aufgeführt. Zuerst muss die Anwendung mehrere gleichzeitige Anforderungen effizient verarbeiten, insbesondere auf multikernservern. Zweitens muss die Anwendung das Software Rendering bei der Ausführung auf Servern mit einer Low-End-Grafikkarte oder einer Grafikkarte verwenden. Schließlich muss die Anwendung als Dienst in Sitzung 0 ausgeführt werden, damit kein Benutzer angemeldet werden muss. Weitere Informationen zu Sitzung 0 finden Sie unter [Auswirkung der Sitzung 0-Isolation auf Dienste und Treiber in Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).

## <a name="options-for-available-apis"></a>Optionen für verfügbare APIs

Es gibt drei Optionen für serverseitiges Rendering: GDI, GDI+ und Direct2D. Wie GDI und GDI+ ist Direct2D eine native 2D-Rendering-API, mit der Anwendungen mehr Kontrolle über die Verwendung von Grafik Geräten erhalten. Außerdem unterstützt Direct2D eindeutig einen Single Thread und eine Multithread-Factory. In den folgenden Abschnitten wird jede API in Bezug auf Zeichnungs Qualitäten und serverseitiges Multithread-Rendering verglichen.

### <a name="gdi"></a>GDI

Im Gegensatz zu Direct2D und GDI+ unterstützt GDI keine hochwertigen Zeichnungs Features. Beispielsweise unterstützt GDI keine Antialiasing zum Erstellen von Smooth Lines und bietet nur eingeschränkte Unterstützung für Transparenz. Basierend auf den Ergebnissen der Grafik Leistungstests unter Windows 7 und Windows Server 2008 R2 skaliert Direct2D effizienter als GDI, trotz der Umgestaltung der Sperren in GDI. Weitere Informationen zu diesen Testergebnissen finden Sie unter [Engineering Windows 7 graphics Performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).

Außerdem sind Anwendungen, die GDI verwenden, auf 10240 GDI-Handles pro Prozess und 65536 GDI-Handles pro Sitzung beschränkt. Der Grund hierfür ist, dass intern in Windows ein 16-Bit-Wort verwendet wird, um den Index von Handles für jede Sitzung zu speichern.

### <a name="gdi"></a>GDI+

Obwohl GDI+ Antialiasing und Alpha Blending für qualitativ hochwertige Zeichnungen unterstützt, besteht das Hauptproblem mit GDI+ für Server Szenarien darin, dass die Ausführung in Sitzung 0 nicht unterstützt wird. Da Sitzung 0 nur nicht interaktive Funktionen unterstützt, erhalten Funktionen, die direkt oder indirekt mit Anzeigegeräten interagieren, Fehler. Bestimmte Beispiele für Funktionen umfassen nicht nur diejenigen, die mit Anzeigegeräten arbeiten, sondern auch diejenigen, die indirekt mit Gerätetreibern arbeiten.

Ähnlich wie bei GDI ist GDI+ durch seinen Sperrmechanismus eingeschränkt. Die Sperrmechanismen in GDI+ sind in Windows 7 und Windows Server 2008 R2 identisch, wie in früheren Versionen.

### <a name="direct2d"></a>Direct2D

Bei Direct2D handelt es sich um eine hardwarebeschleunigte, 2D-Grafik-API, die leistungsstarke und qualitativ hochwertige Rendering bietet. Er bietet eine Single Thread-und Multithread Factory sowie die Lineare Skalierung des Kurs orientierten Software Rendering.

Zu diesem Zweck definiert Direct2D eine root Factory-Schnittstelle. Als Regel kann ein Objekt, das auf einer Factory erstellt wird, nur mit anderen Objekten verwendet werden, die aus derselben Factory erstellt wurden. Der Aufrufer kann bei der Erstellung entweder eine Single Thread-oder eine Multithread-Factory anfordern. Wenn eine Single Thread Factory angefordert wird, wird kein Sperren von Threads ausgeführt. Wenn der Aufrufer eine multithreadfactory anfordert, wird immer dann eine Werks weite Thread Sperre eingerichtet, wenn ein Aufruf in Direct2D erfolgt.

Außerdem ist das Sperren von Threads in Direct2D präziser als in GDI und GDI+, sodass sich die Anzahl der Threads nur minimal auf die Leistung auswirkt.

## <a name="how-to-use-direct2d-for-server-side-rendering"></a>Verwenden von Direct2D zum Server-Side Rendering

In den folgenden Abschnitten wird beschrieben, wie Sie das Software Rendering verwenden, eine Single Thread-und eine Multithread-Factory optimal verwenden und eine komplexe Zeichnung in einer Datei zeichnen und speichern.

### <a name="software-rendering"></a>Software Rendering

Server seitige Anwendungen verwenden das Software Rendering durch Erstellen des [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) -Renderziels, wobei der renderzieltyp entweder auf D2D1 \_ Rendering \_ Target \_ Type \_ Software oder D2D1 \_ renderzieltyp \_ \_ \_ Default festgelegt ist. Weitere Informationen zu [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) -renderzielen finden Sie unter der [**ID2D1Factory:: samatewicbitmaprendertarget**](id2d1factory-createwicbitmaprendertarget.md) -Methode. Weitere Informationen zu den renderzieltypen finden Sie unter [**D2D1 \_ Rendering \_ Target \_ Type**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).

### <a name="multithreading"></a>Multithreading

Wenn Sie wissen, wie Factorys erstellt und freigegeben werden, kann die Leistung einer Anwendung erheblich beeinträchtigt werden. Die folgenden drei Abbildungen zeigen drei verschiedene Ansätze. Der optimale Ansatz ist in Abbildung 3 dargestellt.

![Direct2D Multithreading-Diagramm mit einem einzelnen Renderziel.](images/server-side-rendering-1.png)

In Abbildung 1 verwenden verschiedene Threads dieselbe Factory und dasselbe Renderziel. Diese Vorgehensweise kann zu unvorhersehbaren Ergebnissen in Fällen führen, in denen mehrere Threads gleichzeitig den Status des freigegebenen Renderziels ändern, z. b. das gleichzeitige Festlegen der Transformationsmatrix. Da bei der internen Sperrung in Direct2D keine freigegebene Ressource wie Renderziele synchronisiert wird, kann dieser Ansatz dazu führen, dass der [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Befehl in Thread 1 fehlschlägt, da der **beginDraw** -Befehl in Thread 2 bereits das freigegebene Renderziel verwendet.

![Direct2D Multithreading-Diagramm mit mehreren renderzielen.](images/server-side-rendering-2.png)

Um die in Abbildung 1 gefundenen unvorhersehbaren Ergebnisse zu vermeiden, zeigt Abbildung 2 eine multithreadfactory, bei der jeder Thread über ein eigenes Renderziel verfügt. Diese Vorgehensweise funktioniert, aber Sie fungiert effektiv als Single Thread-Anwendung. Der Grund hierfür ist, dass die Sperre für die Werks weite nur für die Zeichnungs Vorgangs Ebene gilt und dass alle Zeichnungs Aufrufe in derselben Factory serialisiert werden. Infolgedessen wird Thread 1 blockiert, wenn versucht wird, einen Zeichnungs Befehl einzugeben, während Thread 2 in der Mitte der Ausführung eines weiteren Zeichnungs Aufrufes ist.

![Direct2D Multithreading-Diagramm mit mehreren Factorys und mehreren Renderingzielen.](images/server-side-rendering-3.png)

Abbildung 3 zeigt den optimalen Ansatz, bei dem eine Single Thread Factory und ein Single Thread-Renderziel verwendet werden. Da bei der Verwendung einer Single Thread Factory keine Sperre ausgeführt wird, können Zeichnungsvorgänge in jedem Thread gleichzeitig ausgeführt werden, um eine optimale Leistung zu erzielen.

### <a name="generating-a-bitmap-file"></a>Erstellen einer Bitmapdatei

Verwenden Sie zum Generieren einer Bitmapdatei mit dem Software Rendering ein [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) -Renderziel. Verwenden Sie einen [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) , um die Bitmap in eine Datei zu schreiben. Verwenden Sie [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) , um die Bitmap in ein bestimmtes Bildformat zu codieren. Im folgenden Codebeispiel wird gezeigt, wie das folgende Bild gezeichnet und in einer Datei gespeichert wird.

![Beispiel eines Ausgabe Bilds.](images/saveasimagefile-sample.png)

Dieses Codebeispiel erstellt zuerst eine [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) und ein [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) -Renderziel. Anschließend wird eine Zeichnung mit Text, einer Pfad Geometrie, die ein Stundenglas darstellt, und einem transformierten Stundenglas in eine WIC-Bitmap gerendert. Anschließend wird [IWICStream:: initializefromfilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) verwendet, um die Bitmap in einer Datei zu speichern. Wenn die Anwendung die Bitmap im Arbeitsspeicher speichern muss, verwenden Sie stattdessen [IWICStream:: InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) . Schließlich wird [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) verwendet, um die Bitmap zu codieren.


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

Wie oben gezeigt, ist die Verwendung von Direct2D für serverseitiges Rendering einfach und unkompliziert. Außerdem bietet Sie ein hochwertiges und hochgradig parallelisierbares Rendering, das in Umgebungen mit geringen Rechten auf dem Server ausgeführt werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 
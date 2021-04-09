---
title: Direct2D-Schnellstart
description: Fasst die Schritte zusammen, die zum Zeichnen mit Direct2D erforderlich sind, und stellt Beispielcode bereit.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, Codebeispiel zum Zeichnen des Rechtecks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101694"
---
# <a name="direct2d-quickstart"></a>Direct2D-Schnellstart

Direct2D ist eine API im einheitlichen Code zum Erstellen von 2D-Grafiken. In diesem Thema wird veranschaulicht, wie Direct2D innerhalb einer typischen Win32-Anwendung verwendet wird, um ein **HWND** zu zeichnen.

> [!Note]  
> Wenn Sie eine Windows Store-App erstellen möchten, die Direct2D verwendet, lesen Sie das Thema [Direct2D Quick Start for Windows 8](direct2d-quickstart-with-device-context.md) .

 

Dieses Thema enthält folgende Abschnitte:

-   [Zeichnen eines einfachen Rechtecks](#drawing-a-simple-rectangle)
-   [Schritt 1: einschließen des Direct2D-Headers](#step-1-include-direct2d-header)
-   [Schritt 2: Erstellen eines ID2D1Factory](#step-2-create-an-id2d1factory)
-   [Schritt 3: Erstellen eines ID2D1HwndRenderTarget](#step-3-create-an-id2d1hwndrendertarget)
-   [Schritt 4: Erstellen eines Pinsels](#step-4-create-a-brush)
-   [Schritt 5: Zeichnen des Rechtecks](#step-5-draw-the-rectangle)
-   [Schritt 6: Freigeben von Ressourcen](#step-6-release-resources)
-   [Erstellen einer einfachen Direct2D-Anwendung](#create-a-simple-direct2d-application)
-   [Zugehörige Themen](#related-topics)

## <a name="drawing-a-simple-rectangle"></a>Zeichnen eines einfachen Rechtecks

Wenn Sie ein Rechteck mithilfe von [GDI](/windows/desktop/gdi/windows-gdi)zeichnen möchten, können Sie die [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung wie im folgenden Code gezeigt verarbeiten.


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



Der Code zum Zeichnen desselben Rechtecks mit Direct2D ist ähnlich: er erstellt Zeichnungs Ressourcen, beschreibt eine Form, die gezeichnet werden soll, zeichnet die Form und gibt dann die Zeichnungs Ressourcen frei. In den folgenden Abschnitten werden die einzelnen Schritte ausführlich beschrieben.

## <a name="step-1-include-direct2d-header"></a>Schritt 1: einschließen des Direct2D-Headers

Fügen Sie zusätzlich zu den Headern, die für eine Win32-Anwendung erforderlich sind, den d2d1. h-Header ein.

## <a name="step-2-create-an-id2d1factory"></a>Schritt 2: Erstellen eines ID2D1Factory

Eines der ersten Dinge, bei denen es sich bei allen Direct2D-Beispielen um das Erstellen eines [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)handelt.


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



Die [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Schnittstelle ist der Ausgangspunkt für die Verwendung von Direct2D. Verwenden Sie ein **ID2D1Factory** , um Direct2D-Ressourcen zu erstellen.

Beim Erstellen einer Factory können Sie angeben, ob es sich um einen Multithread oder einen Single Thread handelt. (Weitere Informationen zu Multithread-Factorys finden Sie in den Hinweisen auf der [**ID2D1Factory-Referenzseite**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) In diesem Beispiel wird eine Single Thread Factory erstellt.

Im Allgemeinen sollte die Anwendung die Factory einmal erstellen und für die Lebensdauer der Anwendung beibehalten.

## <a name="step-3-create-an-id2d1hwndrendertarget"></a>Schritt 3: Erstellen eines ID2D1HwndRenderTarget

Nachdem Sie eine Factory erstellt haben, verwenden Sie Sie zum Erstellen eines Renderziels.


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



Ein Renderziel ist ein Gerät, das Zeichnungsvorgänge ausführen und Geräte abhängige Zeichnungs Ressourcen erstellen kann, wie z. b. Pinsel. Verschiedene Renderingziele werden auf unterschiedliche Geräte Renderingziele. Im vorangehenden Beispiel wird ein [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)-Wert verwendet, der in einen Teil des Bildschirms gerendert wird.

Wenn möglich verwendet ein Renderziel die GPU, um Renderingvorgänge zu beschleunigen und Zeichnungs Ressourcen zu erstellen. Andernfalls verwendet das Renderziel die CPU, um Renderingerweiterungen zu verarbeiten und Ressourcen zu erstellen. (Sie können dieses Verhalten ändern, indem Sie beim Erstellen des Renderziels die [**D2D1 \_ \_ \_ renderzieltyp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) -Flags verwenden.)

Die Methode " [**kreatehwndrendertarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) " erfordert drei Parameter. Der erste Parameter, eine Struktur des [**D2D1- \_ \_ Renderziel \_ Properties**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , gibt Remote Anzeigeoptionen an, ob das Renderziel zum Renderingziel für Software oder Hardware und für den dpi-Wert erzwungen werden soll. Der Code in diesem Beispiel verwendet die Hilfsfunktion [**D2D1:: rendertargetproperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) , um die Standardeigenschaften des Renderziels zu akzeptieren.

Der zweite Parameter, eine [**D2D1- \_ HWND- \_ \_ Renderziel \_ Eigenschafts**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) Struktur, gibt das **HWND** an, in dem der Inhalt gerendert wird, die anfängliche Größe des Renderziels (in Pixel) und die [**Darstellungs Optionen**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options). In diesem Beispiel wird die Hilfsfunktion [**D2D1:: hwndrendertargetproperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) verwendet, um ein HWND und eine Anfangs Größe anzugeben. Dabei werden Standard Darstellungs Optionen verwendet.

Der dritte Parameter ist die Adresse des Zeigers, der den renderzielverweis empfängt.

Wenn Sie ein Renderziel erstellen und die Hardwarebeschleunigung verfügbar ist, weisen Sie der GPU des Computers Ressourcen zu. Wenn Sie ein Renderziel einmal erstellen und so lange wie möglich aufbewahren, profitieren Sie von Leistungsvorteilen. Die Anwendung sollte einmal Renderziele erstellen und für die Lebensdauer der Anwendung oder bis zum D2DERR-Erstellungs [**\_ \_ Ziel**](direct2d-error-codes.md) Fehler erhalten. Wenn Sie diesen Fehler erhalten, müssen Sie das Renderziel (und alle erstellten Ressourcen) neu erstellen.

## <a name="step-4-create-a-brush"></a>Schritt 4: Erstellen eines Pinsels

Wie eine Factory kann ein Renderziel Zeichnungs Ressourcen erstellen. In diesem Beispiel erstellt das Renderziel einen Pinsel.


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



Ein Pinsel ist ein Objekt, das einen Bereich zeichnet, z. b. den Strich einer Form oder das Ausfüllen einer Geometrie. Der Pinsel in diesem Beispiel zeichnet einen Bereich mit einer vordefinierten voll Tonfarbe, schwarz.

Direct2D bietet auch andere Pinseltypen: Farbverlaufs Pinsel zum Zeichnen von linearen und radialen Farbverläufen und einen bitmappinsel zum Zeichnen mit Bitmaps und Mustern.

Einige Zeichnungs-APIs stellen Stifte zum Zeichnen von Gliederungen und Pinsel zum Auffüllen von Formen bereit. Direct2D unterscheidet sich von einem Stift Objekt, es wird jedoch ein Pinsel zum Zeichnen von Gliederungen und Ausfüllen von Formen verwendet. Wenn Sie Gliederungen zeichnen, verwenden Sie die [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) -Schnittstelle mit einem Pinsel zum Steuern von Pfad-Übergängen.

Ein Pinsel kann nur mit dem Renderziel, von dem es erstellt wurde, und mit anderen renderzielen in derselben Ressourcen Domäne verwendet werden. Im Allgemeinen sollten Sie Pinsel einmal erstellen und Sie für die Lebensdauer des Renderziels aufbewahren, von dem Sie erstellt wurden. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ist die einzige Ausnahme. Da es relativ preiswert ist, zu erstellen, können Sie jedes Mal, wenn Sie einen Frame zeichnen, ein **ID2D1SolidColorBrush** erstellen, ohne dass eine spürbare Leistungs Beeinträchtigung erzielt wird. Sie können auch eine einzelne **ID2D1SolidColorBrush** verwenden und die Farbe jedes Mal ändern, wenn Sie Sie verwenden.

## <a name="step-5-draw-the-rectangle"></a>Schritt 5: Zeichnen des Rechtecks

Verwenden Sie als nächstes das Renderziel zum Zeichnen des Rechtecks.


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



Die [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) -Methode nimmt zwei Parameter an: das zu zeichnende Rechteck und den Pinsel, der zum Zeichnen der Kontur des Rechtecks verwendet werden soll. Optional können Sie auch die Optionen Stroke Width, Dash Pattern, Line Join und End Cap angeben.

Sie müssen die [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode aufrufen, bevor Sie Zeichenbefehle ausgeben, und Sie müssen die [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode aufrufen, nachdem Sie das Ausgeben von Zeichnungs Befehlen abgeschlossen haben. Die **EndDraw** -Methode gibt ein **HRESULT** zurück, das angibt, ob die Zeichnungs Befehle erfolgreich waren.

## <a name="step-6-release-resources"></a>Schritt 6: Freigeben von Ressourcen

Wenn keine weiteren Frames zum Zeichnen vorhanden sind oder wenn Sie den Fehler " [**D2DERR neu \_ Erstellen \_**](direct2d-error-codes.md) " erhalten, geben Sie das Renderziel und alle von ihm erstellten Geräte frei.


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



Wenn Ihre Anwendung die Verwendung von Direct2D-Ressourcen abgeschlossen hat (z. b. beim Beenden), müssen Sie die Direct2D-Factory freigeben.


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a>Erstellen einer einfachen Direct2D-Anwendung

Der Code in diesem Thema zeigt die grundlegenden Elemente einer Direct2D-Anwendung. Aus Gründen der Kürze lässt das Thema das Anwendungs Framework und den Fehler Behandlungs Code aus, der für eine gut geschriebene Anwendung typisch ist. Eine ausführlichere Exemplarische Vorgehensweise, in der der gesamte Code zum Erstellen einer einfachen Direct2D-Anwendung und bewährte Entwurfsmethoden veranschaulicht wird, finden Sie unter [Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md)
</dt> </dl>

 

 
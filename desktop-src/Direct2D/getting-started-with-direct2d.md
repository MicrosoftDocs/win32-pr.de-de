---
title: Direct2D-Schnellstart
description: Fasst die schritte zusammen, die zum Zeichnen mit Direct2D erforderlich sind, und enthält Beispielcode.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, Beispiel zum Zeichnen des Rechteckcodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f9c4f7ee6ca99feb3cf7169a59ce73ff3b8f8c62c08ddad88b9e5acf5d9a814
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260066"
---
# <a name="direct2d-quickstart"></a>Direct2D-Schnellstart

Direct2D ist eine API mit nativem Code im Direktmodus zum Erstellen von 2D-Grafiken. In diesem Thema wird veranschaulicht, wie Direct2D in einer typischen Win32-Anwendung verwendet wird, um auf ein **HWND zu zeichnen.**

> [!Note]  
> Wenn Sie eine app-Windows Store erstellen möchten, die Direct2D verwendet, lesen Sie den [Direct2D-Schnellstart](direct2d-quickstart-with-device-context.md) für Windows 8 Thema.

 

Dieses Thema enthält folgende Abschnitte:

-   [Zeichnen eines einfachen Rechtecks](#drawing-a-simple-rectangle)
-   [Schritt 1: Direct2D-Header hinzufügen](#step-1-include-direct2d-header)
-   [Schritt 2: Erstellen einer ID2D1Factory](#step-2-create-an-id2d1factory)
-   [Schritt 3: Erstellen einer ID2D1HwndRenderTarget](#step-3-create-an-id2d1hwndrendertarget)
-   [Schritt 4: Erstellen eines Pinsels](#step-4-create-a-brush)
-   [Schritt 5: Zeichnen des Rechtecks](#step-5-draw-the-rectangle)
-   [Schritt 6: Veröffentlichen von Ressourcen](#step-6-release-resources)
-   [Erstellen einer einfachen Direct2D-Anwendung](#create-a-simple-direct2d-application)
-   [Zugehörige Themen](#related-topics)

## <a name="drawing-a-simple-rectangle"></a>Zeichnen eines einfachen Rechtecks

Um ein Rechteck mit [GDI zu](/windows/desktop/gdi/windows-gdi)zeichnen, können Sie die [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) verarbeiten, wie im folgenden Code gezeigt.


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



Der Code zum Zeichnen desselben Rechtecks mit Direct2D ist ähnlich: Er erstellt Zeichnungsressourcen, beschreibt eine zu zeichnende Form, zeichnet die Form und gibt dann die Zeichnungsressourcen frei. In den folgenden Abschnitten werden die einzelnen Schritte ausführlich beschrieben.

## <a name="step-1-include-direct2d-header"></a>Schritt 1: Direct2D-Header hinzufügen

Schließen Sie zusätzlich zu den Headern, die für eine Win32-Anwendung erforderlich sind, den Header d2d1.h ein.

## <a name="step-2-create-an-id2d1factory"></a>Schritt 2: Erstellen einer ID2D1Factory

Eines der ersten Dinge, die ein Direct2D-Beispiel tut, ist das Erstellen einer [**ID2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



Die [**ID2D1Factory-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) ist der Ausgangspunkt für die Verwendung von Direct2D. Verwenden Sie eine **ID2D1Factory,** um Direct2D-Ressourcen zu erstellen.

Wenn Sie eine Factory erstellen, können Sie angeben, ob es sich um eine Multithread- oder Singlethread-Factory handelt. (Weitere Informationen zu Multithreadfactorys finden Sie in den Anmerkungen auf der [**Referenzseite zu ID2D1Factory.)**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) In diesem Beispiel wird eine Singlethread-Factory erstellt.

Im Allgemeinen sollte Ihre Anwendung die Factory einmal erstellen und für die Lebensdauer der Anwendung beibehalten.

## <a name="step-3-create-an-id2d1hwndrendertarget"></a>Schritt 3: Erstellen einer ID2D1HwndRenderTarget

Nachdem Sie eine Factory erstellt haben, verwenden Sie sie, um ein Renderziel zu erstellen.


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



Ein Renderziel ist ein Gerät, das Zeichnungsvorgänge ausführen und geräteabhängige Zeichnungsressourcen wie Pinsel erstellen kann. Verschiedene Arten von Renderzielen werden auf verschiedenen Geräten gerendert. Im vorherigen Beispiel wird [**id2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)verwendet, das in einem Teil des Bildschirms gerendert wird.

Wenn möglich, verwendet ein Renderziel die GPU, um Renderingvorgänge zu beschleunigen und Zeichnungsressourcen zu erstellen. Andernfalls verwendet das Renderziel die CPU, um Renderinganweisungen zu verarbeiten und Ressourcen zu erstellen. (Sie können dieses Verhalten ändern, indem Sie die [**D2D1 \_ RENDER \_ TARGET \_ TYPE-Flags**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) verwenden, wenn Sie das Renderziel erstellen.)

Die [**CreateHwndRenderTarget-Methode nimmt**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) drei Parameter an. Der erste Parameter, eine [**D2D1 \_ RENDER \_ TARGET \_ PROPERTIES-Struktur,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) gibt Optionen für die Remoteanzeige an, unabhängig davon, ob das Renderziel auf Software oder Hardware gerendert werden soll, und der DPI. Der Code in diesem Beispiel verwendet die [**Hilfsfunktion D2D1::RenderTargetProperties,**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) um Standardeigenschaften des Renderziels zu akzeptieren.

Der zweite Parameter, eine [**D2D1 \_ HWND \_ RENDER TARGET \_ \_ PROPERTIES-Struktur,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) gibt den **HWND** an, für den Inhalt gerendert wird, die Anfangsgröße des Renderziels (in Pixel) und seine Darstellungsoptionen. [](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options) In diesem Beispiel wird die [**Hilfsfunktion D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) verwendet, um ein HWND und eine Anfangsgröße anzugeben. Es werden Standardpräsentationsoptionen verwendet.

Der dritte Parameter ist die Adresse des Zeigers, der den Renderzielverweis empfängt.

Wenn Sie ein Renderziel erstellen und die Hardwarebeschleunigung verfügbar ist, ordnen Sie Ressourcen auf der GPU des Computers zu. Wenn Sie ein Renderziel einmal erstellen und so lange wie möglich beibehalten, profitieren Sie von Leistungsvorteilen. Ihre Anwendung sollte Renderziele einmal erstellen und für die Lebensdauer der Anwendung oder bis zum Empfangen des [**Fehlers D2DERR \_ RECREATE \_ TARGET**](direct2d-error-codes.md) an ihnen halten. Wenn dieser Fehler angezeigt wird, müssen Sie das Renderziel (und alle erstellten Ressourcen) neu erstellen.

## <a name="step-4-create-a-brush"></a>Schritt 4: Erstellen eines Pinsels

Wie eine Factory kann ein Renderziel Zeichnungsressourcen erstellen. In diesem Beispiel erstellt das Renderziel einen Pinsel.


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



Ein Pinsel ist ein Objekt, das einen Bereich zeichnet, z. B. den Strich einer Form oder die Füllung einer Geometrie. Der Pinsel in diesem Beispiel zeichnet einen Bereich mit einer vordefinierten Volltonfarbe schwarz.

Direct2D bietet auch andere Arten von Pinseln: Farbverlaufspinsel zum Malen von linearen und radialen Farbverläufen und einen Bitmappinsel zum Malen mit Bitmaps und Mustern.

Einige Zeichnungs-APIs stellen Stifte zum Zeichnen von Konturen und Pinseln zum Füllen von Formen zur Verfügung. Direct2D ist anders: Es stellt kein Stiftobjekt zur Verfügung, sondern verwendet einen Pinsel zum Zeichnen von Konturen und Füllen von Formen. Verwenden Sie beim Zeichnen von Konturen die [**ID2D1StrokeStyle-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) mit einem Pinsel, um Pfadsinteraktionen zu steuern.

Ein Pinsel kann nur mit dem Renderziel, das ihn erstellt hat, und mit anderen Renderzielen in derselben Ressourcendomäne verwendet werden. Im Allgemeinen sollten Sie Pinsel einmal erstellen und für die Lebensdauer des Renderziels beibehalten, mit dem sie erstellt wurden. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ist die einzige Ausnahme. Da die Erstellung relativ kostengünstig ist, können Sie jedes Mal, wenn Sie einen Frame zeichnen, einen **ID2D1SolidColorBrush** erstellen, ohne dass eine spürbare Leistungssteigerung auftritt. Sie können auch einen einzelnen **ID2D1SolidColorBrush** verwenden und bei jeder Verwendung einfach seine Farbe ändern.

## <a name="step-5-draw-the-rectangle"></a>Schritt 5: Zeichnen des Rechtecks

Verwenden Sie als Nächstes das Renderziel, um das Rechteck zu zeichnen.


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



Die [**DrawRectangle-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) verwendet zwei Parameter: das zu zeichnende Rechteck und den Pinsel, der zum Zeichnen der Kontur des Rechtecks verwendet werden soll. Optional können Sie auch die Optionen Strichbreite, Bindestrichmuster, Linienverkn seitlich und Endende angeben.

Sie müssen die [**BeginDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) aufrufen, bevor Sie Zeichnungsbefehle ausführen, und Sie müssen die [**EndDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) aufrufen, nachdem Sie das Ausstellen von Zeichnungsbefehlen abgeschlossen haben. Die **EndDraw-Methode** gibt ein **HRESULT zurück,** das angibt, ob die Zeichnungsbefehle erfolgreich waren.

## <a name="step-6-release-resources"></a>Schritt 6: Veröffentlichen von Ressourcen

Wenn keine frames mehr zu zeichnen sind oder wenn Sie den [**D2DERR \_ RECREATE \_ TARGET-Fehler**](direct2d-error-codes.md) erhalten, geben Sie das Renderziel und alle von ihm erstellten Geräte frei.


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



Wenn Ihre Anwendung die Verwendung von Direct2D-Ressourcen beendet hat (z. B. wenn sie beendet wird), veröffentlichen Sie die Direct2D-Factory.


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a>Erstellen einer einfachen Direct2D-Anwendung

Der Code in diesem Thema zeigt die grundlegenden Elemente einer Direct2D-Anwendung. Zur Kürze werden im Thema das Anwendungsframework und der Fehlerbehandlungscode ausgelassen, der für eine gut geschriebene Anwendung eigenschaft ist. Eine ausführlichere exemplarische Vorgehensweise, die den vollständigen Code zum Erstellen einer einfachen Direct2D-Anwendung und bewährte Entwurfsmethoden veranschaulicht, finden Sie unter Erstellen einer einfachen [Direct2D-Anwendung.](direct2d-quickstart.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md)
</dt> </dl>

 

 
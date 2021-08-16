---
title: Renderziele, Geräte und Ressourcen
description: Renderziele, Geräte und Ressourcen
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381d6e696cc9dce47cc8dad05b0e546371d50c51012daba725eb08f20d247eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387633"
---
# <a name="render-targets-devices-and-resources"></a>Renderziele, Geräte und Ressourcen

Ein *Renderziel ist* einfach die Position, an der das Programm zeichnen wird. In der Regel ist das Renderziel ein Fenster (insbesondere der Clientbereich des Fensters). Es kann sich auch um eine Bitmap im Arbeitsspeicher handelt, die nicht angezeigt wird. Ein Renderziel wird durch die [**ID2D1RenderTarget-Schnittstelle**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) dargestellt.

Ein *Gerät ist* eine Abstraktion, die das darstellt, was die Pixel tatsächlich zeichnet. Ein Hardwaregerät verwendet die GPU für eine schnellere Leistung, während ein Softwaregerät die CPU verwendet. Die Anwendung erstellt das Gerät nicht. Stattdessen wird das Gerät implizit erstellt, wenn die Anwendung das Renderziel erstellt. Jedes Renderziel ist einem bestimmten Gerät zugeordnet, entweder Hardware oder Software.

![Ein Diagramm, das die Beziehung zwischen einem Renderziel und einem Gerät zeigt.](images/graphics09.png)

Eine *Ressource ist* ein Objekt, das das Programm zum Zeichnen verwendet. Im Folgenden finden Sie einige Beispiele für Ressourcen, die in Direct2D definiert sind:

-   **Pinsel**. Steuert, wie Linien und Bereiche gestrichen werden. Pinseltypen umfassen Volltonpinsel und Farbverlaufspinsel.
-   **Strichformat**. Steuert die Darstellung einer Linie, z. B. gestrichelt oder voll.
-   **Geometry**. Stellt eine Auflistung von Linien und Kurven dar.
-   **Mesh**. Eine Form, die aus Dreiecken gebildet wird. Gitternetzdaten können im Gegensatz zu Geometriedaten, die vor dem Rendering konvertiert werden müssen, direkt von der GPU genutzt werden.

Renderziele werden auch als Ressourcentyp betrachtet.

Einige Ressourcen profitieren von der Hardwarebeschleunigung. Eine Ressource dieses Typs ist immer einem bestimmten Gerät zugeordnet, entweder Hardware (GPU) oder Software (CPU). Dieser Ressourcentyp wird als *geräteabhängig bezeichnet.* Pinsel und Gitternetze sind Beispiele für geräteabhängige Ressourcen. Wenn das Gerät nicht mehr verfügbar ist, muss die Ressource für ein neues Gerät neu erstellt werden.

Andere Ressourcen werden im CPU-Arbeitsspeicher beibehalten, unabhängig davon, welches Gerät verwendet wird. Diese Ressourcen sind *geräteunabhängig,* da sie nicht einem bestimmten Gerät zugeordnet sind. Es ist nicht erforderlich, geräteunabhängige Ressourcen neu zu erstellen, wenn sich das Gerät ändert. Stricharten und Geometrien sind geräteunabhängige Ressourcen.

Die MSDN-Dokumentation für jede Ressource gibt an, ob die Ressource geräteabhängig oder geräteunabhängig ist. Jeder Ressourcentyp wird durch eine Schnittstelle dargestellt, die von [**ID2D1Resource ableitung.**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource) Pinsel werden beispielsweise durch die [**ID2D1Brush-Schnittstelle**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) dargestellt.

## <a name="the-direct2d-factory-object"></a>Das Direct2D-Factoryobjekt

Der erste Schritt bei Verwendung von Direct2D ist das Erstellen einer Instanz des Direct2D-Factoryobjekts. Bei der Computerprogrammierung ist *eine Factory* ein Objekt, das andere Objekte erstellt. Die Direct2D-Factory erstellt die folgenden Objekttypen:

-   Renderziele.
-   Geräteunabhängige Ressourcen, z. B. Strichstile und Geometrien.

Geräteabhängige Ressourcen wie Pinsel und Bitmaps werden vom Renderzielobjekt erstellt.

![Ein Diagramm, das die direct2d-Factory zeigt.](images/graphics10.png)

Rufen Sie zum Erstellen des Direct2D-Factoryobjekts [**die Funktion D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) auf.


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



Der erste Parameter ist ein Flag, das Erstellungsoptionen angibt. Das **Flag D2D1 \_ FACTORY TYPE SINGLE \_ \_ \_ THREADED** bedeutet, dass Sie Direct2D nicht aus mehreren Threads aufrufen. Um Aufrufe von mehreren Threads zu unterstützen, geben **Sie D2D1 \_ FACTORY TYPE MULTI \_ \_ \_ THREADED an.** Wenn Ihr Programm einen einzelnen Thread zum Aufrufen von Direct2D verwendet, ist die Singlethreadoption effizienter.

Der zweite Parameter der [**D2D1CreateFactory-Funktion**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) empfängt einen Zeiger auf die [**ID2D1Factory-Schnittstelle.**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory)

Sie sollten das Direct2D-Factoryobjekt vor der ersten [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) erstellen. Der [**WM \_ CREATE-Meldungshandler**](/windows/desktop/winmsg/wm-create) ist ein guter Ort zum Erstellen der Factory:


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a>Erstellen von Direct2D-Ressourcen

Das Circle-Programm verwendet die folgenden geräteabhängigen Ressourcen:

-   Ein Renderziel, das dem Anwendungsfenster zugeordnet ist.
-   Ein Volltonfarbpinsel zum Zeichnen des Kreises.

Jede dieser Ressourcen wird durch eine COM-Schnittstelle dargestellt:

-   Die [**ID2D1HwndRenderTarget-Schnittstelle**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) stellt das Renderziel dar.
-   Die [**ID2D1SolidColorBrush-Schnittstelle**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) stellt den Pinsel dar.

Das Circle-Programm speichert Zeiger auf diese Schnittstellen als Membervariablen der `MainWindow` -Klasse:


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



Mit dem folgenden Code werden diese beiden Ressourcen erstellt.


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



Um ein Renderziel für ein Fenster zu erstellen, rufen Sie die [**ID2D1Factory::CreateHwndRenderTarget-Methode**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) in der Direct2D-Factory auf.

-   Der erste Parameter gibt Optionen an, die allen Renderzieltypen gemeinsam sind. Hier übergeben wir Standardoptionen, indem wir die Hilfsfunktion [**D2D1::RenderTargetProperties aufrufen.**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties)
-   Der zweite Parameter gibt das Handle für das Fenster plus die Größe des Renderziels in Pixel an.
-   Der dritte Parameter empfängt einen [**ID2D1HwndRenderTarget-Zeiger.**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget)

Rufen Sie zum Erstellen des Volltonfarbpinsels die [**ID2D1RenderTarget::CreateSolidColorBrush-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) auf dem Renderziel auf. Die Farbe wird als [**D2D1 \_ COLOR \_ F-Wert**](/windows/desktop/Direct2D/d2d1-color-f) angegeben. Weitere Informationen zu Farben in Direct2D finden Sie unter [Verwenden von Farben in Direct2D.](using-color-in-direct2d.md)

Beachten Sie außerdem, dass die Methode S OK zurückgibt, ohne etwas zu tun, wenn das `CreateGraphicsResources` Renderziel bereits vorhanden ist. **\_** Der Grund für diesen Entwurf wird im nächsten Thema deutlich.

## <a name="next"></a>Nächste

[Zeichnen mit Direct2D](drawing-with-direct2d.md)

 

 
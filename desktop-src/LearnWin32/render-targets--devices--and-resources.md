---
title: Renderziele, Geräte und Ressourcen
description: Renderziele, Geräte und Ressourcen
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314930"
---
# <a name="render-targets-devices-and-resources"></a>Renderziele, Geräte und Ressourcen

Ein *Renderziel* ist einfach der Speicherort, an dem das Programm gezeichnet wird. In der Regel ist das Renderziel ein Fenster (insbesondere der Client Bereich des Fensters). Es kann sich auch um eine Bitmap im Arbeitsspeicher handeln, die nicht angezeigt wird. Ein Renderziel wird durch die [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle dargestellt.

Ein *Gerät* ist eine Abstraktion, die darstellt, was die Pixel tatsächlich zeichnet. Ein Hardware Gerät verwendet die GPU, um die Leistung zu beschleunigen, während ein Software Gerät die CPU verwendet. Das Gerät wird von der Anwendung nicht erstellt. Stattdessen wird das Gerät implizit erstellt, wenn die Anwendung das Renderziel erstellt. Jedes Renderziel ist einem bestimmten Gerät zugeordnet, entweder Hardware oder Software.

![ein Diagramm, das die Beziehung zwischen einem Renderziel und einem Gerät anzeigt.](images/graphics09.png)

Eine *Ressource* ist ein Objekt, das das Programm zum Zeichnen verwendet. Im folgenden finden Sie einige Beispiele für Ressourcen, die in Direct2D definiert sind:

-   **Pinsel**. Steuert, wie Linien und Bereiche gezeichnet werden. Pinseltypen enthalten Pinsel mit voll Tonfarbe und Farbverlaufs Pinsel.
-   **Strich Stil**. Steuert das Aussehen einer Linie – z. b. gestrichelt oder Solid.
-   **Geometrie**. Stellt eine Auflistung von Linien und Kurven dar.
-   **Mesh**. Eine Form, die aus Dreiecken gebildet wird. Mesh-Daten können direkt von der GPU genutzt werden, im Gegensatz zu Geometry-Daten, die vor dem Rendering konvertiert werden müssen.

Renderziele werden auch als Ressourcentyp betrachtet.

Einige Ressourcen profitieren von der Hardwarebeschleunigung. Eine Ressource dieses Typs ist immer einem bestimmten Gerät zugeordnet, entweder Hardware (GPU) oder Software (CPU). Dieser Ressourcentyp wird als *Geräte abhängig* bezeichnet. Pinsel und Netzen sind Beispiele für Geräte abhängige Ressourcen. Wenn das Gerät nicht mehr verfügbar ist, muss die Ressource für ein neues Gerät neu erstellt werden.

Andere Ressourcen werden im CPU-Speicher beibehalten, unabhängig davon, welches Gerät verwendet wird. Diese Ressourcen sind *Geräte unabhängig*, da Sie nicht mit einem bestimmten Gerät verknüpft sind. Geräteunabhängige Ressourcen müssen nicht neu erstellt werden, wenn das Gerät geändert wird. Strich Stile und Geometrien sind geräteunabhängige Ressourcen.

In der MSDN-Dokumentation für jede Ressource wird angegeben, ob die Ressource Geräte abhängig oder Geräte unabhängig ist. Jeder Ressourcentyp wird durch eine Schnittstelle dargestellt, die von [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource)abgeleitet ist. Pinsel werden z. b. durch die [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) -Schnittstelle dargestellt.

## <a name="the-direct2d-factory-object"></a>Das Direct2D Factory-Objekt

Der erste Schritt bei der Verwendung von Direct2D besteht darin, eine Instanz des Direct2D Factory-Objekts zu erstellen. Bei der Computerprogrammierung ist eine *Factory* ein Objekt, mit dem andere Objekte erstellt werden. Die Direct2D-Factory erstellt die folgenden Objekttypen:

-   Renderziele.
-   Geräteunabhängige Ressourcen, z. b. Strich Stile und Geometrien.

Geräte abhängige Ressourcen, z. b. Pinsel und Bitmaps, werden vom renderzielobjekt erstellt.

![ein Diagramm, das die Direct2D-Factory anzeigt.](images/graphics10.png)

Um das Direct2D Factory-Objekt zu erstellen, rufen Sie die [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) -Funktion auf.


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



Der erste Parameter ist ein Flag, das Erstellungs Optionen angibt. Das Flag " **D2D1 \_ Factory \_ Type \_ Single \_ threaded** " bedeutet, dass Sie Direct2D nicht aus mehreren Threads abrufen. Zum unterstützen von Aufrufen aus mehreren Threads geben Sie den **D2D1 \_ Factory- \_ Typ \_ \_ Multithread** an. Wenn das Programm einen einzelnen Thread verwendet, um Direct2D aufzurufen, ist die Single Thread-Option effizienter.

Der zweite Parameter für die [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) -Funktion empfängt einen Zeiger auf die [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) -Schnittstelle.

Vor der ersten WM-Zeichnungs Nachricht sollten Sie das [**Direct2D \_**](/windows/desktop/gdi/wm-paint) Factory-Objekt erstellen. Der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) Message-Handler ist ein guter Ort zum Erstellen der Factory:


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
-   Ein vollfarbiger Pinsel zum Zeichnen des Kreises.

Jede dieser Ressourcen wird durch eine COM-Schnittstelle dargestellt:

-   Die [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Schnittstelle stellt das Renderziel dar.
-   Die [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Schnittstelle stellt den Pinsel dar.

Das Circle-Programm speichert Zeiger auf diese Schnittstellen als Element Variablen der- `MainWindow` Klasse:


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



Der folgende Code erstellt diese beiden Ressourcen.


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



Um ein Renderziel für ein Fenster zu erstellen, rufen Sie die [**ID2D1Factory:: | atehwndrendertarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) -Methode für die Direct2D-Factory auf.

-   Der erste Parameter gibt Optionen an, die für jeden renderzieltyp gelten. Hier werden Standardoptionen durch Aufrufen der Hilfsfunktion [**D2D1:: rendertargetproperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties)übergeben.
-   Der zweite Parameter gibt das Handle für das Fenster plus die Größe des Renderziels in Pixel an.
-   Der dritte Parameter empfängt einen [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Zeiger.

Um den Pinsel mit voll Tonfarbe zu erstellen, rufen Sie die [**ID2D1RenderTarget:: froatesolidcolorbrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) -Methode für das Renderziel auf. Die Farbe wird als [**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) -Wert angegeben. Weitere Informationen zu Farben in Direct2D finden Sie unter [Verwenden von Color in Direct2D](using-color-in-direct2d.md).

Beachten Sie auch Folgendes: Wenn das Renderziel bereits vorhanden ist, `CreateGraphicsResources` gibt die Methode **S \_ OK** zurück, ohne etwas zu tun. Der Grund für diesen Entwurf wird im nächsten Thema deutlich.

## <a name="next"></a>Nächste

[Zeichnen mit Direct2D](drawing-with-direct2d.md)

 

 
---
title: Ihr erstes Direct2D-Programm
description: 'Erstellen wir unser erstes Direct2D-Programm. Das Programm hat nichts mit der Phantasie: \ 8212; Es zeichnet lediglich einen Kreis, der den Client Bereich des Fensters füllt. Dieses Programm führt jedoch viele grundlegende Direct2D-Konzepte ein.'
ms.assetid: 940cc5e4-2952-4714-bf32-c611a965f819
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d445f98c5dc6a6e5d1aa91d913010cb406a67992
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390205"
---
# <a name="your-first-direct2d-program"></a>Ihr erstes Direct2D-Programm

Erstellen wir unser erstes Direct2D-Programm. Das Programm tut nichts, – es zeichnet lediglich einen Kreis, der den Client Bereich des Fensters füllt. Dieses Programm führt jedoch viele grundlegende Direct2D-Konzepte ein.

![ein Screenshot des Kreises-Programms.](images/graphics08.png)

Hier ist das Codelisting für das kreisprogramm. Das Programm verwendet die- `BaseWindow` Klasse erneut, die im Thema Verwalten des [Anwendungs Zustands](managing-application-state-.md)definiert wurde. In späteren Themen wird der Code ausführlich untersucht.


```C++
#include <windows.h>
#include <d2d1.h>
#pragma comment(lib, "d2d1")

#include "basewin.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

class MainWindow : public BaseWindow<MainWindow>
{
    ID2D1Factory            *pFactory;
    ID2D1HwndRenderTarget   *pRenderTarget;
    ID2D1SolidColorBrush    *pBrush;
    D2D1_ELLIPSE            ellipse;

    void    CalculateLayout();
    HRESULT CreateGraphicsResources();
    void    DiscardGraphicsResources();
    void    OnPaint();
    void    Resize();

public:

    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL)
    {
    }

    PCWSTR  ClassName() const { return L"Circle Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};

// Recalculate drawing layout when the size of the window changes.

void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}

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

void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}

void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}

void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR, int nCmdShow)
{
    MainWindow win;

    if (!win.Create(L"Circle", WS_OVERLAPPEDWINDOW))
    {
        return 0;
    }

    ShowWindow(win.Window(), nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}

LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;

    case WM_DESTROY:
        DiscardGraphicsResources();
        SafeRelease(&pFactory);
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        OnPaint();
        return 0;



    case WM_SIZE:
        Resize();
        return 0;
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```





Sie können das komplette Visual Studio-Projekt aus dem [Direct2D Circle-Beispiel](direct2d-circle-sample.md)herunterladen.

## <a name="the-d2d1-namespace"></a>Der D2D1-Namespace

Der **D2D1** -Namespace enthält Hilfsfunktionen und Klassen. Diese sind nicht strikt Teil der Direct2D-API – Sie können Direct2D programmieren, ohne Sie zu verwenden – Sie helfen Ihnen jedoch, Ihren Code zu vereinfachen. Der **D2D1** -Namespace enthält:

-   Eine [**colorf**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) -Klasse zum Erstellen von Farbwerten.
-   Ein [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) zum Erstellen von Transformations Matrizen.
-   Eine Reihe von Funktionen zum Initialisieren von Direct2D-Strukturen.

In diesem Modul werden Beispiele für den **D2D1** -Namespace angezeigt.

## <a name="next"></a>Nächste

[Renderziele, Geräte und Ressourcen](render-targets--devices--and-resources.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D Circle-Beispiel](direct2d-circle-sample.md)
</dt> </dl>

 

 
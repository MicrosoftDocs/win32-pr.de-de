---
title: Erstellen einer einfachen Direct2D-Anwendung
description: Führt Sie durch den Prozess zum Erstellen eines Fensters, das Direct2D-Inhalt rendert.
ms.assetid: a627523e-417a-40cd-82c0-4f0380a3a0b1
keywords:
- Direct2D, Tutorial
- Direct2D, Exemplarische Vorgehensweise
- Direct2D, Erstellen von Anwendungen
- Direct2D, Anwendungen
- Anwendungen für Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d023e348e30b4e421ffe177f30c0c55a344fba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104551685"
---
# <a name="creating-a-simple-direct2d-application"></a>Erstellen einer einfachen Direct2D-Anwendung

In diesem Thema wird Schritt für Schritt erläutert, wie Sie die demoApp-Klasse erstellen, die ein Fenster erstellt und Direct2D verwendet, um ein Raster und zwei Rechtecke zu zeichnen. In diesem Tutorial erfahren Sie, wie Sie Direct2D-Ressourcen erstellen und grundlegende Formen zeichnen. Außerdem erfahren Sie, wie Sie Ihre Anwendung strukturieren, um die Leistung zu steigern, indem Sie die Ressourcen Erstellung minimieren

Um dem Tutorial folgen zu können, können Sie Microsoft Visual Studio 2008 verwenden, um ein Win32-Projekt zu erstellen, und dann den Code im Haupt Anwendungs Header und in der CPP-Datei durch den in diesem Tutorial beschriebenen Code ersetzen.

> [!Note]  
> Wenn Sie eine Windows Store-App erstellen möchten, die Direct2D verwendet, lesen Sie das Thema [Direct2D Quick Start for Windows 8](direct2d-quickstart-with-device-context.md) .

 

Eine Übersicht über die Schnittstellen, die Sie zum Erstellen von Direct2D-Inhalten verwenden können, finden Sie in der [Direct2D-API-Übersicht](the-direct2d-api.md).

Dieses Tutorial enthält die folgenden Teile:

-   [Teil 1: Erstellen des demoApp-Headers](#part-1-create-the-demoapp-header)
-   [Teil 2: Implementieren der Klassen Infrastruktur](#part-2-implement-the-class-infrastructure)
-   [Teil 3: Erstellen von Direct2D-Ressourcen](#part-3-create-direct2d-resources)
-   [Teil 4: Rendering Direct2D Inhalt](#part-4-render-direct2d-content)
-   [Zusammenfassung](#summary)
-   [Zugehörige Themen](#related-topics)

Nach Abschluss erstellt die demoApp-Klasse die in der folgenden Abbildung gezeigte Ausgabe.

![Abbildung von zwei Rechtecke in einem Raster Hintergrund](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a>Teil 1: Erstellen des demoApp-Headers

In diesem Schritt richten Sie Ihre Anwendung für die Verwendung von Direct2D ein, indem Sie die erforderlichen Header und Makros hinzufügen. Außerdem deklarieren Sie die Methoden und Datenmember, die Sie in späteren Teilen dieses Tutorials verwenden werden.

1.  Fügen Sie in ihrer Anwendungs Header Datei die folgenden häufig verwendeten Header ein.
```C++
    // Windows Header Files:
    #include <windows.h>

    // C RunTime Header Files:
    #include <stdlib.h>
    #include <malloc.h>
    #include <memory.h>
    #include <wchar.h>
    #include <math.h>

    #include <d2d1.h>
    #include <d2d1helper.h>
    #include <dwrite.h>
    #include <wincodec.h>
```

    

2.  Deklarieren Sie zusätzliche Funktionen für das Freigeben von Schnittstellen und Makros für die Fehlerbehandlung und das Abrufen der Basisadresse des Moduls.
```C++
    template<class Interface>
    inline void SafeRelease(
        Interface **ppInterfaceToRelease
        )
    {
        if (*ppInterfaceToRelease != NULL)
        {
            (*ppInterfaceToRelease)->Release();

            (*ppInterfaceToRelease) = NULL;
        }
    }


    #ifndef Assert
    #if defined( DEBUG ) || defined( _DEBUG )
    #define Assert(b) do {if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}} while(0)
    #else
    #define Assert(b)
    #endif //DEBUG || _DEBUG
    #endif



    #ifndef HINST_THISCOMPONENT
    EXTERN_C IMAGE_DOS_HEADER __ImageBase;
    #define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
    #endif
```

    

3.  Deklarieren Sie Methoden zum Initialisieren der-Klasse, zum Erstellen und Verwerfen von Ressourcen, zum Verarbeiten der Nachrichten Schleife, zum Rendern von Inhalten und zum Windows-Verfahren.
```C++
    class DemoApp
    {
    public:
        DemoApp();
        ~DemoApp();

        // Register the window class and call methods for instantiating drawing resources
        HRESULT Initialize();

        // Process and dispatch messages
        void RunMessageLoop();

    private:
        // Initialize device-independent resources.
        HRESULT CreateDeviceIndependentResources();

        // Initialize device-dependent resources.
        HRESULT CreateDeviceResources();

        // Release device-dependent resource.
        void DiscardDeviceResources();

        // Draw content.
        HRESULT OnRender();

        // Resize the render target.
        void OnResize(
            UINT width,
            UINT height
            );

        // The windows procedure.
        static LRESULT CALLBACK WndProc(
            HWND hWnd,
            UINT message,
            WPARAM wParam,
            LPARAM lParam
            );

    
};
```



    

4.  Deklarieren Sie Zeiger für ein [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Objekt, ein [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Objekt und zwei [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Objekte als Klassenmember.
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a>Teil 2: Implementieren der Klassen Infrastruktur

In diesem Teil implementieren Sie den demoApp-Konstruktor und-debugtor, seine Initialisierungs-und Nachrichten Schleifen Methoden und die WinMain-Funktion. Die meisten dieser Methoden sehen dieselben wie in anderen Win32-Anwendungen aus. Die einzige Ausnahme ist die Initialize-Methode, die die createdeviceindependentresources-Methode aufruft (die Sie im nächsten Teil definieren), mit der mehrere Direct2D-Ressourcen erstellt werden.

1.  Implementieren Sie in der Klassen Implementierungs Datei den-Klassenkonstruktor und-Dekonstruktor. Der Konstruktor sollte seine Member mit **null** initialisieren. Der debugtor sollte alle als Klassenmember gespeicherten Schnittstellen freigeben.
```C++
    DemoApp::DemoApp() :
        m_hwnd(NULL),
        m_pDirect2dFactory(NULL),
        m_pRenderTarget(NULL),
        m_pLightSlateGrayBrush(NULL),
        m_pCornflowerBlueBrush(NULL)
    {
    }

    
DemoApp::~DemoApp()
    {
        SafeRelease(&m_pDirect2dFactory);
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);

    }
```



    

2.  Implementieren Sie die demoApp:: runmessageloop-Methode, mit der Nachrichten übersetzt und gesendet werden.
```C++
    void DemoApp::RunMessageLoop()
    {
        MSG msg;

        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```

    

3.  Implementieren Sie die Initialize-Methode, die das Fenster erstellt, anzeigt und die demoApp:: createdevicindependentresources-Methode aufruft. Sie implementieren die createdevicindependentresources-Methode im nächsten Abschnitt.
```C++
    HRESULT DemoApp::Initialize()
    {
        HRESULT hr;

        // Initialize device-indpendent resources, such
        // as the Direct2D factory.
        hr = CreateDeviceIndependentResources();

        if (SUCCEEDED(hr))
        {
            // Register the window class.
            WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
            wcex.style         = CS_HREDRAW | CS_VREDRAW;
            wcex.lpfnWndProc   = DemoApp::WndProc;
            wcex.cbClsExtra    = 0;
            wcex.cbWndExtra    = sizeof(LONG_PTR);
            wcex.hInstance     = HINST_THISCOMPONENT;
            wcex.hbrBackground = NULL;
            wcex.lpszMenuName  = NULL;
            wcex.hCursor       = LoadCursor(NULL, IDI_APPLICATION);
            wcex.lpszClassName = L"D2DDemoApp";

            RegisterClassEx(&wcex);


            // Because the CreateWindow function takes its size in pixels,
            // obtain the system DPI and use it to scale the window size.
            FLOAT dpiX, dpiY;

            // The factory returns the current system DPI. This is also the value it will use
            // to create its own windows.
            m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


            // Create the window.
            m_hwnd = CreateWindow(
                L"D2DDemoApp",
                L"Direct2D Demo App",
                WS_OVERLAPPEDWINDOW,
                CW_USEDEFAULT,
                CW_USEDEFAULT,
                static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
                static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
                NULL,
                NULL,
                HINST_THISCOMPONENT,
                this
                );
            hr = m_hwnd ? S_OK : E_FAIL;
            if (SUCCEEDED(hr))
            {
                ShowWindow(m_hwnd, SW_SHOWNORMAL);
                UpdateWindow(m_hwnd);
            }
        }

        return hr;
    }
```

    

4.  Erstellen Sie die WinMain-Methode, die als Einstiegspunkt für die Anwendung fungiert. Initialisieren Sie eine Instanz der demoApp-Klasse, und beginnen Sie mit der Nachrichten Schleife.
```C++
    int WINAPI WinMain(
        HINSTANCE /* hInstance */,
        HINSTANCE /* hPrevInstance */,
        LPSTR /* lpCmdLine */,
        int /* nCmdShow */
        )
    {
        // Use HeapSetInformation to specify that the process should
        // terminate if the heap manager detects an error in any heap used
        // by the process.
        // The return value is ignored, because we want to continue running in the
        // unlikely event that HeapSetInformation fails.
        HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

        if (SUCCEEDED(CoInitialize(NULL)))
        {
            {
                DemoApp app;

                if (SUCCEEDED(app.Initialize()))
                {
                    app.RunMessageLoop();
                }
            }
            CoUninitialize();
        }

        return 0;
    }
```

    

## <a name="part-3-create-direct2d-resources"></a>Teil 3: Erstellen von Direct2D-Ressourcen

In diesem Teil erstellen Sie die Direct2D-Ressourcen, die Sie zum Zeichnen verwenden. Direct2D bietet zwei Arten von Ressourcen: geräteunabhängige Ressourcen, die für die Dauer der Anwendung und Geräte abhängige Ressourcen dauern können. Geräte abhängige Ressourcen sind einem bestimmten renderinggerät zugeordnet und funktionieren nicht mehr, wenn das Gerät entfernt wird.

1.  Implementieren Sie die demoApp:: createdevicindependentresources-Methode. Erstellen Sie in der-Methode eine geräteunabhängige Ressource [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), um andere Direct2D-Ressourcen zu erstellen. Verwenden Sie den **m \_ pDirect2DdFactory** -Klassenmember, um die Factory zu speichern.
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  Implementieren Sie die demoApp:: deatedeviceresources-Methode. Diese Methode erstellt die geräteabhängigen Ressourcen des Fensters, ein Renderziel und zwei Pinsel. Rufen Sie die Größe des Client Bereichs ab, und erstellen Sie eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) mit derselben Größe, die in das **HWND** des Fensters gerendert wird. Speichert das **\_ Renderziel im m prendertarget** -Klassenmember.
```C++
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );
    
```

    

3.  Verwenden Sie das Renderziel, um eine graue [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) und einen Kornblumen blauen **ID2D1SolidColorBrush** zu erstellen.
```C++
            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
```

    

4.  Da diese Methode wiederholt aufgerufen wird, fügen Sie eine if-Anweisung hinzu, um zu überprüfen, ob das **\_ Renderziel (m prendertarget** ) bereits vorhanden ist. Der folgende Code zeigt die komplette Methode "devatedeviceresources".
```C++
    HRESULT DemoApp::CreateDeviceResources()
    {
        HRESULT hr = S_OK;

        if (!m_pRenderTarget)
        {
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );


            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
        }

        return hr;
    }
```

    

5.  Implementieren Sie die Methode demoApp::D iscarddeviceresources. Geben Sie in dieser Methode das Renderziel und die beiden Pinsel, die Sie in der demoApp:: deatedeviceresources-Methode erstellt haben, frei.
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a>Teil 4: Rendering Direct2D Inhalt

In diesem Teil implementieren Sie die Windows-Prozedur, die onrendering-Methode, die den Inhalt zeichnet, und die OnResize-Methode, die die Größe des Renderziels anpasst, wenn die Größe des Fensters geändert wird.

1.  Implementieren Sie die demoApp:: WndProc-Methode, um Fenster Meldungen zu verarbeiten. Geben Sie für die [**WM- \_ Größen**](../winmsg/wm-size.md) Nachricht die demoApp:: OnResize-Methode an, und übergeben Sie Ihr die neue Breite und Höhe. Bei den Nachrichten [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) und [**WM \_ Display Change**](/windows/desktop/gdi/wm-displaychange) wird die demoApp:: onrendering-Methode aufgerufen, um das Fenster zu zeichnen. In den folgenden Schritten implementieren Sie die onrendering-Methode und die OnResize-Methode.
```C++
    LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
    {
        LRESULT result = 0;

        if (message == WM_CREATE)
        {
            LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
            DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

            ::SetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA,
                reinterpret_cast<LONG_PTR>(pDemoApp)
                );

            result = 1;
        }
        else
        {
            DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
                ::GetWindowLongPtrW(
                    hwnd,
                    GWLP_USERDATA
                    )));

            bool wasHandled = false;

            if (pDemoApp)
            {
                switch (message)
                {
                case WM_SIZE:
                    {
                        UINT width = LOWORD(lParam);
                        UINT height = HIWORD(lParam);
                        pDemoApp->OnResize(width, height);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DISPLAYCHANGE:
                    {
                        InvalidateRect(hwnd, NULL, FALSE);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_PAINT:
                    {
                        pDemoApp->OnRender();
                        ValidateRect(hwnd, NULL);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DESTROY:
                    {
                        PostQuitMessage(0);
                    }
                    result = 1;
                    wasHandled = true;
                    break;
                }
            }

            if (!wasHandled)
            {
                result = DefWindowProc(hwnd, message, wParam, lParam);
            }
        }

        return result;
    }
    
```

    

2.  Implementieren Sie die demoApp:: onrendering-Methode. Erstellen Sie zunächst ein **HRESULT**. Aufrufen Sie dann die Methode "kreatedeviceresource". Diese Methode wird jedes Mal aufgerufen, wenn das Fenster gezeichnet wird. Denken Sie daran, dass Sie in Schritt 4 von Teil 3 eine **if** -Anweisung hinzugefügt haben, um zu verhindern, dass die Methode eine Aktion durchgeführt, wenn das Renderziel bereits vorhanden ist
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  Überprüfen Sie, ob die Methode "kreatedeviceresource" erfolgreich war. Wenn dies nicht der Fall ist, führen Sie keine Zeichnung aus.
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  Initiieren Sie in der soeben erstellten **if** -Anweisung das Zeichnen, indem Sie die beginDraw-Methode des Renderziels aufrufen. Legen Sie die Transformation für das Renderziel auf die Identitätsmatrix fest, und löschen Sie das Fenster.
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  Ruft die Größe des Zeichen Bereichs ab.
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  Zeichnen Sie einen Raster Hintergrund, indem Sie eine **for** -Schleife und die [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) -Methode des Renderziels verwenden, um eine Reihe von Zeilen zu zeichnen.
```C++
            // Draw a grid background.
            int width = static_cast<int>(rtSize.width);
            int height = static_cast<int>(rtSize.height);

            for (int x = 0; x < width; x += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                    D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }

            for (int y = 0; y < height; y += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                    D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }
```

    

7.  Erstellen Sie zwei Rechteck primitive, die auf dem Bildschirm zentriert sind.
```C++
            // Draw two rectangles.
            D2D1_RECT_F rectangle1 = D2D1::RectF(
                rtSize.width/2 - 50.0f,
                rtSize.height/2 - 50.0f,
                rtSize.width/2 + 50.0f,
                rtSize.height/2 + 50.0f
                );

            D2D1_RECT_F rectangle2 = D2D1::RectF(
                rtSize.width/2 - 100.0f,
                rtSize.height/2 - 100.0f,
                rtSize.width/2 + 100.0f,
                rtSize.height/2 + 100.0f
                );
    
```

    

8.  Verwenden Sie die [**fillrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) -Methode des Renderziels, um das Innere des ersten Rechtecks mit dem grauen Pinsel zu zeichnen.
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  Verwenden Sie die [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) -Methode des Renderziels, um die Kontur des zweiten Rechtecks mit dem Kornblumen blauen Pinsel zu zeichnen.
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. Aufrufen der [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode des Renderziels. Die **EndDraw** -Methode gibt ein **HRESULT** zurück, um anzugeben, ob die Zeichnungsvorgänge erfolgreich waren. Schließen Sie die **if** -Anweisung, die Sie in Schritt 3 gestartet haben.
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. Überprüfen Sie das von [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)zurückgegebene **HRESULT** . Wenn Sie angibt, dass das Renderziel neu erstellt werden muss, müssen Sie die demoApp::D iscarddeviceresources-Methode abrufen, um Sie freizugeben. Es wird neu erstellt, wenn das Fenster das nächste Mal eine [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -oder eine [**WM \_ Display Change**](/windows/desktop/gdi/wm-displaychange) -Meldung empfängt.
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. Geben Sie das **HRESULT** zurück, und schließen Sie die-Methode.
```C++
        return hr;
    }
```

    

13. Implementieren Sie die demoApp:: OnResize-Methode, sodass die Größe des Renderziels an die neue Fenstergröße angepasst wird.
```C++
    void DemoApp::OnResize(UINT width, UINT height)
    {
        if (m_pRenderTarget)
        {
            // Note: This method can fail, but it's okay to ignore the
            // error here, because the error will be returned again
            // the next time EndDraw is called.
            m_pRenderTarget->Resize(D2D1::SizeU(width, height));
        }
    }
```

    

Sie haben das Tutorial abgeschlossen.

> [!Note]  
> Um Direct2D zu verwenden, stellen Sie sicher, dass die Anwendung die Header Datei d2d1. h enthält und mit der Bibliothek d2d1. lib kompiliert wird. D2d1. h und d2d1. lib finden Sie im [Windows Software Development Kit (SDK) für Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

 

## <a name="summary"></a>Zusammenfassung

In diesem Tutorial haben Sie gelernt, wie Sie Direct2D-Ressourcen erstellen und grundlegende Formen zeichnen. Außerdem haben Sie gelernt, wie Sie Ihre Anwendung strukturieren, um die Leistung zu verbessern, indem Sie die Ressourcen Erstellung

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Direct2D-API](the-direct2d-api.md)
</dt> <dt>

[Verbessern der Leistung von Direct2D](improving-direct2d-performance.md)
</dt> </dl>

 

 
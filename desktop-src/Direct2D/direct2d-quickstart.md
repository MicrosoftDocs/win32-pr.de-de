---
title: Erstellen einer einfachen Direct2D-Anwendung
description: Führt Sie durch den Prozess der Erstellung eines Fensters, das Direct2D-Inhalte rendert.
ms.assetid: a627523e-417a-40cd-82c0-4f0380a3a0b1
keywords:
- Direct2D, Tutorial
- Direct2D, exemplarische Vorgehensweise
- Direct2D, Erstellen von Anwendungen
- Direct2D, Anwendungen
- -Anwendungen für Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907ec9a026005fec03b034978873f012cd956a8a7533d97b85b9122664ef1163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825338"
---
# <a name="creating-a-simple-direct2d-application"></a>Erstellen einer einfachen Direct2D-Anwendung

Dieses Thema führt Sie durch den Prozess der Erstellung der DemoApp-Klasse, die ein Fenster erstellt und Direct2D verwendet, um ein Raster und zwei Rechtecke zu zeichnen. In diesem Tutorial erfahren Sie, wie Sie Direct2D-Ressourcen erstellen und grundlegende Formen zeichnen. Außerdem erfahren Sie, wie Sie Ihre Anwendung strukturieren, um die Leistung zu verbessern, indem Sie die Ressourcenerstellung minimieren.

Um das Tutorial zu befolgen, können Sie Microsoft Visual Studio 2008 verwenden, um ein Win32-Projekt zu erstellen und dann den Code im Hauptanwendungsheader und in der CPP-Datei durch den in diesem Tutorial beschriebenen Code zu ersetzen.

> [!Note]  
> Wenn Sie eine Windows Store-App erstellen möchten, die Direct2D verwendet, lesen Sie das Thema [Direct2D-Schnellstart für Windows 8.](direct2d-quickstart-with-device-context.md)

 

Eine Übersicht über die Schnittstellen, die Sie zum Erstellen von Direct2D-Inhalten verwenden können, finden Sie in der Übersicht über die [Direct2D-API.](the-direct2d-api.md)

Dieses Tutorial enthält die folgenden Teile:

-   [Teil 1: Erstellen des DemoApp-Headers](#part-1-create-the-demoapp-header)
-   [Teil 2: Implementieren der Klasseninfrastruktur](#part-2-implement-the-class-infrastructure)
-   [Teil 3: Erstellen von Direct2D-Ressourcen](#part-3-create-direct2d-resources)
-   [Teil 4: Rendern von Direct2D-Inhalten](#part-4-render-direct2d-content)
-   [Zusammenfassung](#summary)
-   [Zugehörige Themen](#related-topics)

Nach Abschluss des Abschlusses erzeugt die DemoApp-Klasse die In der folgenden Abbildung gezeigte Ausgabe.

![Abbildung von zwei Rechtecke auf einem Rasterhintergrund](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a>Teil 1: Erstellen des DemoApp-Headers

In diesem Schritt richten Sie Ihre Anwendung für die Verwendung von Direct2D ein, indem Sie die erforderlichen Header und Makros hinzufügen. Sie deklarieren auch die Methoden und Datenmember, die Sie in späteren Teilen dieses Tutorials verwenden werden.

1.  Schließen Sie die folgenden häufig verwendeten Header in ihre Anwendungsheaderdatei ein.
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

    

2.  Deklarieren Sie zusätzliche Funktionen zum Freigeben von Schnittstellen und Makros für die Fehlerbehandlung und das Abrufen der Basisadresse des Moduls.
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

    

3.  Deklarieren Sie Methoden zum Initialisieren der -Klasse, zum Erstellen und Verwerfen von Ressourcen, zum Verarbeiten der Nachrichtenschleife, zum Rendern von Inhalten und zur Windows-Prozedur.
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



    

4.  Deklarieren Sie Zeiger für ein [**ID2D1Factory-Objekt,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) ein [**ID2D1HwndRenderTarget-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) und zwei [**ID2D1SolidColorBrush-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) als Klassenmember.
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a>Teil 2: Implementieren der Klasseninfrastruktur

In diesem Teil implementieren Sie den DemoApp-Konstruktor und -Destruktor, seine Initialisierungs- und Nachrichtenschleifenmethoden und die WinMain-Funktion. Die meisten dieser Methoden sehen genauso aus wie in jeder anderen Win32-Anwendung. Die einzige Ausnahme ist die Initialize-Methode, die die CreateDeviceIndependentResources-Methode aufruft (die Sie im nächsten Teil definieren), die mehrere Direct2D-Ressourcen erstellt.

1.  Implementieren Sie in der Klassenimplementierungensdatei den Klassenkonstruktor und den Destruktor. Der Konstruktor sollte seine Member mit **NULL** initialisieren. Der Destruktor sollte alle Schnittstellen freigeben, die als Klassenmember gespeichert sind.
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



    

2.  Implementieren Sie die DemoApp::RunMessageLoop-Methode, die Nachrichten übersetzt und verteilt.
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

    

3.  Implementieren Sie die Initialize-Methode, die das Fenster erstellt, anzeigt und die DemoApp::CreateDeviceIndependentResources-Methode aufruft. Sie implementieren die CreateDeviceIndependentResources-Methode im nächsten Abschnitt.
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

    

4.  Erstellen Sie die WinMain-Methode, die als Einstiegspunkt für die Anwendung dient. Initialisieren Sie eine Instanz der DemoApp-Klasse, und beginnen Sie mit ihrer Nachrichtenschleife.
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

In diesem Teil erstellen Sie die Direct2D-Ressourcen, die Sie zum Zeichnen verwenden. Direct2D bietet zwei Arten von Ressourcen: geräteunabhängige Ressourcen, die für die Dauer der Anwendung bestehen können, und geräteabhängige Ressourcen. Geräteabhängige Ressourcen sind einem bestimmten Renderinggerät zugeordnet und funktionieren nicht mehr, wenn dieses Gerät entfernt wird.

1.  Implementieren Sie die DemoApp::CreateDeviceIndependentResources-Methode. Erstellen Sie in der -Methode eine [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), eine geräteunabhängige Ressource, zum Erstellen anderer Direct2D-Ressourcen. Verwenden Sie den **\_ m pDirect2DdFactory-Klassenmember,** um die Factory zu speichern.
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  Implementieren Sie die DemoApp::CreateDeviceResources-Methode. Diese Methode erstellt die geräteabhängigen Ressourcen des Fensters, ein Renderziel und zwei Pinsel. Rufen Sie die Größe des Clientbereichs ab, und erstellen Sie eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) derselben Größe, die im **HWND** des Fensters gerendert wird. Store das Renderziel im **\_ m pRenderTarget-Klassenmember.**
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

    

3.  Verwenden Sie das Renderziel, um eine graue [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) und eine blau-Blau-ID2D1SolidColorBrush zu erstellen. 
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

    

4.  Da diese Methode wiederholt aufgerufen wird, fügen Sie eine if-Anweisung hinzu, um zu überprüfen, ob das Renderziel (**m \_ pRenderTarget** ) bereits vorhanden ist. Der folgende Code zeigt die vollständige CreateDeviceResources-Methode.
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

    

5.  Implementieren Sie die DemoApp::D iscardDeviceResources-Methode. Geben Sie in dieser Methode das Renderziel und die beiden Pinsel frei, die Sie in der DemoApp::CreateDeviceResources-Methode erstellt haben.
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a>Teil 4: Rendern von Direct2D-Inhalten

In diesem Teil implementieren Sie die Windows-Prozedur, die OnRender-Methode, die Inhalte zeichnet, und die OnResize-Methode, die die Größe des Renderziels anpasst, wenn die Größe des Fensters geändert wird.

1.  Implementieren Sie die DemoApp::WndProc-Methode, um Fenstermeldungen zu verarbeiten. Rufen Sie für die [**WM \_ SIZE-Nachricht**](../winmsg/wm-size.md) die DemoApp::OnResize-Methode auf, und übergeben Sie ihr die neue Breite und Höhe. Rufen Sie für die [**WM \_ PAINT-**](/windows/desktop/gdi/wm-paint) und [**WM \_ DISPLAYCHANGE-Meldungen**](/windows/desktop/gdi/wm-displaychange) die DemoApp::OnRender-Methode auf, um das Fenster zu zeichnen. Sie implementieren die Methoden OnRender und OnResize in den folgenden Schritten.
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

    

2.  Implementieren Sie die DemoApp::OnRender-Methode. Erstellen Sie zunächst ein **HRESULT.** Rufen Sie dann die CreateDeviceResource-Methode auf. Diese Methode wird jedes Mal aufgerufen, wenn das Fenster gezeichnet wird. Denken Sie daran, dass Sie in Schritt 4 von Teil 3 eine **if-Anweisung** hinzugefügt haben, um zu verhindern, dass die -Methode Arbeit leistet, wenn das Renderziel bereits vorhanden ist.
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  Überprüfen Sie, ob die CreateDeviceResource-Methode erfolgreich war. Wenn dies nicht der Fall ist, sollten Sie keine Zeichnungen ausführen.
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  Initiieren Sie innerhalb der soeben erstellten **if-Anweisung** das Zeichnen, indem Sie die BeginDraw-Methode des Renderziels aufrufen. Legen Sie die Transformation des Renderziels auf die Identitätsmatrix fest, und löschen Sie das Fenster.
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  Ruft die Größe des Zeichnungsbereichs ab.
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  Zeichnen Sie einen Rasterhintergrund mithilfe einer **for-Schleife** und der [**DrawLine-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) des Renderziels, um eine Reihe von Linien zu zeichnen.
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

    

7.  Erstellen Sie zwei Primitive des Rechtecks, die auf dem Bildschirm zentriert sind.
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

    

8.  Verwenden Sie die [**FillRectangle-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) des Renderziels, um das Innere des ersten Rechtecks mit dem grauen Pinsel zu zeichnen.
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  Verwenden Sie die [**DrawRectangle-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) des Renderziels, um den Umriss des zweiten Rechtecks mit dem blauen Pinsel "kornflower" zu zeichnen.
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. Rufen Sie die [**EndDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) des Renderziels auf. Die **EndDraw-Methode** gibt ein **HRESULT** zurück, um anzugeben, ob die Zeichnungsvorgänge erfolgreich waren. Schließen  Sie die if-Anweisung, die Sie in Schritt 3 gestartet haben.
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. Überprüfen Sie das von [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)zurückgegebene **HRESULT.** Wenn das Renderziel neu erstellt werden muss, rufen Sie die DemoApp::D iscardDeviceResources-Methode auf, um es freizugeben. Sie wird neu erstellt, wenn das Fenster das nächste Mal eine [**WM \_ PAINT-**](/windows/desktop/gdi/wm-paint) oder [**WM \_ DISPLAYCHANGE-Meldung**](/windows/desktop/gdi/wm-displaychange) empfängt.
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. Geben Sie das **HRESULT zurück,** und schließen Sie die -Methode.
```C++
        return hr;
    }
```

    

13. Implementieren Sie die DemoApp::OnResize-Methode, um die Größe des Renderziels auf die neue Größe des Fensters zu ändern.
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
> Um Direct2D zu verwenden, stellen Sie sicher, dass Ihre Anwendung die Headerdatei d2d1.h enthält und mit der Bibliothek d2d1.lib kompiliert wird. Sie finden d2d1.h und d2d1.lib in [Windows Software Development Kit (SDK) für Windows 7.](https://msdn.microsoft.com/windows/bb980924.aspx)

 

## <a name="summary"></a>Zusammenfassung

In diesem Tutorial haben Sie erfahren, wie Sie Direct2D-Ressourcen erstellen und grundlegende Formen zeichnen. Außerdem haben Sie gelernt, wie Sie Ihre Anwendung strukturieren, um die Leistung zu verbessern, indem Sie die Ressourcenerstellung minimieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Direct2D-API](the-direct2d-api.md)
</dt> <dt>

[Verbessern der Leistung von Direct2D](improving-direct2d-performance.md)
</dt> </dl>

 

 
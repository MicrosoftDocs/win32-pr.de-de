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
# <a name="creating-a-simple-direct2d-application"></a><span data-ttu-id="4d9e3-108">Erstellen einer einfachen Direct2D-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4d9e3-108">Creating a Simple Direct2D Application</span></span>

<span data-ttu-id="4d9e3-109">In diesem Thema wird Schritt für Schritt erläutert, wie Sie die demoApp-Klasse erstellen, die ein Fenster erstellt und Direct2D verwendet, um ein Raster und zwei Rechtecke zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-109">This topic walks you through the process of creating the DemoApp class, which creates a window and uses Direct2D to draw a grid and two rectangles.</span></span> <span data-ttu-id="4d9e3-110">In diesem Tutorial erfahren Sie, wie Sie Direct2D-Ressourcen erstellen und grundlegende Formen zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-110">In this tutorial, you learn how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="4d9e3-111">Außerdem erfahren Sie, wie Sie Ihre Anwendung strukturieren, um die Leistung zu steigern, indem Sie die Ressourcen Erstellung minimieren</span><span class="sxs-lookup"><span data-stu-id="4d9e3-111">You also learn how to structure your application to enhance performance by minimizing resource creation.</span></span>

<span data-ttu-id="4d9e3-112">Um dem Tutorial folgen zu können, können Sie Microsoft Visual Studio 2008 verwenden, um ein Win32-Projekt zu erstellen, und dann den Code im Haupt Anwendungs Header und in der CPP-Datei durch den in diesem Tutorial beschriebenen Code ersetzen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-112">To follow the tutorial, you can use Microsoft Visual Studio 2008 to create a Win32 project and then replace the code in the main application header and cpp file with the code described in this tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="4d9e3-113">Wenn Sie eine Windows Store-App erstellen möchten, die Direct2D verwendet, lesen Sie das Thema [Direct2D Quick Start for Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="4d9e3-113">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="4d9e3-114">Eine Übersicht über die Schnittstellen, die Sie zum Erstellen von Direct2D-Inhalten verwenden können, finden Sie in der [Direct2D-API-Übersicht](the-direct2d-api.md).</span><span class="sxs-lookup"><span data-stu-id="4d9e3-114">For an overview of the interfaces you can use to create Direct2D content, see the [Direct2D API Overview](the-direct2d-api.md).</span></span>

<span data-ttu-id="4d9e3-115">Dieses Tutorial enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="4d9e3-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="4d9e3-116">Teil 1: Erstellen des demoApp-Headers</span><span class="sxs-lookup"><span data-stu-id="4d9e3-116">Part 1: Create the DemoApp Header</span></span>](#part-1-create-the-demoapp-header)
-   [<span data-ttu-id="4d9e3-117">Teil 2: Implementieren der Klassen Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="4d9e3-117">Part 2: Implement the Class Infrastructure</span></span>](#part-2-implement-the-class-infrastructure)
-   [<span data-ttu-id="4d9e3-118">Teil 3: Erstellen von Direct2D-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4d9e3-118">Part 3: Create Direct2D Resources</span></span>](#part-3-create-direct2d-resources)
-   [<span data-ttu-id="4d9e3-119">Teil 4: Rendering Direct2D Inhalt</span><span class="sxs-lookup"><span data-stu-id="4d9e3-119">Part 4: Render Direct2D Content</span></span>](#part-4-render-direct2d-content)
-   [<span data-ttu-id="4d9e3-120">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4d9e3-120">Summary</span></span>](#summary)
-   [<span data-ttu-id="4d9e3-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d9e3-121">Related topics</span></span>](#related-topics)

<span data-ttu-id="4d9e3-122">Nach Abschluss erstellt die demoApp-Klasse die in der folgenden Abbildung gezeigte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-122">Upon completion, the DemoApp class produces the output shown in the following illustration.</span></span>

![Abbildung von zwei Rechtecke in einem Raster Hintergrund](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a><span data-ttu-id="4d9e3-124">Teil 1: Erstellen des demoApp-Headers</span><span class="sxs-lookup"><span data-stu-id="4d9e3-124">Part 1: Create the DemoApp Header</span></span>

<span data-ttu-id="4d9e3-125">In diesem Schritt richten Sie Ihre Anwendung für die Verwendung von Direct2D ein, indem Sie die erforderlichen Header und Makros hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-125">In this step, you set up your application to use Direct2D by adding the necessary headers and macros.</span></span> <span data-ttu-id="4d9e3-126">Außerdem deklarieren Sie die Methoden und Datenmember, die Sie in späteren Teilen dieses Tutorials verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-126">You also declare the methods and data members you'll use in later parts of this tutorial.</span></span>

1.  <span data-ttu-id="4d9e3-127">Fügen Sie in ihrer Anwendungs Header Datei die folgenden häufig verwendeten Header ein.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-127">In your application header file, include the following frequently used headers.</span></span>
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

    

2.  <span data-ttu-id="4d9e3-128">Deklarieren Sie zusätzliche Funktionen für das Freigeben von Schnittstellen und Makros für die Fehlerbehandlung und das Abrufen der Basisadresse des Moduls.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-128">Declare additional functions for releasing interfaces and macros for error handling and retrieving the module's base address.</span></span>
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

    

3.  <span data-ttu-id="4d9e3-129">Deklarieren Sie Methoden zum Initialisieren der-Klasse, zum Erstellen und Verwerfen von Ressourcen, zum Verarbeiten der Nachrichten Schleife, zum Rendern von Inhalten und zum Windows-Verfahren.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-129">Declare methods for initializing the class, creating and discarding resources, handling the message loop, rendering content, and the windows procedure.</span></span>
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



    

4.  <span data-ttu-id="4d9e3-130">Deklarieren Sie Zeiger für ein [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Objekt, ein [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Objekt und zwei [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Objekte als Klassenmember.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-130">Declare pointers for an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object, and two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) objects as class members.</span></span>
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a><span data-ttu-id="4d9e3-131">Teil 2: Implementieren der Klassen Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="4d9e3-131">Part 2: Implement the Class Infrastructure</span></span>

<span data-ttu-id="4d9e3-132">In diesem Teil implementieren Sie den demoApp-Konstruktor und-debugtor, seine Initialisierungs-und Nachrichten Schleifen Methoden und die WinMain-Funktion.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-132">In this part, you implement the DemoApp constructor and destructor, its initialization and message looping methods, and the WinMain function.</span></span> <span data-ttu-id="4d9e3-133">Die meisten dieser Methoden sehen dieselben wie in anderen Win32-Anwendungen aus.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-133">Most of these methods look the same as those found in any other Win32 application.</span></span> <span data-ttu-id="4d9e3-134">Die einzige Ausnahme ist die Initialize-Methode, die die createdeviceindependentresources-Methode aufruft (die Sie im nächsten Teil definieren), mit der mehrere Direct2D-Ressourcen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-134">The only exception is the Initialize method, which calls the CreateDeviceIndependentResources method (which you define in the next part) that creates several Direct2D resources.</span></span>

1.  <span data-ttu-id="4d9e3-135">Implementieren Sie in der Klassen Implementierungs Datei den-Klassenkonstruktor und-Dekonstruktor.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-135">In the class implementation file, implement the class constructor and destructor.</span></span> <span data-ttu-id="4d9e3-136">Der Konstruktor sollte seine Member mit **null** initialisieren.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-136">The constructor should initialize its members to **NULL**.</span></span> <span data-ttu-id="4d9e3-137">Der debugtor sollte alle als Klassenmember gespeicherten Schnittstellen freigeben.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-137">The destructor should release any interfaces stored as class members.</span></span>
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



    

2.  <span data-ttu-id="4d9e3-138">Implementieren Sie die demoApp:: runmessageloop-Methode, mit der Nachrichten übersetzt und gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-138">Implement the DemoApp::RunMessageLoop method that translates and dispatches messages.</span></span>
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

    

3.  <span data-ttu-id="4d9e3-139">Implementieren Sie die Initialize-Methode, die das Fenster erstellt, anzeigt und die demoApp:: createdevicindependentresources-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-139">Implement the Initialize method that creates the window, shows it, and calls the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="4d9e3-140">Sie implementieren die createdevicindependentresources-Methode im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-140">You implement the CreateDeviceIndependentResources method in the next section.</span></span>
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

    

4.  <span data-ttu-id="4d9e3-141">Erstellen Sie die WinMain-Methode, die als Einstiegspunkt für die Anwendung fungiert.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-141">Create the WinMain method that serves as the application entry point.</span></span> <span data-ttu-id="4d9e3-142">Initialisieren Sie eine Instanz der demoApp-Klasse, und beginnen Sie mit der Nachrichten Schleife.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-142">Initialize an instance of the DemoApp class and begin its message loop.</span></span>
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

    

## <a name="part-3-create-direct2d-resources"></a><span data-ttu-id="4d9e3-143">Teil 3: Erstellen von Direct2D-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4d9e3-143">Part 3: Create Direct2D Resources</span></span>

<span data-ttu-id="4d9e3-144">In diesem Teil erstellen Sie die Direct2D-Ressourcen, die Sie zum Zeichnen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-144">In this part, you create the Direct2D resources that you use to draw.</span></span> <span data-ttu-id="4d9e3-145">Direct2D bietet zwei Arten von Ressourcen: geräteunabhängige Ressourcen, die für die Dauer der Anwendung und Geräte abhängige Ressourcen dauern können.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-145">Direct2D provides two types of resources: device-independent resources that can last for the duration of the application, and device-dependent resources.</span></span> <span data-ttu-id="4d9e3-146">Geräte abhängige Ressourcen sind einem bestimmten renderinggerät zugeordnet und funktionieren nicht mehr, wenn das Gerät entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-146">Device-dependent resources are associated with a particular rendering device and will cease to function if that device is removed.</span></span>

1.  <span data-ttu-id="4d9e3-147">Implementieren Sie die demoApp:: createdevicindependentresources-Methode.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-147">Implement the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="4d9e3-148">Erstellen Sie in der-Methode eine geräteunabhängige Ressource [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), um andere Direct2D-Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-148">In the method, create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), a device-independent resource, for creating other Direct2D resources.</span></span> <span data-ttu-id="4d9e3-149">Verwenden Sie den **m \_ pDirect2DdFactory** -Klassenmember, um die Factory zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-149">Use the **m\_pDirect2DdFactory** class member to store the factory.</span></span>
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  <span data-ttu-id="4d9e3-150">Implementieren Sie die demoApp:: deatedeviceresources-Methode.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-150">Implement the DemoApp::CreateDeviceResources method.</span></span> <span data-ttu-id="4d9e3-151">Diese Methode erstellt die geräteabhängigen Ressourcen des Fensters, ein Renderziel und zwei Pinsel.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-151">This method creates the window's device-dependent resources, a render target, and two brushes.</span></span> <span data-ttu-id="4d9e3-152">Rufen Sie die Größe des Client Bereichs ab, und erstellen Sie eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) mit derselben Größe, die in das **HWND** des Fensters gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-152">Retrieve the size of the client area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of the same size that renders to the window's **HWND**.</span></span> <span data-ttu-id="4d9e3-153">Speichert das **\_ Renderziel im m prendertarget** -Klassenmember.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-153">Store the render target in the **m\_pRenderTarget** class member.</span></span>
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

    

3.  <span data-ttu-id="4d9e3-154">Verwenden Sie das Renderziel, um eine graue [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) und einen Kornblumen blauen **ID2D1SolidColorBrush** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-154">Use the render target to create a gray [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) and a cornflower blue **ID2D1SolidColorBrush**.</span></span>
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

    

4.  <span data-ttu-id="4d9e3-155">Da diese Methode wiederholt aufgerufen wird, fügen Sie eine if-Anweisung hinzu, um zu überprüfen, ob das **\_ Renderziel (m prendertarget** ) bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-155">Because this method will be called repeatedly, add an if statement to check whether the render target (**m\_pRenderTarget** ) already exists.</span></span> <span data-ttu-id="4d9e3-156">Der folgende Code zeigt die komplette Methode "devatedeviceresources".</span><span class="sxs-lookup"><span data-stu-id="4d9e3-156">The following code shows the complete CreateDeviceResources method.</span></span>
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

    

5.  <span data-ttu-id="4d9e3-157">Implementieren Sie die Methode demoApp::D iscarddeviceresources.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-157">Implement the DemoApp::DiscardDeviceResources method.</span></span> <span data-ttu-id="4d9e3-158">Geben Sie in dieser Methode das Renderziel und die beiden Pinsel, die Sie in der demoApp:: deatedeviceresources-Methode erstellt haben, frei.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-158">In this method, release the render target and the two brushes you created in the DemoApp::CreateDeviceResources method.</span></span>
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a><span data-ttu-id="4d9e3-159">Teil 4: Rendering Direct2D Inhalt</span><span class="sxs-lookup"><span data-stu-id="4d9e3-159">Part 4: Render Direct2D Content</span></span>

<span data-ttu-id="4d9e3-160">In diesem Teil implementieren Sie die Windows-Prozedur, die onrendering-Methode, die den Inhalt zeichnet, und die OnResize-Methode, die die Größe des Renderziels anpasst, wenn die Größe des Fensters geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-160">In this part, you implement the windows procedure, the OnRender method that paints content, and the OnResize method that adjusts the size of the render target when the window is resized.</span></span>

1.  <span data-ttu-id="4d9e3-161">Implementieren Sie die demoApp:: WndProc-Methode, um Fenster Meldungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-161">Implement the DemoApp::WndProc method to handle window messages.</span></span> <span data-ttu-id="4d9e3-162">Geben Sie für die [**WM- \_ Größen**](../winmsg/wm-size.md) Nachricht die demoApp:: OnResize-Methode an, und übergeben Sie Ihr die neue Breite und Höhe.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-162">For the [**WM\_SIZE**](../winmsg/wm-size.md) message, call the DemoApp::OnResize method and pass it the new width and height.</span></span> <span data-ttu-id="4d9e3-163">Bei den Nachrichten [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) und [**WM \_ Display Change**](/windows/desktop/gdi/wm-displaychange) wird die demoApp:: onrendering-Methode aufgerufen, um das Fenster zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-163">For the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) messages, call the DemoApp::OnRender method to paint the window.</span></span> <span data-ttu-id="4d9e3-164">In den folgenden Schritten implementieren Sie die onrendering-Methode und die OnResize-Methode.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-164">You implement the OnRender and OnResize methods in the steps that follow.</span></span>
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

    

2.  <span data-ttu-id="4d9e3-165">Implementieren Sie die demoApp:: onrendering-Methode.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-165">Implement the DemoApp::OnRender method.</span></span> <span data-ttu-id="4d9e3-166">Erstellen Sie zunächst ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-166">First, create an **HRESULT**.</span></span> <span data-ttu-id="4d9e3-167">Aufrufen Sie dann die Methode "kreatedeviceresource".</span><span class="sxs-lookup"><span data-stu-id="4d9e3-167">Then call the CreateDeviceResource method.</span></span> <span data-ttu-id="4d9e3-168">Diese Methode wird jedes Mal aufgerufen, wenn das Fenster gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-168">This method is called every time the window is painted.</span></span> <span data-ttu-id="4d9e3-169">Denken Sie daran, dass Sie in Schritt 4 von Teil 3 eine **if** -Anweisung hinzugefügt haben, um zu verhindern, dass die Methode eine Aktion durchgeführt, wenn das Renderziel bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="4d9e3-169">Recall that, in step 4 of Part 3, you added an **if** statement to prevent the method from doing any work if the render target already exists.</span></span>
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  <span data-ttu-id="4d9e3-170">Überprüfen Sie, ob die Methode "kreatedeviceresource" erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-170">Verify that the CreateDeviceResource method succeeded.</span></span> <span data-ttu-id="4d9e3-171">Wenn dies nicht der Fall ist, führen Sie keine Zeichnung aus.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-171">If it didn't, don't perform any drawing.</span></span>
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  <span data-ttu-id="4d9e3-172">Initiieren Sie in der soeben erstellten **if** -Anweisung das Zeichnen, indem Sie die beginDraw-Methode des Renderziels aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-172">Inside the **if** statement you just created, initiate drawing by calling the render target's BeginDraw method.</span></span> <span data-ttu-id="4d9e3-173">Legen Sie die Transformation für das Renderziel auf die Identitätsmatrix fest, und löschen Sie das Fenster.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-173">Set the render target's transform to the identity matrix, and clear the window.</span></span>
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  <span data-ttu-id="4d9e3-174">Ruft die Größe des Zeichen Bereichs ab.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-174">Retrieve the size of the drawing area.</span></span>
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  <span data-ttu-id="4d9e3-175">Zeichnen Sie einen Raster Hintergrund, indem Sie eine **for** -Schleife und die [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) -Methode des Renderziels verwenden, um eine Reihe von Zeilen zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-175">Draw a grid background by using a **for** loop and the render target's [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) method to draw a series of lines.</span></span>
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

    

7.  <span data-ttu-id="4d9e3-176">Erstellen Sie zwei Rechteck primitive, die auf dem Bildschirm zentriert sind.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-176">Create two rectangle primitives that are centered on the screen.</span></span>
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

    

8.  <span data-ttu-id="4d9e3-177">Verwenden Sie die [**fillrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) -Methode des Renderziels, um das Innere des ersten Rechtecks mit dem grauen Pinsel zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-177">Use the render target's [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the first rectangle with the gray brush.</span></span>
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  <span data-ttu-id="4d9e3-178">Verwenden Sie die [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) -Methode des Renderziels, um die Kontur des zweiten Rechtecks mit dem Kornblumen blauen Pinsel zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-178">Use the render target's [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the second rectangle with the cornflower blue brush.</span></span>
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. <span data-ttu-id="4d9e3-179">Aufrufen der [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-179">Call the render target's [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="4d9e3-180">Die **EndDraw** -Methode gibt ein **HRESULT** zurück, um anzugeben, ob die Zeichnungsvorgänge erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-180">The **EndDraw** method returns an **HRESULT** to indicate whether the drawing operations were successful.</span></span> <span data-ttu-id="4d9e3-181">Schließen Sie die **if** -Anweisung, die Sie in Schritt 3 gestartet haben.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-181">Close the **if** statement you began in Step 3.</span></span>
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. <span data-ttu-id="4d9e3-182">Überprüfen Sie das von [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)zurückgegebene **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4d9e3-182">Check the **HRESULT** returned by [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span> <span data-ttu-id="4d9e3-183">Wenn Sie angibt, dass das Renderziel neu erstellt werden muss, müssen Sie die demoApp::D iscarddeviceresources-Methode abrufen, um Sie freizugeben. Es wird neu erstellt, wenn das Fenster das nächste Mal eine [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -oder eine [**WM \_ Display Change**](/windows/desktop/gdi/wm-displaychange) -Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-183">If it indicates that the render target needs to be recreated, call the DemoApp::DiscardDeviceResources method to release it; it will be recreated the next time the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) or [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span>
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. <span data-ttu-id="4d9e3-184">Geben Sie das **HRESULT** zurück, und schließen Sie die-Methode.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-184">Return the **HRESULT** and close the method.</span></span>
```C++
        return hr;
    }
```

    

13. <span data-ttu-id="4d9e3-185">Implementieren Sie die demoApp:: OnResize-Methode, sodass die Größe des Renderziels an die neue Fenstergröße angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-185">Implement the DemoApp::OnResize method so that it resizes the render target to the new size of the window.</span></span>
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

    

<span data-ttu-id="4d9e3-186">Sie haben das Tutorial abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-186">You've completed the tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="4d9e3-187">Um Direct2D zu verwenden, stellen Sie sicher, dass die Anwendung die Header Datei d2d1. h enthält und mit der Bibliothek d2d1. lib kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-187">To use Direct2D, ensure that your application includes the d2d1.h header file and compiles against the d2d1.lib library.</span></span> <span data-ttu-id="4d9e3-188">D2d1. h und d2d1. lib finden Sie im [Windows Software Development Kit (SDK) für Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4d9e3-188">You can find d2d1.h and d2d1.lib in [Windows Software Development Kit (SDK) for Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

 

## <a name="summary"></a><span data-ttu-id="4d9e3-189">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4d9e3-189">Summary</span></span>

<span data-ttu-id="4d9e3-190">In diesem Tutorial haben Sie gelernt, wie Sie Direct2D-Ressourcen erstellen und grundlegende Formen zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4d9e3-190">In this tutorial, you learned how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="4d9e3-191">Außerdem haben Sie gelernt, wie Sie Ihre Anwendung strukturieren, um die Leistung zu verbessern, indem Sie die Ressourcen Erstellung</span><span class="sxs-lookup"><span data-stu-id="4d9e3-191">You also learned how to structure your application to enhance performance by minimizing resource creation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d9e3-192">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d9e3-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d9e3-193">Übersicht über die Direct2D-API</span><span class="sxs-lookup"><span data-stu-id="4d9e3-193">Direct2D API Overview</span></span>](the-direct2d-api.md)
</dt> <dt>

[<span data-ttu-id="4d9e3-194">Verbessern der Leistung von Direct2D</span><span class="sxs-lookup"><span data-stu-id="4d9e3-194">Improving the Performance of Direct2D</span></span>](improving-direct2d-performance.md)
</dt> </dl>

 

 
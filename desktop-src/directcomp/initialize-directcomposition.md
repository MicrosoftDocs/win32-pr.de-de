---
title: Initialisieren von directcomposition
description: In diesem Thema wird veranschaulicht, wie der minimale Satz von Microsoft directcomposition-Objekten, die zum Erstellen einer einfachen Komposition benötigt werden, erstellt und initialisiert wird.
ms.assetid: F2BF9CE2-05EF-4345-A00E-F5C8A8660B24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8d248c3036bd0c901ee318ae0274809dafdf20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102106"
---
# <a name="how-to-initialize-directcomposition"></a>Initialisieren von directcomposition

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema wird veranschaulicht, wie der minimale Satz von Microsoft directcomposition-Objekten, die zum Erstellen einer einfachen Komposition benötigt werden, erstellt und initialisiert wird.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [DirectComposition](directcomposition-portal.md)
-   [Direct3D 11-Grafik](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [DirectX-Grafik Infrastruktur (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Microsoft Win32
-   Component Object Model (COM)

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-the-direct3d-device-object"></a>Schritt 1: Erstellen des Direct3D-Geräte Objekts

Verwenden Sie die [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) -Funktion aus der Microsoft Direct3D-API, um eine Instanz eines Geräte Objekts zu erstellen, das den Anzeige Adapter darstellt.


```C++
    ID3D11Device *m_pD3D11Device;


    D3D_FEATURE_LEVEL featureLevelSupported;

    // Create the D3D device object. The D3D11_CREATE_DEVICE_BGRA_SUPPORT
    // flag enables rendering on surfaces using Direct2D.
    hr = D3D11CreateDevice(
        nullptr,
        D3D_DRIVER_TYPE_HARDWARE,
        NULL,
        D3D11_CREATE_DEVICE_BGRA_SUPPORT, 
        NULL,
        0,
        D3D11_SDK_VERSION,
        &m_pD3D11Device,
        &featureLevelSupported,
        nullptr);
```





### <a name="step-2-retrieve-a-pointer-to-the-dxgi-object"></a>Schritt 2: Abrufen eines Zeigers auf das DXGI-Objekt

Verwenden Sie die **QueryInterface** -Methode, um den [**idxgidevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) -Zeiger aus dem Direct3D-Geräte Objekt abzurufen. Directcomposition verwendet das Microsoft DirectX Graphics Infrastructure (DXGI)-Objekt, um alle Surface-Objekte für das directcomposition-Gerät zu erstellen.


```C++
    IDXGIDevice *pDXGIDevice = nullptr;

    // Check the result of calling D3D11CreateDriver.
    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = m_pD3D11Device->QueryInterface(&pDXGIDevice);
    }
```



### <a name="step-3-create-the-directcomposition-device-object"></a>Schritt 3: Erstellen des directcomposition-Geräte Objekts

Verwenden Sie die [**dcompositionkreatedevice**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) -Funktion, um eine Instanz des directcomposition-Geräte Objekts zu erstellen. Geben Sie dabei den [**idxgidevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) -Zeiger an, den Sie im vorherigen Schritt abgerufen haben. Die-Funktion Ruft einen [**idcompositiondevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) -Zeiger ab, der zum Erstellen aller anderen directcomposition-Objekte verwendet wird, die in einer Komposition verwendet werden.


```C++
    IDCompositionDevice *m_pDCompDevice;


    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, 
                __uuidof(IDCompositionDevice), 
                reinterpret_cast<void **>(&m_pDCompDevice));
    }
```





### <a name="step-4-create-the-composition-target-object"></a>Schritt 4: Erstellen des Kompositions Zielobjekts

Verwenden Sie die [**idcompositiondevice:: kreatetargetforhwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) -Methode, um eine Instanz des Kompositions Zielobjekts zu erstellen. Durch Aufrufen von **createtargetforhwnd** wird das Geräte Objekt an das Anwendungsfenster gebunden, in dem die Komposition angezeigt wird.


```C++
    IDCompositionTarget *m_pDCompTarget;


    if (SUCCEEDED(hr))
    {
        // Create the composition target object based on the 
        // specified application window.
        hr = m_pDCompDevice->CreateTargetForHwnd(m_hwnd, TRUE, &m_pDCompTarget);   
    }
```





### <a name="step-5-create-a-visual-object"></a>Schritt 5: Erstellen eines visuellen Objekts

Verwenden Sie die [**idcompositiondevice:: anatevisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual) -Methode, um ein visuelles Objekt zu erstellen. Die-Methode ruft einen [**idcompositionvisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual) -Zeiger ab, der verwendet wird, um die Eigenschaften des visuellen Elements festzulegen. Weitere Informationen finden Sie unter [Eigenschaften eines visuellen Objekts](basic-concepts.md).


```C++
    IDCompositionVisual *pVisual = nullptr;

    // Create a visual object.          
    hr = m_pDCompDevice->CreateVisual(&pVisual);  
```



### <a name="step-6-create-a-composition-surface-and-render-a-bitmap-to-the-surface"></a>Schritt 6: Erstellen einer Kompositions Oberfläche und renderens einer Bitmap auf der Oberfläche

Erstellen Sie einen [**idcompositionsurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface) -Zeiger.


```C++
    IDCompositionSurface *pSurface = nullptr;

    if (SUCCEEDED(hr))
    {
        // Create a composition surface and render a GDI bitmap 
        // to the surface.
        hr = MyCreateGDIRenderedDCompSurface(m_hBitmap, &pSurface);
    }
```



Die folgende Funktion erstellt eine Microsoft directcomposition-Oberfläche und zeichnet die Bitmap auf der-Oberfläche.


```C++
// MyCreateGDIRenderedDCompSurface - Creates a DirectComposition surface and 
//   copies the bitmap to the surface. 
//
// Parameters:
//   hBitmap - a GDI bitmap.
//   ppSurface - the composition surface object.
//                                                                 
HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface)
{
    HRESULT hr = S_OK;

    int bitmapWidth = 0;
    int bitmapHeight = 0;
    int bmpSize = 0;
    BITMAP bmp = { };
    HBITMAP hBitmapOld = NULL;

    HDC hSurfaceDC = NULL;  
    HDC hBitmapDC = NULL;

    IDXGISurface1 *pDXGISurface = nullptr;
    IDCompositionSurface *pDCSurface = nullptr;
    POINT pointOffset = { };

    if (ppSurface == nullptr)
        return E_INVALIDARG;

    // Get information about the bitmap.
    bmpSize = GetObject(hBitmap, sizeof(BITMAP), &bmp);

    hr = bmpSize ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Save the bitmap dimensions.
        bitmapWidth = bmp.bmWidth;
        bitmapHeight = bmp.bmHeight;

        // Create a DirectComposition-compatible surface that is the same size 
        // as the bitmap. The DXGI_FORMAT_B8G8R8A8_UNORM flag is required for 
        // rendering on the surface using GDI via GetDC.
        hr = m_pDCompDevice->CreateSurface(bitmapWidth, bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, &pDCSurface);
    }

    if (SUCCEEDED(hr)) 
    {
        // Begin rendering to the surface.
        hr = pDCSurface->BeginDraw(NULL, __uuidof(IDXGISurface1), 
            reinterpret_cast<void**>(&pDXGISurface), &pointOffset);
    }

    if (SUCCEEDED(hr)) 
    {
        // Get the device context (DC) for the surface.
        hr = pDXGISurface->GetDC(FALSE, &hSurfaceDC);
    }

    if (SUCCEEDED(hr))
    {
        // Create a compatible DC and select the surface 
        // into the DC.
        hBitmapDC = CreateCompatibleDC(hSurfaceDC);
        if (hBitmapDC != NULL)
        {
            hBitmapOld = (HBITMAP)SelectObject(hBitmapDC, hBitmap);
            BitBlt(hSurfaceDC, pointOffset.x, pointOffset.y, 
                bitmapWidth, bitmapHeight, hBitmapDC, 0, 0, SRCCOPY);
            
            if (hBitmapOld)
            {
                SelectObject(hBitmapDC, hBitmapOld);
            }
            DeleteDC(hBitmapDC);
        }

        pDXGISurface->ReleaseDC(NULL);
    }

    // End the rendering.
    pDCSurface->EndDraw();
    *ppSurface = pDCSurface;

    // Call an application-defined macro to free the surface pointer.
    SafeRelease(&pDXGISurface);

    return hr;
}
```



### <a name="step-7-bind-surface-to-visual-and-set-the-properties-of-the-visual-object"></a>Schritt 7: Binden der Oberfläche an die Visualisierung und Festlegen der Eigenschaften des visuellen Objekts

Rufen Sie die Methoden der [**idcompositionvisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual) -Schnittstelle des visuellen Objekts auf, um die Eigenschaften des visuellen Objekts festzulegen.

Im nächsten Beispiel wird der Bitmapinhalt für das visuelle Element und die horizontale und vertikale Position des visuellen Elements relativ zur oberen linken Ecke des Containers festgelegt. Da es sich um das visuelle Stamm Element handelt, ist der Container für dieses visuelle Element das Fenster Kompositions Ziel.


```C++
    if (SUCCEEDED(hr))
    {
        // Set the bitmap content of the visual. 
        hr = pVisual->SetContent(pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the horizontal and vertical position of the visual relative
        // to the upper-left corner of the composition target window.
        hr = pVisual->SetOffsetX(xOffset);  
        if (SUCCEEDED(hr))
        {
            hr = pVisual->SetOffsetY(yOffset);  
        }
    }
```



### <a name="step-8-set-the-root-visual-of-the-visual-tree"></a>Schritt 8: Festlegen der visuellen Stamm Visualisierung der visuellen Struktur

Legen Sie das visuelle Stamm Element der visuellen Struktur fest, indem Sie die [**idcompositiontarget:: setRoot**](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot) -Methode aufrufen.


```C++
    if (SUCCEEDED(hr))
    {
        // Set the visual to be the root of the visual tree.          
        hr = m_pDCompTarget->SetRoot(pVisual);  
    }
```



### <a name="step-9-commit-the-composition"></a>Schritt 9: Commit der Komposition ausführen

Rufen Sie die [**idcompositiondevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) -Methode auf, um den Batch von Befehlen für die Verarbeitung in directcomposition zu committen. Die resultierende Komposition wird im Zielfenster angezeigt.


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDCompDevice->Commit();  
    }
```



### <a name="step-10-free-the-directcomposition-objects"></a>Schritt 10: Freigeben der directcomposition-Objekte

Es empfiehlt sich, alle visuellen Objekte freizugeben, sobald Sie Sie nicht mehr benötigen. Im folgenden Beispiel wird das Anwendungs definierte [**saferelease**](/windows/desktop/medfound/saferelease) -Makro aufgerufen, um das visuelle Objekt freizugeben.


```C++
    // Free the visual. 
    SafeRelease(&pVisual);
```



Denken Sie auch daran, das DXGI-Objekt, das Geräte Objekt und das Kompositions Zielobjekt freizugeben, bevor die Anwendung beendet wird.


```C++
    SafeRelease(&pDXGIDevice);
```




```C++
    SafeRelease(&m_pDCompDevice);
    SafeRelease(&m_pDCompTarget);
    SafeRelease(&m_pD3D11Device);
```



## <a name="complete-example"></a>Vollständiges Beispiel


```C++
//
// SimpleComposition.h
//
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

#pragma once
// Modify the following definitions if you need to target a platform prior to the ones specified below.
// Refer to MSDN for the latest info on corresponding values for different platforms.
#ifndef WINVER              // Allow use of features specific to Windows 7 or later.
#define WINVER 0x0700       // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT        // Allow use of features specific to Windows 7 or later.
#define _WIN32_WINNT 0x0700 // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN     // Exclude rarely-used items from Windows headers

// Windows Header Files:
#include <windows.h>

// C RunTime Header Files
#include <math.h>

// DirectComposition Header Files
#include <dcomp.h>

// Direct3D Header Files
#include <d3d11.h>

/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
    )
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}

#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT Initialize();

    void RunMessageLoop();

private:
    HRESULT InitializeDirectCompositionDevice();

    HRESULT CreateResources();
    void DiscardResources();

    HRESULT OnClientClick();

    HRESULT LoadResourceGDIBitmap(
        PCWSTR resourceName, 
        HBITMAP &hbmp
        );

    HRESULT MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface);

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

 private:
    HWND m_hwnd;
    HBITMAP m_hBitmap;
    ID3D11Device *m_pD3D11Device;
    IDCompositionDevice *m_pDCompDevice;
    IDCompositionTarget *m_pDCompTarget;
 };


//
// SimpleComposition.cpp
//
// THIS CODE AND INFORMATION IS PROVIDED &quot;AS IS&quot; WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

// Instructions: Right-click in the client area to cause DirectCompostion
// to create a simple composition consisting of a single GDI bitmap.

#include &quot;SimpleComposition.h&quot;

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE /* hInstance */,
    HINSTANCE /* hPrevInstance */,
    LPSTR /* lpCmdLine */,
    int /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
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

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                         *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_hwnd(NULL),
    m_hBitmap(NULL),
    m_pDCompDevice(nullptr),
    m_pDCompTarget(nullptr),
    m_pD3D11Device(nullptr)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()
{
    SafeRelease(&m_pDCompDevice);
    SafeRelease(&m_pDCompTarget);
    SafeRelease(&m_pD3D11Device);
}

/*******************************************************************
*                                                                  *
*  Create the application window.                                  *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::Initialize()
{
    HRESULT hr;

    // Register the window class.
    WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
    wcex.style         = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc   = DemoApp::WndProc;
    wcex.cbClsExtra    = 0;
    wcex.cbWndExtra    = sizeof(LONG_PTR);
    wcex.hInstance     = HINST_THISCOMPONENT;
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
    wcex.lpszMenuName  = nullptr;
    wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wcex.lpszClassName = L&quot;DirectCompDemoApp&quot;;

    RegisterClassEx(&wcex);

    // Create the application window.
    //
    // Because the CreateWindow function takes its size in pixels, we
    // obtain the system DPI and use it to scale the window size.
    int dpiX = 0;
    int dpiY = 0;
    HDC hdc = GetDC(NULL);
    if (hdc)
    {
        dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
        dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
        ReleaseDC(NULL, hdc);
    }

    m_hwnd = CreateWindow(
        L&quot;DirectCompDemoApp&quot;,
        L&quot;DirectComposition Demo Application&quot;,
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

        // Initialize DirectComposition resources, such as the
        // device object and composition target object.
        hr = InitializeDirectCompositionDevice();
    }

    if (SUCCEEDED(hr))
    {
        hr = CreateResources();
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the DirectComposition device object and    *
*  and the composition target object. These objects endure for    *
*  the lifetime of the application.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::InitializeDirectCompositionDevice()
{
    HRESULT hr = S_OK;

    D3D_FEATURE_LEVEL featureLevelSupported;

    // Create the D3D device object. The D3D11_CREATE_DEVICE_BGRA_SUPPORT
    // flag enables rendering on surfaces using Direct2D.
    hr = D3D11CreateDevice(
        nullptr,
        D3D_DRIVER_TYPE_HARDWARE,
        NULL,
        D3D11_CREATE_DEVICE_BGRA_SUPPORT, 
        NULL,
        0,
        D3D11_SDK_VERSION,
        &m_pD3D11Device,
        &featureLevelSupported,
        nullptr);

    IDXGIDevice *pDXGIDevice = nullptr;

    // Check the result of calling D3D11CreateDriver.
    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = m_pD3D11Device->QueryInterface(&pDXGIDevice);
    }

    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, 
                __uuidof(IDCompositionDevice), 
                reinterpret_cast<void **>(&m_pDCompDevice));
    }
    if (SUCCEEDED(hr))
    {
        // Create the composition target object based on the 
        // specified application window.
        hr = m_pDCompDevice->CreateTargetForHwnd(m_hwnd, TRUE, &m_pDCompTarget);   
    }

    SafeRelease(&pDXGIDevice);

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the GDI bitmap that the application gives  *
*  to DirectComposition to be composed.                           *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateResources()
{
    HRESULT hr = S_OK;

    hr = LoadResourceGDIBitmap(L&quot;Logo&quot;, m_hBitmap);
   
    return hr;
}

/******************************************************************
*                                                                 *
*  Discard device-specific resources.                             *
*                                                                 *
******************************************************************/

void DemoApp::DiscardResources()
{
    DeleteObject(m_hBitmap);
}

/******************************************************************
*                                                                 *
*  The main window&#39;s message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}

/******************************************************************
*                                                                 *
*  Called whenever the user clicks in client area of the main     *
*  window. This method builds a simple visual tree and passes it  *   
*  to DirectComposition.
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnClientClick()
{
    HRESULT hr = S_OK;
    float xOffset = 20; // horizonal position of visual
    float yOffset = 20; // vertical position of visual

    IDCompositionVisual *pVisual = nullptr;

    // Create a visual object.          
    hr = m_pDCompDevice->CreateVisual(&pVisual);  

    IDCompositionSurface *pSurface = nullptr;

    if (SUCCEEDED(hr))
    {
        // Create a composition surface and render a GDI bitmap 
        // to the surface.
        hr = MyCreateGDIRenderedDCompSurface(m_hBitmap, &pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the bitmap content of the visual. 
        hr = pVisual->SetContent(pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the horizontal and vertical position of the visual relative
        // to the upper-left corner of the composition target window.
        hr = pVisual->SetOffsetX(xOffset);  
        if (SUCCEEDED(hr))
        {
            hr = pVisual->SetOffsetY(yOffset);  
        }
    }

    if (SUCCEEDED(hr))
    {
        // Set the visual to be the root of the visual tree.          
        hr = m_pDCompTarget->SetRoot(pVisual);  
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDCompDevice->Commit();  
    }

    // Free the visual. 
    SafeRelease(&pVisual);

    return hr;
}

/******************************************************************
*                                                                 *
*  The window&#39;s message handler.                                  *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
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
            case WM_LBUTTONDOWN:
                {
                    pDemoApp->OnClientClick();
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                    pDemoApp->DiscardResources();
                }
                wasHandled = true;
                result = 1;
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

/******************************************************************
*                                                                 *
*  This method loads the specified GDI bitmap from the            *
*  application resources, creates a new bitmap that is in a       *
*  format that DirectComposition can use, and copies the contents *
*  of the original bitmap to the new bitmap.                      *
*                                                                 *
******************************************************************/

HRESULT DemoApp::LoadResourceGDIBitmap(PCWSTR resourceName, HBITMAP &hbmp)
{
    hbmp = static_cast<HBITMAP>(LoadImageW(HINST_THISCOMPONENT, resourceName, 
        IMAGE_BITMAP, 0, 0, LR_DEFAULTCOLOR));  
 
    return hbmp ? S_OK : E_FAIL;
}


// MyCreateGDIRenderedDCompSurface - Creates a DirectComposition surface and 
//   copies the bitmap to the surface. 
//
// Parameters:
//   hBitmap - a GDI bitmap.
//   ppSurface - the composition surface object.
//                                                                 
HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface)
{
    HRESULT hr = S_OK;

    int bitmapWidth = 0;
    int bitmapHeight = 0;
    int bmpSize = 0;
    BITMAP bmp = { };
    HBITMAP hBitmapOld = NULL;

    HDC hSurfaceDC = NULL;  
    HDC hBitmapDC = NULL;

    IDXGISurface1 *pDXGISurface = nullptr;
    IDCompositionSurface *pDCSurface = nullptr;
    POINT pointOffset = { };

    if (ppSurface == nullptr)
        return E_INVALIDARG;

    // Get information about the bitmap.
    bmpSize = GetObject(hBitmap, sizeof(BITMAP), &bmp);

    hr = bmpSize ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Save the bitmap dimensions.
        bitmapWidth = bmp.bmWidth;
        bitmapHeight = bmp.bmHeight;

        // Create a DirectComposition-compatible surface that is the same size 
        // as the bitmap. The DXGI_FORMAT_B8G8R8A8_UNORM flag is required for 
        // rendering on the surface using GDI via GetDC.
        hr = m_pDCompDevice->CreateSurface(bitmapWidth, bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, &pDCSurface);
    }

    if (SUCCEEDED(hr)) 
    {
        // Begin rendering to the surface.
        hr = pDCSurface->BeginDraw(NULL, __uuidof(IDXGISurface1), 
            reinterpret_cast<void**>(&pDXGISurface), &pointOffset);
    }

    if (SUCCEEDED(hr)) 
    {
        // Get the device context (DC) for the surface.
        hr = pDXGISurface->GetDC(FALSE, &hSurfaceDC);
    }

    if (SUCCEEDED(hr))
    {
        // Create a compatible DC and select the surface 
        // into the DC.
        hBitmapDC = CreateCompatibleDC(hSurfaceDC);
        if (hBitmapDC != NULL)
        {
            hBitmapOld = (HBITMAP)SelectObject(hBitmapDC, hBitmap);
            BitBlt(hSurfaceDC, pointOffset.x, pointOffset.y, 
                bitmapWidth, bitmapHeight, hBitmapDC, 0, 0, SRCCOPY);
            
            if (hBitmapOld)
            {
                SelectObject(hBitmapDC, hBitmapOld);
            }
            DeleteDC(hBitmapDC);
        }

        pDXGISurface->ReleaseDC(NULL);
    }

    // End the rendering.
    pDCSurface->EndDraw();
    *ppSurface = pDCSurface;

    // Call an application-defined macro to free the surface pointer.
    SafeRelease(&pDXGISurface);

    return hr;
}

```





## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Dcompositionkreatedevice**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice)
</dt> <dt>

[**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice)
</dt> <dt>

[**Idcompositiondevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
</dt> <dt>

[**Idcompositiondevice:: kreatetargetforhwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd)
</dt> <dt>

[**Idcompositiondevice:: kreatevisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual)
</dt> <dt>

[**Idcompositionsurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface)
</dt> <dt>

[**Idcompositiontarget:: Abort**](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot)
</dt> <dt>

[**Idcompositionvisual:: setContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent)
</dt> <dt>

[**Idxgidevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)
</dt> <dt>

[**Saferelease**](/windows/desktop/medfound/saferelease)
</dt> </dl>

 

 
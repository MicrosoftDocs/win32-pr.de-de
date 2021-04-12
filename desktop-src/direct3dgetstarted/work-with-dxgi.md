---
title: Arbeiten mit DirectX-Geräte Ressourcen
description: Erfahren Sie mehr über die Rolle der Microsoft DirectX Graphics Infrastructure (DXGI) in Ihrem Windows Store DirectX-Spiel.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096e2be6f957d99bc6e5055f845c14448ecd647f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473540"
---
# <a name="work-with-directx-device-resources"></a>Arbeiten mit DirectX-Geräte Ressourcen

Erfahren Sie mehr über die Rolle der Microsoft DirectX Graphics Infrastructure (DXGI) in Ihrem Windows Store DirectX-Spiel. DXGI ist ein Satz von APIs, die zum Konfigurieren und Verwalten von Grafik-und Grafikadapter Ressourcen auf niedriger Ebene verwendet werden. Ohne diese Methode haben Sie keine Möglichkeit, die Grafik des Spiels in ein Fenster zu zeichnen.

Betrachten Sie DXGI auf diese Weise: um direkt auf die GPU zuzugreifen und ihre Ressourcen zu verwalten, müssen Sie eine Möglichkeit haben, Sie für Ihre APP zu beschreiben. Die wichtigste Information, die Sie über die GPU benötigen, ist der Ort zum Zeichnen von Pixeln, damit diese Pixel an den Bildschirm gesendet werden können. Dies wird in der Regel als "BackBuffer" bezeichnet – ein Speicherort im GPU-Speicher, in dem Sie die Pixel zeichnen und dann "geflippt" oder "getauscht" und an den Bildschirm mit einem Aktualisierungs Signal gesendet werden können. Mit DXGI können Sie diesen Speicherort und die Möglichkeit zur Verwendung dieses Puffers abrufen (die als *SwapChain* bezeichnet wird, da es sich um eine Kette von austauschbaren Puffern handelt, die mehrere Puffer Strategien zulässt).

Um dies zu erreichen, benötigen Sie Zugriff zum Schreiben in die Swapkette und ein Handle für das Fenster, in dem der aktuelle Hintergrund Puffer für die SwapChain angezeigt wird. Sie müssen auch die beiden verbinden, um sicherzustellen, dass das Betriebssystem das Fenster mit dem Inhalt des Hintergrund Puffers aktualisiert, wenn Sie dies anfordern.

Der Gesamtprozess zum Zeichnen auf dem Bildschirm lautet wie folgt:

-   Sie erhalten ein [**corewindow-Fenster**](/uwp/api/Windows.UI.Core.CoreWindow) für Ihre APP.
-   Sie erhalten eine Schnittstelle für das Direct3D-Gerät und den Kontext.
-   Erstellen Sie die Swapkette, um Ihr gerendertes Bild im [**corewindow**](/uwp/api/Windows.UI.Core.CoreWindow)anzuzeigen.
-   Erstellen Sie ein Renderziel zum Zeichnen, und füllen Sie es mit Pixel.
-   Präsentieren Sie die Swapkette!

## <a name="create-a-window-for-your-app"></a>Erstellen eines Fensters für Ihre APP

Zuerst muss ein Fenster erstellt werden. Erstellen Sie zunächst eine Fenster Klasse, indem Sie eine Instanz von [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)auffüllen, und registrieren Sie Sie dann mithilfe von [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa). Die Fenster Klasse enthält wichtige Eigenschaften des Fensters, einschließlich des verwendeten Symbols, der statischen Nachrichten Verarbeitungs Funktion (mehr dazu später) und eines eindeutigen Namens für die Fenster Klasse.


```C++
if(m_hInstance == NULL) 
    m_hInstance = (HINSTANCE)GetModuleHandle(NULL);

HICON hIcon = NULL;
WCHAR szExePath[MAX_PATH];
    GetModuleFileName(NULL, szExePath, MAX_PATH);

// If the icon is NULL, then use the first one found in the exe
if(hIcon == NULL)
    hIcon = ExtractIcon(m_hInstance, szExePath, 0); 

// Register the windows class
WNDCLASS wndClass;
wndClass.style = CS_DBLCLKS;
wndClass.lpfnWndProc = MainClass::StaticWindowProc;
wndClass.cbClsExtra = 0;
wndClass.cbWndExtra = 0;
wndClass.hInstance = m_hInstance;
wndClass.hIcon = hIcon;
wndClass.hCursor = LoadCursor(NULL, IDC_ARROW);
wndClass.hbrBackground = (HBRUSH)GetStockObject(BLACK_BRUSH);
wndClass.lpszMenuName = NULL;
wndClass.lpszClassName = m_windowClassName.c_str();

if(!RegisterClass(&wndClass))
{
    DWORD dwError = GetLastError();
    if(dwError != ERROR_CLASS_ALREADY_EXISTS)
        return HRESULT_FROM_WIN32(dwError);
}
```



Als Nächstes erstellen Sie das Fenster. Wir müssen außerdem Größen Informationen für das Fenster und den Namen der soeben erstellten Fenster Klasse angeben. Wenn Sie " [**kreatewindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa)" aufrufen, erhalten Sie einen nicht transparenten Zeiger auf das Fenster, das als HWND bezeichnet wird. Sie müssen den HWND-Zeiger behalten und ihn jedes Mal verwenden, wenn Sie auf das Fenster verweisen müssen, einschließlich zerstören oder neu erstellen, und (besonders wichtig) Wenn Sie die DXGI-SwapChain erstellen, die Sie zum Zeichnen im Fenster verwenden.


```C++
m_rc;
int x = CW_USEDEFAULT;
int y = CW_USEDEFAULT;

// No menu in this example.
m_hMenu = NULL;

// This example uses a non-resizable 640 by 480 viewport for simplicity.
int nDefaultWidth = 640;
int nDefaultHeight = 480;
SetRect(&m_rc, 0, 0, nDefaultWidth, nDefaultHeight);        
AdjustWindowRect(
    &m_rc,
    WS_OVERLAPPEDWINDOW,
    (m_hMenu != NULL) ? true : false
    );

// Create the window for our viewport.
m_hWnd = CreateWindow(
    m_windowClassName.c_str(),
    L"Cube11",
    WS_OVERLAPPEDWINDOW,
    x, y,
    (m_rc.right-m_rc.left), (m_rc.bottom-m_rc.top),
    0,
    m_hMenu,
    m_hInstance,
    0
    );

if(m_hWnd == NULL)
{
    DWORD dwError = GetLastError();
    return HRESULT_FROM_WIN32(dwError);
}
```



Das Windows-Desktop-App-Modell enthält einen Hook in die Windows-Nachrichten Schleife. Sie müssen ihre Hauptprogramm Schleife auf diesem Hook basieren, indem Sie eine "staticwindowproc"-Funktion schreiben, um windowingereignisse zu verarbeiten. Dabei muss es sich um eine statische Funktion handeln, da Windows Sie außerhalb des Kontexts einer beliebigen Klasseninstanz aufruft. Hier ist ein sehr einfaches Beispiel für eine statische Nachrichten Verarbeitungs Funktion.


```C++
LRESULT CALLBACK MainClass::StaticWindowProc(
    HWND hWnd,
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam
    )
{
    switch(uMsg)
    {
        case WM_CLOSE:
        {
            HMENU hMenu;
            hMenu = GetMenu(hWnd);
            if (hMenu != NULL)
            {
                DestroyMenu(hMenu);
            }
            DestroyWindow(hWnd);
            UnregisterClass(
                m_windowClassName.c_str(),
                m_hInstance
                );
            return 0;
        }

        case WM_DESTROY:
            PostQuitMessage(0);
            break;
    }
    
    return DefWindowProc(hWnd, uMsg, wParam, lParam);
}
```



In diesem einfachen Beispiel werden nur die Programm Beendigungs Bedingungen überprüft: [**WM \_ Close**](/windows/desktop/winmsg/wm-close), gesendet, wenn das Fenster geschlossen werden soll, und [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy), das gesendet wird, nachdem das Fenster tatsächlich vom Bildschirm entfernt wurde. Eine vollständige, Produktions-app muss auch andere windowingereignisse verarbeiten – die vollständige Liste der Fenster-Ereignisse finden Sie unter [Fenster Benachrichtigungen](/windows/desktop/winmsg/window-notifications).

Die Hauptprogramm Schleife selbst muss Windows-Meldungen bestätigen, indem es Windows die Möglichkeit erhält, den statischen Nachrichten proc auszuführen. Helfen Sie, das Programm effizient auszuführen, indem Sie das Verhalten auslassen: jede Iteration sollte neue Windows-Meldungen verarbeiten, wenn Sie verfügbar sind, und wenn sich keine Nachrichten in der Warteschlange befinden, sollte ein neuer Frame renderert werden. Hier ist ein sehr einfaches Beispiel:


```C++
bool bGotMsg;
MSG  msg;
msg.message = WM_NULL;
PeekMessage(&msg, NULL, 0U, 0U, PM_NOREMOVE);

while (WM_QUIT != msg.message)
{
    // Process window events.
    // Use PeekMessage() so we can use idle time to render the scene. 
    bGotMsg = (PeekMessage(&msg, NULL, 0U, 0U, PM_REMOVE) != 0);

    if (bGotMsg)
    {
        // Translate and dispatch the message
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
    else
    {
        // Update the scene.
        renderer->Update();

        // Render frames during idle time (when no messages are waiting).
        renderer->Render();

        // Present the frame to the screen.
        deviceResources->Present();
    }
}
```



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a>Eine Schnittstelle für das Direct3D-Gerät und den Kontext erhalten

Der erste Schritt bei der Verwendung von Direct3D besteht darin, eine Schnittstelle für die Direct3D-Hardware (die GPU) zu erwerben, die als Instanzen von [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2)dargestellt wird. Bei der ersten handelt es sich um eine virtuelle Darstellung der GPU-Ressourcen. letztere ist eine geräteunabhängige Abstraktion der Renderingpipeline und des Prozesses. Im folgenden finden Sie eine einfache Möglichkeit: **ID3D11Device** enthält die Grafik Methoden, die Sie nur selten aufzurufen, normalerweise vor dem Auftreten eines Renderings, um die Ressourcen zu erhalten und zu konfigurieren, die Sie benötigen, um mit dem Zeichnen von Pixeln zu beginnen. **Verknüpfung id3d11devicecontext aus** hingegen enthält die Methoden, die Sie für jeden Frame aufrufen: Laden in Puffer und Sichten und andere Ressourcen, Ändern der Ausgabe von Fusion-und Raster-Status, Verwalten von Shadern und Zeichnen der Ergebnisse der Übergabe dieser Ressourcen über die Zustände und Shader.

Es gibt einen sehr wichtigen Teil dieses Prozesses: das Festlegen der Funktionsebene. Die Featureebene informiert DirectX über die minimale Hardwareebene, die ihre App unterstützt, wobei die D3D \_ \_ Featureebene \_ 9 \_ 1 als niedrigste featuremenge und die D3D- \_ Funktions \_ Ebene \_ 11 \_ 1 als die aktuelle höchste Stufe hat. Sie sollten 9 \_ 1 als minimal unterstützen, wenn Sie die größtmögliche Zielgruppe erreichen möchten. Nehmen Sie sich etwas Zeit, um auf Direct3D- [featureebenen](/previous-versions/windows/apps/hh994923(v=win.10)) zu lesen und die Mindest-und höchst Funktionsebenen zu bewerten, die Ihr Spiel unterstützen soll, und um die Auswirkungen ihrer Wahl zu verstehen.

Rufen Sie Verweise (Zeiger) auf das Direct3D-Gerät und den Gerätekontext ab, und speichern Sie Sie als Variablen auf Klassenebene in der **deviceresources** -Instanz (als **comptr** -intelligente Zeiger). Verwenden Sie diese Verweise, wenn Sie auf das Direct3D-Gerät oder den Gerätekontext zugreifen müssen.


```C++
D3D_FEATURE_LEVEL levels[] = {
    D3D_FEATURE_LEVEL_9_1,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_11_1
};

// This flag adds support for surfaces with a color-channel ordering different
// from the API default. It is required for compatibility with Direct2D.
UINT deviceFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;

#if defined(DEBUG) || defined(_DEBUG)
deviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif

// Create the Direct3D 11 API device object and a corresponding context.
Microsoft::WRL::ComPtr<ID3D11Device>        device;
Microsoft::WRL::ComPtr<ID3D11DeviceContext> context;

hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    deviceFlags,                // Set debug and Direct2D compatibility flags.
    levels,                     // List of feature levels this app can support.
    ARRAYSIZE(levels),          // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_featureLevel,            // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (FAILED(hr))
{
    // Handle device interface creation failure if it occurs.
    // For example, reduce the feature level requirement, or fail over 
    // to WARP rendering.
}

// Store pointers to the Direct3D 11.1 API device and immediate context.
device.As(&m_pd3dDevice);
context.As(&m_pd3dDeviceContext);
```



## <a name="create-the-swap-chain"></a>Austausch Kette erstellen

Okay: Sie verfügen über ein Fenster, in dem Sie zeichnen können, und Sie verfügen über eine Schnittstelle zum Senden von Daten und zum Übergeben von Befehlen an die GPU. Sehen wir uns nun an, wie Sie zusammengeführt werden.

Zuerst teilen Sie DXGI mit, welche Werte für die Eigenschaften der Austausch Kette verwendet werden sollen. Verwenden Sie hierfür eine [**DXGI \_ - \_ SwapChain \_**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) -Struktur. Sechs Felder sind besonders wichtig für Desktop-Apps:

-   **Windowed**: gibt an, ob die Austausch Kette voll Bildschirm ist oder auf das Fenster zugeschnitten ist. Legen Sie diese Einstellung auf "true" fest, um die Austausch Kette in dem zuvor erstellten Fenster abzulegen.
-   **Bufferusage**: Legen Sie dies auf die Ausgabe des DXGI- \_ Verwendungs \_ \_ Renderziels fest \_ . Dies weist darauf hin, dass die SwapChain eine Zeichen Oberfläche ist, die es Ihnen ermöglicht, Sie als Direct3D-Renderziel zu verwenden.
-   **SwapEffect**: Legen Sie diese Einstellung auf den DXGI- \_ Swap- \_ Effekt als \_ \_ sequenziell fest.
-   **Format**: das \_ \_ B8G8R8A8 unorm-Format im DXGI-Format gibt die \_ 32-Bit-Farbe an: 8 Bits für jeden der drei RGB-Farbkanäle und 8 Bits für den Alphakanal.
-   **BUFFERCOUNT**: Legen Sie diese Einstellung auf "2" fest, um ein herkömmliches Verhalten mit doppelter puffert zu vermeiden. Legen Sie für die Puffer Anzahl den Wert 3 fest, wenn Ihr Grafik Inhalt mehr als einen Monitor Aktualisierungszyklen zum Renderingvorgang für einen einzelnen Frame benötigt (z. b. 60 Hz, wenn der Schwellenwert größer als 16 ms ist)
-   **SampleDesc**: Dieses Feld steuert das Multisampling. Legen Sie **Anzahl** auf 1 und **Qualität** für Swapketten des Flip-Modells auf 0 fest. (Um multisamplinggrad mit Flip-Model-Austausch Ketten zu verwenden, zeichnen Sie ein separates multisamplinggrad-Renderziel, und lösen Sie dieses Ziel dann in der SwapChain direkt vor der Präsentation auf. Beispielcode wird in [Multisampling in Windows Store-Apps](/previous-versions/windows/apps/dn458384(v=win.10))bereitgestellt.)

Nachdem Sie eine Konfiguration für die SwapChain angegeben haben, müssen Sie die gleiche DXGI-Factory verwenden, die das Direct3D-Gerät (und den Gerätekontext) erstellt hat, um die Swapkette zu erstellen.

**Kurzform:  **

Beziehen Sie den zuvor erstellten [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) -Verweis. Upcast Sie in [**"idxgidevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (sofern nicht bereits geschehen), und rufen Sie dann [**idxgidevice:: GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) auf, um den DXGI-Adapter abzurufen. Abrufen der übergeordneten Factory für diesen Adapter durch Aufrufen von [**IDXGIFactory2:: GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) erbt von [**idxgiobject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)) – jetzt können Sie diese Factory verwenden, um die [**Swapkette durch Aufrufen von createswapchaparent HWND**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)zu erstellen, wie im folgenden Codebeispiel gezeigt.


```C++
DXGI_SWAP_CHAIN_DESC desc;
ZeroMemory(&desc, sizeof(DXGI_SWAP_CHAIN_DESC));
desc.Windowed = TRUE; // Sets the initial state of full-screen mode.
desc.BufferCount = 2;
desc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
desc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
desc.SampleDesc.Count = 1;      //multisampling setting
desc.SampleDesc.Quality = 0;    //vendor-specific flag
desc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL;
desc.OutputWindow = hWnd;

// Create the DXGI device object to use in other factories, such as Direct2D.
Microsoft::WRL::ComPtr<IDXGIDevice3> dxgiDevice;
m_pd3dDevice.As(&dxgiDevice);

// Create swap chain.
Microsoft::WRL::ComPtr<IDXGIAdapter> adapter;
Microsoft::WRL::ComPtr<IDXGIFactory> factory;

hr = dxgiDevice->GetAdapter(&adapter);

if (SUCCEEDED(hr))
{
    adapter->GetParent(IID_PPV_ARGS(&factory));

    hr = factory->CreateSwapChain(
        m_pd3dDevice.Get(),
        &desc,
        &m_pDXGISwapChain
        );
}
```



Wenn Sie gerade erst beginnen, ist es wahrscheinlich, dass die hier gezeigte Konfiguration verwendet wird. Wenn Sie nun bereits mit früheren Versionen von DirectX vertraut sind, stellen Sie möglicherweise Folgendes in Frage: "Warum haben wir das Gerät nicht erstellt und die Kette nicht gleichzeitig ausgetauscht, sondern nicht durch alle diese Klassen zurück?" Die Antwort ist die Effizienz: Austausch Ketten sind Direct3D Geräte Ressourcen, und Geräte Ressourcen sind an das jeweilige Direct3D-Gerät gebunden, von dem Sie erstellt wurden. Wenn Sie ein neues Gerät mit einer neuen austauschkette erstellen, müssen Sie alle Geräte Ressourcen mithilfe des neuen Direct3D-Geräts neu erstellen. Wenn Sie also die SwapChain mit derselben Factory erstellen (wie oben gezeigt), können Sie die Swapkette neu erstellen und weiterhin die Direct3D-Geräte Ressourcen verwenden, die Sie bereits geladen haben!

Nun haben Sie ein Fenster vom Betriebssystem, eine Möglichkeit für den Zugriff auf die GPU und deren Ressourcen und eine SwapChain zum Anzeigen der renderingergebnisse. Alles, was übrig bleibt, besteht darin, die gesamte Aufgabe zu verbinden.

## <a name="create-a-render-target-for-drawing"></a>Renderziel zum Zeichnen erstellen

Die Shader-Pipeline benötigt eine Ressource, in der Pixel gezeichnet werden. Die einfachste Möglichkeit zum Erstellen dieser Ressource besteht darin, eine [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) -Ressource als Hintergrund Puffer zu definieren, in den der Pixelshader gezeichnet werden soll, und dann diese Textur in der SwapChain zu lesen.

Zu diesem Zweck erstellen Sie eine renderzielansicht . In Direct3D ist eine Sicht eine Möglichkeit, auf eine bestimmte Ressource zuzugreifen. In diesem Fall ermöglicht die-Sicht dem Pixelshader das Schreiben in die Textur, während er die pro-Pixel-Vorgänge abschließt.

Sehen wir uns den Code für diese an. Wenn Sie die Ausgabe des DXGI- \_ Verwendungs \_ \_ Renderziels \_ in der SwapChain festlegen, wird dadurch die zugrunde liegende Direct3D-Ressource als Zeichen Oberfläche verwendet. Um unsere renderzielansicht zu erhalten, muss lediglich der Hintergrund Puffer aus der Swapkette und eine renderzielansicht erstellt werden, die an die backpufferressource gebunden ist.


```C++
hr = m_pDXGISwapChain->GetBuffer(
    0,
    __uuidof(ID3D11Texture2D),
    (void**) &m_pBackBuffer);

hr = m_pd3dDevice->CreateRenderTargetView(
    m_pBackBuffer.Get(),
    nullptr,
    m_pRenderTarget.GetAddressOf()
    );

m_pBackBuffer->GetDesc(&m_bbDesc);
```



Erstellen Sie außerdem einen *tiefen Schablonen Puffer*. Ein tiefen Schablone-Puffer ist nur eine bestimmte Form der [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) -Ressource, die normalerweise verwendet wird, um zu bestimmen, welche Pixel während der rasterisierung auf der Grundlage der Entfernung der Objekte in der Szene von der Kamera gezeichnet werden. Ein tiefen Schablone-Puffer kann auch für Schablonen Effekte verwendet werden, bei denen bestimmte Pixel während der rasterisierung verworfen oder ignoriert werden. Dieser Puffer muss dieselbe Größe aufweisen wie das Renderziel. Beachten Sie, dass Sie die Rahmen Puffer Tiefe der tiefen Schablone nicht lesen oder Rendern können, da Sie ausschließlich von der Shader-Pipeline vor und während der endgültigen rasterisierung verwendet wird.

Erstellen Sie außerdem eine Ansicht für den tiefen Schablone-Puffer als [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview). Die Ansicht teilt der Shader-Pipeline mit, wie die zugrunde liegende [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) -Ressource interpretiert werden soll. Wenn Sie diese Ansicht nicht bereitstellen, werden keine pro-Pixel-tiefen Tests durchgeführt, und die Objekte in Ihrer Szene erscheinen möglicherweise sehr wenig.


```C++
CD3D11_TEXTURE2D_DESC depthStencilDesc(
    DXGI_FORMAT_D24_UNORM_S8_UINT,
    static_cast<UINT> (m_bbDesc.Width),
    static_cast<UINT> (m_bbDesc.Height),
    1, // This depth stencil view has only one texture.
    1, // Use a single mipmap level.
    D3D11_BIND_DEPTH_STENCIL
    );

m_pd3dDevice->CreateTexture2D(
    &depthStencilDesc,
    nullptr,
    &m_pDepthStencil
    );

CD3D11_DEPTH_STENCIL_VIEW_DESC depthStencilViewDesc(D3D11_DSV_DIMENSION_TEXTURE2D);

m_pd3dDevice->CreateDepthStencilView(
    m_pDepthStencil.Get(),
    &depthStencilViewDesc,
    &m_pDepthStencilView
    );
```



Der letzte Schritt besteht darin, einen Viewport zu erstellen. Definiert das sichtbare Rechteck des Hintergrund Puffers, der auf dem Bildschirm angezeigt wird. Sie können den Teil des Puffers ändern, der auf dem Bildschirm angezeigt wird, indem Sie die Parameter für den Viewport ändern. Dieser Code bezieht sich auf die gesamte Fenstergröße – oder auf die Bildschirmauflösung, bei voll Bildaustausch Ketten. Wenn Sie Spaß machen, ändern Sie die angegebenen Koordinaten Werte, und beobachten Sie die Ergebnisse.


```C++
ZeroMemory(&m_viewport, sizeof(D3D11_VIEWPORT));
m_viewport.Height = (float) m_bbDesc.Height;
m_viewport.Width = (float) m_bbDesc.Width;
m_viewport.MinDepth = 0;
m_viewport.MaxDepth = 1;

m_pd3dDeviceContext->RSSetViewports(
    1,
    &m_viewport
    );
```



Und das ist, wie Sie in einem Fenster von nichts zum Zeichnen von Pixeln gelangen! Wenn Sie beginnen, sollten Sie sich damit vertraut machen, wie DirectX, über DXGI, die Kernressourcen verwaltet, die Sie für das Zeichnen von Pixeln benötigen.

Als nächstes betrachten Sie die Struktur der Grafik Pipeline. Siehe Grundlegendes [zur Renderingpipeline der DirectX-App-Vorlage](understand-the-directx-11-2-graphics-pipeline.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Als Nächstes**
</dt> <dt>

[Arbeiten mit Shader und Shaderressourcen](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
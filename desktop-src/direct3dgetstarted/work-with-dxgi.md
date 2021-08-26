---
title: Arbeiten mit DirectX-Geräteressourcen
description: Machen Sie sich mit der Rolle des Microsoft DirectX Graphic Infrastructure (DXGI) in Ihrem DirectX Windows Store Spiel aus.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600af9c5ca2d2ba8ce8a7b078c769e195c4a7898384d102a21be3aaaf2c936bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068660"
---
# <a name="work-with-directx-device-resources"></a>Arbeiten mit DirectX-Geräteressourcen

Machen Sie sich mit der Rolle des Microsoft DirectX Graphic Infrastructure (DXGI) in Ihrem DirectX Windows Store Spiel aus. DXGI ist eine Gruppe von APIs, die zum Konfigurieren und Verwalten von Grafik- und Grafikkartenressourcen auf niedriger Ebene verwendet werden. Ohne sie hätten Sie keine Möglichkeit, die Grafiken Ihres Spiels in ein Fenster zu zeichnen.

Stellen Sie sich DXGI auf diese Weise vor: Um direkt auf die GPU zu zugreifen und ihre Ressourcen zu verwalten, müssen Sie eine Möglichkeit haben, sie für Ihre App zu beschreiben. Die wichtigste Information, die Sie über die GPU benötigen, ist der Ort zum Zeichnen von Pixeln, damit diese Pixel an den Bildschirm gesendet werden können. In der Regel wird dies als "Backpuffer" bezeichnet– eine Position im GPU-Arbeitsspeicher, an der Sie die Pixel zeichnen und dann "gekippt" oder "getauscht" und bei einem Aktualisierungssignal an den Bildschirm senden können. MIT DXGI können Sie diesen Speicherort und die  Mittel zur Verwendung dieses Puffers (als Austauschkette bezeichnet) erhalten, da es sich um eine Kette aus austauschbaren Puffern handelt, die mehrere Pufferstrategien ermöglichen.

Dazu benötigen Sie Zugriff auf das Schreiben in die Swapkette und ein Handle für das Fenster, das den aktuellen Hintergrundpuffer für die Swapkette zeigt. Sie müssen auch die beiden verbinden, um sicherzustellen, dass das Betriebssystem das Fenster mit dem Inhalt des Hintergrundpuffers aktualisiert, wenn Sie dies anfordern.

Der gesamte Prozess zum Zeichnen auf dem Bildschirm ist wie folgt:

-   Erhalten Sie [**ein CoreWindow-Gerät**](/uwp/api/Windows.UI.Core.CoreWindow) für Ihre App.
-   Hier erhalten Sie eine Schnittstelle für das Direct3D-Gerät und den Kontext.
-   Erstellen Sie die Swapkette, um das gerenderte Bild im [**CoreWindow anzuzeigen.**](/uwp/api/Windows.UI.Core.CoreWindow)
-   Erstellen Sie ein Renderziel zum Zeichnen, und füllen Sie es mit Pixeln auf.
-   Präsentieren Sie die Auslagerungskette!

## <a name="create-a-window-for-your-app"></a>Erstellen eines Fensters für Ihre App

Zunächst müssen wir ein Fenster erstellen. Erstellen Sie zunächst eine Fensterklasse, indem Sie eine Instanz von [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)aufpopulieren und sie dann mit [**registerClass registrieren.**](/windows/desktop/api/winuser/nf-winuser-registerclassa) Die Fensterklasse enthält wichtige Eigenschaften des Fensters, einschließlich des von ihm verwendeten Symbols, der statischen Nachrichtenverarbeitungsfunktion (mehr dazu später) und eines eindeutigen Namens für die Fensterklasse.


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



Als Nächstes erstellen Sie das Fenster. Wir müssen auch Größeninformationen für das Fenster und den Namen der fenster-Klasse angeben, die wir gerade erstellt haben. Wenn Sie [**CreateWindow aufrufen,**](/windows/desktop/api/winuser/nf-winuser-createwindowa)erhalten Sie einen nicht transparenten Zeiger auf das Fenster, das als HWND bezeichnet wird. Sie müssen den HWND-Zeiger behalten und ihn immer dann verwenden, wenn Sie auf das Fenster verweisen müssen, einschließlich des Zerstörens oder Neuererstellens, und (besonders wichtig) beim Erstellen der DXGI-Swapkette, die Sie zum Zeichnen im Fenster verwenden.


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



Das Windows Desktop-App-Modell enthält einen Hook in Windows Nachrichtenschleife. Sie müssen Ihre Hauptprogrammschleife von diesem Hook abschalten, indem Sie eine "StaticWindowProc"-Funktion schreiben, um Fensterereignisse zu verarbeiten. Dies muss eine statische Funktion sein, da Windows außerhalb des Kontexts einer Klasseninstanz aufruft. Hier ist ein sehr einfaches Beispiel für eine statische Nachrichtenverarbeitungsfunktion.


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



In diesem einfachen Beispiel wird nur auf Programmabstiegsbedingungen überprüft: [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close), wird gesendet, wenn das Fenster geschlossen werden soll, und [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy), das gesendet wird, nachdem das Fenster tatsächlich vom Bildschirm entfernt wurde. Eine vollständige Produktions-App muss auch andere Fensterereignisse verarbeiten. Eine vollständige Liste der Fensterereignisse finden Sie unter [Fensterbenachrichtigungen.](/windows/desktop/winmsg/window-notifications)

Die Hauptprogrammschleife selbst muss die Windows bestätigen, indem sie Windows die Möglichkeit zum Ausführen der statischen Nachrichtenproc ermöglicht. Unterstützen Sie die effiziente Ausführung des Programms, indem Sie das Verhalten forking: Jede Iteration sollte neue Windows-Nachrichten verarbeiten, wenn sie verfügbar sind, und wenn sich keine Nachrichten in der Warteschlange befinden, sollte ein neuer Frame gerendert werden. Hier ist ein sehr einfaches Beispiel:


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



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a>Hier erhalten Sie eine Schnittstelle für das Direct3D-Gerät und den Kontext.

Der erste Schritt bei der Verwendung von Direct3D besteht im Erwerben einer Schnittstelle für die Direct3D-Hardware (GPU), die als Instanzen von [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) und [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2)dargestellt wird. Erstere ist eine virtuelle Darstellung der GPU-Ressourcen, und die zweite ist eine geräteunabhängige Abstraktion der Renderingpipeline und des Renderingprozesses. Dies ist eine einfache Möglichkeit, sich dies zu weisen: **ID3D11Device** enthält die Grafikmethoden, die Sie selten aufrufen, in der Regel vor einem Rendering, um die Ressourcen zu erhalten und zu konfigurieren, die Sie zum Zeichnen von Pixeln benötigen. **ID3D11DeviceContext** enthält hingegen die Methoden, die Sie jeden Frame aufrufen: Laden von Puffern und Ansichten und anderen Ressourcen, Ändern des Ausgabe merger- und rasterizer-Zustands, Verwalten von Shadern und Zeichnen der Ergebnisse der Übergabe dieser Ressourcen durch die Zustände und Shader.

Es gibt einen sehr wichtigen Teil dieses Prozesses: das Festlegen der Featureebene. Die Featureebene informiert DirectX über die Mindesthardware, die Ihre App unterstützt, mit D3D FEATURE LEVEL 9 1 als niedrigstem Featuresatz und \_ \_ \_ \_ D3D \_ FEATURE LEVEL \_ \_ 11 1 als \_ aktuellem höchstwert. Sie sollten mindestens 9 1 unterstützen, wenn \_ Sie eine möglichst große Zielgruppe erreichen möchten. Nehmen Sie sich etwas Zeit, [](/previous-versions/windows/apps/hh994923(v=win.10)) um sich mit den Direct3D-Featureebenen durchlesen und die minimalen und maximalen Featureebenen, die Ihr Spiel unterstützen soll, selbst zu bewerten und die Auswirkungen Ihrer Wahl zu verstehen.

Abrufen von Verweisen (Zeigern) auf den Direct3D-Geräte- und -Gerätekontext und Speichern dieser Verweise als Variablen auf Klassenebene auf der **DeviceResources-Instanz** (als intelligente **ComPtr-Zeiger).** Verwenden Sie diese Verweise immer dann, wenn Sie auf das Direct3D-Gerät oder den Direct3D-Gerätekontext zugreifen müssen.


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



## <a name="create-the-swap-chain"></a>Erstellen der Swapkette

Ok: Sie haben ein Fenster zum Zeichnen, und Sie verfügen über eine Schnittstelle zum Senden von Daten und Zum Senden von Befehlen an die GPU. Sehen wir uns nun an, wie sie zusammenkommen.

Zuerst teilen Sie DXGI mit, welche Werte für die Eigenschaften der Austauschkette verwendet werden. Verwenden Sie dazu eine [**DXGI \_ SWAP CHAIN \_ \_ DESC-Struktur.**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) Sechs Felder sind besonders wichtig für Desktop-Apps:

-   **Windowed**: Gibt an, ob die Auslagerungskette im Vollbildmodus oder im Fenster abgeschnitten ist. Legen Sie dies auf TRUE fest, um die Auslagerungskette in das fenster zu setzen, das Sie zuvor erstellt haben.
-   **BufferUsage:** Legen Sie dies auf DXGI \_ USAGE RENDER TARGET OUTPUT \_ \_ \_ fest. Dies gibt an, dass die Swapkette eine Zeichenoberfläche ist, sodass Sie sie als Direct3D-Renderziel verwenden können.
-   **SwapEffect:** Legen Sie dies auf DXGI \_ SWAP EFFECT FLIP SEQUENTIAL \_ \_ \_ fest.
-   **Format:** Das DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM-Format gibt eine 32-Bit-Farbe an: 8 Bits für jeden der drei RGB-Farbkanäle und 8 Bits für den Alphakanal.
-   **BufferCount:** Legen Sie dies auf 2 fest, um ein herkömmliches Verhalten mit doppelter Pufferung zu vermeiden. Legen Sie die Pufferanzahl auf 3 fest, wenn ihr Grafikinhalt mehr als einen Monitoraktualisierungszyklus benötigt, um einen einzelnen Frame zu rendern (bei 60 Hz beträgt der Schwellenwert beispielsweise mehr als 16 ms).
-   **SampleDesc:** Dieses Feld steuert multisampling. Legen **Sie Anzahl** auf 1 und **Qualität** für Flip-Modell-Austauschketten auf 0 fest. (Um Multisampling mit Swapketten für Flip-Modelle zu verwenden, zeichnen Sie auf ein separates Renderziel mit mehrerenAmplings, und lösen Sie dieses Ziel dann kurz vor der Präsentation in die Swapkette auf. Beispielcode wird in [Multisampling in Windows Store-Apps bereitgestellt.)](/previous-versions/windows/apps/dn458384(v=win.10))

Nachdem Sie eine Konfiguration für die Austauschkette angegeben haben, müssen Sie dieselbe DXGI-Factory verwenden, die das Direct3D-Gerät (und den Gerätekontext) erstellt hat, um die Austauschkette zu erstellen.

**Kurzform: **

Erhalten Sie [**den ID3D11Device-Verweis,**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) den Sie zuvor erstellt haben. Übertragen Sie sie in [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (falls noch nicht vorhanden), und rufen Sie [**dann IDXGIDevice::GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) auf, um den DXGI-Adapter zu erhalten. Rufen Sie die übergeordnete Factory für diesen Adapter ab, indem Sie [**IDXGIFactory2::GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) aufrufen ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) erbt von [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)). Nun können Sie diese Factory verwenden, um die Auslagerungskette zu erstellen, indem Sie [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)aufrufen, wie im folgenden Codebeispiel zu sehen.


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



Wenn Sie gerade erst beginnen, ist es wahrscheinlich am besten, die hier gezeigte Konfiguration zu verwenden. Wenn Sie nun bereits mit früheren Versionen von DirectX vertraut sind, fragen Sie sich vielleicht: "Warum haben wir das Gerät nicht gleichzeitig erstellt und die Kette ausgetauscht, anstatt alle diese Klassen zu durchgehen?" Die Antwort ist Effizienz: Austauschketten sind Direct3D-Geräteressourcen, und Geräteressourcen sind an das bestimmte Direct3D-Gerät gebunden, von dem sie erstellt wurden. Wenn Sie ein neues Gerät mit einer neuen Austauschkette erstellen, müssen Sie alle Geräteressourcen mit dem neuen Direct3D-Gerät neu erstellen. Indem Sie also die Swapkette mit derselben Factory erstellen (wie oben gezeigt), können Sie die Swapkette neu erstellen und weiterhin die Direct3D-Geräteressourcen verwenden, die Sie bereits geladen haben.

Sie verfügen nun über ein Fenster des Betriebssystems, eine Möglichkeit, auf die GPU und ihre Ressourcen zu zugreifen, und eine Austauschkette, um die Renderingergebnisse anzuzeigen. Alles, was noch übrig bleibt, ist, das Ganze zusammen zu verkabeln!

## <a name="create-a-render-target-for-drawing"></a>Erstellen eines Renderziels zum Zeichnen

Die Shaderpipeline benötigt eine Ressource, in die Pixel gepunktet werden können. Die einfachste Möglichkeit, diese Ressource zu erstellen, besteht im Definieren einer [**ID3D11Texture2D-Ressource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) als Hintergrundpuffer für den Pixel-Shader, in den der Shader gelost werden soll, und anschließendes Lesen dieser Textur in die Auslagerungskette.

Dazu erstellen Sie eine *Renderzielansicht.* In Direct3D ist eine Ansicht eine Möglichkeit, auf eine bestimmte Ressource zu zugreifen. In diesem Fall ermöglicht die Ansicht dem Pixel-Shader, in die Textur zu schreiben, während er seine Vorgänge pro Pixel ab schließt.

Sehen wir uns den Code dafür an. Wenn Sie DXGI USAGE RENDER TARGET OUTPUT für die Swapkette festlegen, wurde die zugrunde liegende \_ \_ \_ \_ Direct3D-Ressource als Zeichenoberfläche verwendet. Um unsere Renderzielansicht zu erhalten, müssen wir nur den Backpuffer aus der Swapkette erhalten und eine Renderzielansicht erstellen, die an die Backpufferressource gebunden ist.


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



Erstellen Sie außerdem *einen Tiefen-Schablonenpuffer.* Ein Tiefen-Schablonenpuffer ist nur eine bestimmte Form der [**ID3D11Texture2D-Ressource,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) die in der Regel verwendet wird, um zu bestimmen, welche Pixel während der Rasterung die Zeichnen-Priorität haben, basierend auf dem Abstand der Objekte in der Szene von der Kamera. Ein Tiefen-Schablonenpuffer kann auch für Schabloneneffekte verwendet werden, bei denen bestimmte Pixel während der Rasterung verworfen oder ignoriert werden. Dieser Puffer muss die gleiche Größe wie das Renderziel haben. Beachten Sie, dass Sie die Tiefenschablonentextur des Framepuffers nicht lesen oder in diese rendern können, da sie ausschließlich von der Shaderpipeline vor und während der endgültigen Rasterung verwendet wird.

Erstellen Sie außerdem eine Ansicht für den Tiefen-Schablonenpuffer als [**ID3D11DepthStencilView.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview) Die Ansicht teilt der Shaderpipeline mit, wie die zugrunde liegende [**ID3D11Texture2D-Ressource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) interpretiert werden soll. Wenn Sie diese Ansicht also nicht zur Verfügung stellen, werden keine Tiefentests pro Pixel durchgeführt, und die Objekte in Ihrer Szene können zumindest ein wenig nach außen erscheinen!


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



Der letzte Schritt besteht im Erstellen eines Viewports. Dadurch wird das sichtbare Rechteck des auf dem Bildschirm angezeigten Hintergrundpuffers definiert. Sie können den Teil des Puffers ändern, der auf dem Bildschirm angezeigt wird, indem Sie die Parameter des Viewports ändern. Dieser Code ist auf die gesamte Fenstergröße oder die Bildschirmauflösung im Fall von Vollbild-Auslagerungsketten festgelegt. Ändern Sie aus Spaß die angegebenen Koordinatenwerte, und beobachten Sie die Ergebnisse.


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



Und so gehen Sie von nichts zum Zeichnen von Pixeln in einem Fenster! Wenn Sie beginnen, ist es eine gute Idee, sich damit vertraut zu machen, wie DirectX über DXGI die Kernressourcen verwaltet, die Sie zum Zeichnen von Pixeln benötigen.

Als Nächstes sehen Sie sich die Struktur der Grafikpipeline an. Weitere [Informationen finden Sie unter Verstehen der Renderingpipeline der DirectX-App-Vorlage.](understand-the-directx-11-2-graphics-pipeline.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Als Nächstes**
</dt> <dt>

[Arbeiten mit Shadern und Shaderressourcen](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
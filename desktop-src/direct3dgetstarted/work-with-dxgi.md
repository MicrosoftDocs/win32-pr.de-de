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
# <a name="work-with-directx-device-resources"></a><span data-ttu-id="61c57-103">Arbeiten mit DirectX-Geräte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="61c57-103">Work with DirectX device resources</span></span>

<span data-ttu-id="61c57-104">Erfahren Sie mehr über die Rolle der Microsoft DirectX Graphics Infrastructure (DXGI) in Ihrem Windows Store DirectX-Spiel.</span><span class="sxs-lookup"><span data-stu-id="61c57-104">Understand the role of the Microsoft DirectX Graphics Infrastructure (DXGI) in your Windows Store DirectX game.</span></span> <span data-ttu-id="61c57-105">DXGI ist ein Satz von APIs, die zum Konfigurieren und Verwalten von Grafik-und Grafikadapter Ressourcen auf niedriger Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61c57-105">DXGI is a set of APIs used to configure and manage low-level graphics and graphics adapter resources.</span></span> <span data-ttu-id="61c57-106">Ohne diese Methode haben Sie keine Möglichkeit, die Grafik des Spiels in ein Fenster zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="61c57-106">Without it, you'd have no way to draw your game's graphics to a window.</span></span>

<span data-ttu-id="61c57-107">Betrachten Sie DXGI auf diese Weise: um direkt auf die GPU zuzugreifen und ihre Ressourcen zu verwalten, müssen Sie eine Möglichkeit haben, Sie für Ihre APP zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="61c57-107">Think of DXGI this way: to directly access the GPU and manage its resources, you must have a way to describe it to your app.</span></span> <span data-ttu-id="61c57-108">Die wichtigste Information, die Sie über die GPU benötigen, ist der Ort zum Zeichnen von Pixeln, damit diese Pixel an den Bildschirm gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="61c57-108">The most important piece of info you need about the GPU is the place to draw pixels so it can send those pixels to the screen.</span></span> <span data-ttu-id="61c57-109">Dies wird in der Regel als "BackBuffer" bezeichnet – ein Speicherort im GPU-Speicher, in dem Sie die Pixel zeichnen und dann "geflippt" oder "getauscht" und an den Bildschirm mit einem Aktualisierungs Signal gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="61c57-109">Typically this is called the "back buffer"—a location in GPU memory where you can draw the pixels and then have it "flipped" or "swapped" and sent to the screen on a refresh signal.</span></span> <span data-ttu-id="61c57-110">Mit DXGI können Sie diesen Speicherort und die Möglichkeit zur Verwendung dieses Puffers abrufen (die als *SwapChain* bezeichnet wird, da es sich um eine Kette von austauschbaren Puffern handelt, die mehrere Puffer Strategien zulässt).</span><span class="sxs-lookup"><span data-stu-id="61c57-110">DXGI lets you acquire that location and the means to use that buffer (called a *swap chain* because it is a chain of swappable buffers, allowing for multiple buffering strategies).</span></span>

<span data-ttu-id="61c57-111">Um dies zu erreichen, benötigen Sie Zugriff zum Schreiben in die Swapkette und ein Handle für das Fenster, in dem der aktuelle Hintergrund Puffer für die SwapChain angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="61c57-111">To do this, you need access to write to the swap chain, and a handle to the window that will display the current back buffer for the swap chain.</span></span> <span data-ttu-id="61c57-112">Sie müssen auch die beiden verbinden, um sicherzustellen, dass das Betriebssystem das Fenster mit dem Inhalt des Hintergrund Puffers aktualisiert, wenn Sie dies anfordern.</span><span class="sxs-lookup"><span data-stu-id="61c57-112">You also need to connect the two to ensure that the operating system will refresh the window with the contents of the back buffer when you request it to do so.</span></span>

<span data-ttu-id="61c57-113">Der Gesamtprozess zum Zeichnen auf dem Bildschirm lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="61c57-113">The overall process for drawing to the screen is as follows:</span></span>

-   <span data-ttu-id="61c57-114">Sie erhalten ein [**corewindow-Fenster**](/uwp/api/Windows.UI.Core.CoreWindow) für Ihre APP.</span><span class="sxs-lookup"><span data-stu-id="61c57-114">Get a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) for your app.</span></span>
-   <span data-ttu-id="61c57-115">Sie erhalten eine Schnittstelle für das Direct3D-Gerät und den Kontext.</span><span class="sxs-lookup"><span data-stu-id="61c57-115">Get an interface for the Direct3D device and context.</span></span>
-   <span data-ttu-id="61c57-116">Erstellen Sie die Swapkette, um Ihr gerendertes Bild im [**corewindow**](/uwp/api/Windows.UI.Core.CoreWindow)anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="61c57-116">Create the swap chain to display your rendered image in the [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>
-   <span data-ttu-id="61c57-117">Erstellen Sie ein Renderziel zum Zeichnen, und füllen Sie es mit Pixel.</span><span class="sxs-lookup"><span data-stu-id="61c57-117">Create a render target for drawing and populate it with pixels.</span></span>
-   <span data-ttu-id="61c57-118">Präsentieren Sie die Swapkette!</span><span class="sxs-lookup"><span data-stu-id="61c57-118">Present the swap chain!</span></span>

## <a name="create-a-window-for-your-app"></a><span data-ttu-id="61c57-119">Erstellen eines Fensters für Ihre APP</span><span class="sxs-lookup"><span data-stu-id="61c57-119">Create a window for your app</span></span>

<span data-ttu-id="61c57-120">Zuerst muss ein Fenster erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="61c57-120">The first thing we need to do is create a window.</span></span> <span data-ttu-id="61c57-121">Erstellen Sie zunächst eine Fenster Klasse, indem Sie eine Instanz von [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)auffüllen, und registrieren Sie Sie dann mithilfe von [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="61c57-121">First, create a window class by populating an instance of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa), then register it using [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="61c57-122">Die Fenster Klasse enthält wichtige Eigenschaften des Fensters, einschließlich des verwendeten Symbols, der statischen Nachrichten Verarbeitungs Funktion (mehr dazu später) und eines eindeutigen Namens für die Fenster Klasse.</span><span class="sxs-lookup"><span data-stu-id="61c57-122">The window class contains essential properties of the window, including the icon it uses, the static message processing function (more on this later), and a unique name for the window class.</span></span>


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



<span data-ttu-id="61c57-123">Als Nächstes erstellen Sie das Fenster.</span><span class="sxs-lookup"><span data-stu-id="61c57-123">Next, you create the window.</span></span> <span data-ttu-id="61c57-124">Wir müssen außerdem Größen Informationen für das Fenster und den Namen der soeben erstellten Fenster Klasse angeben.</span><span class="sxs-lookup"><span data-stu-id="61c57-124">We also need to provide size information for the window and the name of the window class we just created.</span></span> <span data-ttu-id="61c57-125">Wenn Sie " [**kreatewindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa)" aufrufen, erhalten Sie einen nicht transparenten Zeiger auf das Fenster, das als HWND bezeichnet wird. Sie müssen den HWND-Zeiger behalten und ihn jedes Mal verwenden, wenn Sie auf das Fenster verweisen müssen, einschließlich zerstören oder neu erstellen, und (besonders wichtig) Wenn Sie die DXGI-SwapChain erstellen, die Sie zum Zeichnen im Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="61c57-125">When you call [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), you get back an opaque pointer to the window called an HWND; you'll need to keep the HWND pointer and use it any time you need to reference the window, including destroying or recreating it, and (especially important) when creating the DXGI swap chain you use to draw in the window.</span></span>


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



<span data-ttu-id="61c57-126">Das Windows-Desktop-App-Modell enthält einen Hook in die Windows-Nachrichten Schleife.</span><span class="sxs-lookup"><span data-stu-id="61c57-126">The Windows desktop app model includes a hook into the Windows message loop.</span></span> <span data-ttu-id="61c57-127">Sie müssen ihre Hauptprogramm Schleife auf diesem Hook basieren, indem Sie eine "staticwindowproc"-Funktion schreiben, um windowingereignisse zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="61c57-127">You'll need to base your main program loop off of this hook by writing a "StaticWindowProc" function to process windowing events.</span></span> <span data-ttu-id="61c57-128">Dabei muss es sich um eine statische Funktion handeln, da Windows Sie außerhalb des Kontexts einer beliebigen Klasseninstanz aufruft.</span><span class="sxs-lookup"><span data-stu-id="61c57-128">This must be a static function because Windows will call it outside of the context of any class instance.</span></span> <span data-ttu-id="61c57-129">Hier ist ein sehr einfaches Beispiel für eine statische Nachrichten Verarbeitungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="61c57-129">Here's a very simple example of a static message processing function.</span></span>


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



<span data-ttu-id="61c57-130">In diesem einfachen Beispiel werden nur die Programm Beendigungs Bedingungen überprüft: [**WM \_ Close**](/windows/desktop/winmsg/wm-close), gesendet, wenn das Fenster geschlossen werden soll, und [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy), das gesendet wird, nachdem das Fenster tatsächlich vom Bildschirm entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="61c57-130">This simple example only checks for program exit conditions: [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), sent when the window is requested to be closed, and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy), which is sent after the window is actually removed from the screen.</span></span> <span data-ttu-id="61c57-131">Eine vollständige, Produktions-app muss auch andere windowingereignisse verarbeiten – die vollständige Liste der Fenster-Ereignisse finden Sie unter [Fenster Benachrichtigungen](/windows/desktop/winmsg/window-notifications).</span><span class="sxs-lookup"><span data-stu-id="61c57-131">A full, production app needs to handle other windowing events too—for the complete list of windowing events, see [Window Notifications](/windows/desktop/winmsg/window-notifications).</span></span>

<span data-ttu-id="61c57-132">Die Hauptprogramm Schleife selbst muss Windows-Meldungen bestätigen, indem es Windows die Möglichkeit erhält, den statischen Nachrichten proc auszuführen.</span><span class="sxs-lookup"><span data-stu-id="61c57-132">The main program loop itself needs to acknowledge Windows messages by allowing Windows the opportunity to run the static message proc.</span></span> <span data-ttu-id="61c57-133">Helfen Sie, das Programm effizient auszuführen, indem Sie das Verhalten auslassen: jede Iteration sollte neue Windows-Meldungen verarbeiten, wenn Sie verfügbar sind, und wenn sich keine Nachrichten in der Warteschlange befinden, sollte ein neuer Frame renderert werden.</span><span class="sxs-lookup"><span data-stu-id="61c57-133">Help the program run efficiently by forking the behavior: each iteration should choose to process new Windows messages if they are available, and if no messages are in the queue it should render a new frame.</span></span> <span data-ttu-id="61c57-134">Hier ist ein sehr einfaches Beispiel:</span><span class="sxs-lookup"><span data-stu-id="61c57-134">Here's a very simple example:</span></span>


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



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a><span data-ttu-id="61c57-135">Eine Schnittstelle für das Direct3D-Gerät und den Kontext erhalten</span><span class="sxs-lookup"><span data-stu-id="61c57-135">Get an interface for the Direct3D device and context</span></span>

<span data-ttu-id="61c57-136">Der erste Schritt bei der Verwendung von Direct3D besteht darin, eine Schnittstelle für die Direct3D-Hardware (die GPU) zu erwerben, die als Instanzen von [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2)dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="61c57-136">The first step to using Direct3D is to acquire an interface for the Direct3D hardware (the GPU), represented as instances of [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2).</span></span> <span data-ttu-id="61c57-137">Bei der ersten handelt es sich um eine virtuelle Darstellung der GPU-Ressourcen. letztere ist eine geräteunabhängige Abstraktion der Renderingpipeline und des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="61c57-137">The former is a virtual representation of the GPU resources, and the latter is a device-agnostic abstraction of the rendering pipeline and process.</span></span> <span data-ttu-id="61c57-138">Im folgenden finden Sie eine einfache Möglichkeit: **ID3D11Device** enthält die Grafik Methoden, die Sie nur selten aufzurufen, normalerweise vor dem Auftreten eines Renderings, um die Ressourcen zu erhalten und zu konfigurieren, die Sie benötigen, um mit dem Zeichnen von Pixeln zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="61c57-138">Here's an easy way to think of it: **ID3D11Device** contains the graphics methods you call infrequently, usually before any rendering occurs, to acquire and configure the set of resources you need to start drawing pixels.</span></span> <span data-ttu-id="61c57-139">**Verknüpfung id3d11devicecontext aus** hingegen enthält die Methoden, die Sie für jeden Frame aufrufen: Laden in Puffer und Sichten und andere Ressourcen, Ändern der Ausgabe von Fusion-und Raster-Status, Verwalten von Shadern und Zeichnen der Ergebnisse der Übergabe dieser Ressourcen über die Zustände und Shader.</span><span class="sxs-lookup"><span data-stu-id="61c57-139">**ID3D11DeviceContext**, on the other hand, contains the methods you call every frame: loading in buffers and views and other resources, changing output-merger and rasterizer state, managing shaders, and drawing the results of passing those resources through the states and shaders.</span></span>

<span data-ttu-id="61c57-140">Es gibt einen sehr wichtigen Teil dieses Prozesses: das Festlegen der Funktionsebene.</span><span class="sxs-lookup"><span data-stu-id="61c57-140">There's one very important part of this process: setting the feature level.</span></span> <span data-ttu-id="61c57-141">Die Featureebene informiert DirectX über die minimale Hardwareebene, die ihre App unterstützt, wobei die D3D \_ \_ Featureebene \_ 9 \_ 1 als niedrigste featuremenge und die D3D- \_ Funktions \_ Ebene \_ 11 \_ 1 als die aktuelle höchste Stufe hat.</span><span class="sxs-lookup"><span data-stu-id="61c57-141">The feature level tells DirectX the minimum level of hardware your app supports, with D3D\_FEATURE\_LEVEL\_9\_1 as the lowest feature set and D3D\_FEATURE\_LEVEL\_11\_1 as the current highest.</span></span> <span data-ttu-id="61c57-142">Sie sollten 9 \_ 1 als minimal unterstützen, wenn Sie die größtmögliche Zielgruppe erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="61c57-142">You should support 9\_1 as the minimum if you want to reach the widest possible audience.</span></span> <span data-ttu-id="61c57-143">Nehmen Sie sich etwas Zeit, um auf Direct3D- [featureebenen](/previous-versions/windows/apps/hh994923(v=win.10)) zu lesen und die Mindest-und höchst Funktionsebenen zu bewerten, die Ihr Spiel unterstützen soll, und um die Auswirkungen ihrer Wahl zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="61c57-143">Take some time to read up on Direct3D [feature levels](/previous-versions/windows/apps/hh994923(v=win.10)) and assess for yourself the minimum and maximum feature levels you want your game to support and to understand the implications of your choice.</span></span>

<span data-ttu-id="61c57-144">Rufen Sie Verweise (Zeiger) auf das Direct3D-Gerät und den Gerätekontext ab, und speichern Sie Sie als Variablen auf Klassenebene in der **deviceresources** -Instanz (als **comptr** -intelligente Zeiger).</span><span class="sxs-lookup"><span data-stu-id="61c57-144">Obtain references (pointers) to both the Direct3D device and device context and store them as class-level variables on the **DeviceResources** instance (as **ComPtr** smart pointers).</span></span> <span data-ttu-id="61c57-145">Verwenden Sie diese Verweise, wenn Sie auf das Direct3D-Gerät oder den Gerätekontext zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="61c57-145">Use these references whenever you need to access the Direct3D device or device context.</span></span>


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



## <a name="create-the-swap-chain"></a><span data-ttu-id="61c57-146">Austausch Kette erstellen</span><span class="sxs-lookup"><span data-stu-id="61c57-146">Create the swap chain</span></span>

<span data-ttu-id="61c57-147">Okay: Sie verfügen über ein Fenster, in dem Sie zeichnen können, und Sie verfügen über eine Schnittstelle zum Senden von Daten und zum Übergeben von Befehlen an die GPU.</span><span class="sxs-lookup"><span data-stu-id="61c57-147">Okay: You have a window to draw in, and you have an interface to send data and give commands to the GPU.</span></span> <span data-ttu-id="61c57-148">Sehen wir uns nun an, wie Sie zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="61c57-148">Now let's see how to bring them together.</span></span>

<span data-ttu-id="61c57-149">Zuerst teilen Sie DXGI mit, welche Werte für die Eigenschaften der Austausch Kette verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61c57-149">First, you tell DXGI what values to use for the properties of the swap chain.</span></span> <span data-ttu-id="61c57-150">Verwenden Sie hierfür eine [**DXGI \_ - \_ SwapChain \_**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="61c57-150">Do this using a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure.</span></span> <span data-ttu-id="61c57-151">Sechs Felder sind besonders wichtig für Desktop-Apps:</span><span class="sxs-lookup"><span data-stu-id="61c57-151">Six fields are particularly important for desktop apps:</span></span>

-   <span data-ttu-id="61c57-152">**Windowed**: gibt an, ob die Austausch Kette voll Bildschirm ist oder auf das Fenster zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="61c57-152">**Windowed**: Indicates whether the swap chain is full-screen or clipped to the window.</span></span> <span data-ttu-id="61c57-153">Legen Sie diese Einstellung auf "true" fest, um die Austausch Kette in dem zuvor erstellten Fenster abzulegen.</span><span class="sxs-lookup"><span data-stu-id="61c57-153">Set this to TRUE to put the swap chain in the window you created earlier.</span></span>
-   <span data-ttu-id="61c57-154">**Bufferusage**: Legen Sie dies auf die Ausgabe des DXGI- \_ Verwendungs \_ \_ Renderziels fest \_ .</span><span class="sxs-lookup"><span data-stu-id="61c57-154">**BufferUsage**: Set this to DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT.</span></span> <span data-ttu-id="61c57-155">Dies weist darauf hin, dass die SwapChain eine Zeichen Oberfläche ist, die es Ihnen ermöglicht, Sie als Direct3D-Renderziel zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="61c57-155">This indicates that the swap chain will be a drawing surface, allowing you to use it as a Direct3D render-target.</span></span>
-   <span data-ttu-id="61c57-156">**SwapEffect**: Legen Sie diese Einstellung auf den DXGI- \_ Swap- \_ Effekt als \_ \_ sequenziell fest.</span><span class="sxs-lookup"><span data-stu-id="61c57-156">**SwapEffect**: Set this to DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL.</span></span>
-   <span data-ttu-id="61c57-157">**Format**: das \_ \_ B8G8R8A8 unorm-Format im DXGI-Format gibt die \_ 32-Bit-Farbe an: 8 Bits für jeden der drei RGB-Farbkanäle und 8 Bits für den Alphakanal.</span><span class="sxs-lookup"><span data-stu-id="61c57-157">**Format**: The DXGI\_FORMAT\_B8G8R8A8\_UNORM format specifies 32-bit color: 8 bits for each of the three RGB color channels, and 8 bits for the alpha channel.</span></span>
-   <span data-ttu-id="61c57-158">**BUFFERCOUNT**: Legen Sie diese Einstellung auf "2" fest, um ein herkömmliches Verhalten mit doppelter puffert zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="61c57-158">**BufferCount**: Set this to 2 for a traditional double-buffered behavior to avoid tearing.</span></span> <span data-ttu-id="61c57-159">Legen Sie für die Puffer Anzahl den Wert 3 fest, wenn Ihr Grafik Inhalt mehr als einen Monitor Aktualisierungszyklen zum Renderingvorgang für einen einzelnen Frame benötigt (z. b. 60 Hz, wenn der Schwellenwert größer als 16 ms ist)</span><span class="sxs-lookup"><span data-stu-id="61c57-159">Set the buffer count to 3 if your graphics content takes more than one monitor refresh cycle to render a single frame (at 60 Hz for example, the threshold is more than 16 ms).</span></span>
-   <span data-ttu-id="61c57-160">**SampleDesc**: Dieses Feld steuert das Multisampling.</span><span class="sxs-lookup"><span data-stu-id="61c57-160">**SampleDesc**: This field controls multisampling.</span></span> <span data-ttu-id="61c57-161">Legen Sie **Anzahl** auf 1 und **Qualität** für Swapketten des Flip-Modells auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="61c57-161">Set **Count** to 1 and **Quality** to 0 for flip-model swap chains.</span></span> <span data-ttu-id="61c57-162">(Um multisamplinggrad mit Flip-Model-Austausch Ketten zu verwenden, zeichnen Sie ein separates multisamplinggrad-Renderziel, und lösen Sie dieses Ziel dann in der SwapChain direkt vor der Präsentation auf.</span><span class="sxs-lookup"><span data-stu-id="61c57-162">(To use multisampling with flip-model swap chains, draw on a separate multisampled render target and then resolve that target to the swap chain just before presenting it.</span></span> <span data-ttu-id="61c57-163">Beispielcode wird in [Multisampling in Windows Store-Apps](/previous-versions/windows/apps/dn458384(v=win.10))bereitgestellt.)</span><span class="sxs-lookup"><span data-stu-id="61c57-163">Example code is provided in [Multisampling in Windows Store apps](/previous-versions/windows/apps/dn458384(v=win.10)).)</span></span>

<span data-ttu-id="61c57-164">Nachdem Sie eine Konfiguration für die SwapChain angegeben haben, müssen Sie die gleiche DXGI-Factory verwenden, die das Direct3D-Gerät (und den Gerätekontext) erstellt hat, um die Swapkette zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="61c57-164">After you have specified a configuration for the swap chain, you must use the same DXGI factory that created the Direct3D device (and device context) in order to create the swap chain.</span></span>

<span data-ttu-id="61c57-165">**Kurzform:  **</span><span class="sxs-lookup"><span data-stu-id="61c57-165">**Short form:  **</span></span>

<span data-ttu-id="61c57-166">Beziehen Sie den zuvor erstellten [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) -Verweis.</span><span class="sxs-lookup"><span data-stu-id="61c57-166">Get the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) reference you created previously.</span></span> <span data-ttu-id="61c57-167">Upcast Sie in [**"idxgidevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (sofern nicht bereits geschehen), und rufen Sie dann [**idxgidevice:: GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) auf, um den DXGI-Adapter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="61c57-167">Upcast it to [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (if you haven't already) and then call [**IDXGIDevice::GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) to acquire the DXGI adapter.</span></span> <span data-ttu-id="61c57-168">Abrufen der übergeordneten Factory für diesen Adapter durch Aufrufen von [**IDXGIFactory2:: GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) erbt von [**idxgiobject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)) – jetzt können Sie diese Factory verwenden, um die [**Swapkette durch Aufrufen von createswapchaparent HWND**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)zu erstellen, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="61c57-168">Get the parent factory for that adapter by calling [**IDXGIFactory2::GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) inherits from [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject))—now you can use that factory to create the swap chain by calling [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), as seen in the following code sample.</span></span>


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



<span data-ttu-id="61c57-169">Wenn Sie gerade erst beginnen, ist es wahrscheinlich, dass die hier gezeigte Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61c57-169">If you're just starting out, it's probably best to use the configuration shown here.</span></span> <span data-ttu-id="61c57-170">Wenn Sie nun bereits mit früheren Versionen von DirectX vertraut sind, stellen Sie möglicherweise Folgendes in Frage: "Warum haben wir das Gerät nicht erstellt und die Kette nicht gleichzeitig ausgetauscht, sondern nicht durch alle diese Klassen zurück?"</span><span class="sxs-lookup"><span data-stu-id="61c57-170">Now at this point, if you are already familiar with previous versions of DirectX you might be asking: "Why didn't we create the device and swap chain at the same time, instead of walking back through all of those classes?"</span></span> <span data-ttu-id="61c57-171">Die Antwort ist die Effizienz: Austausch Ketten sind Direct3D Geräte Ressourcen, und Geräte Ressourcen sind an das jeweilige Direct3D-Gerät gebunden, von dem Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="61c57-171">The answer is efficiency: swap chains are Direct3D device resources, and device resources are tied to the particular Direct3D device that created them.</span></span> <span data-ttu-id="61c57-172">Wenn Sie ein neues Gerät mit einer neuen austauschkette erstellen, müssen Sie alle Geräte Ressourcen mithilfe des neuen Direct3D-Geräts neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="61c57-172">If you create a new device with a new swap chain, you have to recreate all your device resources using the new Direct3D device.</span></span> <span data-ttu-id="61c57-173">Wenn Sie also die SwapChain mit derselben Factory erstellen (wie oben gezeigt), können Sie die Swapkette neu erstellen und weiterhin die Direct3D-Geräte Ressourcen verwenden, die Sie bereits geladen haben!</span><span class="sxs-lookup"><span data-stu-id="61c57-173">So by creating the swap chain with the same factory (as shown above), you are able to recreate the swap chain and continue using the Direct3D device resources you already have loaded!</span></span>

<span data-ttu-id="61c57-174">Nun haben Sie ein Fenster vom Betriebssystem, eine Möglichkeit für den Zugriff auf die GPU und deren Ressourcen und eine SwapChain zum Anzeigen der renderingergebnisse.</span><span class="sxs-lookup"><span data-stu-id="61c57-174">Now you've got a window from the operating system, a way to access the GPU and its resources, and a swap chain to display the rendering results.</span></span> <span data-ttu-id="61c57-175">Alles, was übrig bleibt, besteht darin, die gesamte Aufgabe zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="61c57-175">All that's left is to wire the whole thing together!</span></span>

## <a name="create-a-render-target-for-drawing"></a><span data-ttu-id="61c57-176">Renderziel zum Zeichnen erstellen</span><span class="sxs-lookup"><span data-stu-id="61c57-176">Create a render target for drawing</span></span>

<span data-ttu-id="61c57-177">Die Shader-Pipeline benötigt eine Ressource, in der Pixel gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="61c57-177">The shader pipeline needs a resource to draw pixels into.</span></span> <span data-ttu-id="61c57-178">Die einfachste Möglichkeit zum Erstellen dieser Ressource besteht darin, eine [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) -Ressource als Hintergrund Puffer zu definieren, in den der Pixelshader gezeichnet werden soll, und dann diese Textur in der SwapChain zu lesen.</span><span class="sxs-lookup"><span data-stu-id="61c57-178">The simplest way to create this resource is to define a [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource as a back buffer for the pixel shader to draw into, and then read that texture into the swap chain.</span></span>

<span data-ttu-id="61c57-179">Zu diesem Zweck erstellen Sie eine renderzielansicht .</span><span class="sxs-lookup"><span data-stu-id="61c57-179">To do this, you create a render-target *view*.</span></span> <span data-ttu-id="61c57-180">In Direct3D ist eine Sicht eine Möglichkeit, auf eine bestimmte Ressource zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="61c57-180">In Direct3D, a view is a way to access a specific resource.</span></span> <span data-ttu-id="61c57-181">In diesem Fall ermöglicht die-Sicht dem Pixelshader das Schreiben in die Textur, während er die pro-Pixel-Vorgänge abschließt.</span><span class="sxs-lookup"><span data-stu-id="61c57-181">In this case, the view enables the pixel shader to write into the texture as it completes its per-pixel operations.</span></span>

<span data-ttu-id="61c57-182">Sehen wir uns den Code für diese an.</span><span class="sxs-lookup"><span data-stu-id="61c57-182">Let's look at the code for this.</span></span> <span data-ttu-id="61c57-183">Wenn Sie die Ausgabe des DXGI- \_ Verwendungs \_ \_ Renderziels \_ in der SwapChain festlegen, wird dadurch die zugrunde liegende Direct3D-Ressource als Zeichen Oberfläche verwendet.</span><span class="sxs-lookup"><span data-stu-id="61c57-183">When you set DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT on the swap chain, that enabled the underlying Direct3D resource to be used as a drawing surface.</span></span> <span data-ttu-id="61c57-184">Um unsere renderzielansicht zu erhalten, muss lediglich der Hintergrund Puffer aus der Swapkette und eine renderzielansicht erstellt werden, die an die backpufferressource gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="61c57-184">So to get our render target view, we just need to get the back buffer from the swap chain and create a render target view bound to the back buffer resource.</span></span>


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



<span data-ttu-id="61c57-185">Erstellen Sie außerdem einen *tiefen Schablonen Puffer*.</span><span class="sxs-lookup"><span data-stu-id="61c57-185">Also create a *depth-stencil buffer*.</span></span> <span data-ttu-id="61c57-186">Ein tiefen Schablone-Puffer ist nur eine bestimmte Form der [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) -Ressource, die normalerweise verwendet wird, um zu bestimmen, welche Pixel während der rasterisierung auf der Grundlage der Entfernung der Objekte in der Szene von der Kamera gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="61c57-186">A depth-stencil buffer is just a particular form of [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource, which is typically used to determine which pixels have draw priority during rasterization based on the distance of the objects in the scene from the camera.</span></span> <span data-ttu-id="61c57-187">Ein tiefen Schablone-Puffer kann auch für Schablonen Effekte verwendet werden, bei denen bestimmte Pixel während der rasterisierung verworfen oder ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="61c57-187">A depth-stencil buffer can also be used for stencil effects, where specific pixels are discarded or ignored during rasterization.</span></span> <span data-ttu-id="61c57-188">Dieser Puffer muss dieselbe Größe aufweisen wie das Renderziel.</span><span class="sxs-lookup"><span data-stu-id="61c57-188">This buffer must be the same size as the render target.</span></span> <span data-ttu-id="61c57-189">Beachten Sie, dass Sie die Rahmen Puffer Tiefe der tiefen Schablone nicht lesen oder Rendern können, da Sie ausschließlich von der Shader-Pipeline vor und während der endgültigen rasterisierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61c57-189">Note that you cannot read from or render to the frame buffer depth-stencil texture because it is used exclusively by the shader pipeline before and during final rasterization.</span></span>

<span data-ttu-id="61c57-190">Erstellen Sie außerdem eine Ansicht für den tiefen Schablone-Puffer als [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="61c57-190">Also create a view for the depth-stencil buffer as an [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span></span> <span data-ttu-id="61c57-191">Die Ansicht teilt der Shader-Pipeline mit, wie die zugrunde liegende [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) -Ressource interpretiert werden soll. Wenn Sie diese Ansicht nicht bereitstellen, werden keine pro-Pixel-tiefen Tests durchgeführt, und die Objekte in Ihrer Szene erscheinen möglicherweise sehr wenig.</span><span class="sxs-lookup"><span data-stu-id="61c57-191">The view tells the shader pipeline how to interpret the underlying [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource - so if you don't supply this view no per-pixel depth testing is performed, and the objects in your scene may seem a bit inside-out at the very least!</span></span>


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



<span data-ttu-id="61c57-192">Der letzte Schritt besteht darin, einen Viewport zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="61c57-192">The last step is to create a viewport.</span></span> <span data-ttu-id="61c57-193">Definiert das sichtbare Rechteck des Hintergrund Puffers, der auf dem Bildschirm angezeigt wird. Sie können den Teil des Puffers ändern, der auf dem Bildschirm angezeigt wird, indem Sie die Parameter für den Viewport ändern.</span><span class="sxs-lookup"><span data-stu-id="61c57-193">This defines the visible rectangle of the back buffer displayed on the screen; you can change the part of the buffer that is displayed on the screen by changing the parameters of the viewport.</span></span> <span data-ttu-id="61c57-194">Dieser Code bezieht sich auf die gesamte Fenstergröße – oder auf die Bildschirmauflösung, bei voll Bildaustausch Ketten.</span><span class="sxs-lookup"><span data-stu-id="61c57-194">This code targets the whole window size—or the screen resolution, in the case of full-screen swap chains.</span></span> <span data-ttu-id="61c57-195">Wenn Sie Spaß machen, ändern Sie die angegebenen Koordinaten Werte, und beobachten Sie die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="61c57-195">For fun, change the supplied coordinate values and observe the results.</span></span>


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



<span data-ttu-id="61c57-196">Und das ist, wie Sie in einem Fenster von nichts zum Zeichnen von Pixeln gelangen!</span><span class="sxs-lookup"><span data-stu-id="61c57-196">And that's how you go from nothing to drawing pixels in a window!</span></span> <span data-ttu-id="61c57-197">Wenn Sie beginnen, sollten Sie sich damit vertraut machen, wie DirectX, über DXGI, die Kernressourcen verwaltet, die Sie für das Zeichnen von Pixeln benötigen.</span><span class="sxs-lookup"><span data-stu-id="61c57-197">As you start out, it's a good idea to become familiar with how DirectX, through DXGI, manages the core resources you need to start drawing pixels.</span></span>

<span data-ttu-id="61c57-198">Als nächstes betrachten Sie die Struktur der Grafik Pipeline. Siehe Grundlegendes [zur Renderingpipeline der DirectX-App-Vorlage](understand-the-directx-11-2-graphics-pipeline.md).</span><span class="sxs-lookup"><span data-stu-id="61c57-198">Next you'll look at the structure of the graphics pipeline; see [Understand the DirectX app template's rendering pipeline](understand-the-directx-11-2-graphics-pipeline.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61c57-199">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61c57-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="61c57-200">**Als Nächstes**</span><span class="sxs-lookup"><span data-stu-id="61c57-200">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="61c57-201">Arbeiten mit Shader und Shaderressourcen</span><span class="sxs-lookup"><span data-stu-id="61c57-201">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
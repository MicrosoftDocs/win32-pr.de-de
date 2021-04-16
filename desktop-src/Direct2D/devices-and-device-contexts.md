---
title: Vorgehensweise beim Rendering mithilfe eines Direct2D-Geräte Kontexts
description: In diesem Thema erfahren Sie mehr über das Erstellen von Direct2D \ 32; Gerätekontext in Windows 8.
ms.assetid: D4563FEA-767E-4B16-8F3C-3D548A64B206
keywords:
- Direct2D-Gerät
- Direct2D-Gerätekontext
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2858861956a40bf969309be474105052e4692cde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104567545"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a><span data-ttu-id="5b211-105">Vorgehensweise beim Rendering mithilfe eines Direct2D-Geräte Kontexts</span><span class="sxs-lookup"><span data-stu-id="5b211-105">How to render by using a Direct2D device context</span></span>

<span data-ttu-id="5b211-106">In diesem Thema erfahren Sie mehr über das Erstellen des [Direct2D](./direct2d-portal.md) - [**Geräte Kontexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5b211-106">In this topic you will learn about creating [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) in Windows 8.</span></span> <span data-ttu-id="5b211-107">Diese Informationen gelten für Sie, wenn Sie Windows Store-Apps oder eine Desktop-App mithilfe von Direct2D entwickeln.</span><span class="sxs-lookup"><span data-stu-id="5b211-107">This information applies to you if you are developing Windows Store apps or a desktop app by using Direct2D.</span></span> <span data-ttu-id="5b211-108">In diesem Thema wird der Zweck von Direct2D-Gerätekontext Objekten, das Erstellen dieses Objekts und eine Schritt-für-Schritt-Anleitung zum Rendern und Anzeigen von Direct2D Primitives und Bildern beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5b211-108">This topic describes the purpose of Direct2D device context objects, how to create that object , and a step by step guide about rendering and displaying Direct2D primitives and images.</span></span> <span data-ttu-id="5b211-109">Außerdem erfahren Sie mehr über das Wechseln von renderzielen und das Hinzufügen von Effekten zu Ihrer APP.</span><span class="sxs-lookup"><span data-stu-id="5b211-109">You will also learn about switching render targets and adding effects to your app.</span></span>

-   [<span data-ttu-id="5b211-110">Was ist ein Direct2D-Gerät?</span><span class="sxs-lookup"><span data-stu-id="5b211-110">What is a Direct2D device?</span></span>](#what-is-a-direct2d-device)
-   [<span data-ttu-id="5b211-111">Was ist ein Direct2D-Gerätekontext?</span><span class="sxs-lookup"><span data-stu-id="5b211-111">What is a Direct2D device context?</span></span>](#what-is-a-direct2d-device-context)
-   [<span data-ttu-id="5b211-112">Rendering mit Direct2D unter Windows 8</span><span class="sxs-lookup"><span data-stu-id="5b211-112">Rendering with Direct2D on Windows 8</span></span>](#rendering-with-direct2d-on-windows-8)
-   [<span data-ttu-id="5b211-113">Gründe für die Verwendung eines Geräte Kontexts zum Rendering</span><span class="sxs-lookup"><span data-stu-id="5b211-113">Why use a device context to render?</span></span>](#why-use-a-device-context-to-render)
-   [<span data-ttu-id="5b211-114">Erstellen eines Direct2D-Geräte Kontexts für das Rendering</span><span class="sxs-lookup"><span data-stu-id="5b211-114">How to create a Direct2D device context for rendering</span></span>](#how-to-create-a-direct2d-device-context-for-rendering)
-   [<span data-ttu-id="5b211-115">Auswählen eines Ziels</span><span class="sxs-lookup"><span data-stu-id="5b211-115">Selecting a target</span></span>](#selecting-a-target)
-   [<span data-ttu-id="5b211-116">Rendering und Anzeige</span><span class="sxs-lookup"><span data-stu-id="5b211-116">How to render and display</span></span>](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a><span data-ttu-id="5b211-117">Was ist ein Direct2D-Gerät?</span><span class="sxs-lookup"><span data-stu-id="5b211-117">What is a Direct2D device?</span></span>

<span data-ttu-id="5b211-118">Sie benötigen ein Direct2D-Gerät und ein Direct3D-Gerät, um einen Direct2D-Gerätekontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b211-118">You need a Direct2D device and a Direct3D device to create a Direct2D device context.</span></span> <span data-ttu-id="5b211-119">Ein [**Direct2D-Gerät**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (das einen **ID2D1Device** -Schnittstellen Zeiger verfügbar macht) stellt einen Anzeige Adapter dar.</span><span class="sxs-lookup"><span data-stu-id="5b211-119">A [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (exposes an **ID2D1Device** interface pointer) represents a display adapter.</span></span> <span data-ttu-id="5b211-120">Ein Direct3D-Gerät (das einen [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) -Schnittstellen Zeiger verfügbar macht) ist einem Direct2D-Gerät zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5b211-120">A Direct3D device (exposes an [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) interface pointer) is associated with a Direct2D device.</span></span> <span data-ttu-id="5b211-121">Jede APP muss über ein **Direct2D-Gerät** verfügen, kann aber über mehrere **Geräte** verfügen.</span><span class="sxs-lookup"><span data-stu-id="5b211-121">Each app must have one **Direct2D device**, but can have more than one **device**.</span></span>

## <a name="what-is-a-direct2d-device-context"></a><span data-ttu-id="5b211-122">Was ist ein Direct2D-Gerätekontext?</span><span class="sxs-lookup"><span data-stu-id="5b211-122">What is a Direct2D device context?</span></span>

<span data-ttu-id="5b211-123">Ein [Direct2D](./direct2d-portal.md) - [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (macht einen **ID2D1DeviceContext** -Schnittstellen Zeiger verfügbar) stellt einen Satz von Status-und Befehls Puffern dar, die Sie verwenden, um ein Ziel zu rendieren.</span><span class="sxs-lookup"><span data-stu-id="5b211-123">A [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (exposes an **ID2D1DeviceContext** interface pointer) represents a set of state and command buffers that you use to render to a target.</span></span> <span data-ttu-id="5b211-124">Sie können Methoden für den Gerätekontext aufzurufen, um den Pipeline Status festzulegen und renderingbefehle zu generieren, indem Sie die Ressourcen eines Geräts verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b211-124">You can call methods on the device context to set pipeline state and generate rendering commands by using the resources owned by a device.</span></span>

## <a name="rendering-with-direct2d-on-windows-8"></a><span data-ttu-id="5b211-125">Rendering mit Direct2D unter Windows 8</span><span class="sxs-lookup"><span data-stu-id="5b211-125">Rendering with Direct2D on Windows 8</span></span>

<span data-ttu-id="5b211-126">Unter Windows 7 und früher verwenden Sie eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) oder eine andere renderzielschnittstelle, um Sie in einem Fenster oder einer Oberfläche zu renderzielen.</span><span class="sxs-lookup"><span data-stu-id="5b211-126">On Windows 7 and earlier, you use a [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) or another render target interface to render to a window or surface.</span></span> <span data-ttu-id="5b211-127">Ab Windows 8 empfiehlt es sich nicht, das Rendering mithilfe von Methoden durchzuführen, die auf Schnittstellen wie **ID2D1HwndRenderTarget** basieren, da Sie nicht mit Windows Store-Apps funktionieren.</span><span class="sxs-lookup"><span data-stu-id="5b211-127">Starting with Windows 8, we do not recommend rendering by using methods that rely on interfaces like **ID2D1HwndRenderTarget** because they won't work with Windows Store apps.</span></span> <span data-ttu-id="5b211-128">Sie können einen [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) verwenden, um ein HWND zu erzeugen, wenn Sie eine Desktop-App erstellen möchten, und die zusätzlichen Features des **Geräte Kontexts** weiterhin nutzen.</span><span class="sxs-lookup"><span data-stu-id="5b211-128">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to render to an Hwnd if you want to make a desktop app and still take advantage of the **device context's** additional features.</span></span> <span data-ttu-id="5b211-129">Der **Gerätekontext** ist jedoch zum Rendering von Inhalten in Windows Store-Apps mit [Direct2D](./direct2d-portal.md)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5b211-129">However, the **device context** is required to render content in a Windows Store apps with [Direct2D](./direct2d-portal.md).</span></span>

## <a name="why-use-a-device-context-to-render"></a><span data-ttu-id="5b211-130">Gründe für die Verwendung eines Geräte Kontexts zum Rendering</span><span class="sxs-lookup"><span data-stu-id="5b211-130">Why use a device context to render?</span></span>

-   <span data-ttu-id="5b211-131">Sie können für Windows Store-Apps Rendering.</span><span class="sxs-lookup"><span data-stu-id="5b211-131">You can render for Windows Store apps.</span></span>
-   <span data-ttu-id="5b211-132">Sie können das Renderziel jederzeit vor, während und nach dem Rendering ändern.</span><span class="sxs-lookup"><span data-stu-id="5b211-132">You can change the render target at any time before, during, and after rendering.</span></span> <span data-ttu-id="5b211-133">Der Gerätekontext stellt sicher, dass die Aufrufe von Zeichnungs Methoden in der richtigen Reihenfolge ausgeführt werden, und wendet sie an, wenn Sie das Renderziel wechseln.</span><span class="sxs-lookup"><span data-stu-id="5b211-133">The device context ensures that the calls to drawing methods are executed in order and applies them when you switch the render target.</span></span>
-   <span data-ttu-id="5b211-134">Sie können mehr als einen Fenstertyp mit einem Gerätekontext verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b211-134">You can use more than one type of window with a device context.</span></span> <span data-ttu-id="5b211-135">Sie können einen [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) und eine [**DXGI-SwapChain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) verwenden, um direkt in ein [**Windows:: UI:: Core:: corewindow**](/uwp/api/Windows.UI.Core.CoreWindow) oder ein [**Windows:: UI:: XAML:: swapchainbackgroundpanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel)-Element gerenstet zu werden.</span><span class="sxs-lookup"><span data-stu-id="5b211-135">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) to render directly to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) or a [**Windows::UI::XAML::SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span></span>
-   <span data-ttu-id="5b211-136">Sie können den [Direct2D](./direct2d-portal.md) - [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) zum Erstellen von [Direct2D-Effekten](effects-overview.md) und zum renderingrendering der Ausgabe eines Bild Effekts oder eines Effekt Diagramms in ein Renderziel verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b211-136">You can use the [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to create [Direct2D effects](effects-overview.md) and to render the output of an image effect or effect graph to a render target.</span></span>
-   <span data-ttu-id="5b211-137">Sie können über mehrere [**Geräte Kontexte**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)verfügen. Dies kann hilfreich sein, um die Leistung in einer Thread-APP zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="5b211-137">You can have multiple [**device contexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), which can be helpful for improving performance in a threaded app.</span></span> <span data-ttu-id="5b211-138">Weitere Informationen finden Sie unter [Multithreaded Direct2D-apps](multi-threaded-direct2d-apps.md) .</span><span class="sxs-lookup"><span data-stu-id="5b211-138">See [Multithreaded Direct2D apps](multi-threaded-direct2d-apps.md) for more information.</span></span>
-   <span data-ttu-id="5b211-139">Der [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interagiert eng mit Direct3D und bietet Ihnen mehr Zugriff auf Direct3D-Optionen.</span><span class="sxs-lookup"><span data-stu-id="5b211-139">The [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interoperates closely with Direct3D, giving you more access to Direct3D options.</span></span>

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a><span data-ttu-id="5b211-140">Erstellen eines Direct2D-Geräte Kontexts für das Rendering</span><span class="sxs-lookup"><span data-stu-id="5b211-140">How to create a Direct2D device context for rendering</span></span>

<span data-ttu-id="5b211-141">Der folgende Code zeigt, wie Sie ein Direct3D11-Gerät erstellen, das zugehörige DXGI-Gerät erhalten, ein [**Direct2D-Gerät**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)erstellen und schließlich den Direct2D- [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) für das Rendering erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b211-141">The code here shows you how to create a Direct3D11 device, get the associated DXGI device, create a [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device), and then finally create the Direct2D [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) for rendering.</span></span>

<span data-ttu-id="5b211-142">Im folgenden finden Sie ein Diagramm der Methodenaufrufe und der von diesem Code verwendeten Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="5b211-142">Here is a diagram of the method calls and the interfaces this code uses.</span></span>

![Diagramm der Direct2D-und Direct3D-Geräte und-Geräte Kontexte.](images/devicecontextdiagram.png)

> [!Note]  
> <span data-ttu-id="5b211-144">Dieser Code setzt voraus, dass Sie bereits über ein [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) -Objekt verfügen. Weitere Informationen finden Sie auf der [**ID2D1Factory-Referenzseite**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="5b211-144">This code assumes you already have an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) object, for more information see the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>

 


```C++
    // This flag adds support for surfaces with a different color channel ordering than the API default.
    // You need it for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    
    // This array defines the set of DirectX hardware feature levels this app  supports.
    // The ordering is important and you should  preserve it.
    // Don't forget to declare your app's minimum required feature level in its
    // description.  All apps are assumed to support 9.1 unless otherwise stated.
    D3D_FEATURE_LEVEL featureLevels[] = 
    {
        D3D_FEATURE_LEVEL_11_1,
        D3D_FEATURE_LEVEL_11_0,
        D3D_FEATURE_LEVEL_10_1,
        D3D_FEATURE_LEVEL_10_0,
        D3D_FEATURE_LEVEL_9_3,
        D3D_FEATURE_LEVEL_9_2,
        D3D_FEATURE_LEVEL_9_1
    };

    // Create the DX11 API device object, and get a corresponding context.
    ComPtr<ID3D11Device> device;
    ComPtr<ID3D11DeviceContext> context;

    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of possible feature levels
            D3D11_SDK_VERSION,          
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );

    ComPtr<IDXGIDevice> dxgiDevice;
    // Obtain the underlying DXGI device of the Direct3D11 device.
    DX::ThrowIfFailed(
        device.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // Get Direct2D device's corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



<span data-ttu-id="5b211-145">Gehen wir die Schritte im vorangehenden Codebeispiel durch.</span><span class="sxs-lookup"><span data-stu-id="5b211-145">Let's walk through the steps in the preceding code sample.</span></span>

1.  <span data-ttu-id="5b211-146">Rufen Sie einen ID3D11Device-Schnittstellen Zeiger ab, der zum Erstellen des Geräte Kontexts benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="5b211-146">Get an ID3D11Device interface pointer you will need this to create the device context.</span></span>

    -   <span data-ttu-id="5b211-147">Deklarieren Sie die Erstellungs Flags, um das [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -Gerät für die BGRA-Unterstützung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="5b211-147">Declare the creation flags to set up the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) device for BGRA support.</span></span> <span data-ttu-id="5b211-148">[Direct2D](./direct2d-portal.md) erfordert die BGRA-Farb Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="5b211-148">[Direct2D](./direct2d-portal.md) requires BGRA color order.</span></span>
    -   <span data-ttu-id="5b211-149">Deklarieren Sie ein Array von [**D3D- \_ Funktions \_**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) Ebenen-Einträgen, die den Satz von featureebenen darstellen, die ihre App unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5b211-149">Declare an array of [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) entries representing the set of feature levels that your app will support.</span></span>
        > [!Note]  
        > <span data-ttu-id="5b211-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) durchsucht die Liste, bis die von dem Host System unterstützte Funktionsebene gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="5b211-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) searches your list until it finds the feature level supported by the host system.</span></span>

         

    -   <span data-ttu-id="5b211-151">Verwenden Sie die [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) -Funktion zum Erstellen eines [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) -Objekts, die Funktion gibt auch ein [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) -Objekt zurück, aber dieses Objekt ist für dieses Beispiel nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5b211-151">Use the [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) function to create an [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) object, the function will also return an [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) object, but that object is not needed for this example.</span></span>

2.  <span data-ttu-id="5b211-152">Fragen Sie das [**Gerät Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) nach seiner [**DXGI-Geräte**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="5b211-152">Query the [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) for its [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) interface.</span></span>
3.  <span data-ttu-id="5b211-153">Erstellen Sie ein [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) -Objekt, indem Sie die [**ID2D1Factory:: createdevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) -Methode aufrufen und das [**idxgidevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) -Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="5b211-153">Create an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) object by calling the [**ID2D1Factory::CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) method and passing in the [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) object.</span></span>
4.  <span data-ttu-id="5b211-154">Erstellen Sie mithilfe der Methode [**ID2D1Device:: | atedevicecontext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) einen [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="5b211-154">Create an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pointer using the [**ID2D1Device::CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) method.</span></span>

## <a name="selecting-a-target"></a><span data-ttu-id="5b211-155">Auswählen eines Ziels</span><span class="sxs-lookup"><span data-stu-id="5b211-155">Selecting a target</span></span>

<span data-ttu-id="5b211-156">Der folgende Code zeigt, wie Sie die [**2 dimensionale Direct3D-Textur**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) für den Fenster Hintergrund Puffer erhalten und ein bitmapziel erstellen, das mit dieser Textur verknüpft ist, mit der der [**Direct2D-Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="5b211-156">The code here shows you how to get the [**2 dimensional Direct3D texture**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) for the window back buffer and create a bitmap target that links to this texture to which the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) renders.</span></span>


```C++
        // Allocate a descriptor.
        DXGI_SWAP_CHAIN_DESC1 swapChainDesc = {0};
        swapChainDesc.Width = 0;                           // use automatic sizing
        swapChainDesc.Height = 0;
        swapChainDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM; // this is the most common swapchain format
        swapChainDesc.Stereo = false; 
        swapChainDesc.SampleDesc.Count = 1;                // don't use multi-sampling
        swapChainDesc.SampleDesc.Quality = 0;
        swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapChainDesc.BufferCount = 2;                     // use double buffering to enable flip
        swapChainDesc.Scaling = DXGI_SCALING_NONE;
        swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL; // all apps must use this SwapEffect
        swapChainDesc.Flags = 0;

        // Identify the physical adapter (GPU or card) this device is runs on.
        ComPtr<IDXGIAdapter> dxgiAdapter;
        DX::ThrowIfFailed(
            dxgiDevice->GetAdapter(&dxgiAdapter)
            );

        // Get the factory object that created the DXGI device.
        ComPtr<IDXGIFactory2> dxgiFactory;
        DX::ThrowIfFailed(
            dxgiAdapter->GetParent(IID_PPV_ARGS(&dxgiFactory))
            );

        // Get the final swap chain for this window from the DXGI factory.
        DX::ThrowIfFailed(
            dxgiFactory->CreateSwapChainForCoreWindow(
                device.Get(),
                reinterpret_cast<IUnknown*>(m_window),
                &swapChainDesc,
                nullptr,    // allow on all displays
                &m_swapChain
                )
            );

        // Ensure that DXGI doesn't queue more than one frame at a time.
        DX::ThrowIfFailed(
            dxgiDevice->SetMaximumFrameLatency(1)
            );

    // Get the backbuffer for this window which is be the final 3D render target.
    ComPtr<ID3D11Texture2D> backBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&backBuffer))
        );

    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it is directly rendered to the 
    // swap chain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_IGNORE),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // Now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



<span data-ttu-id="5b211-157">Gehen wir die Schritte im vorangehenden Codebeispiel durch.</span><span class="sxs-lookup"><span data-stu-id="5b211-157">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="5b211-158">Zuordnen einer [**DXGI \_ - \_ SwapChain \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) -Struktur und Definieren der Einstellungen für die Swapkette. [](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)</span><span class="sxs-lookup"><span data-stu-id="5b211-158">Allocate a [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and define the settings for the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

    <span data-ttu-id="5b211-159">Diese Einstellungen zeigen ein Beispiel für das Erstellen einer Austausch Kette, die von einer Windows Store-App verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5b211-159">These settings show an example of how to create a swap chain that a Windows Store app can use.</span></span>

2.  <span data-ttu-id="5b211-160">Holen Sie den Adapter, auf dem das [**Direct3D-Gerät**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) und das [**DXGI-Gerät**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) ausgeführt werden, und erhalten Sie das [**idxgifactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5b211-160">Get the adapter that the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) are running on and get the [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) object associated with them.</span></span> <span data-ttu-id="5b211-161">Sie müssen diese **DXGI-Factory** verwenden, um sicherzustellen, dass die SwapChain auf dem gleichen Adapter erstellt wird. [](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)</span><span class="sxs-lookup"><span data-stu-id="5b211-161">You must use this **DXGI factory** to ensure the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) is created on the same adapter.</span></span>

3.  <span data-ttu-id="5b211-162">Rufen Sie die [**IDXGIFactory2:: kreateswapchainforcorewindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) -Methode auf, um die Swapkette zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b211-162">Call the [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) method to create the swap chain.</span></span> <span data-ttu-id="5b211-163">Verwenden Sie die [**Windows:: UI:: corewindow**](/uwp/api/Windows.UI.Core.CoreWindow) -Klasse für das Hauptfenster einer Windows Store-App.</span><span class="sxs-lookup"><span data-stu-id="5b211-163">Use the [**Windows::UI::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) class for the main window of a Windows Store app.</span></span>

    <span data-ttu-id="5b211-164">Stellen Sie sicher, dass die maximale Frame Latenz auf 1 festgelegt ist, um den Energieverbrauch zu minimieren</span><span class="sxs-lookup"><span data-stu-id="5b211-164">Make sure to set the maximum frame latency to 1 to minimize power consumption.</span></span>

    <span data-ttu-id="5b211-165">Wenn Sie Direct2D-Inhalt in einer Windows Store-App Rendering möchten, finden Sie weitere Informationen unter der Methode " [**kreateswapchainforcomposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) ".</span><span class="sxs-lookup"><span data-stu-id="5b211-165">If you want to render Direct2D content in a Windows Store app, see the [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method.</span></span>

4.  <span data-ttu-id="5b211-166">Den Hintergrund Puffer aus der [**Swapkette**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)erhalten.</span><span class="sxs-lookup"><span data-stu-id="5b211-166">Get the back buffer from the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span> <span data-ttu-id="5b211-167">Der Hintergrund Puffer macht eine von der **austauschkette** zugeordnete [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5b211-167">The back buffer exposes an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) interface allocated by the **swap chain**</span></span>

5.  <span data-ttu-id="5b211-168">Deklarieren Sie eine [**D2D1 \_ Bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) -Struktur und legen Sie die Eigenschaftswerte fest.</span><span class="sxs-lookup"><span data-stu-id="5b211-168">Declare a [**D2D1\_BITMAP\_PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct and set the property values.</span></span> <span data-ttu-id="5b211-169">Legen Sie das Pixel Format auf BGRA fest, da dies das Format ist, das vom [**Direct3D-Gerät**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) und vom [**DXGI-Gerät**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5b211-169">Set the pixel format to BGRA because this is the format the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) use.</span></span>

6.  <span data-ttu-id="5b211-170">Gibt den Hintergrund Puffer als [**idxgisurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) an, der an Direct2D übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b211-170">Get the back buffer as an [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) to pass to Direct2D.</span></span> <span data-ttu-id="5b211-171">Direct2D akzeptiert [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) nicht direkt.</span><span class="sxs-lookup"><span data-stu-id="5b211-171">Direct2D doesn't accept an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) directly.</span></span>

    <span data-ttu-id="5b211-172">Erstellen Sie ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Objekt aus dem Hintergrund Puffer mithilfe der [**ID2D1DeviceContext:: deatebitmapfromdxgisurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5b211-172">Create a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object from the back buffer using the [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method.</span></span>

7.  <span data-ttu-id="5b211-173">Nun ist die [**Direct2D-Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit dem Hintergrund Puffer verknüpft.</span><span class="sxs-lookup"><span data-stu-id="5b211-173">Now the [**Direct2D bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is linked to the back buffer.</span></span> <span data-ttu-id="5b211-174">Legen Sie das Ziel für den [**Direct2D-Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) auf die **Bitmap** fest.</span><span class="sxs-lookup"><span data-stu-id="5b211-174">Set the target on the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to the **bitmap**.</span></span>

## <a name="how-to-render-and-display"></a><span data-ttu-id="5b211-175">Rendering und Anzeige</span><span class="sxs-lookup"><span data-stu-id="5b211-175">How to render and display</span></span>

<span data-ttu-id="5b211-176">Nachdem Sie nun über eine Zielbitmap verfügen, können Sie mithilfe des [**Direct2D-Geräte Kontexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)primitive, Bilder, Bildeffekte und Text zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5b211-176">Now that you have a target bitmap, you can draw primitives, images, image effects, and text to it using the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span> <span data-ttu-id="5b211-177">Der folgende Code zeigt, wie Sie ein Rechteck zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5b211-177">The code here shows you how to draw a rectangle.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);

m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



<span data-ttu-id="5b211-178">Gehen wir die Schritte im vorangehenden Codebeispiel durch.</span><span class="sxs-lookup"><span data-stu-id="5b211-178">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="5b211-179">Rufen Sie den Befehl " [**kreatesolidcolorbrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) " auf, um einen Pinsel zum Zeichnen des Rechtecks erstellen</span><span class="sxs-lookup"><span data-stu-id="5b211-179">Call the [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) to create a brush to paint the rectangle.</span></span>
2.  <span data-ttu-id="5b211-180">Aufrufen der [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode vor dem Ausgeben von Zeichnungs Befehlen.</span><span class="sxs-lookup"><span data-stu-id="5b211-180">Call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands.</span></span>
3.  <span data-ttu-id="5b211-181">Ruft die [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) -Methode das Rechteck ab, das gezeichnet werden soll, und den Pinsel.</span><span class="sxs-lookup"><span data-stu-id="5b211-181">Call the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method the rectangle to be drawn and the brush.</span></span>
4.  <span data-ttu-id="5b211-182">Aufrufen der [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode nach Abschluss der Ausgabe von Zeichnungs Befehlen.</span><span class="sxs-lookup"><span data-stu-id="5b211-182">Call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span>
5.  <span data-ttu-id="5b211-183">Zeigen Sie das Ergebnis an, indem Sie die [**idxgiswapchain::P Resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5b211-183">Display the result by calling the [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method.</span></span>

<span data-ttu-id="5b211-184">Nun können Sie den [**Direct2D-Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) zeichnen Primitives, Bilder, Bildeffekte und Text auf dem Bildschirm verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b211-184">Now you can use the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) draw primitives, images, image effects, and text to the screen.</span></span>

 

 
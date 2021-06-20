---
title: Windows Touch Scratchpad mithilfe des Echtzeit-Tablettstiftbeispiels (C++)
description: Sehen Sie sich Windows Touch Scratchpad C++-Beispiel (MTScratchpadRTStylus) an, das zeigt, wie sie Windows Touch-Nachrichten verwenden, um Ablaufverfolgungen der Berührungspunkte in ein Fenster zu zeichnen.
ms.assetid: c72ddc71-48b7-4c26-af2b-10919038eaf8
keywords:
- Windows Touch,Codebeispiele
- Windows Touch,Beispielcode
- Windows Touch,Scratchpad-Beispiele
- Scratchpad-Beispiele
- Windows Touch RTS-Objekt (Real-Time Stylus)
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 42e32e66942f3dcfad11b8b777e846e0cee6c0b3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406293"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="d044e-108">Windows Touch Scratchpad mithilfe des Echtzeit-Tablettstiftbeispiels (C++)</span><span class="sxs-lookup"><span data-stu-id="d044e-108">Windows Touch Scratchpad using the Real-time Stylus Sample (C++)</span></span>

<span data-ttu-id="d044e-109">Das Windows Touch Scratchpad-Beispiel ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) zeigt, wie Sie Windows Touch-Nachrichten verwenden, um Ablaufverfolgungen der Berührungspunkte in ein Fenster zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d044e-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="d044e-110">Die Ablaufverfolgung des primären Fingers, der zuerst auf den Digitizer gezogen wurde, wird schwarz gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d044e-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="d044e-111">Sekundäre Finger werden in sechs weiteren Farben gezeichnet: Rot, Grün, Blau, Zyan, Magenta und Gelb.</span><span class="sxs-lookup"><span data-stu-id="d044e-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta, and yellow.</span></span> <span data-ttu-id="d044e-112">Der folgende Screenshot zeigt, wie die Anwendung während der Ausführung aussehen könnte.</span><span class="sxs-lookup"><span data-stu-id="d044e-112">The following screen shot shows how the application could look while running.</span></span>

![Screenshot des Beispiels "Windows Touch Scratchpad" mithilfe des Echtzeit-Tablettstifts mit einer grünen, roten, drei schwarzen und blauen Linie auf dem Bildschirm](images/mtscratchpadrtstylus.png)

<span data-ttu-id="d044e-114">Für dieses Beispiel wird das RTS-Objekt (Real-Time Stylus) erstellt, und die Unterstützung für mehrere Kontaktpunkte ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d044e-114">For this sample, the Real-time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="d044e-115">Dem RTS wird ein DynamicRenderer-Plug-In hinzugefügt, um Inhalt zu rendern.</span><span class="sxs-lookup"><span data-stu-id="d044e-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="d044e-116">Ein Plug-In, **CSyncEventHandlerRTS,** wird implementiert, um die Anzahl der Finger zu verfolgen und die Farbe zu ändern, die der dynamische Renderer zeichnen soll.</span><span class="sxs-lookup"><span data-stu-id="d044e-116">A plug-in, **CSyncEventHandlerRTS**, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="d044e-117">Bei beiden Plug-Ins im RTS-Plug-In-Stapel rendert die Windows Touch Scratchpad-Anwendung den primären Kontakt schwarz und die restlichen Kontakte in den verschiedenen Farben.</span><span class="sxs-lookup"><span data-stu-id="d044e-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="d044e-118">Der folgende Code zeigt, wie das RTS-Objekt mit Unterstützung für mehrere Kontaktpunkte erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d044e-118">The following code shows how the RTS object is created with support for multiple contact points.</span></span>

```C++
IRealTimeStylus* CreateRealTimeStylus(HWND hWnd)
{
    // Check input argument
    if (hWnd == NULL)
    {
        ASSERT(hWnd && L"CreateRealTimeStylus: invalid argument hWnd");
        return NULL;
    }

    // Create RTS object
    IRealTimeStylus* pRealTimeStylus = NULL;
    HRESULT hr = CoCreateInstance(CLSID_RealTimeStylus, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pRealTimeStylus));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to CoCreateInstance of RealTimeStylus");
        return NULL;
    }

    // Attach RTS object to a window
    hr = pRealTimeStylus->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to set window handle");
        pRealTimeStylus->Release();
        return NULL;
    }

    // Register RTS object for receiving multi-touch input.
    IRealTimeStylus3* pRealTimeStylus3 = NULL;
    hr = pRealTimeStylus->QueryInterface(&pRealTimeStylus3);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: cannot access IRealTimeStylus3");
        pRealTimeStylus->Release();
        return NULL;
    }
    hr = pRealTimeStylus3->put_MultiTouchEnabled(TRUE);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to enable multi-touch");
        pRealTimeStylus->Release();
        pRealTimeStylus3->Release();
        return NULL;
    }
    pRealTimeStylus3->Release();

    return pRealTimeStylus;
}
```

<span data-ttu-id="d044e-119">Der folgende Code zeigt, wie das Dynamische Renderer-Plug-In erstellt und dem RTS hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d044e-119">The following code shows how the dynamic renderer plug-in is created and added to the RTS.</span></span>

```C++
IDynamicRenderer* CreateDynamicRenderer(IRealTimeStylus* pRealTimeStylus)
{
    // Check input argument
    if (pRealTimeStylus == NULL)
    {
        ASSERT(pRealTimeStylus && L"CreateDynamicRenderer: invalid argument RealTimeStylus");
        return NULL;
    }

    // Get window handle from RTS object
    HWND hWnd = NULL;
    HRESULT hr = pRealTimeStylus->get_HWND((HANDLE_PTR*)&hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to get window handle");
        return NULL;
    }

    // Create DynamicRenderer object
    IDynamicRenderer* pDynamicRenderer = NULL;
    hr = CoCreateInstance(CLSID_DynamicRenderer, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pDynamicRenderer));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to CoCreateInstance of DynamicRenderer");
        return NULL;
    }

    // Add DynamicRenderer to the RTS object as a synchronous plugin
    IStylusSyncPlugin* pSyncDynamicRenderer = NULL;
    hr = pDynamicRenderer->QueryInterface(&pSyncDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to access IStylusSyncPlugin of DynamicRenderer");
        pDynamicRenderer->Release();
        return NULL;
    }

    hr = pRealTimeStylus->AddStylusSyncPlugin(
        0,                      // insert plugin at position 0 in the sync plugin list
        pSyncDynamicRenderer);  // plugin to be inserted - DynamicRenderer
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to add DynamicRenderer to the RealTimeStylus plugins");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    // Attach DynamicRenderer to the same window RTS object is attached to
    hr = pDynamicRenderer->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to set window handle");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    pSyncDynamicRenderer->Release();

    return pDynamicRenderer;
}
```

<span data-ttu-id="d044e-120">Der folgende Code ändert die Stiftstrichfarbe für den **StylusDown-Ereignishandler** im **CSyncEventHandlerRTS,** einem benutzerdefinierten RTS-Plug-In.</span><span class="sxs-lookup"><span data-stu-id="d044e-120">The following code changes the stylus stroke color for the **StylusDown** event handler in the **CSyncEventHandlerRTS**, a custom RTS plug-in.</span></span>

```C++
HRESULT CSyncEventHandlerRTS::StylusDown(
    IRealTimeStylus* /* piRtsSrc */,
    const StylusInfo* /* pStylusInfo */,
    ULONG /* cPropCountPerPkt */,
    LONG* /* pPacket */,
    LONG** /* ppInOutPkt */)
{
    // Get DrawingAttributes of DynamicRenderer
    IInkDrawingAttributes* pDrawingAttributesDynamicRenderer;
    HRESULT hr = g_pDynamicRenderer->get_DrawingAttributes(&pDrawingAttributesDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to get RTS's drawing attributes");
        return hr;
    }

    // Set new stroke color to the DrawingAttributes of the DynamicRenderer
    // If there are no fingers down, this is a primary contact
    hr = pDrawingAttributesDynamicRenderer->put_Color(GetTouchColor(m_nContacts == 0));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to set color");
        pDrawingAttributesDynamicRenderer->Release();
        return hr;
    }

    pDrawingAttributesDynamicRenderer->Release();

    ++m_nContacts;  // Increment finger-down counter

    return S_OK;
}
```

<span data-ttu-id="d044e-121">Wenn der *m_nContacts* erhöht wird, ändert er die im dynamischen Renderer festgelegte Farbe.</span><span class="sxs-lookup"><span data-stu-id="d044e-121">When the *m_nContacts* value is incremented, it will change the color set in the dynamic renderer.</span></span> <span data-ttu-id="d044e-122">Striche, die nicht der primäre Kontakt sind, werden mit unterschiedlichen Farben gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d044e-122">Strokes that are not the primary contact will be drawn with different colors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d044e-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d044e-123">Related topics</span></span>

<span data-ttu-id="d044e-124">[Scratchpad-Multi-Touch-Anwendung (RTS/C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS) [Multi-Touch Scratchpad-Anwendung (RTS/C++),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp) [Windows Touch Beispiele](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="d044e-124">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>

---
title: Windows touchscratchpad mit dem Beispiel für echt Zeit Stift (C++)
description: Das Windows touchscratchpad-Beispiel (mtscratchpadrtstylus) zeigt, wie Sie Windows-touchnachrichten verwenden, um Ablauf Verfolgungen der touchpunkte zu einem Fenster zu zeichnen.
ms.assetid: c72ddc71-48b7-4c26-af2b-10919038eaf8
keywords:
- Windows-Fingereingabe, Codebeispiele
- Windows-Fingereingabe, Beispielcode
- Windows Toucheingabe, Scratchpad-Beispiele
- Scratchpad-Beispiele
- Windows-Fingereingabe, RTS-Objekt (Echt Zeit Stift)
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 94d425bcb39dd35d3bd71636fb19b6b408af9477
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341703"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Windows touchscratchpad mit dem Beispiel für echt Zeit Stift (C++)

Das Windows touchscratchpad-Beispiel ([mtscratchpadrtstylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) zeigt, wie Sie Windows-touchnachrichten verwenden, um Ablauf Verfolgungen der touchpunkte zu einem Fenster zu zeichnen. Die Ablauf Verfolgung des primären Fingers, die zuerst auf dem Digitalisierer abgelegt wurde, wird schwarz gezeichnet. Sekundäre Finger werden in sechs anderen Farben gezeichnet: rot, grün, blau, Cyan, Magenta und gelb. Der folgende Screenshot zeigt, wie die Anwendung während der Ausführung aussehen könnte.

![Screenshot mit dem Windows touchscratchpad-Beispiel mit dem Echt Zeit Stift, mit einem grünen, roten, drei schwarzen und einer blauen Linie auf dem Bildschirm](images/mtscratchpadrtstylus.png)

In diesem Beispiel wird das Objekt des Echt Zeit Tablettstifts (RTS) erstellt, und die Unterstützung für mehrere Kontaktpunkte ist aktiviert. Dem RTS wird ein DynamicRenderer-Plug-in hinzugefügt, um Inhalt zu Renderern. Ein Plug-in, **csynceventhandlerrts**, wird implementiert, um die Anzahl der Finger zu verfolgen und die Farbe zu ändern, die der dynamische Renderer zeichnet. Mit beiden Plug-ins im RTS-Plug-in-Stapel wird der primäre Kontakt von der Windows touchscratchpad-Anwendung in schwarz und den restlichen Kontakten in den verschiedenen Farben dargestellt.

Der folgende Code zeigt, wie das RTS-Objekt mit Unterstützung für mehrere Kontaktpunkte erstellt wird.

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

Der folgende Code zeigt, wie das Plug-in für dynamische Renderer erstellt und dem RTS hinzugefügt wird.

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

Der folgende Code ändert die tablettstiftfarbe für den **StylusDown** -Ereignishandler im **csynceventhandlerrts**, einem benutzerdefinierten RTS-Plug-in.

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

Wenn der *m_nContacts* Wert inkrementiert wird, wird der Farbsatz im dynamischen Renderer geändert. Striche, die nicht der primäre Kontakt sind, werden mit unterschiedlichen Farben gezeichnet.

## <a name="related-topics"></a>Zugehörige Themen

[Multitouch Scratchpad-Anwendung (RTS/c#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multitouch Scratchpad-Anwendung (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch-Beispiele](windows-touch-samples.md)

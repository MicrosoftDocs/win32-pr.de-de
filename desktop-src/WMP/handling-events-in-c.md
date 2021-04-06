---
title: Behandeln von Ereignissen in C++
description: Behandeln von Ereignissen in C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Windows Media Player, C++
- Windows Media Player-Objektmodell, C++
- Objektmodell, C++
- Windows Media Player Mobile, C++
- Windows Media Player ActiveX-Steuerelement, C++
- Windows Media Player Mobile ActiveX-Steuerelement, C++
- ActiveX-Steuerelement, C++
- C++-Programm Einbettung
- einbetten, C++-Programme
- Windows Media Player ActiveX-Steuerelement, Ereignis Behandlung
- Windows Media Player Mobile ActiveX-Steuerelement, Ereignis Behandlung
- ActiveX-Steuerelement, Ereignis Behandlung
- Ereignisse, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cbef547ab2604244c5c204707a08eb87a6b70a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100746"
---
# <a name="handling-events-in-c"></a><span data-ttu-id="691ad-116">Behandeln von Ereignissen in C++</span><span class="sxs-lookup"><span data-stu-id="691ad-116">Handling Events in C++</span></span>

<span data-ttu-id="691ad-117">Sie können Ereignisse von Windows Media Player auf zweierlei Weise empfangen.</span><span class="sxs-lookup"><span data-stu-id="691ad-117">You can receive events from Windows Media Player in two ways.</span></span>

-   <span data-ttu-id="691ad-118">Über **IDispatch** mithilfe der **\_ wmpocxevents** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="691ad-118">Through **IDispatch** by using the **\_WMPOCXEvents** interface.</span></span> <span data-ttu-id="691ad-119">Dies ist die Schnittstelle, die für die meisten Einbettungs Szenarien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="691ad-119">This is the interface to use for most embedding scenarios.</span></span>
-   <span data-ttu-id="691ad-120">Über die **iwmpevents** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="691ad-120">Through the **IWMPEvents** interface.</span></span> <span data-ttu-id="691ad-121">Diese Schnittstelle ist verfügbar, wenn Ihr Code mit dem vollmodusplayer verbunden ist, z. b. beim Remoting des Windows Media Player-Steuer Elements oder eines UI-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="691ad-121">This interface is available when your code is connected to the full mode Player, such as when remoting the Windows Media Player control or in a UI plug-in.</span></span>

<span data-ttu-id="691ad-122">In jedem Szenario beginnen Sie mit dem lauschen an Ereignissen mithilfe von com-Verbindungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="691ad-122">In each scenario, you start listening to events by using COM connection points.</span></span>

<span data-ttu-id="691ad-123">Der folgende Beispielcode verwendet drei Element Variablen:</span><span class="sxs-lookup"><span data-stu-id="691ad-123">The following example code uses three member variables:</span></span>


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



<span data-ttu-id="691ad-124">Zum Abrufen eines Verbindungs Punkts müssen Sie zuerst **QueryInterface** für den Verbindungspunkt Container durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="691ad-124">To retrieve a connection point, you first **QueryInterface** for the connection point container.</span></span>


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



<span data-ttu-id="691ad-125">Fordern Sie als nächstes den Verbindungspunkt für die Ereignis Schnittstelle an, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="691ad-125">Next, request the connection point for the event interface you want to use.</span></span> <span data-ttu-id="691ad-126">Der folgende Beispielcode versucht zunächst, **iwmpevents** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="691ad-126">The following example code first attempts to use **IWMPEvents**.</span></span> <span data-ttu-id="691ad-127">Wenn diese Schnittstelle nicht verfügbar ist, verwendet Sie **\_ wmpocxevents**.</span><span class="sxs-lookup"><span data-stu-id="691ad-127">If that interface isn't available, it uses **\_WMPOCXEvents**.</span></span>


```C++
// Test whether the control supports the IWMPEvents interface.
if(SUCCEEDED(hr))
{
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(IWMPEvents), &m_spConnectionPoint);
    if (FAILED(hr))
    {
        // If not, try the _WMPOCXEvents interface, which uses IDispatch.
        hr = spConnectionContainer->FindConnectionPoint(__uuidof(_WMPOCXEvents), &m_spConnectionPoint);
    }
}

```



<span data-ttu-id="691ad-128">Zum Schluss wird **IConnectionPoint:: Empfehlung** aufgerufen, um Ereignisse anzufordern.</span><span class="sxs-lookup"><span data-stu-id="691ad-128">Finally, call **IConnectionPoint::Advise** to request events.</span></span>


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



<span data-ttu-id="691ad-129">Im vorherigen Beispiel geht der erste Parameter davon aus, dass die aufrufende Klasse sowohl **iwmpevents** als auch **\_ wmpocxevents** implementiert.</span><span class="sxs-lookup"><span data-stu-id="691ad-129">In the preceding example, the first parameter assumes that the calling class implements both **IWMPEvents** and **\_WMPOCXEvents**.</span></span> <span data-ttu-id="691ad-130">Der zweite Parameter ist ein Rückgabewert, den Sie verwenden, um das Lauschen auf Ereignisse zu beenden, z. b. wenn das Programm beendet wird, indem Sie Code wie den folgenden verwenden:</span><span class="sxs-lookup"><span data-stu-id="691ad-130">The second parameter is a return value that you use to stop listening to events, such as when your program exits, using code similar to the following:</span></span>


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



<span data-ttu-id="691ad-131">Das Implementieren von Ereignis Handlern für **iwmpevents** und **\_ wmpocxevents** ist unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="691ad-131">Implementing the event handlers for **IWMPEvents** and **\_WMPOCXEvents** differs.</span></span> <span data-ttu-id="691ad-132">Für **iwmpevents** müssen Sie eine Funktion implementieren, die jedes von der-Schnittstelle definierte Ereignis behandelt, auch wenn Sie nicht beabsichtigen, das-Ereignis zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="691ad-132">For **IWMPEvents**, you must implement a function to handle every event defined by the interface, even if you don't intend to use the event.</span></span>


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



<span data-ttu-id="691ad-133">Zum Implementieren von **\_ wmpocxevents** -Handlern müssen Sie **IDispatch:: Aufrufen** verwenden, bei dem es sich um eine Implementierung eines einzelnen Ereignis Handlers für alle Ereignisse handelt, die in der **IDispatch** -Schnittstelle auftreten.</span><span class="sxs-lookup"><span data-stu-id="691ad-133">To implement **\_WMPOCXEvents** handlers, you must use **IDispatch::Invoke**, which is a single event handler implementation for all the events happening on the **IDispatch** interface.</span></span> <span data-ttu-id="691ad-134">Dies bedeutet, dass Sie auswählen können, dass nur bestimmte Ereignisse behandelt und andere ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="691ad-134">This means that you can choose to handle only certain events and ignore others.</span></span> <span data-ttu-id="691ad-135">Der folgende Beispielcode zeigt einen **\_ wmpocxevents** -Handler, der den **Aufruf** verwendet, der nur die Ereignisse **OpenStateChange** und **PlayStateChange** behandelt:</span><span class="sxs-lookup"><span data-stu-id="691ad-135">The following example code shows a **\_WMPOCXEvents** handler, using **Invoke**, that handles only the **OpenStateChange** and **PlayStateChange** events:</span></span>


```C++
HRESULT CMyClass::Invoke(
    DISPID  dispIdMember,      
    REFIID  riid,              
    LCID  lcid,                
    WORD  wFlags,              
    DISPPARAMS FAR*  pDispParams,  
    VARIANT FAR*  pVarResult,  
    EXCEPINFO FAR*  pExcepInfo,  
    unsigned int FAR*  puArgErr )
{
    if (!pDispParams)
        return E_POINTER;

    if (pDispParams->cNamedArgs != 0)
        return DISP_E_NONAMEDARGS;

    HRESULT hr = DISP_E_MEMBERNOTFOUND;

    switch (dispIdMember)
    {
        case DISPID_WMPCOREEVENT_OPENSTATECHANGE:
            OpenStateChange(pDispParams->rgvarg[0].lVal /* NewState */ );
            break;

        case DISPID_WMPCOREEVENT_PLAYSTATECHANGE:
            PlayStateChange(pDispParams->rgvarg[0].lVal /* NewState */);
            break;

        // Other cases can handle additional events by using DISPIDs.
    }

    return( hr );
}

```



<span data-ttu-id="691ad-136">Im vorangehenden Beispielcode ruft jeder Fall einfach bis zum **iwmpevents** -Handler für das entsprechende-Ereignis auf.</span><span class="sxs-lookup"><span data-stu-id="691ad-136">In the preceding example code, each case simply calls through to the **IWMPEvents** handler for the corresponding event.</span></span> <span data-ttu-id="691ad-137">Wenn Ihr Code nur **\_ wmpocxevents** behandelt, können Sie einfach eine benutzerdefinierte Funktion oder das Ereignis nach der **Case** -Anweisung Inline verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="691ad-137">If your code only handles **\_WMPOCXEvents**, you can simply call a custom function or handle the event inline after the **case** statement.</span></span>

## <a name="receiving-events-from-windows-media-player-10-mobile"></a><span data-ttu-id="691ad-138">Empfangen von Ereignissen von Windows Media Player 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="691ad-138">Receiving Events from Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="691ad-139">Das Windows Media Player 10 Mobile-Steuerelement unterstützt nur das Empfangen bestimmter Ereignisse über **\_ wmpocxevents** und **iwmpevents**.</span><span class="sxs-lookup"><span data-stu-id="691ad-139">The Windows Media Player 10 Mobile control only supports receiving certain events through **\_WMPOCXEvents** and **IWMPEvents**.</span></span> <span data-ttu-id="691ad-140">Weitere Informationen finden Sie in der Dokumentation zu **iwmpevents**.</span><span class="sxs-lookup"><span data-stu-id="691ad-140">For more information, please see the documentation for **IWMPEvents**.</span></span>

## <a name="samples"></a><span data-ttu-id="691ad-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="691ad-141">Samples</span></span>

<span data-ttu-id="691ad-142">Das Windows Media Player Setup-Paket installiert ein Beispiel, das die Ereignis Behandlung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="691ad-142">The Windows Media Player setup package installs a sample that demonstrates event handling.</span></span> <span data-ttu-id="691ad-143">Weitere Informationen finden Sie im wmphost-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="691ad-143">See the WMPHost sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="691ad-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="691ad-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="691ad-145">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="691ad-145">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="691ad-146">**Verwenden des Windows Media Player-Steuer Elements in einem C++-Programm**</span><span class="sxs-lookup"><span data-stu-id="691ad-146">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 





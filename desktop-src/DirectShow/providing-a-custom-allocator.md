---
description: Bereitstellen einer benutzerdefinierten Zuweisung
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Bereitstellen einer benutzerdefinierten Zuweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e85a8d133ee5b686e25bc0d7d4a3e2444cb2791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392521"
---
# <a name="providing-a-custom-allocator"></a><span data-ttu-id="0705e-103">Bereitstellen einer benutzerdefinierten Zuweisung</span><span class="sxs-lookup"><span data-stu-id="0705e-103">Providing a Custom Allocator</span></span>

<span data-ttu-id="0705e-104">In diesem Abschnitt wird beschrieben, wie Sie einen benutzerdefinierten Zuweiser für einen Filter bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0705e-104">This section describes how to provide a custom allocator for a filter.</span></span> <span data-ttu-id="0705e-105">Es werden nur [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Verbindungen beschrieben, die Schritte für eine [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Verbindung sind jedoch ähnlich.</span><span class="sxs-lookup"><span data-stu-id="0705e-105">Only [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) connections are described, but the steps for an [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) connection are similar.</span></span>

<span data-ttu-id="0705e-106">Definieren Sie zuerst eine C++-Klasse für die Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="0705e-106">First, define a C++ class for the allocator.</span></span> <span data-ttu-id="0705e-107">Ihre Zuweisung kann von einer der standardzuordnerklassen, [**cbasezucator**](cbaseallocator.md) oder [**cmemzuordcator**](cmemallocator.md)abgeleitet werden, oder Sie können eine vollständig neue zuordnerklasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="0705e-107">Your allocator can derive from one of the standard allocator classes, [**CBaseAllocator**](cbaseallocator.md) or [**CMemAllocator**](cmemallocator.md), or you can create an entirely new allocator class.</span></span> <span data-ttu-id="0705e-108">Wenn Sie eine neue Klasse erstellen, muss Sie die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="0705e-108">If you create a new class, it must expose the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="0705e-109">Die verbleibenden Schritte hängen davon ab, ob ihre Zuweisung zu einer Eingabe-PIN oder einer Ausgabe-PIN in Ihrem Filter gehört.</span><span class="sxs-lookup"><span data-stu-id="0705e-109">The remaining steps depend on whether your allocator belongs to an input pin or an output pin on your filter.</span></span> <span data-ttu-id="0705e-110">Eingabe Pins spielen während der zuordneraushandlungs Phase eine andere Rolle als Ausgabe Pins, da die Ausgabepin letztendlich die Zuweisung auswählt.</span><span class="sxs-lookup"><span data-stu-id="0705e-110">Input pins play a different role than output pins during the allocator negotiation phase, because the output pin ultimately selects the allocator.</span></span>

<span data-ttu-id="0705e-111">**Bereitstellen einer benutzerdefinierten Zuweisung für eine Eingabe-PIN**</span><span class="sxs-lookup"><span data-stu-id="0705e-111">**Providing a Custom Allocator for an Input Pin**</span></span>

<span data-ttu-id="0705e-112">Um eine Zuweisung für eine Eingabe-PIN bereitzustellen, überschreiben Sie die [**cbaseinputpin:: getallocator**](cbaseinputpin-getallocator.md) -Methode der Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="0705e-112">To provide an allocator for an input pin, override the input pin's [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) method.</span></span> <span data-ttu-id="0705e-113">Überprüfen Sie in dieser Methode die **m \_ pallocator** -Member-Variable.</span><span class="sxs-lookup"><span data-stu-id="0705e-113">Within this method, check the **m\_pAllocator** member variable.</span></span> <span data-ttu-id="0705e-114">Wenn diese Variable nicht **null** ist, bedeutet dies, dass die Zuweisung bereits für diese Verbindung ausgewählt wurde. Daher muss die **getallocator** -Methode einen Zeiger auf diese Zuweisung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0705e-114">If this variable is non-**NULL**, it means the allocator has already been selected for this connection, so the **GetAllocator** method must return a pointer to that allocator.</span></span> <span data-ttu-id="0705e-115">Wenn **m \_ pallocator** **null** ist, bedeutet dies, dass die Zuweisung nicht ausgewählt wurde. Daher sollte die **getallocator** -Methode einen Zeiger auf die bevorzugte Zuweisung der Eingabe-PIN zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0705e-115">If **m\_pAllocator** is **NULL**, it means the allocator has not been selected, so the **GetAllocator** method should return a pointer to the input pin's preferred allocator.</span></span> <span data-ttu-id="0705e-116">Erstellen Sie in diesem Fall eine Instanz Ihrer benutzerdefinierten Zuweisung, und geben Sie den [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="0705e-116">In that case, create an instance of your custom allocator and return its [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) pointer.</span></span> <span data-ttu-id="0705e-117">Der folgende Code zeigt, wie die **getallocator** -Methode implementiert wird:</span><span class="sxs-lookup"><span data-stu-id="0705e-117">The following code shows how to implement the **GetAllocator** method:</span></span>


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="0705e-118">Wenn der upstreamfilter eine Zuweisung auswählt, ruft er die [**IMemInputPin:: notifyzuweisung**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) -Methode der Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="0705e-118">When the upstream filter selects an allocator, it calls the input pin's [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span> <span data-ttu-id="0705e-119">Überschreiben Sie die [**cbaseinputpin:: notifyzuweisung**](cbaseinputpin-notifyallocator.md) -Methode, um die zuordnereigenschaften zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0705e-119">Override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method to check the allocator properties.</span></span> <span data-ttu-id="0705e-120">In einigen Fällen kann die Eingabe-PIN die Zuweisung ablehnen, wenn Sie nicht Ihre benutzerdefinierte Zuweisung ist, obwohl dies dazu führen kann, dass die gesamte Pin-Verbindung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0705e-120">In some cases, the input pin might reject the allocator if it is not your custom allocator, although this may cause the entire pin connection to fail.</span></span>

<span data-ttu-id="0705e-121">**Bereitstellen einer benutzerdefinierten Zuweisung für eine Ausgabepin**</span><span class="sxs-lookup"><span data-stu-id="0705e-121">**Providing a Custom Allocator for an Output Pin**</span></span>

<span data-ttu-id="0705e-122">Zum Bereitstellen einer Zuweisung für eine Ausgabepin überschreiben Sie die [**cbaseoutputpin:: initaccesscator**](cbaseoutputpin-initallocator.md) -Methode, um eine Instanz Ihrer Zuweisung zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="0705e-122">To provide an allocator for an output pin, override the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) method to create an instance of your allocator:</span></span>


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="0705e-123">Standardmäßig fordert die [**cbaseoutputpin**](cbaseoutputpin.md) -Klasse zuerst einen Zuweiser von der eingabepin an.</span><span class="sxs-lookup"><span data-stu-id="0705e-123">By default, the [**CBaseOutputPin**](cbaseoutputpin.md) class requests an allocator from the input pin first.</span></span> <span data-ttu-id="0705e-124">Wenn diese Zuweisung nicht geeignet ist, erstellt die Ausgabe-PIN eine eigene Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="0705e-124">If that allocator is not suitable, the output pin creates its own allocator.</span></span> <span data-ttu-id="0705e-125">Um die Verbindung mit der benutzerdefinierten Zuweisung zu erzwingen, überschreiben Sie die [**cbaseoutputpin::D ecidezuordcator**](cbaseoutputpin-decideallocator.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0705e-125">To force the connection to use your custom allocator, override the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method.</span></span> <span data-ttu-id="0705e-126">Beachten Sie jedoch, dass dadurch verhindert werden kann, dass Ihre Ausgabe-PIN eine Verbindung mit bestimmten Filtern herstellt, da der andere Filter möglicherweise auch eine eigene benutzerdefinierte Zuweisung erfordert.</span><span class="sxs-lookup"><span data-stu-id="0705e-126">However, be aware that this can prevent your output pin from connecting with certain filters, because the other filter may also require its own custom allocator.</span></span> <span data-ttu-id="0705e-127">Eine dritte Möglichkeit besteht darin, die Reihenfolge zu ändern: Testen Sie zuerst die benutzerdefinierte Zuweisung, und greifen Sie dann auf die Zuweisung des anderen Filters zurück.</span><span class="sxs-lookup"><span data-stu-id="0705e-127">A third option is to switch the order: Try your custom allocator first, and then fall back to the other filter's allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0705e-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0705e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0705e-129">Aushandeln von Zuweisungen</span><span class="sxs-lookup"><span data-stu-id="0705e-129">Negotiating Allocators</span></span>](negotiating-allocators.md)
</dt> </dl>

 

 




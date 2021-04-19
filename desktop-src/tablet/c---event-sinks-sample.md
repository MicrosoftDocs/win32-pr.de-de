---
description: Dieses Programm veranschaulicht, wie Sie eine Anwendung erstellen können, die InkCollector-Ereignisse nur mit C++ aufzeichnet. Dieses Programm erstellt ein InkCollector-Objekt, um das Fenster frei zu aktivieren. Es wird immer dann ein Meldungs Feld angezeigt, wenn ein Stroke-Ereignis empfangen wird.
ms.assetid: 91450559-ae47-457a-a709-b4e4e78bde22
title: C++ Event senken-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e950254293b676088d8b281624c089b098e5dca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346463"
---
# <a name="c-event-sinks-sample"></a><span data-ttu-id="ee7bd-105">C++ Event senken-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ee7bd-105">C++ Event Sinks Sample</span></span>

<span data-ttu-id="ee7bd-106">Dieses Programm veranschaulicht, wie Sie eine Anwendung erstellen können, die InkCollector-Ereignisse nur mit C++ aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-106">This program demonstrates how you can build an application that captures InkCollector events using only C++.</span></span> <span data-ttu-id="ee7bd-107">Dieses Programm erstellt ein [**InkCollector**](inkcollector-class.md) -Objekt, um das Fenster frei zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-107">This program co-creates an [**InkCollector**](inkcollector-class.md) object to ink -enable the window.</span></span> <span data-ttu-id="ee7bd-108">Es wird immer dann ein Meldungs Feld angezeigt, wenn ein [**Stroke**](inkcollector-stroke.md) -Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-108">It displays a message box whenever a [**Stroke**](inkcollector-stroke.md) event is received.</span></span>

## <a name="defining-a-wrapper-for-ink-collector-events"></a><span data-ttu-id="ee7bd-109">Definieren eines Wrappers für frei Hand Sammler Ereignisse</span><span class="sxs-lookup"><span data-stu-id="ee7bd-109">Defining a Wrapper for Ink Collector Events</span></span>

<span data-ttu-id="ee7bd-110">Die- `InkCollectorEvents` Klasse verarbeitet die Übergabe von Ink Collector-Ereignissen vom Ink Collector an den Benutzer dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-110">The `InkCollectorEvents` Class handles passing ink collector events from the ink collector to the user of this class.</span></span> <span data-ttu-id="ee7bd-111">Die `AdviseInkCollector` -Methode richtet die Verbindung zwischen dem [**InkCollector**](inkcollector-class.md) -Objekt und dieser Klasse ein.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-111">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="ee7bd-112">Die- `Invoke` Methode konvertiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Ereignis Benachrichtigung in einen-Befehl für eine virtuelle Funktion, die der Benutzer dieser Klasse außer Kraft setzen kann, um ein bestimmtes Ereignis zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-112">The `Invoke` method converts the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) event notification into a call to a virtual function that the user of this class can override to process a particular event.</span></span>

> [!Note]  
> <span data-ttu-id="ee7bd-113">Sie müssen mehr als die virtuelle Funktion für einen Ereignishandler überschreiben, um dieses Ereignis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-113">You must do more than override the virtual function for an event handler to get that event.</span></span> <span data-ttu-id="ee7bd-114">Für alle außer Standard Ereignisse müssen Sie [**die Methode "**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) Methode" von Ink Collector aufrufen, um ein Ereignis zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-114">For all but default events, you have to call the ink collector's [**SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) method to guarantee getting an event.</span></span> <span data-ttu-id="ee7bd-115">Zweitens marshallte dieses Objekt selbst einen frei Hand Thread, sodass alle implementierten Ereignishandler ebenfalls frei Thread sein müssen.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-115">Secondly, this object marshals itself free threaded so all implemented event handlers need to be free threaded as well.</span></span> <span data-ttu-id="ee7bd-116">Besonders wichtig ist die Verwendung von Windows-APIs, die einen Wechsel zu einem anderen Thread verursachen können, da der Ereignishandler nicht sicher ist, dass er im gleichen Thread ausgeführt wird wie das Fenster, das mit dem Ink Collector verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-116">Of particular importance is using Windows APIs, which may cause a switch to another thread as the event handler is not guaranteed to be running on the same thread as the window connected with the ink collector.</span></span>

 


```C++
// Invoke translates from IDispatch to an event callout
//  that can be overriden by a subclass of this class.
STDMETHOD(Invoke)(
   DISPID dispidMember, 
    REFIID riid,
    LCID lcid, 
    WORD /*wFlags*/, 
    DISPPARAMS* pdispparams, 
    VARIANT* pvarResult,
    EXCEPINFO* /*pexcepinfo*/, 
    UINT* /*puArgErr*/)
{
    switch(dispidMember)
    {
        case DISPID_ICEStroke:
            Stroke(
                (IInkCursor*) pdispparams->rgvarg[2].pdispVal,
                (IInkStrokeDisp*) pdispparams->rgvarg[1].pdispVal,
                (VARIANT_BOOL *)pdispparams->rgvarg[0].pboolVal);
            break;
        ...
    }
    return S_OK;
}

virtual void Stroke(
    IInkCursor* Cursor,
    IInkStrokeDisp* Stroke,
    VARIANT_BOOL *Cancel)
{
    // This is a place holder designed to be overridden by
    //  user of this class.
    return;
}
...
```



<span data-ttu-id="ee7bd-117">Die- `Init` Methode ruft [cofroatefreethreadedmarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) auf, um einen kostenlosen Thread-Mars Haller einzurichten.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-117">The `Init` method calls [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) to set up a free threaded marshaler.</span></span>


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



<span data-ttu-id="ee7bd-118">Die `AdviseInkCollector` -Methode richtet die Verbindung zwischen dem [**InkCollector**](inkcollector-class.md) -Objekt und dieser Klasse ein.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-118">The `AdviseInkCollector` method sets up the connection between the [**InkCollector**](inkcollector-class.md) object and this class.</span></span> <span data-ttu-id="ee7bd-119">Zuerst wird ein Verbindungspunkt an den frei Hand Sammler abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-119">It first retrieves a connection point to the ink collector.</span></span> <span data-ttu-id="ee7bd-120">Anschließend wird ein Zeiger auf das-Element abgerufen `IInkCollectorEvents` , um eine Beratungs Verbindung mit dem Steuerelement herstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-120">Then it retrieves a pointer to the `IInkCollectorEvents` so that it may establish an advisory connection to the control.</span></span>


```C++
// Set up connection between sink and InkCollector
HRESULT AdviseInkCollector(
    IInkCollector *pIInkCollector)
{
    // Get the connection point container
    IConnectionPointContainer *pIConnectionPointContainer;
    HRESULT hr = pIInkCollector->QueryInterface(IID_IConnectionPointContainer, (void **) &pIConnectionPointContainer);
        
    if (FAILED(hr))
        ...
    
    // Find the connection point for Ink Collector events
    hr = pIConnectionPointContainer->FindConnectionPoint(__uuidof(_IInkCollectorEvents), &m_pIConnectionPoint);
        
    if (SUCCEEDED(hr))
    {
        // Hook up sink to connection point
        hr = m_pIConnectionPoint->Advise(this, &m_dwCookie);
    }
    
    if (FAILED(hr))
        ...
    
    // Don't need the connection point container any more.
    pIConnectionPointContainer->Release();
    return hr;
}
```



<span data-ttu-id="ee7bd-121">Die- `UnadviseInkCollector` Methode gibt die Verbindungen frei, die das-Objekt für das Steuerelement besitzt.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-121">The `UnadviseInkCollector` method releases the connections the object has to the control.</span></span>


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a><span data-ttu-id="ee7bd-122">Definieren eines Ink Collector-Ereignis Handlers</span><span class="sxs-lookup"><span data-stu-id="ee7bd-122">Defining an Ink Collector Events Handler</span></span>

<span data-ttu-id="ee7bd-123">Die cmyinkevents-Klasse überschreibt das Standardverhalten des [**Stroke**](inkcollector-stroke.md) -Ereignis Handlers der inkcollectorevents-Klasse.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-123">The CMyInkEvents Class overrides the default behavior of the [**Stroke**](inkcollector-stroke.md) event handler of the InkCollectorEvents Class.</span></span> <span data-ttu-id="ee7bd-124">Die Stroke-Methode zeigt ein Meldungs Feld an, wenn [**InkCollector**](inkcollector-class.md) ein **Stroke** -Ereignis empfängt.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-124">The Stroke method displays a message box when the [**InkCollector**](inkcollector-class.md) receives a **Stroke** event.</span></span>


```C++
class CMyInkEvents : public InkCollectorEvents
{
public:

    // Event: Stroke
    virtual void Stroke(
        IInkCursor* Cursor,
        IInkStrokeDisp* Stroke,
        VARIANT_BOOL *Cancel)
    {
        // Demonstrate that the event notification was received.
        MessageBox(m_hWnd, "Stroke Event", "Event Received", MB_OK);
    }
    
    CMyInkEvents()
    {
        m_hWnd = NULL;
    }
    
    HRESULT Init(
        HWND hWnd)
    {
        m_hWnd = hWnd;
        return InkCollectorEvents::Init();
    }    
    
    HWND m_hWnd;
};
```



## <a name="defining-an-ink-collector-wrapper"></a><span data-ttu-id="ee7bd-125">Definieren eines Ink Collector-Wrapper</span><span class="sxs-lookup"><span data-stu-id="ee7bd-125">Defining an Ink Collector Wrapper</span></span>

<span data-ttu-id="ee7bd-126">Die Init-Methode der cmyinkcollector-Klasse deklariert und initialisiert ein cmyinkevents-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-126">The CMyInkCollector Class's Init method declares and initializes a CMyInkEvents object.</span></span> <span data-ttu-id="ee7bd-127">Anschließend wird ein [**InkCollector**](inkcollector-class.md) -Objekt erstellt und der Ink Collector und der Ereignishandler zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-127">It then creates an [**InkCollector**](inkcollector-class.md) object and associates the ink collector and the event handler.</span></span> <span data-ttu-id="ee7bd-128">Schließlich wird der **InkCollector** an das Fenster angefügt und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-128">Finally, the **InkCollector** is attached to the window and enabled.</span></span>


```C++
// Handle all initializaton
HRESULT Init(
HWND hWnd)
{
    // Initialize event sink. This consists of setting
    //  up the free threaded marshaler.
    HRESULT hr = m_InkEvents.Init(hWnd);

    if (FAILED(hr))
        ...

    // Create the ink collector
    hr = CoCreateInstance(CLSID_InkCollector, NULL, CLSCTX_ALL, IID_IInkCollector, (void **) &m_pInkCollector);

    if (FAILED(hr))
        ...

    // Set up connection between Ink Collector and our event sink
    hr = m_InkEvents.AdviseInkCollector(m_pInkCollector);

    if (FAILED(hr))
        ...

    // Attach Ink Collector to window
    hr = m_pInkCollector->put_hWnd((long) hWnd);

    if (FAILED(hr))
        ...

    // Allow Ink Collector to receive input.
    return m_pInkCollector->put_Enabled(VARIANT_TRUE);
}
```



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a><span data-ttu-id="ee7bd-129">Zugreifen auf die Tablet PC-Schnittstellen und die Wrapper Klassen</span><span class="sxs-lookup"><span data-stu-id="ee7bd-129">Accessing the Tablet PC Interfaces and the Wrapper Classes</span></span>

<span data-ttu-id="ee7bd-130">Fügen Sie zunächst die Header für die Schnittstellen von Tablet PC Automation ein.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-130">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="ee7bd-131">Diese werden mit dem Microsoft <entity type="reg"/> Windows <entity type="reg"/> XP Tablet PC Edition Development Kit 1,7 installiert.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-131">These are installed with the Microsoft<entity type="reg"/> Windows<entity type="reg"/> XP Tablet PC Edition Development Kit 1.7.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="ee7bd-132">Fügen Sie dann die Header für die Wrapper Klassen und den Ereignishandler für [**InkCollector**](inkcollector-class.md) fest.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-132">Then, include the headers for the wrapper classes and [**InkCollector**](inkcollector-class.md) event handler was defined.</span></span>


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a><span data-ttu-id="ee7bd-133">Aufrufen der Wrapper Klassen</span><span class="sxs-lookup"><span data-stu-id="ee7bd-133">Calling the Wrapper Classes</span></span>

<span data-ttu-id="ee7bd-134">Wenn das Fenster erstellt wird, erstellt die Fenster Prozedur einen Ink Collector-Wrapper und initialisiert den Wrapper.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-134">When the window is created, the Window procedure creates an ink collector wrapper and initializes the wrapper.</span></span> <span data-ttu-id="ee7bd-135">Wenn das Fenster zerstört wird, löscht die Fenster Prozedur den Ink Collector-Wrapper.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-135">When the window is destroyed, the Window procedure deletes the ink collector wrapper.</span></span> <span data-ttu-id="ee7bd-136">Der Ink Collector-Wrapper übernimmt das Erstellen und Löschen des zugehörigen Ereignis Handlers.</span><span class="sxs-lookup"><span data-stu-id="ee7bd-136">The ink collector wrapper handles the creation and deletion of its associated event handler.</span></span>


```C++
case WM_CREATE:

    // Allocate and initialize memory for object
    pmic = new CMyInkCollector();

    if (pmic != NULL)
    {
        // Real initialization. This consists of creating
        //  an ink collector object and attaching it to
        //  the current window. 
        if (SUCCEEDED(pmic->Init(hWnd)))
        {
            return 0;
        }
        
        // Failure free resources.
        delete pmic;
        pmic = NULL;
    }
    
    return -1;
...
case WM_DESTROY:
    // The destructor for the object handles releasing the
    //  InkCollector and disconnecting the InkCollector
    //  from the object's event sink. 
    delete pmic;
    pmic = NULL;
    PostQuitMessage(0);
    break;
```



 

 

---
title: Hinzufügen von Manipulations Unterstützung in nicht verwaltetem Code
description: In diesem Abschnitt wird erläutert, wie Sie nicht verwaltetem Code Manipulations Unterstützung hinzufügen, indem Sie eine Ereignis Senke für die \_ imanipulationevents-Schnittstelle implementieren.
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Windows-Fingereingabe, Manipulationen
- Windows-Touchscreen, _IManipulationEvents-Schnittstelle
- Windows-Berührungs-, IManipulationProcessor-Schnittstelle
- Manipulationen, Hinzufügen von Unterstützung in nicht verwaltetem Code
- Manipulationen, Unterstützung von nicht verwaltetem Code
- Manipulationen, Unterstützung in nicht verwaltetem Code
- Manipulationen, _IManipulationEvents-Schnittstelle
- Manipulationen, IManipulationProcessor-Schnittstelle
- _IManipulationEvents-Schnittstelle, Manipulations Unterstützung in nicht verwaltetem Code
- IManipulationProcessor-Schnittstelle, Manipulations Unterstützung in nicht verwaltetem Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2e000b6d3518c4e90eb5ae03b581e81037edf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102070"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a><span data-ttu-id="4758d-113">Hinzufügen von Manipulations Unterstützung in nicht verwaltetem Code</span><span class="sxs-lookup"><span data-stu-id="4758d-113">Adding Manipulation Support in Unmanaged Code</span></span>

<span data-ttu-id="4758d-114">In diesem Abschnitt wird erläutert, wie Sie nicht verwaltetem Code Manipulations Unterstützung hinzufügen, indem Sie eine Ereignis Senke für die [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="4758d-114">This section explains how to add manipulation support to unmanaged code by implementing an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

<span data-ttu-id="4758d-115">In der folgenden Abbildung wird die Manipulations Architektur dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4758d-115">The following image outlines the manipulation architecture.</span></span>

![Darstellung von Windows-Finger Eingabenachrichten, die an den Manipulations Prozessor eines Objekts übermittelt werden, das Ereignisse mit der \- imanipulationevents-Schnittstelle behandelt](images/manipulation-arch.png)

<span data-ttu-id="4758d-117">Berührungs Daten, die von [**WM- \_**](wm-touchdown.md) Fingereingabe Nachrichten empfangen werden, werden in Verbindung mit der Kontakt-ID aus der Fingereingabe Nachricht an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4758d-117">Touch data that is received from [**WM\_TOUCH**](wm-touchdown.md) messages is passed to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) together with the contact ID from the touch message.</span></span> <span data-ttu-id="4758d-118">Basierend auf der Nachrichten Sequenz wird von der **IManipulationProcessor** -Schnittstelle berechnet, welche Art von Transformation ausgeführt wird und welche Werte dieser Transformation zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4758d-118">Based on the message sequence, the **IManipulationProcessor** interface will calculate what kind of transformation is being performed and what the values associated with this transformation are.</span></span> <span data-ttu-id="4758d-119">Der **IManipulationProcessor** generiert dann [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) , die von einer Ereignis Senke behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="4758d-119">The **IManipulationProcessor** will then generate [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) which are handled by an event sink.</span></span> <span data-ttu-id="4758d-120">Die Ereignis Senke kann diese Werte dann verwenden, um benutzerdefinierte Vorgänge für das Objekt auszuführen, das transformiert wird.</span><span class="sxs-lookup"><span data-stu-id="4758d-120">The event sink can then use these values to perform custom operations on the object being transformed.</span></span>

<span data-ttu-id="4758d-121">Sie müssen die folgenden Schritte ausführen, um der Anwendung Bearbeitungs Unterstützung hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="4758d-121">To add manipulation support to your application, you must follow these steps:</span></span>

1.  <span data-ttu-id="4758d-122">Implementieren Sie eine Ereignis Senke für die [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4758d-122">Implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>
2.  <span data-ttu-id="4758d-123">Erstellen Sie eine Instanz einer [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4758d-123">Create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>
3.  <span data-ttu-id="4758d-124">Erstellen Sie eine Instanz der Ereignis Senke, und richten Sie Berührungs Ereignisse ein.</span><span class="sxs-lookup"><span data-stu-id="4758d-124">Create an instance of your event sink and set up touch events.</span></span>
4.  <span data-ttu-id="4758d-125">Senden von Berührungs Ereignisdaten an den Manipulations Prozessor.</span><span class="sxs-lookup"><span data-stu-id="4758d-125">Send touch event data to the manipulation processor.</span></span>

<span data-ttu-id="4758d-126">In diesem Abschnitt werden die Schritte erläutert, die Sie befolgen müssen, um der Anwendung Bearbeitungs Unterstützung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4758d-126">This section explains the steps that you must follow to add manipulation support to your application.</span></span> <span data-ttu-id="4758d-127">In jedem Schritt wird Code bereitgestellt, um Ihnen den Einstieg zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="4758d-127">Code is provided at each step to get you started.</span></span>

> [!Note]  
> <span data-ttu-id="4758d-128">Manipulationen und Gesten können nicht gleichzeitig verwendet werden, da Gesten-und touchnachrichten sich gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="4758d-128">You cannot use manipulations and gestures at the same time because gesture and touch messages are mutually exclusive.</span></span>

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a><span data-ttu-id="4758d-129">Implementieren einer Ereignis Senke für die \_ IManipualtionEvents-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4758d-129">Implement an Event Sink for \_IManipualtionEvents Interface</span></span>

<span data-ttu-id="4758d-130">Bevor Sie eine Instanz der Ereignis Senke erstellen können, müssen Sie eine Klasse erstellen, die die [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle für Ereignisse implementiert.</span><span class="sxs-lookup"><span data-stu-id="4758d-130">Before you can create an instance of your event sink, you must create a class that implements the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface for eventing.</span></span> <span data-ttu-id="4758d-131">Dies ist die Ereignis Senke.</span><span class="sxs-lookup"><span data-stu-id="4758d-131">This is your event sink.</span></span> <span data-ttu-id="4758d-132">Ereignisse, die von der [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle generiert werden, werden von der Ereignis Senke behandelt.</span><span class="sxs-lookup"><span data-stu-id="4758d-132">Events generated by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface are handled by your event sink.</span></span> <span data-ttu-id="4758d-133">Der folgende Code zeigt einen Beispiel Header für eine Klasse, die die **\_ imanipulationevents** -Schnittstelle erbt.</span><span class="sxs-lookup"><span data-stu-id="4758d-133">The following code shows an example header for a class that inherits the **\_IManipulationEvents** interface.</span></span>

```C++
// Manipulation Header Files
#include <comdef.h>
#include <manipulations.h>
#include <ocidl.h>

class CManipulationEventSink : _IManipulationEvents
{
public:
    CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd);

    int GetStartedEventCount();
    int GetDeltaEventCount();
    int GetCompletedEventCount();
    double CManipulationEventSink::GetX();
    double CManipulationEventSink::GetY();        

    ~CManipulationEventSink();

    //////////////////////////////
    // IManipulationEvents methods
    //////////////////////////////
    virtual HRESULT STDMETHODCALLTYPE ManipulationStarted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationDelta( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y,
        /* [in] */ FLOAT translationDeltaX,
        /* [in] */ FLOAT translationDeltaY,
        /* [in] */ FLOAT scaleDelta,
        /* [in] */ FLOAT expansionDelta,
        /* [in] */ FLOAT rotationDelta,
        /* [in] */ FLOAT cumulativeTranslationX,
        /* [in] */ FLOAT cumulativeTranslationY,
        /* [in] */ FLOAT cumulativeScale,
        /* [in] */ FLOAT cumulativeExpansion,
        /* [in] */ FLOAT cumulativeRotation);
    
    virtual HRESULT STDMETHODCALLTYPE ManipulationCompleted( 
        /* [in] */ FLOAT x,
        /* [in] */ FLOAT y,
        /* [in] */ FLOAT cumulativeTranslationX,
        /* [in] */ FLOAT cumulativeTranslationY,
        /* [in] */ FLOAT cumulativeScale,
        /* [in] */ FLOAT cumulativeExpansion,
        /* [in] */ FLOAT cumulativeRotation);

    ////////////////////////////////////////////////////////////
    // IUnknown methods
    ////////////////////////////////////////////////////////////
    STDMETHOD_(ULONG, AddRef)(void);
    STDMETHOD_(ULONG, Release)(void);
    STDMETHOD(QueryInterface)(REFIID riid, LPVOID *ppvObj);

private:
    double m_fX;
    double m_fY;

    int m_cRefCount;
    int m_cStartedEventCount;
    int m_cDeltaEventCount;
    int m_cCompletedEventCount;

    IManipulationProcessor* m_pManip;

    IConnectionPointContainer* m_pConPointContainer;
    IConnectionPoint* m_pConnPoint;
    
    HWND m_hWnd;
};     
```

<span data-ttu-id="4758d-134">Wenn der Header angegeben ist, müssen Sie eine Implementierung der Ereignis Schnittstelle erstellen, damit Ihre Klasse die Aktionen ausführt, die der Manipulations Prozessor ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="4758d-134">Given the header, you must create an implementation of the events interface so that your class performs the actions that you want the manipulation processor to perform.</span></span> <span data-ttu-id="4758d-135">Der folgende Code ist eine Vorlage, die die minimale Funktionalität einer Ereignis Senke für die [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="4758d-135">The following code is a template that implements the minimum functionality of an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface.</span></span>

```C++
#include "stdafx.h"
#include "cmanipulationeventsink.h"

CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *manip, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    m_pManip = manip;
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = manip->QueryInterface(
      IID_IConnectionPointContainer, 
          (LPVOID*) &spConnectionContainer
        );
    //hr = manip->QueryInterface(&spConnectionContainer);
    if (spConnectionContainer == NULL){
        // something went wrong, try to gracefully quit
        
    }

    //Get a connection point.
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(_IManipulationEvents), &m_pConnPoint);
    if (m_pConnPoint == NULL){
        // something went wrong, try to gracefully quit
    }

    DWORD dwCookie;

    //Advise.
    hr = m_pConnPoint->Advise(this, &dwCookie);
}

int CManipulationEventSink::GetStartedEventCount()
{
    return m_cStartedEventCount;
}

int CManipulationEventSink::GetDeltaEventCount()
{
    return m_cDeltaEventCount;
}

int CManipulationEventSink::GetCompletedEventCount()
{
    return m_cCompletedEventCount;
}

double CManipulationEventSink::GetX()
{
    return m_fX;
}

double CManipulationEventSink::GetY()
{
    return m_fY;
}

CManipulationEventSink::~CManipulationEventSink()
{
    //Cleanup.
}

///////////////////////////////////
//Implement IManipulationEvents
///////////////////////////////////

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;
    
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT translationDeltaX,
    /* [in] */ FLOAT translationDeltaY,
    /* [in] */ FLOAT scaleDelta,
    /* [in] */ FLOAT expansionDelta,
    /* [in] */ FLOAT rotationDelta,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cDeltaEventCount ++;
    
    RECT rect;
        
    GetWindowRect(m_hWnd, &rect);
    
    int oldWidth =  rect.right-rect.left;
    int oldHeight = rect.bottom-rect.top;            

    // scale and translate the window size / position    
    MoveWindow(m_hWnd,                                                     // the window to move
               static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
               static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
               static_cast<int>(oldWidth * scaleDelta),                    // width
               static_cast<int>(oldHeight * scaleDelta),                   // height
               TRUE);                                                      // redraw
                     
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationCompleted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y,
    /* [in] */ FLOAT cumulativeTranslationX,
    /* [in] */ FLOAT cumulativeTranslationY,
    /* [in] */ FLOAT cumulativeScale,
    /* [in] */ FLOAT cumulativeExpansion,
    /* [in] */ FLOAT cumulativeRotation)
{
    m_cCompletedEventCount ++;

    m_fX = x;
    m_fY = y;

    // place your code handler here to do any operations based on the manipulation   

    return S_OK;
}


/////////////////////////////////
//Implement IUnknown
/////////////////////////////////

ULONG CManipulationEventSink::AddRef(void) 
{
    return ++m_cRefCount;
}

ULONG CManipulationEventSink::Release(void)
{ 
    m_cRefCount --;

    if(0 == m_cRefCount) {
        delete this;
        return 0;
    }

    return m_cRefCount;
}

HRESULT CManipulationEventSink::QueryInterface(REFIID riid, LPVOID *ppvObj) 
{
    if (IID__IManipulationEvents == riid) {
        *ppvObj = (_IManipulationEvents *)(this); AddRef(); return S_OK;
    } else if (IID_IUnknown == riid) {
        *ppvObj = (IUnknown *)(this); AddRef(); return S_OK;
    } else {
        return E_NOINTERFACE;
    }
}         
```

<span data-ttu-id="4758d-136">Achten Sie besonders auf Implementierungen von [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted)-, [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)-und [**manipulationabgeschlossene**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) -Methoden in der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="4758d-136">Pay extra attention to implementations of [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted), [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta), and [**ManipulationCompleted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) methods in the class.</span></span> <span data-ttu-id="4758d-137">Dies sind die wahrscheinlichsten Methoden in der-Schnittstelle, die das Ausführen von Vorgängen auf der Grundlage der Bearbeitungs Informationen erfordern, die im Ereignis weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4758d-137">These are the most likely methods in the interface that will require you to perform operations based on the manipulation information that is passed around in the event.</span></span> <span data-ttu-id="4758d-138">Beachten Sie auch, dass der zweite Parameter im Konstruktor das Objekt ist, das in den Ereignis Manipulationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4758d-138">Note also that the second parameter in the constructor is the object that is used in the event manipulations.</span></span> <span data-ttu-id="4758d-139">Im Code, der zum Erstellen des Beispiels verwendet wird, wird das HWND für die Anwendung an den Konstruktor gesendet, sodass es neu positioniert und seine Größe geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4758d-139">In the code used for producing the sample, the hWnd for the application is sent to the constructor so that it can be repositioned and resized.</span></span>

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a><span data-ttu-id="4758d-140">Erstellen einer Instanz einer IManipulationProcessor-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4758d-140">Create an instance of an IManipulationProcessor Interface</span></span>

<span data-ttu-id="4758d-141">In dem Code, in dem Sie Manipulationen verwenden werden, müssen Sie eine Instanz einer [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle erstellen.</span><span class="sxs-lookup"><span data-stu-id="4758d-141">In the code where you will use manipulations, you must create an instance of an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="4758d-142">Zuerst müssen Sie Unterstützung für die Manipulations Klasse hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4758d-142">First you must add support for the manipulations class.</span></span> <span data-ttu-id="4758d-143">Der folgende Code zeigt, wie Sie dies in der-Klasse durchführen können.</span><span class="sxs-lookup"><span data-stu-id="4758d-143">The following code shows how you can do this in your class.</span></span>

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

<span data-ttu-id="4758d-144">Nachdem Sie über die Variable für den Manipulations Prozessor verfügen und die Header für Manipulationen eingefügt haben, müssen Sie eine Instanz der [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle erstellen.</span><span class="sxs-lookup"><span data-stu-id="4758d-144">After you have your variable for the manipulation processor and you have included the headers for manipulations, you have to create an instance of the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span> <span data-ttu-id="4758d-145">Dies ist ein COM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4758d-145">This is a COM object.</span></span> <span data-ttu-id="4758d-146">Daher müssen Sie [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)aufrufen und dann eine Instanz des Verweises auf **IManipulationProcessor** erstellen.</span><span class="sxs-lookup"><span data-stu-id="4758d-146">Therefore, you must call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), and then create an instance of your reference to the **IManipulationProcessor**.</span></span> <span data-ttu-id="4758d-147">Der folgende Code zeigt, wie Sie eine Instanz dieser Schnittstelle erstellen können.</span><span class="sxs-lookup"><span data-stu-id="4758d-147">The following code shows how you can create an instance of this interface.</span></span>

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a><span data-ttu-id="4758d-148">Erstellen Sie eine Instanz der Ereignis Senke, und richten Sie Berührungs Ereignisse ein.</span><span class="sxs-lookup"><span data-stu-id="4758d-148">Create an instance of your Event Sink and set up Touch Events</span></span>

<span data-ttu-id="4758d-149">Schließen Sie die Definition für die Klasse "Event Sink" in Ihren Code ein, und fügen Sie dann eine Variable für die Klasse "Manipulation Event Sink" hinzu.</span><span class="sxs-lookup"><span data-stu-id="4758d-149">Include the definition for your event sink class to your code and then add a variable for the manipulation event sink class.</span></span> <span data-ttu-id="4758d-150">Das folgende Codebeispiel enthält den-Header für die-Klassen Implementierung und richtet eine globale Variable zum Speichern der Ereignis Senke ein.</span><span class="sxs-lookup"><span data-stu-id="4758d-150">The following code example includes the header for the class implementation and sets up a global variable to store the event sink.</span></span>

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

<span data-ttu-id="4758d-151">Nachdem Sie die-Variable verwendet haben und die Definition für die neue Ereignis Senke-Klasse eingefügt haben, können Sie die-Klasse mit dem Bearbeitungs Prozessor erstellen, den Sie im vorherigen Schritt eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="4758d-151">After you have the variable and have included your definition for the new event sink class, you can construct the class by using the manipulation processor that you have set up in the previous step.</span></span> <span data-ttu-id="4758d-152">Der folgende Code zeigt, wie eine Instanz dieser Klasse aus **OnInitDialog** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4758d-152">The following code shows how an instance of this class would be created from **OnInitDialog**.</span></span>

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> <span data-ttu-id="4758d-153">Die Art und Weise, wie Sie eine Instanz Ihrer Ereignis Senke erstellen, hängt davon ab, was Sie mit den Manipulations Daten tun.</span><span class="sxs-lookup"><span data-stu-id="4758d-153">The way that you create an instance of your event sink depends on what you are doing with the manipulation data.</span></span> <span data-ttu-id="4758d-154">In den meisten Fällen erstellen Sie eine Ereignis Senke für den Manipulations Prozessor, die nicht denselben Konstruktor wie dieses Beispiel hat.</span><span class="sxs-lookup"><span data-stu-id="4758d-154">In most cases, you will create a manipulation processor event sink that does not have the same constructor as this example.</span></span>

### <a name="send-touch-event-data-to-the-manipulation-processor"></a><span data-ttu-id="4758d-155">Senden von Berührungs Ereignisdaten an den Manipulations Prozessor</span><span class="sxs-lookup"><span data-stu-id="4758d-155">Send Touch Event Data to the Manipulation Processor</span></span>

<span data-ttu-id="4758d-156">Nachdem Sie den Manipulations Prozessor und die Ereignis Senke eingerichtet haben, müssen Sie die Berührungs Daten in den Manipulations Prozessor einspeisen, um Manipulations Ereignisse zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="4758d-156">Now that you have your manipulation processor and event sink set up, you must feed touch data to the manipulation processor to trigger manipulation events.</span></span>

> [!Note]  
> <span data-ttu-id="4758d-157">Dies ist das gleiche Verfahren wie unter " [Getting Started with Windows Touchscreen Messages](getting-started-with-multi-touch-messages.md)" erläutert.</span><span class="sxs-lookup"><span data-stu-id="4758d-157">This is the same procedure as discussed in [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md).</span></span>

<span data-ttu-id="4758d-158">Zuerst erstellen Sie Code zum Decodieren der WM-Finger [**Abdruck \_**](wm-touchdown.md) Nachrichten und senden Sie an die [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle, um Ereignisse zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="4758d-158">First, you will create some code to decode the [**WM\_TOUCH**](wm-touchdown.md) messages and send them to the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface to raise events.</span></span> <span data-ttu-id="4758d-159">Der folgende Code zeigt eine Beispiel Implementierung, die von der **WndProc** -Methode aufgerufen wird und ein **LRESULT** für Messaging zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4758d-159">The following code shows an example implementation that is called from the **WndProc** method and return an **LRESULT** for messaging.</span></span>

```C++
LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam )
{
  UINT cInputs = LOWORD(wParam);
  PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
  
  BOOL bHandled = FALSE;
  
  if (NULL != pInputs) {
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
      cInputs,
      pInputs,
      sizeof(TOUCHINPUT))) {      
      for (UINT i=0; i<cInputs; i++){
        if (pInputs[i].dwFlags & TOUCHEVENTF_DOWN){
            g_pIManipProc->ProcessDown(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_UP){
            g_pIManipProc->ProcessUp(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
        if (pInputs[i].dwFlags & TOUCHEVENTF_MOVE){
            g_pIManipProc->ProcessMove(pInputs[i].dwID, static_cast<FLOAT>(pInputs[i].x), static_cast<FLOAT>(pInputs[i].y));
            bHandled = TRUE;
        }
      }      
    } else {
      // GetLastError() and error handling
    }
    delete [] pInputs;
  } else {
    // error handling, presumably out of memory
  }
  if (bHandled){
    // if you don't want to pass to DefWindowProc, close the touch input handle
    if (!CloseTouchInputHandle((HTOUCHINPUT)lParam)) {
        // error handling
    }
    return 0;
  }else{
    return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
  }
}
```

<span data-ttu-id="4758d-160">Nachdem Sie nun über eine hilfsprogrammmethode zum Decodieren der [**WM- \_ Berührungs**](wm-touchdown.md) Nachricht verfügen, müssen Sie die WM-Fingereingabe Meldungen von der **WndProc** -Methode an die Utility-Funktion übergeben. **\_**</span><span class="sxs-lookup"><span data-stu-id="4758d-160">Now that you have a utility method for decoding the [**WM\_TOUCH**](wm-touchdown.md) message, you must pass the **WM\_TOUCH** messages to the utility function from your **WndProc** method.</span></span> <span data-ttu-id="4758d-161">Der folgende Code zeigt, wie Sie dies tun können.</span><span class="sxs-lookup"><span data-stu-id="4758d-161">The following code shows how you can do this.</span></span>

```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_TOUCH:
        return OnTouch(hWnd, wParam, lParam);
    case WM_PAINT:
        hdc = BeginPaint(hWnd, &ps);
        // TODO: Add any drawing code here...
        EndPaint(hWnd, &ps);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```

<span data-ttu-id="4758d-162">Die benutzerdefinierten Methoden, die Sie in der Ereignis Senke implementiert haben, sollten jetzt funktionieren.</span><span class="sxs-lookup"><span data-stu-id="4758d-162">The custom methods that you have implemented in your event sink should now work.</span></span> <span data-ttu-id="4758d-163">In diesem Beispiel wird Sie durch Berühren des Fensters verschoben.</span><span class="sxs-lookup"><span data-stu-id="4758d-163">In this example, touching the window will move it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4758d-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4758d-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4758d-165">Manipulationen</span><span class="sxs-lookup"><span data-stu-id="4758d-165">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>


 
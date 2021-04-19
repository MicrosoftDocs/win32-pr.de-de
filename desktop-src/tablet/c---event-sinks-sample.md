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
# <a name="c-event-sinks-sample"></a>C++ Event senken-Beispiel

Dieses Programm veranschaulicht, wie Sie eine Anwendung erstellen können, die InkCollector-Ereignisse nur mit C++ aufzeichnet. Dieses Programm erstellt ein [**InkCollector**](inkcollector-class.md) -Objekt, um das Fenster frei zu aktivieren. Es wird immer dann ein Meldungs Feld angezeigt, wenn ein [**Stroke**](inkcollector-stroke.md) -Ereignis empfangen wird.

## <a name="defining-a-wrapper-for-ink-collector-events"></a>Definieren eines Wrappers für frei Hand Sammler Ereignisse

Die- `InkCollectorEvents` Klasse verarbeitet die Übergabe von Ink Collector-Ereignissen vom Ink Collector an den Benutzer dieser Klasse. Die `AdviseInkCollector` -Methode richtet die Verbindung zwischen dem [**InkCollector**](inkcollector-class.md) -Objekt und dieser Klasse ein. Die- `Invoke` Methode konvertiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Ereignis Benachrichtigung in einen-Befehl für eine virtuelle Funktion, die der Benutzer dieser Klasse außer Kraft setzen kann, um ein bestimmtes Ereignis zu verarbeiten.

> [!Note]  
> Sie müssen mehr als die virtuelle Funktion für einen Ereignishandler überschreiben, um dieses Ereignis zu erhalten. Für alle außer Standard Ereignisse müssen Sie [**die Methode "**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) Methode" von Ink Collector aufrufen, um ein Ereignis zu gewährleisten. Zweitens marshallte dieses Objekt selbst einen frei Hand Thread, sodass alle implementierten Ereignishandler ebenfalls frei Thread sein müssen. Besonders wichtig ist die Verwendung von Windows-APIs, die einen Wechsel zu einem anderen Thread verursachen können, da der Ereignishandler nicht sicher ist, dass er im gleichen Thread ausgeführt wird wie das Fenster, das mit dem Ink Collector verbunden ist.

 


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



Die- `Init` Methode ruft [cofroatefreethreadedmarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) auf, um einen kostenlosen Thread-Mars Haller einzurichten.


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



Die `AdviseInkCollector` -Methode richtet die Verbindung zwischen dem [**InkCollector**](inkcollector-class.md) -Objekt und dieser Klasse ein. Zuerst wird ein Verbindungspunkt an den frei Hand Sammler abgerufen. Anschließend wird ein Zeiger auf das-Element abgerufen `IInkCollectorEvents` , um eine Beratungs Verbindung mit dem Steuerelement herstellen zu können.


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



Die- `UnadviseInkCollector` Methode gibt die Verbindungen frei, die das-Objekt für das Steuerelement besitzt.


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a>Definieren eines Ink Collector-Ereignis Handlers

Die cmyinkevents-Klasse überschreibt das Standardverhalten des [**Stroke**](inkcollector-stroke.md) -Ereignis Handlers der inkcollectorevents-Klasse. Die Stroke-Methode zeigt ein Meldungs Feld an, wenn [**InkCollector**](inkcollector-class.md) ein **Stroke** -Ereignis empfängt.


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



## <a name="defining-an-ink-collector-wrapper"></a>Definieren eines Ink Collector-Wrapper

Die Init-Methode der cmyinkcollector-Klasse deklariert und initialisiert ein cmyinkevents-Objekt. Anschließend wird ein [**InkCollector**](inkcollector-class.md) -Objekt erstellt und der Ink Collector und der Ereignishandler zugeordnet. Schließlich wird der **InkCollector** an das Fenster angefügt und aktiviert.


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



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a>Zugreifen auf die Tablet PC-Schnittstellen und die Wrapper Klassen

Fügen Sie zunächst die Header für die Schnittstellen von Tablet PC Automation ein. Diese werden mit dem Microsoft <entity type="reg"/> Windows <entity type="reg"/> XP Tablet PC Edition Development Kit 1,7 installiert.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Fügen Sie dann die Header für die Wrapper Klassen und den Ereignishandler für [**InkCollector**](inkcollector-class.md) fest.


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a>Aufrufen der Wrapper Klassen

Wenn das Fenster erstellt wird, erstellt die Fenster Prozedur einen Ink Collector-Wrapper und initialisiert den Wrapper. Wenn das Fenster zerstört wird, löscht die Fenster Prozedur den Ink Collector-Wrapper. Der Ink Collector-Wrapper übernimmt das Erstellen und Löschen des zugehörigen Ereignis Handlers.


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



 

 

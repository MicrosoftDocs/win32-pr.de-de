---
description: Dieses Programm veranschaulicht, wie Sie eine Anwendung erstellen können, die InkCollector-Ereignisse nur mit C++ erfasst. Dieses Programm erstellt gemeinsam ein InkCollector-Objekt, um das Fenster zu aktivieren. Jedes Mal, wenn ein Stroke-Ereignis empfangen wird, wird ein Meldungsfeld angezeigt.
ms.assetid: 91450559-ae47-457a-a709-b4e4e78bde22
title: Beispiel für C++-Ereignissenken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b24cb718eb0d16830c285691ac5cfedf66d572f447870dc0219beb14c04548a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111130"
---
# <a name="c-event-sinks-sample"></a>Beispiel für C++-Ereignissenken

Dieses Programm veranschaulicht, wie Sie eine Anwendung erstellen können, die InkCollector-Ereignisse nur mit C++ erfasst. Dieses Programm erstellt gemeinsam ein [**InkCollector-Objekt,**](inkcollector-class.md) um das Fenster zu aktivieren. Jedes Mal, wenn ein [**Stroke-Ereignis**](inkcollector-stroke.md) empfangen wird, wird ein Meldungsfeld angezeigt.

## <a name="defining-a-wrapper-for-ink-collector-events"></a>Definieren eines Wrappers für Ink Collector-Ereignisse

Die `InkCollectorEvents` -Klasse behandelt die Übergabe von Ink-Collectorereignissen vom Ink-Collector an den Benutzer dieser Klasse. Die `AdviseInkCollector` -Methode richtet die Verbindung zwischen dem [**InkCollector-Objekt**](inkcollector-class.md) und dieser Klasse ein. Die `Invoke` -Methode konvertiert die [**IDispatch-Ereignisbenachrichtigung**](/windows/win32/api/oaidl/nn-oaidl-idispatch) in einen Aufruf einer virtuellen Funktion, die der Benutzer dieser Klasse überschreiben kann, um ein bestimmtes Ereignis zu verarbeiten.

> [!Note]  
> Sie müssen mehr als die virtuelle Funktion für einen Ereignishandler überschreiben, um dieses Ereignis zu erhalten. Bei allen Standardereignissen müssen Sie die [**SetEventInterest-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest) des Ink-Collectors aufrufen, um das Abrufen eines Ereignisses zu gewährleisten. Zweitens marshallt sich dieses Objekt selbst als free threaded, sodass auch alle implementierten Ereignishandler frei gethreadt werden müssen. Von besonderer Bedeutung ist die Verwendung von Windows-APIs. Dies kann dazu führen, dass ein Wechsel zu einem anderen Thread ausgeführt wird, da nicht garantiert wird, dass der Ereignishandler im selben Thread ausgeführt wird wie das Fenster, das mit dem Ink-Collector verbunden ist.

 


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



Die `Init` -Methode ruft [CoCreateFreeThreadedMarshaler](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) auf, um einen Marshaller mit freiem Thread zu erstellen.


```C++
// Init: set up free threaded marshaller.
HRESULT Init()
{
    return CoCreateFreeThreadedMarshaler(this, &m_punkFTM);
}
```



Die `AdviseInkCollector` -Methode richtet die Verbindung zwischen dem [**InkCollector-Objekt**](inkcollector-class.md) und dieser Klasse ein. Zuerst wird ein Verbindungspunkt zum Ink-Collector abgerufen. Anschließend wird ein Zeiger auf die abgerufen, damit eine Beratungsverbindung mit dem `IInkCollectorEvents` Steuerelement hergestellt werden kann.


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



Die `UnadviseInkCollector` -Methode gibt die Verbindungen frei, die das -Objekt mit dem -Steuerelement hat.


```C++
// Remove the connection of the sink to the Ink Collector
HRESULT UnadviseInkCollector()
{
    HRESULT hr = m_pIConnectionPoint->Unadvise(m_dwCookie);m_pIConnectionPoint->Release();
m_pIConnectionPoint = NULL;
    return hr;
}
```



## <a name="defining-an-ink-collector-events-handler"></a>Definieren eines Ink Collector-Ereignishandlers

Die CMyInkEvents-Klasse überschreibt das [](inkcollector-stroke.md) Standardverhalten des Stroke-Ereignishandlers der InkCollectorEvents-Klasse. Die Stroke-Methode zeigt ein Meldungsfeld an, wenn [**der InkCollector**](inkcollector-class.md) ein **Stroke-Ereignis** empfängt.


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



## <a name="defining-an-ink-collector-wrapper"></a>Definieren eines Ink Collector Wrappers

Die Init-Methode der CMyInkCollector-Klasse deklariert und initialisiert ein CMyInkEvents-Objekt. Anschließend wird ein [**InkCollector-Objekt**](inkcollector-class.md) erstellt und der Ink-Collector und der Ereignishandler verknüpft. Schließlich wird **der InkCollector** an das Fenster angefügt und aktiviert.


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



## <a name="accessing-the-tablet-pc-interfaces-and-the-wrapper-classes"></a>Zugreifen auf die Tablet PC-Schnittstellen und die Wrapperklassen

Schließen Sie zunächst die Header für Tablet PC Automation-Schnittstellen ein. Diese werden mit dem Microsoft <entity type="reg"/> Windows XP Tablet PC Edition Development Kit <entity type="reg"/> 1.7 installiert.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Schließen Sie dann die Header für die Wrapperklassen ein, und [**der InkCollector-Ereignishandler**](inkcollector-class.md) wurde definiert.


```C++
#include "TpcConpt.h"
#include "EventSink.h"
```



## <a name="calling-the-wrapper-classes"></a>Aufrufen der Wrapperklassen

Wenn das Fenster erstellt wird, erstellt die Window-Prozedur einen Ink Collector-Wrapper und initialisiert den Wrapper. Wenn das Fenster zerstört wird, löscht die Window-Prozedur den Wrapper für den Ink-Collector. Der Wrapper für den Ink-Collector verarbeitet das Erstellen und Löschen des zugehörigen Ereignishandlers.


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



 

 

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
# <a name="adding-manipulation-support-in-unmanaged-code"></a>Hinzufügen von Manipulations Unterstützung in nicht verwaltetem Code

In diesem Abschnitt wird erläutert, wie Sie nicht verwaltetem Code Manipulations Unterstützung hinzufügen, indem Sie eine Ereignis Senke für die [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle implementieren.

In der folgenden Abbildung wird die Manipulations Architektur dargestellt.

![Darstellung von Windows-Finger Eingabenachrichten, die an den Manipulations Prozessor eines Objekts übermittelt werden, das Ereignisse mit der \- imanipulationevents-Schnittstelle behandelt](images/manipulation-arch.png)

Berührungs Daten, die von [**WM- \_**](wm-touchdown.md) Fingereingabe Nachrichten empfangen werden, werden in Verbindung mit der Kontakt-ID aus der Fingereingabe Nachricht an [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) übermittelt. Basierend auf der Nachrichten Sequenz wird von der **IManipulationProcessor** -Schnittstelle berechnet, welche Art von Transformation ausgeführt wird und welche Werte dieser Transformation zugeordnet sind. Der **IManipulationProcessor** generiert dann [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) , die von einer Ereignis Senke behandelt werden. Die Ereignis Senke kann diese Werte dann verwenden, um benutzerdefinierte Vorgänge für das Objekt auszuführen, das transformiert wird.

Sie müssen die folgenden Schritte ausführen, um der Anwendung Bearbeitungs Unterstützung hinzuzufügen:

1.  Implementieren Sie eine Ereignis Senke für die [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle.
2.  Erstellen Sie eine Instanz einer [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle.
3.  Erstellen Sie eine Instanz der Ereignis Senke, und richten Sie Berührungs Ereignisse ein.
4.  Senden von Berührungs Ereignisdaten an den Manipulations Prozessor.

In diesem Abschnitt werden die Schritte erläutert, die Sie befolgen müssen, um der Anwendung Bearbeitungs Unterstützung hinzuzufügen. In jedem Schritt wird Code bereitgestellt, um Ihnen den Einstieg zu erleichtern.

> [!Note]  
> Manipulationen und Gesten können nicht gleichzeitig verwendet werden, da Gesten-und touchnachrichten sich gegenseitig ausschließen.

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a>Implementieren einer Ereignis Senke für die \_ IManipualtionEvents-Schnittstelle

Bevor Sie eine Instanz der Ereignis Senke erstellen können, müssen Sie eine Klasse erstellen, die die [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle für Ereignisse implementiert. Dies ist die Ereignis Senke. Ereignisse, die von der [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle generiert werden, werden von der Ereignis Senke behandelt. Der folgende Code zeigt einen Beispiel Header für eine Klasse, die die **\_ imanipulationevents** -Schnittstelle erbt.

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

Wenn der Header angegeben ist, müssen Sie eine Implementierung der Ereignis Schnittstelle erstellen, damit Ihre Klasse die Aktionen ausführt, die der Manipulations Prozessor ausführen soll. Der folgende Code ist eine Vorlage, die die minimale Funktionalität einer Ereignis Senke für die [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle implementiert.

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

Achten Sie besonders auf Implementierungen von [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted)-, [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)-und [**manipulationabgeschlossene**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) -Methoden in der-Klasse. Dies sind die wahrscheinlichsten Methoden in der-Schnittstelle, die das Ausführen von Vorgängen auf der Grundlage der Bearbeitungs Informationen erfordern, die im Ereignis weitergegeben werden. Beachten Sie auch, dass der zweite Parameter im Konstruktor das Objekt ist, das in den Ereignis Manipulationen verwendet wird. Im Code, der zum Erstellen des Beispiels verwendet wird, wird das HWND für die Anwendung an den Konstruktor gesendet, sodass es neu positioniert und seine Größe geändert werden kann.

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a>Erstellen einer Instanz einer IManipulationProcessor-Schnittstelle

In dem Code, in dem Sie Manipulationen verwenden werden, müssen Sie eine Instanz einer [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle erstellen. Zuerst müssen Sie Unterstützung für die Manipulations Klasse hinzufügen. Der folgende Code zeigt, wie Sie dies in der-Klasse durchführen können.

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

Nachdem Sie über die Variable für den Manipulations Prozessor verfügen und die Header für Manipulationen eingefügt haben, müssen Sie eine Instanz der [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle erstellen. Dies ist ein COM-Objekt. Daher müssen Sie [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)aufrufen und dann eine Instanz des Verweises auf **IManipulationProcessor** erstellen. Der folgende Code zeigt, wie Sie eine Instanz dieser Schnittstelle erstellen können.

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a>Erstellen Sie eine Instanz der Ereignis Senke, und richten Sie Berührungs Ereignisse ein.

Schließen Sie die Definition für die Klasse "Event Sink" in Ihren Code ein, und fügen Sie dann eine Variable für die Klasse "Manipulation Event Sink" hinzu. Das folgende Codebeispiel enthält den-Header für die-Klassen Implementierung und richtet eine globale Variable zum Speichern der Ereignis Senke ein.

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

Nachdem Sie die-Variable verwendet haben und die Definition für die neue Ereignis Senke-Klasse eingefügt haben, können Sie die-Klasse mit dem Bearbeitungs Prozessor erstellen, den Sie im vorherigen Schritt eingerichtet haben. Der folgende Code zeigt, wie eine Instanz dieser Klasse aus **OnInitDialog** erstellt wird.

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> Die Art und Weise, wie Sie eine Instanz Ihrer Ereignis Senke erstellen, hängt davon ab, was Sie mit den Manipulations Daten tun. In den meisten Fällen erstellen Sie eine Ereignis Senke für den Manipulations Prozessor, die nicht denselben Konstruktor wie dieses Beispiel hat.

### <a name="send-touch-event-data-to-the-manipulation-processor"></a>Senden von Berührungs Ereignisdaten an den Manipulations Prozessor

Nachdem Sie den Manipulations Prozessor und die Ereignis Senke eingerichtet haben, müssen Sie die Berührungs Daten in den Manipulations Prozessor einspeisen, um Manipulations Ereignisse zu initiieren.

> [!Note]  
> Dies ist das gleiche Verfahren wie unter " [Getting Started with Windows Touchscreen Messages](getting-started-with-multi-touch-messages.md)" erläutert.

Zuerst erstellen Sie Code zum Decodieren der WM-Finger [**Abdruck \_**](wm-touchdown.md) Nachrichten und senden Sie an die [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle, um Ereignisse zu erzeugen. Der folgende Code zeigt eine Beispiel Implementierung, die von der **WndProc** -Methode aufgerufen wird und ein **LRESULT** für Messaging zurückgibt.

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

Nachdem Sie nun über eine hilfsprogrammmethode zum Decodieren der [**WM- \_ Berührungs**](wm-touchdown.md) Nachricht verfügen, müssen Sie die WM-Fingereingabe Meldungen von der **WndProc** -Methode an die Utility-Funktion übergeben. **\_** Der folgende Code zeigt, wie Sie dies tun können.

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

Die benutzerdefinierten Methoden, die Sie in der Ereignis Senke implementiert haben, sollten jetzt funktionieren. In diesem Beispiel wird Sie durch Berühren des Fensters verschoben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Manipulationen](getting-started-with-manipulations.md)
</dt> </dl>


 
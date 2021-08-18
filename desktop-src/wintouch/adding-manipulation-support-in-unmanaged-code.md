---
title: Hinzufügen von Manipulationsunterstützung in nicht verwaltetem Code
description: In diesem Abschnitt wird erläutert, wie Sie Manipulationsunterstützung zu nicht verwaltetem Code hinzufügen, indem Sie eine Ereignissenke für die \_ IManipulationEvents-Schnittstelle implementieren.
ms.assetid: 7d8c6230-eaca-43c7-ad2f-651851b69d7f
keywords:
- Windows Touch,Manipulationen
- Windows Touch-,_IManipulationEvents-Schnittstelle
- Windows Touch,IManipulationProcessor-Schnittstelle
- Manipulationen,Hinzufügen von Unterstützung in nicht verwaltetem Code
- Manipulationen,Unterstützung von nicht verwaltetem Code
- Manipulationen,Unterstützung in nicht verwaltetem Code
- Manipulationen,_IManipulationEvents Schnittstelle
- Manipulationen,IManipulationProcessor-Schnittstelle
- _IManipulationEvents-Schnittstelle,Bearbeitungsunterstützung in nicht verwaltetem Code
- IManipulationProcessor-Schnittstelle, Manipulationsunterstützung in nicht verwaltetem Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ff526c128b6da83fae3a74b88cd3bb21bc3a81c507c0a76a7c70dbddc5f76d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710000"
---
# <a name="adding-manipulation-support-in-unmanaged-code"></a>Hinzufügen von Manipulationsunterstützung in nicht verwaltetem Code

In diesem Abschnitt wird erläutert, wie Sie Manipulationsunterstützung zu nicht verwaltetem Code hinzufügen, indem Sie eine Ereignissenke für die [**\_ IManipulationEvents-Schnittstelle**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) implementieren.

Die folgende Abbildung zeigt die Bearbeitungsarchitektur.

![Abbildung, die Touchnachrichten von Fenstern zeigt, die an den Bearbeitungsprozessor eines Objekts übergeben werden, das Ereignisse mit der \- Imanipulationevents-Schnittstelle behandelt](images/manipulation-arch.png)

Touchdaten, die von [**WM \_ TOUCH-Nachrichten**](wm-touchdown.md) empfangen werden, werden zusammen mit der Kontakt-ID aus der Touchnachricht an den [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) übergeben. Basierend auf der Nachrichtensequenz berechnet die **IManipulationProcessor-Schnittstelle,** welche Art von Transformation ausgeführt wird und welche Werte dieser Transformation zugeordnet sind. Der **IManipulationProcessor** generiert dann [**\_ IManipulationEvents,**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) die von einer Ereignissenke verarbeitet werden. Die Ereignissenke kann diese Werte dann verwenden, um benutzerdefinierte Vorgänge für das zu transformierte Objekt durchzuführen.

Um Ihrer Anwendung Manipulationsunterstützung hinzuzufügen, müssen Sie die folgenden Schritte ausführen:

1.  Implementieren Sie eine Ereignissenke für die [**\_ IManipulationEvents-Schnittstelle.**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)
2.  Erstellen Sie eine Instanz einer [**IManipulationProcessor-Schnittstelle.**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
3.  Erstellen Sie eine Instanz Ihrer Ereignissenke, und richten Sie Touchereignisse ein.
4.  Senden von Touchereignisdaten an den Bearbeitungsprozessor.

In diesem Abschnitt werden die Schritte erläutert, die Sie ausführen müssen, um Ihrer Anwendung Bearbeitungsunterstützung hinzuzufügen. Code wird in jedem Schritt bereitgestellt, um Ihnen den Einstieg zu geben.

> [!Note]  
> Manipulationen und Gesten können nicht gleichzeitig verwendet werden, da gesten- und berührungsmeldungen sich gegenseitig ausschließen.

### <a name="implement-an-event-sink-for-_imanipualtionevents-interface"></a>Implementieren einer Ereignissenke für \_ die IManipualtionEvents-Schnittstelle

Bevor Sie eine Instanz Ihrer Ereignissenke erstellen können, müssen Sie eine Klasse erstellen, die die [**\_ IManipulationEvents-Schnittstelle**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) für Das Ereignis implementiert. Dies ist Ihre Ereignissenke. Ereignisse, die von der [**IManipulationProcessor-Schnittstelle**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) generiert werden, werden von Ihrer Ereignissenke verarbeitet. Der folgende Code zeigt einen Beispielheader für eine Klasse, die die **\_ IManipulationEvents-Schnittstelle** erbt.

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

Angesichts des Headers müssen Sie eine Implementierung der Ereignisschnittstelle erstellen, damit Ihre Klasse die Aktionen ausführt, die der Bearbeitungsprozessor ausführen soll. Der folgende Code ist eine Vorlage, die die Mindestfunktionalität einer Ereignissenke für die [**\_ IManipulationEvents-Schnittstelle**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) implementiert.

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

Achten Sie besonders auf Implementierungen der [**ManipulationStarted-,**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted) [**ManipulationDelta-**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta)und [**ManipulationCompleted-Methoden**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted) in der -Klasse. Dies sind die wahrscheinlichsten Methoden in der -Schnittstelle, die erfordern, dass Sie Vorgänge basierend auf den Manipulationsinformationen ausführen, die im Ereignis übergeben werden. Beachten Sie auch, dass der zweite Parameter im Konstruktor das Objekt ist, das in den Ereignisbearbeitungen verwendet wird. In dem Code, der zum Erstellen des Beispiels verwendet wird, wird der hWnd für die Anwendung an den Konstruktor gesendet, damit er neu positioniert und die Größe geändert werden kann.

### <a name="create-an-instance-of-an-imanipulationprocessor-interface"></a>Erstellen einer Instanz einer IManipulationProcessor-Schnittstelle

In dem Code, in dem Sie Manipulationen verwenden, müssen Sie eine Instanz einer [**IManipulationProcessor-Schnittstelle**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) erstellen. Zuerst müssen Sie Unterstützung für die Manipulationsklasse hinzufügen. Der folgende Code zeigt, wie Sie dies in Ihrer -Klasse tun können.

```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;     
```

Nachdem Sie über die Variable für den Bearbeitungsprozessor verfügen und die Header für Manipulationen eingeschlossen haben, müssen Sie eine Instanz der [**IManipulationProcessor-Schnittstelle**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) erstellen. Dies ist ein COM-Objekt. Daher müssen Sie [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)aufrufen und dann eine Instanz Ihres Verweises auf **den IManipulationProcessor erstellen.** Der folgende Code zeigt, wie Sie eine Instanz dieser Schnittstelle erstellen können.

```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
```

### <a name="create-an-instance-of-your-event-sink-and-set-up-touch-events"></a>Erstellen einer Instanz Ihrer Ereignissenke und Einrichten von Touchereignissen

Fügen Sie dem Code die Definition für die Ereignissenkenklasse hinzu, und fügen Sie dann eine Variable für die Senkeklasse des Manipulationsereignis hinzu. Das folgende Codebeispiel enthält den Header für die Klassenimplementierung und richtet eine globale Variable zum Speichern der Ereignissenke ein.

```C++
//Include your definition of the event sink, CManipulationEventSink.h in this case
#include "CManipulationEventSink.h"    
     
// Set up a variable to point to the manipulation event sink implementation class    
CManipulationEventSink* g_pManipulationEventSink;   
```

Nachdem Sie über die -Variable verfügen und Ihre Definition für die neue Ereignissenkenklasse eingeschlossen haben, können Sie die -Klasse mithilfe des Bearbeitungsprozessors erstellen, den Sie im vorherigen Schritt eingerichtet haben. Der folgende Code zeigt, wie eine Instanz dieser Klasse aus **OnInitDialog erstellt wird.**

```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```

> [!Note]  
> Die Art und Weise, wie Sie eine Instanz Ihrer Ereignissenke erstellen, hängt davon ab, was Sie mit den Bearbeitungsdaten machen. In den meisten Fällen erstellen Sie eine Manipulationsprozessor-Ereignissenke, die nicht über den gleichen Konstruktor wie in diesem Beispiel verfügt.

### <a name="send-touch-event-data-to-the-manipulation-processor"></a>Senden von Touchereignisdaten an den Manipulationsprozessor

Nachdem Sie den Bearbeitungsprozessor und die Ereignissenke eingerichtet haben, müssen Sie Touchdaten an den Bearbeitungsprozessor weiterverlangen, um Manipulationsereignisse auszulösen.

> [!Note]  
> Dies ist das gleiche Verfahren, das in der Erste Schritte [mit touch messages Windows erläutert wird.](getting-started-with-multi-touch-messages.md)

Zunächst erstellen Sie Code zum Decodieren der [**WM \_ TOUCH-Nachrichten**](wm-touchdown.md) und senden sie an die [**IManipulationProcessor-Schnittstelle,**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) um Ereignisse zu erzeugen. Der folgende Code zeigt eine Beispielimplementierung, die von der **WndProc-Methode aufgerufen** wird und ein **LRESULT für Messaging** zurückgibt.

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

Nachdem Sie nun über eine Hilfsmethode zum Decodieren der [**WM \_ TOUCH-Nachricht**](wm-touchdown.md) verfügen, müssen Sie die **WM \_ TOUCH-Nachrichten** von Ihrer **WndProc-Methode** an die Hilfsfunktion übergeben. Der folgende Code zeigt, wie Sie dies tun können.

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

Die benutzerdefinierten Methoden, die Sie in der Ereignissenke implementiert haben, sollten nun funktionieren. In diesem Beispiel wird es durch Das Berühren des Fensters bewegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Manipulationen](getting-started-with-manipulations.md)
</dt> </dl>


 
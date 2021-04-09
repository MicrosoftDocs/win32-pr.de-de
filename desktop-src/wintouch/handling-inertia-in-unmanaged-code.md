---
title: Behandeln von Trägheit in nicht verwaltetem Code
description: In diesem Abschnitt wird erläutert, wie Sie die IInertiaProcessor-Schnittstelle für die Handhabung von Trägheit in nicht verwaltetem Code verwenden.
ms.assetid: 3261b461-add2-4e92-9a51-b2d46630fb4f
keywords:
- Windows-Fingereingabe, Trägheit
- Windows-Fingereingabe, Manipulations Prozessor
- Trägheit, nicht verwalteter Code
- Trägheit, IInertiaProcessor-Schnittstelle
- Trägheit, Manipulations Prozessor
- Manipulations Prozessor, Trägheit
- IInertiaProcessor-Schnittstelle, nicht verwalteter Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de56d06547f426de252a89ef5172df3fe4ca439
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036445"
---
# <a name="handling-inertia-in-unmanaged-code"></a>Behandeln von Trägheit in nicht verwaltetem Code

In diesem Abschnitt wird erläutert, wie Sie die [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle für die Handhabung von Trägheit in nicht verwaltetem Code verwenden.

## <a name="overview"></a>Übersicht

Um Trägheit in nicht verwaltetem Code zu verwenden, müssen Sie sowohl für den Manipulations Prozessor als auch für den Trägheits Prozessor Ereignis senken implementieren. Beginnen Sie mit dem Hinzufügen von Bearbeitungs Unterstützung zu Ihrer Anwendung, wie im Abschnitt [Hinzufügen von Manipulations Unterstützung zu nicht verwaltetem Code](adding-manipulation-support-in-unmanaged-code.md)beschrieben. Beachten Sie, dass die Bearbeitungs Unterstützung erfordert, dass Sie touchnachrichten anstelle von Gesten Nachrichten verwenden, um Ereignisdaten an den Manipulations Prozessor zu senden. Nachdem Sie die Bearbeitung bearbeitet haben, müssen Sie auch eine zweite Ereignis Senke für die Ereignisse implementieren, die von der [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle generiert werden, oder Sie müssen die vorhandene Ereignis Senke ändern, damit die von den **IInertiaProcessor** -und [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstellen generierten Ereignisse berücksichtigt werden. Im Rahmen dieses Beispiels ist es einfacher, von der Ereignis Senke zu starten, die für den Abschnitt Hinzufügen von Manipulations Unterstützung zu nicht verwaltetem Code erstellt wurde, und einen zweiten Konstruktor hinzuzufügen, der mit dem Trägheits Prozessor anstelle des Manipulations Prozessors funktioniert. Auf diese Weise kann die Implementierung der Ereignis Senke entweder für den Bearbeitungs Prozessor oder den Trägheits Prozessor funktionieren. Zusätzlich zum Hinzufügen eines zweiten Konstruktors hat die Ereignis Senke eine Variable, die angibt, ob die Vorgänge auf der Grundlage von Trägheit-Eingaben anstelle von Bearbeitungs Eingaben durchgeführt werden.

### <a name="add-inertia-support-to-a-manipulation-processor-event-sink"></a>Hinzufügen der trägheitunterstützung zu einer Bearbeitungs Prozessor-Ereignis

Der folgende Code zeigt den neuen ereignisenkenkonstruktor, neue Member-Variablen für eine [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle und ein Flag, das angibt, ob die Senke für Trägheit extrapoliert.


```C++
    CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd);
    CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd);
```




```C++
    IInertiaProcessor*      m_pInert;
    BOOL fExtrapolating; 
```



Nachdem der Klassen Header über die neuen Konstruktoren und ein Flag verfügt, das angibt, ob Sie die Extrapolierung durchführen, können Sie die Ereignis Senke implementieren, um separate Verarbeitungsblöcke für die [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Ereignisse und [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Ereignisse zu verwenden. Der Konstruktor, der einen **IManipulationProcessor** und einen **IInertiaProcessor** akzeptiert, sollte das **fextrapolierungsflag** auf false festlegen, was darauf hinweist, dass es sich hierbei um einen **IManipulationProcessor** -Ereignishandler handelt. Der folgende Code zeigt, wie der Konstruktor für eine Ereignis Senke, die den **IManipulationProcessor** verwendet, implementiert werden kann.


```C++
CManipulationEventSink::CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=FALSE;

    m_pManip = pManip;
    
    m_pInert = pInert;
    
    m_pManip->put_PivotRadius(-1);

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pManip->QueryInterface(
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
```



Der folgende Code zeigt, wie der Konstruktor für eine Ereignis Senke, die den [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) verwendet, implementiert werden kann. Dieser Konstruktor legt das **fextraktions** Flag auf true fest und gibt an, dass diese Instanz der Ereignis Senkenklasse eine extra Polierung ausführt und alle Verschiebungs Vorgänge ausführt, die zuvor von den Manipulations Prozessor Ereignissen durchgeführt wurden.


```C++
CManipulationEventSink::CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd)
{
    m_hWnd = hWnd;

    m_pInert = pInert;
    //Set initial ref count to 1.
    m_cRefCount = 1;

    fExtrapolating=TRUE;

    m_cStartedEventCount = 0;
    m_cDeltaEventCount = 0;
    m_cCompletedEventCount = 0;

    HRESULT hr = S_OK;

    //Get the container with the connection points.
    IConnectionPointContainer* spConnectionContainer;
    
    hr = pInert->QueryInterface(
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
```



> [!Note]  
> Die Implementierung der Implementierung der Ereignis Senke von der Manipulations Prozessor-Ereignis Senke wird als Ereignis Senke für den Trägheits Prozessor wieder verwendet

 

Wenn Sie diese Klasse ( **CManipulationEventSink**) erstellen, kann Sie nun entweder als Ereignis Senke für einen Bearbeitungs Prozessor oder als Ereignis Senke für einen Trägheits Prozessor erstellt werden. Wenn Sie als Trägheits-Prozessor-Ereignis Senke erstellt wird, wird das **fextrahierende** Flag auf true festgelegt, um anzugeben, dass Manipulations Ereignisse extrapoliert werden sollen.

> [!Note]  
> [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted) wird von den Schnittstellen [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) und [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) ausgelöst.

 

Wenn die Manipulation gestartet wird, werden die Eigenschaften der [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle festgelegt. Der folgende Code zeigt, wie das gestartete Ereignis behandelt wird.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationStarted( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;       

    // set origins in manipulation processor
    m_pInert->put_InitialOriginX(x);
    m_pInert->put_InitialOriginY(y);
    
    RECT screenRect;

    HWND desktop = GetDesktopWindow();
    GetClientRect(desktop, &screenRect);

    // physics settings
    // deceleration is units per square millisecond
    m_pInert->put_DesiredDeceleration(.1f);

    // set the boundaries        
    screenRect.left-= 1024;
    m_pInert->put_BoundaryLeft  ( static_cast<float>(screenRect.left   * 100));
    m_pInert->put_BoundaryTop   ( static_cast<float>(screenRect.top    * 100));
    m_pInert->put_BoundaryRight ( static_cast<float>(screenRect.right  * 100));
    m_pInert->put_BoundaryBottom( static_cast<float>(screenRect.bottom * 100));
    
    
    // Elastic boundaries - I set these to 90% of the screen 
    // so... 5% at left, 95% right, 5% top,  95% bottom
    // Values are whole numbers because units are in centipixels
    m_pInert->put_ElasticMarginLeft  (static_cast<float>(screenRect.left   * 5));
    m_pInert->put_ElasticMarginTop   (static_cast<float>(screenRect.top    * 5));
    m_pInert->put_ElasticMarginRight (static_cast<float>(screenRect.right  * 95));
    m_pInert->put_ElasticMarginBottom(static_cast<float>(screenRect.bottom * 95));
    
    
    return S_OK;
}
```



In diesem Beispiel werden Manipulations Delta Vorgänge verwendet, um das Fenster zu verschieben. Der folgende Code zeigt, wie das Delta Ereignis behandelt wird.


```C++
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
    MoveWindow(m_hWnd,                                              // the window to move
        static_cast<int>(rect.left + (translationDeltaX / 100.0f)), // the x position
        static_cast<int>(rect.top + (translationDeltaY/100.0f)),    // the y position
        static_cast<int>(oldWidth * scaleDelta),                    // width
        static_cast<int>(oldHeight * scaleDelta),                   // height
        TRUE);                                                      // redraw
                     
    return S_OK;
}
```



In diesem Beispiel wird durch die Bearbeitung von abgeschlossenen Ereignissen entweder ein Timer gestartet oder angehalten, der [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) für die [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle aufruft. Der folgende Code zeigt, wie das abgeschlossene Manipulations Ereignis behandelt wird.


```C++
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
    
    if (fExtrapolating){
        //Inertia Complete, stop the timer used for processing      
        KillTimer(m_hWnd,0);        
    }else{ 
        // setup velocities for inertia processor
        float vX = 0.0f;
        float vY = 0.0f;
        float vA = 0.0f;
        m_pManip->GetVelocityX(&vX);
        m_pManip->GetVelocityY(&vY);
        m_pManip->GetAngularVelocity(&vA);

        // complete any previous processing
        m_pInert->Complete();
        
        // Reset sets the  initial timestamp
        m_pInert->Reset();
                
        // 
        m_pInert->put_InitialVelocityX(vX);
        m_pInert->put_InitialVelocityY(vY);        
        
        m_pInert->put_InitialOriginX(x);
        m_pInert->put_InitialOriginY(y);
        
           
        // Start a timer
        SetTimer(m_hWnd,0, 50, 0);        
    }

    return S_OK;
}
```



Der folgende Code zeigt, wie Sie die **WM \_** -Zeit Geber Meldungen in **WndProc** interpretieren können, um Aufrufe für die [**Verarbeitung**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) auf der [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle auszuführen.


```C++
case WM_TIMER:       
  if (g_pIInertProc){
    BOOL b;       
    g_pIInertProc->Process(&b);        
  }
  break;
```



### <a name="coinitialize-the-inertia-processor-and-manipulation-processor-and-initialize-the-event-sinks"></a>Coinitialisieren des Trägheits Prozessor-und Bearbeitungs Prozessors und Initialisieren der Ereignis senken

Nachdem Sie die Ereignis Senke so geändert haben, dass Sie sowohl [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) als auch [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)unterstützt, können Sie die Ereignis senken initialisieren und Sie so einrichten, dass Sie von der Anwendung ausgeführt werden. Der folgende Code zeigt, wie die Schnittstellen Zeiger zugeordnet werden.


```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;
IInertiaProcessor*      g_pIInertProc;
```



Im folgenden Codebeispiel wird gezeigt, wie Sie die Schnittstellen instanziieren.


```C++
   HRESULT hr = CoInitialize(0);
        
   hr = CoCreateInstance(CLSID_ManipulationProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIManipProc)
   );
   
   hr = CoCreateInstance(CLSID_InertiaProcessor,
       NULL,
       CLSCTX_INPROC_SERVER,
       IID_IUnknown,
       (VOID**)(&g_pIInertProc)
   );
```



Im folgenden Codebeispiel wird gezeigt, wie Sie die Ereignis senken anhand der Schnittstellen Zeiger erstellen und das Fenster für die Berührungs Eingabe registrieren.


```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, g_pIInertProc, hWnd);
   g_pManipulationEventSink = new CManipulationEventSink(g_pIInertProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Trägheit](getting-started-with-inertia.md)
</dt> </dl>

 

 





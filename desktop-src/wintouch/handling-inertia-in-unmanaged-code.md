---
title: Behandeln von Trägheit in nicht verwaltetem Code
description: In diesem Abschnitt wird erläutert, wie die IInertiaProcessor-Schnittstelle zum Behandeln von Trägheit in nicht verwaltetem Code verwendet wird.
ms.assetid: 3261b461-add2-4e92-9a51-b2d46630fb4f
keywords:
- Windows Touch,Trägheit
- Windows Touch,Manipulationsprozessor
- Trägheit, nicht verwalteter Code
- Trägheit, IInertiaProcessor-Schnittstelle
- Trägheit, Manipulationsprozessor
- Manipulationsprozessor,Trägheit
- IInertiaProcessor-Schnittstelle, nicht verwalteter Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e112605b1f998b850c3a04a045166b376fc3a12d98615b9c2af72e756a1c1b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346500"
---
# <a name="handling-inertia-in-unmanaged-code"></a>Behandeln von Trägheit in nicht verwaltetem Code

In diesem Abschnitt wird erläutert, wie die [**IInertiaProcessor-Schnittstelle**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) zum Behandeln von Trägheit in nicht verwaltetem Code verwendet wird.

## <a name="overview"></a>Übersicht

Um Trägheit in nicht verwaltetem Code zu verwenden, müssen Sie Ereignissenken sowohl für den Manipulationsprozessor als auch für den Trägheitsprozessor implementieren. Fügen Sie ihrer Anwendung zunächst Bearbeitungsunterstützung hinzu, wie im Abschnitt Hinzufügen von [Manipulationsunterstützung zu nicht verwaltetem Code beschrieben.](adding-manipulation-support-in-unmanaged-code.md) Beachten Sie, dass die Manipulationsunterstützung erfordert, dass Sie Touchnachrichten anstelle von Gestennachrichten verwenden, um Ereignisdaten an den Bearbeitungsprozessor zu senden. Nachdem die Bearbeitung funktioniert hat, müssen Sie auch eine zweite Ereignissenke für die Ereignisse implementieren, die von der [**IInertiaProcessor-Schnittstelle**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) generiert werden, oder Sie müssen Ihre vorhandene Ereignissenke so ändern, dass sie sowohl die von der **IInertiaProcessor-** als auch der [**IManipulationProcessor-Schnittstelle**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) generierten Ereignisse aufnehmen kann. Für dieses Beispiel ist es einfacher, mit der Ereignissenke zu beginnen, die für den Abschnitt Adding Manipulation Support to Unmanaged Code (Hinzufügen von Manipulationsunterstützung zu nicht verwaltetem Code) erstellt wurde, und einen zweiten Konstruktor hinzuzufügen, der mit dem Trägheitsprozessor anstelle des Bearbeitungsprozessors funktioniert. Auf diese Weise kann die Implementierung der Ereignissenke entweder für den Manipulationsprozessor oder den Trägheitsprozessor funktionieren. Zusätzlich zum Hinzufügen eines zweiten Konstruktors verfügt die Ereignissenke über eine Variable, die angibt, ob die Vorgänge basierend auf Trägheitseingaben und nicht auf Bearbeitungseingaben ausgeführt werden.

### <a name="add-inertia-support-to-a-manipulation-processor-event-sink"></a>Hinzufügen von Trägheitsunterstützung zu einer Manipulation Processor-Ereignissenke

Der folgende Code zeigt den neuen Ereignissenkenkonstruktor, neue Membervariablen für eine [**IInertiaProcessor-Schnittstelle**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) und ein Flag, das angibt, ob die Senke für Trägheit extrapoliert wird.


```C++
    CManipulationEventSink(IManipulationProcessor *pManip, IInertiaProcessor *pInert, HWND hWnd);
    CManipulationEventSink(IInertiaProcessor *pInert, HWND hWnd);
```




```C++
    IInertiaProcessor*      m_pInert;
    BOOL fExtrapolating; 
```



Nachdem der Klassenheader über die neuen Konstruktoren und ein Flag verfügt, das angibt, ob Sie extrapolieren, können Sie die Ereignissenke implementieren, um separate Behandlungsblöcke für die [**IManipulationProcessor-Ereignisse**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) und [**IInertiaProcessor-Ereignisse**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) zu erhalten. Der Konstruktor, der einen **IManipulationProcessor** und einen **IInertiaProcessor** akzeptiert, sollte das **fExtrapolating-Flag** auf false festlegen, was angibt, dass es sich um einen **IManipulationProcessor-Ereignishandler** handelt. Der folgende Code zeigt, wie der Konstruktor für eine Ereignissenke, die **den IManipulationProcessor** verwendet, implementiert werden kann.


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



Der folgende Code zeigt, wie der Konstruktor für eine Ereignissenke, die [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) verwendet, implementiert werden kann. Dieser Konstruktor legt das **fExtrapolating-Flag** auf TRUE fest, was angibt, dass diese Instanz der Ereignissenkeklasse Eine Extrapolierung und alle Zuvor von den Manipulationsprozessorereignissen ausgeführten Bewegungsvorgänge ausführen wird.


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
> Die Implementierung der Ereignissenkenklasse aus der Manipulationsprozessor-Ereignissenke wird als Ereignissenke für den Trägheitsprozessor wiederverwendet.

 

Wenn Sie nun diese Klasse **(CManipulationEventSink)** erstellen, kann sie entweder als Ereignissenke für einen Manipulationsprozessor oder als Ereignissenke für einen Trägheitsprozessor erstellt werden. Wenn es als Trägheitsprozessor-Ereignissenke erstellt wird, ist das **fExtrapolating-Flag** auf TRUE festgelegt, was angibt, dass Manipulationsereignisse extrapoliert werden sollen.

> [!Note]  
> [**ManipulationStarted**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted) wird von den Schnittstellen [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) und [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) ausgelöst.

 

Wenn die Bearbeitung beginnt, werden die [**IInertiaProcessor-Schnittstelleneigenschaften**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) festgelegt. Der folgende Code zeigt, wie das gestartete Ereignis behandelt wird.


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



In diesem Beispiel werden Manipulationsdelta verwendet, um das Fenster zu verschieben. Der folgende Code zeigt, wie das Deltaereignis behandelt wird.


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



In diesem Beispiel starten oder beenden Manipulationsereignisse entweder einen Timer, der [**Process auf**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) der [**IInertiaProcessor-Schnittstelle aufruft.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) Der folgende Code zeigt, wie das abgeschlossene Manipulationsereignis behandelt wird.


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



Der folgende Code zeigt, wie Sie **WM \_ TIMER-Nachrichten** in **WndProc** interpretieren können, um Aufrufe von [**Process auf**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process) der [**IInertiaProcessor-Schnittstelle**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) durchzuführen.


```C++
case WM_TIMER:       
  if (g_pIInertProc){
    BOOL b;       
    g_pIInertProc->Process(&b);        
  }
  break;
```



### <a name="coinitialize-the-inertia-processor-and-manipulation-processor-and-initialize-the-event-sinks"></a>CoInitialisieren des Trägheitsprozessors und des Manipulationsprozessors und Initialisieren der Ereignissenken

Nachdem Sie ihre Ereignissenke so geändert haben, dass sie sowohl [**den IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) als auch den [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)unterstützt, können Sie die Ereignissenken initialisieren und für die Ausführung über Ihre Anwendung einrichten. Der folgende Code zeigt, wie die Schnittstellenzeker zugeordnet werden.


```C++
//Include windows.h for touch events
#include "windows.h"  

// Manipulation implementation file
#include <manipulations_i.c>
    
// Smart Pointer to a global reference of a manipulation processor, event sink
IManipulationProcessor* g_pIManipProc;
IInertiaProcessor*      g_pIInertProc;
```



Das folgende Codebeispiel zeigt, wie Sie Ihre Schnittstellen instanziieren.


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



Das folgende Codebeispiel zeigt, wie Sie Ihre Ereignissenken mit den Schnittstellenzeern erstellen und das Fenster für Toucheingaben registrieren.


```C++
   g_pManipulationEventSink = new CManipulationEventSink(g_pIManipProc, g_pIInertProc, hWnd);
   g_pManipulationEventSink = new CManipulationEventSink(g_pIInertProc, hWnd);


   RegisterTouchWindow(hWnd, 0);  
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Trägheit](getting-started-with-inertia.md)
</dt> </dl>

 

 





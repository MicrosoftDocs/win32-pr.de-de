---
title: Aktualisieren des Animations-Managers und Zeichnen von Frames
description: Jedes Mal, wenn eine Anwendung ein Storyboard plant, muss die Anwendung die aktuelle Zeit für den Animations-Manager bereitstellen.
ms.assetid: c4f746c3-e47c-4b82-a41b-e2c0d177d097
keywords:
- Animation-Manager-Objekte Windows-Animation, aktualisieren
- Animation Zeit Geber Objekte Windows-Animation, verbinden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9a48e8d6e273174e502c374727e69b61bc478d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039090"
---
# <a name="update-the-animation-manager-and-draw-frames"></a>Aktualisieren des Animations-Managers und Zeichnen von Frames

Jedes Mal, wenn eine Anwendung ein Storyboard plant, muss die Anwendung die aktuelle Zeit für den Animations-Manager bereitstellen. Die aktuelle Zeit ist auch erforderlich, wenn der Animations-Manager weitergeleitet wird, um seinen Zustand zu aktualisieren, und alle Animations Variablen auf die entsprechenden interintermierten Werte festzulegen.

## <a name="overview"></a>Übersicht

Von der Windows-Animation werden zwei Konfigurationen unterstützt: die Anwendungs gesteuerte Animation und die Zeit Geber gesteuerte Animation.

Um die Anwendungs gesteuerte Animation in der Anwendung zu verwenden, müssen Sie den Animations-Manager vor dem Zeichnen der einzelnen Frames aktualisieren und einen geeigneten Mechanismus verwenden, um Frames für Animationen häufig genug zu zeichnen. Eine Anwendung, die die Anwendungs gesteuerte Animation verwendet, kann einen beliebigen Mechanismus verwenden, um die aktuelle Zeit zu bestimmen, aber das Windows Animation Timer-Objekt gibt eine genaue Zeit in den Einheiten zurück, die vom Animations-Manager akzeptiert werden. Um unnötige Zeichnungen zu vermeiden, wenn keine Animationen abgespielt werden, sollten Sie auch einen Manager-Ereignishandler bereitstellen, um die Neuzeichnung zu starten, wenn Animationen geplant sind, und nach jedem Frame prüfen, ob das Neuzeichnen angehalten werden kann. Weitere Informationen finden Sie unter [Anwendungs gesteuerte Animation](scenic-animation-api-overview.md).

In der Anwendungs gesteuerten Konfiguration kann eine Anwendung die [**iuianimationmanager:: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) -Methode aufrufen, um zu überprüfen, ob Animationen aktuell geplant sind, und weiterhin Frames zeichnen, wenn Sie sind. Da das Neuzeichnen beendet wird, wenn keine Animationen geplant sind, muss es bei der nächsten geplanten Animation neu gestartet werden. Eine Anwendung kann einen Manager-Ereignishandler registrieren, um benachrichtigt zu werden, wenn sich der Status des Animations-Managers von "im Leerlauf" (keine Animationen sind aktuell geplant) in "ausgelastet" ändert.

Um die Zeit Geber gesteuerte Animation in der Anwendung zu verwenden, müssen Sie den Animations-Manager mit einem Animations Zeit Geber verbinden und einen Timer-Ereignishandler bereitstellen. Wenn der Animations-Manager mit einem Timer verbunden ist, kann der Timer den Vorgesetzten darüber informieren, wann der Animations Zustand im Laufe der Zeit aktualisiert werden soll. Die Anwendung sollte einen Frame für jeden Zeit Geber Takt zeichnen. Der Animations-Manager kann den Timer wiederum anweisen, wenn Animationen abgespielt werden. Daher kann der Timer in Leerlaufzeiten deaktiviert werden, wenn das erneute zeichnen unnötig ist. Um unnötige Zeichnungen zu vermeiden, wenn keine Animationen abgespielt werden, sollten Sie den Timer so konfigurieren, dass er sich automatisch selbst deaktiviert. Weitere Informationen finden Sie unter [Timer-gesteuerte Animation](scenic-animation-api-overview.md).

## <a name="example-code"></a>Beispielcode

-   [Anwendungs gesteuerte Animation](#application-driven-animation)
-   [Zeit Geber gesteuerte Animation](#timer-driven-animation)

### <a name="application-driven-animation"></a>Animation Application-Driven

Der folgende Beispielcode wird von managereventhandler. h aus den Windows-Animations Beispielen [Anwendungs gesteuerte Animation](application-driven-animation-sample.md) und [Raster Layout](/windows/desktop/UIAnimation/grid-layout-sample)entnommen. Er definiert den Manager-Ereignishandler.


```C++
#include "UIAnimationHelper.h"

// Event handler object for manager status changes

class CManagerEventHandler :
    public CUIAnimationManagerEventHandlerBase<CManagerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationManagerEventHandler **ppManagerEventHandler
    ) throw()
    {
        CManagerEventHandler *pManagerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppManagerEventHandler,
            &pManagerEventHandler
            );
        if (SUCCEEDED(hr))
        {
            pManagerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationManagerEventHandler

    IFACEMETHODIMP
    OnManagerStatusChanged
    (
        UI_ANIMATION_MANAGER_STATUS newStatus,
        UI_ANIMATION_MANAGER_STATUS previousStatus
    )
    {
        HRESULT hr = S_OK;

        if (newStatus == UI_ANIMATION_MANAGER_BUSY)
        {
            hr = m_pMainWindow->Invalidate();
        }

        return hr;
    }

    ...

};
```



Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" aus der [Anwendungs gesteuerten Animation](application-driven-animation-sample.md)"Windows Animation Sample". Weitere Informationen finden Sie unter CMainWindow:: initializeanimation. In diesem Beispiel wird mithilfe der Methode " [**kreateinstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) " eine Instanz des Manager-Ereignis Handlers erstellt und mithilfe der [**iuianimationmanager:: setmanagereventhandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) -Methode an den Animations-Manager übergeben.


```C++
// Create and set the ManagerEventHandler to start updating when animations are scheduled

IUIAnimationManagerEventHandler *pManagerEventHandler;
HRESULT hr = CManagerEventHandler::CreateInstance(
    this,
    &pManagerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->SetManagerEventHandler(
        pManagerEventHandler
        );
    pManagerEventHandler->Release();
}
```



Da der Manager-Ereignishandler einen Verweis auf das Hauptfenster Objekt beibehält, sollte der Manager-Ereignishandler gelöscht werden (durch Übergeben von **null** an [**setmanagereventhandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)), oder der Animations-Manager muss vollständig freigegeben werden, bevor das Hauptfenster zerstört wird.

Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" in der [Anwendungs gesteuerten Animation](application-driven-animation-sample.md)"Windows Animation Sample". Weitere Informationen finden Sie unter der CMainWindow:: OnPaint-Methode. Er ruft die [**iuianimationmanager:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) -Methode auf, um die Zeit in den Einheiten abzurufen, die für die [**iuianimationmanager:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) -Methode erforderlich sind.


```C++
// Update the animation manager with the current time

UI_ANIMATION_SECONDS secondsNow;
HRESULT hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->Update(
        secondsNow
        );

    ...

}
```



Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" aus den Windows-Animations Beispielen [Anwendungs gesteuerte Animation](application-driven-animation-sample.md) und [Raster Layout](/windows/desktop/UIAnimation/grid-layout-sample). Weitere Informationen finden Sie unter der CMainWindow:: OnPaint-Methode. Dabei wird davon ausgegangen, dass die Anwendung eine Grafik-API verwendet, die automatisch mit der Aktualisierungsrate des Monitors (z. b. Direct2D mit ihren Standardeinstellungen) synchronisiert wird. in diesem Fall genügt ein Aufruf der [**invalidatenfunktion**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) , um sicherzustellen, dass der Zeichnungs Code erneut aufgerufen wird, wenn der nächste Frame gezeichnet werden soll. Anstatt **ungültig** zu machen, sollten Sie überprüfen, ob noch Animationen mit [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)geplant sind.


```C++
// Read the values of the animation variables and draw the client area

hr = DrawClientArea();
if (SUCCEEDED(hr))
{          
    // Continue redrawing the client area as long as there are animations scheduled
    UI_ANIMATION_MANAGER_STATUS status;
    hr = m_pAnimationManager->GetStatus(
        &status
        );
    if (SUCCEEDED(hr))
    {
        if (status == UI_ANIMATION_MANAGER_BUSY)
        {
            InvalidateRect(
                m_hwnd,
                NULL,
                FALSE
                );
        }
    }
}
```



### <a name="timer-driven-animation"></a>Animation Timer-Driven

Der folgende Beispielcode stammt aus der timereventhandler. h-Datei aus der Zeit Geber [gesteuerten Animation](timer-driven-animation-sample.md)für Windows-Animation. Im Beispielcode wird der Timer-Ereignishandler definiert, der den Client Bereich des Fensters für ungültig erklärt, damit nach jedem Update des Animations Zustands ein Repaint ausgelöst wird.


```C++
#include "UIAnimationHelper.h"

// Event handler object for timer events

class CTimerEventHandler :
    public CUIAnimationTimerEventHandlerBase<CTimerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationTimerEventHandler **ppTimerEventHandler
    ) throw()
    {
        CTimerEventHandler *pTimerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppTimerEventHandler,
            &pTimerEventHandler
            );

        if (SUCCEEDED(hr))
        {
            pTimerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationTimerEventHandler

    IFACEMETHODIMP
    OnPreUpdate()
    {
        return S_OK;
    }

    IFACEMETHODIMP
    OnPostUpdate()
    {
        HRESULT hr = m_pMainWindow->Invalidate();

        return hr;
    }

    IFACEMETHODIMP
    OnRenderingTooSlow
    (
        UINT32 /* fps */
    )
    {
        return S_OK;
    }

    ...

};
```



Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" aus der Zeit Geber [gesteuerten Animation](timer-driven-animation-sample.md)der Windows-Animation. Weitere Informationen finden Sie unter CMainWindow:: initializeanimation. In diesem Beispiel wird mithilfe der Methode " [**kreateinstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) " eine Instanz des timerereignishandlers erstellt und mithilfe der [**iuianimationtimer::-Methode der Methode "iuianimationtimer::**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) " übergeben. Da der Timer-Ereignishandler einen Verweis auf das Hauptfenster Objekt beibehält, sollte der Timer-Ereignishandler gelöscht werden (durch Übergeben von **null** an **settimereventhandler**), oder der Timer wird vollständig freigegeben, bevor das Hauptfenster zerstört wird.


```C++
// Create and set the timer event handler

IUIAnimationTimerEventHandler *pTimerEventHandler;
hr = CTimerEventHandler::CreateInstance(
    this,
    &pTimerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerEventHandler(
        pTimerEventHandler
        );
    pTimerEventHandler->Release();
}
```



Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" im Windows Animation Sample [Timer-gesteuerte Animation](timer-driven-animation-sample.md). Weitere Informationen finden Sie unter der CMainWindow:: initializeanimation-Methode. Sie ruft die [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode für das Animation Manager-Objekt auf, um einen Zeiger auf [**iuianimationtimerupdatehandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler)zu erhalten, und verbindet dann die Objekte [**uianimationmanager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) und [**uianimationtimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) , indem der Animations-Manager mithilfe der [**iuianimationtimer**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) Beachten Sie, dass es nicht erforderlich ist, diese Verbindung explizit zu löschen. die Verbindung wird sicher gelöscht, nachdem die Anwendung sowohl den Animations-Manager als auch den Animations Timer freigegeben hat.


```C++
// Connect the animation manager to the timer

IUIAnimationTimerUpdateHandler *pTimerUpdateHandler;
hr = m_pAnimationManager->QueryInterface(
    IID_PPV_ARGS(&pTimerUpdateHandler)
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerUpdateHandler(
        pTimerUpdateHandler
        UI_ANIMATION_IDLE_BEHAVIOR_DISABLE  // timer will shut itself off when there are no animations playing
        );
    pTimerUpdateHandler->Release();
    if (SUCCEEDED(hr))
    {
        // Create and set the timer event handler

        ...

    }
}
```



Wenn das **Verhalten der UI- \_ Animation im \_ Leerlauf \_ \_** nicht verwendet wird, ist es auch erforderlich, den Timer zu aktivieren, um ihn zu starten.

## <a name="previous-step"></a>Vorheriger Schritt

Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Erstellen von Animations Variablen](create-animation-variables.md).

## <a name="next-step"></a>Nächster Schritt

Nachdem Sie diesen Schritt abgeschlossen haben, ist der nächste Schritt: [Lesen der Animations Variablen Werte](updating---application-driven-animation.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iuianimationmanager:: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[**Iuianimationmanager:: setmanagereventhandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[**Iuianimationmanager:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[**Iuianimationtimer:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[**Iuianimationtimer:: lttimerupdatehandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

[**Uianimationmanager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))
</dt> <dt>

[**Uianimationtimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))
</dt> <dt>

[Übersicht über Windows-Animationen](scenic-animation-api-overview.md)
</dt> </dl>

 

 
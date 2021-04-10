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
# <a name="update-the-animation-manager-and-draw-frames"></a><span data-ttu-id="95001-105">Aktualisieren des Animations-Managers und Zeichnen von Frames</span><span class="sxs-lookup"><span data-stu-id="95001-105">Update the Animation Manager and Draw Frames</span></span>

<span data-ttu-id="95001-106">Jedes Mal, wenn eine Anwendung ein Storyboard plant, muss die Anwendung die aktuelle Zeit für den Animations-Manager bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="95001-106">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="95001-107">Die aktuelle Zeit ist auch erforderlich, wenn der Animations-Manager weitergeleitet wird, um seinen Zustand zu aktualisieren, und alle Animations Variablen auf die entsprechenden interintermierten Werte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="95001-107">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span>

## <a name="overview"></a><span data-ttu-id="95001-108">Übersicht</span><span class="sxs-lookup"><span data-stu-id="95001-108">Overview</span></span>

<span data-ttu-id="95001-109">Von der Windows-Animation werden zwei Konfigurationen unterstützt: die Anwendungs gesteuerte Animation und die Zeit Geber gesteuerte Animation.</span><span class="sxs-lookup"><span data-stu-id="95001-109">There are two configurations supported by Windows Animation: application-driven animation and timer-driven animation.</span></span>

<span data-ttu-id="95001-110">Um die Anwendungs gesteuerte Animation in der Anwendung zu verwenden, müssen Sie den Animations-Manager vor dem Zeichnen der einzelnen Frames aktualisieren und einen geeigneten Mechanismus verwenden, um Frames für Animationen häufig genug zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="95001-110">To use application-driven animation in your application, you must update the animation manager before drawing each frame and use an appropriate mechanism to draw frames frequently enough for animation.</span></span> <span data-ttu-id="95001-111">Eine Anwendung, die die Anwendungs gesteuerte Animation verwendet, kann einen beliebigen Mechanismus verwenden, um die aktuelle Zeit zu bestimmen, aber das Windows Animation Timer-Objekt gibt eine genaue Zeit in den Einheiten zurück, die vom Animations-Manager akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="95001-111">An application using application-driven animation can use any mechanism to determine the current time, but the Windows Animation timer object returns a precise time in the units accepted by the animation manager.</span></span> <span data-ttu-id="95001-112">Um unnötige Zeichnungen zu vermeiden, wenn keine Animationen abgespielt werden, sollten Sie auch einen Manager-Ereignishandler bereitstellen, um die Neuzeichnung zu starten, wenn Animationen geplant sind, und nach jedem Frame prüfen, ob das Neuzeichnen angehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="95001-112">To avoid unnecessary drawing when no animations are playing, you should also provide a manager event handler to start redrawing when animations are scheduled and check after each frame whether redrawing can be suspended.</span></span> <span data-ttu-id="95001-113">Weitere Informationen finden Sie unter [Anwendungs gesteuerte Animation](scenic-animation-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="95001-113">For more information, see [Application-Driven Animation](scenic-animation-api-overview.md).</span></span>

<span data-ttu-id="95001-114">In der Anwendungs gesteuerten Konfiguration kann eine Anwendung die [**iuianimationmanager:: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) -Methode aufrufen, um zu überprüfen, ob Animationen aktuell geplant sind, und weiterhin Frames zeichnen, wenn Sie sind.</span><span class="sxs-lookup"><span data-stu-id="95001-114">In the application-driven configuration, an application can call the [**IUIAnimationManager::GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) method to verify that animations are currently scheduled and continue to draw frames if they are.</span></span> <span data-ttu-id="95001-115">Da das Neuzeichnen beendet wird, wenn keine Animationen geplant sind, muss es bei der nächsten geplanten Animation neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="95001-115">Because redrawing stops when there are no animations scheduled, it is necessary to restart it the next time an animation is scheduled.</span></span> <span data-ttu-id="95001-116">Eine Anwendung kann einen Manager-Ereignishandler registrieren, um benachrichtigt zu werden, wenn sich der Status des Animations-Managers von "im Leerlauf" (keine Animationen sind aktuell geplant) in "ausgelastet" ändert.</span><span class="sxs-lookup"><span data-stu-id="95001-116">An application can register a manager event handler to be notified when the status of the animation manager changes from idle (no animations are currently scheduled) to busy.</span></span>

<span data-ttu-id="95001-117">Um die Zeit Geber gesteuerte Animation in der Anwendung zu verwenden, müssen Sie den Animations-Manager mit einem Animations Zeit Geber verbinden und einen Timer-Ereignishandler bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="95001-117">To use timer-driven animation in your application, you must connect the animation manager to an animation timer and provide a timer event handler.</span></span> <span data-ttu-id="95001-118">Wenn der Animations-Manager mit einem Timer verbunden ist, kann der Timer den Vorgesetzten darüber informieren, wann der Animations Zustand im Laufe der Zeit aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="95001-118">When the animation manager is connected to a timer, the timer can tell the manager when the animation state should be updated as time progresses.</span></span> <span data-ttu-id="95001-119">Die Anwendung sollte einen Frame für jeden Zeit Geber Takt zeichnen.</span><span class="sxs-lookup"><span data-stu-id="95001-119">The application should draw a frame for each timer tick.</span></span> <span data-ttu-id="95001-120">Der Animations-Manager kann den Timer wiederum anweisen, wenn Animationen abgespielt werden. Daher kann der Timer in Leerlaufzeiten deaktiviert werden, wenn das erneute zeichnen unnötig ist.</span><span class="sxs-lookup"><span data-stu-id="95001-120">The animation manager can in turn tell the timer when there are animations playing, so the timer can shut itself off during idle periods when redrawing is unnecessary.</span></span> <span data-ttu-id="95001-121">Um unnötige Zeichnungen zu vermeiden, wenn keine Animationen abgespielt werden, sollten Sie den Timer so konfigurieren, dass er sich automatisch selbst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="95001-121">To avoid unnecessary drawing when no animations are playing, you should configure the timer to disable itself automatically.</span></span> <span data-ttu-id="95001-122">Weitere Informationen finden Sie unter [Timer-gesteuerte Animation](scenic-animation-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="95001-122">For more information, see [Timer-Driven Animation](scenic-animation-api-overview.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="95001-123">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="95001-123">Example Code</span></span>

-   [<span data-ttu-id="95001-124">Anwendungs gesteuerte Animation</span><span class="sxs-lookup"><span data-stu-id="95001-124">Application-Driven Animation</span></span>](#application-driven-animation)
-   [<span data-ttu-id="95001-125">Zeit Geber gesteuerte Animation</span><span class="sxs-lookup"><span data-stu-id="95001-125">Timer-Driven Animation</span></span>](#timer-driven-animation)

### <a name="application-driven-animation"></a><span data-ttu-id="95001-126">Animation Application-Driven</span><span class="sxs-lookup"><span data-stu-id="95001-126">Application-Driven Animation</span></span>

<span data-ttu-id="95001-127">Der folgende Beispielcode wird von managereventhandler. h aus den Windows-Animations Beispielen [Anwendungs gesteuerte Animation](application-driven-animation-sample.md) und [Raster Layout](/windows/desktop/UIAnimation/grid-layout-sample)entnommen.</span><span class="sxs-lookup"><span data-stu-id="95001-127">The following example code is taken from ManagerEventHandler.h from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample).</span></span> <span data-ttu-id="95001-128">Er definiert den Manager-Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="95001-128">It defines the manager event handler.</span></span>


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



<span data-ttu-id="95001-129">Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" aus der [Anwendungs gesteuerten Animation](application-driven-animation-sample.md)"Windows Animation Sample". Weitere Informationen finden Sie unter CMainWindow:: initializeanimation.</span><span class="sxs-lookup"><span data-stu-id="95001-129">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="95001-130">In diesem Beispiel wird mithilfe der Methode " [**kreateinstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) " eine Instanz des Manager-Ereignis Handlers erstellt und mithilfe der [**iuianimationmanager:: setmanagereventhandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) -Methode an den Animations-Manager übergeben.</span><span class="sxs-lookup"><span data-stu-id="95001-130">This example creates an instance of the manager event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the animation manager using the [**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) method.</span></span>


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



<span data-ttu-id="95001-131">Da der Manager-Ereignishandler einen Verweis auf das Hauptfenster Objekt beibehält, sollte der Manager-Ereignishandler gelöscht werden (durch Übergeben von **null** an [**setmanagereventhandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)), oder der Animations-Manager muss vollständig freigegeben werden, bevor das Hauptfenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="95001-131">Because the manager event handler retains a reference to the main window object, the manager event handler should be cleared (by passing **NULL** to [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) or the animation manager should be completely released before the main window is destroyed.</span></span>

<span data-ttu-id="95001-132">Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" in der [Anwendungs gesteuerten Animation](application-driven-animation-sample.md)"Windows Animation Sample". Weitere Informationen finden Sie unter der CMainWindow:: OnPaint-Methode.</span><span class="sxs-lookup"><span data-stu-id="95001-132">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="95001-133">Er ruft die [**iuianimationmanager:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) -Methode auf, um die Zeit in den Einheiten abzurufen, die für die [**iuianimationmanager:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) -Methode erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="95001-133">It calls the [**IUIAnimationManager::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) method to retrieve the time in the units required by the [**IUIAnimationManager::Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) method.</span></span>


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



<span data-ttu-id="95001-134">Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" aus den Windows-Animations Beispielen [Anwendungs gesteuerte Animation](application-driven-animation-sample.md) und [Raster Layout](/windows/desktop/UIAnimation/grid-layout-sample). Weitere Informationen finden Sie unter der CMainWindow:: OnPaint-Methode.</span><span class="sxs-lookup"><span data-stu-id="95001-134">The following example code is taken from MainWindow.cpp from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="95001-135">Dabei wird davon ausgegangen, dass die Anwendung eine Grafik-API verwendet, die automatisch mit der Aktualisierungsrate des Monitors (z. b. Direct2D mit ihren Standardeinstellungen) synchronisiert wird. in diesem Fall genügt ein Aufruf der [**invalidatenfunktion**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) , um sicherzustellen, dass der Zeichnungs Code erneut aufgerufen wird, wenn der nächste Frame gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95001-135">It assumes that the application is using a graphics API that automatically synchronizes to the monitor refresh rate (such as Direct2D with its default settings), in which case a call to the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function is enough to ensure that the painting code will be called again when it is time to draw the next frame.</span></span> <span data-ttu-id="95001-136">Anstatt **ungültig** zu machen, sollten Sie überprüfen, ob noch Animationen mit [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)geplant sind.</span><span class="sxs-lookup"><span data-stu-id="95001-136">Rather than call **InvalidateRect** unconditionally, it is better to check if there are still any animations scheduled using [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span></span>


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



### <a name="timer-driven-animation"></a><span data-ttu-id="95001-137">Animation Timer-Driven</span><span class="sxs-lookup"><span data-stu-id="95001-137">Timer-Driven Animation</span></span>

<span data-ttu-id="95001-138">Der folgende Beispielcode stammt aus der timereventhandler. h-Datei aus der Zeit Geber [gesteuerten Animation](timer-driven-animation-sample.md)für Windows-Animation.</span><span class="sxs-lookup"><span data-stu-id="95001-138">The following example code is taken from TimerEventHandler.h from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="95001-139">Im Beispielcode wird der Timer-Ereignishandler definiert, der den Client Bereich des Fensters für ungültig erklärt, damit nach jedem Update des Animations Zustands ein Repaint ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="95001-139">The example code defines the timer event handler, which invalidates the window's client area to cause a repaint after each update of the animation state.</span></span>


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



<span data-ttu-id="95001-140">Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" aus der Zeit Geber [gesteuerten Animation](timer-driven-animation-sample.md)der Windows-Animation. Weitere Informationen finden Sie unter CMainWindow:: initializeanimation.</span><span class="sxs-lookup"><span data-stu-id="95001-140">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="95001-141">In diesem Beispiel wird mithilfe der Methode " [**kreateinstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) " eine Instanz des timerereignishandlers erstellt und mithilfe der [**iuianimationtimer::-Methode der Methode "iuianimationtimer::**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) " übergeben.</span><span class="sxs-lookup"><span data-stu-id="95001-141">This example creates an instance of the timer event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the timer using the [**IUIAnimationTimer::SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) method.</span></span> <span data-ttu-id="95001-142">Da der Timer-Ereignishandler einen Verweis auf das Hauptfenster Objekt beibehält, sollte der Timer-Ereignishandler gelöscht werden (durch Übergeben von **null** an **settimereventhandler**), oder der Timer wird vollständig freigegeben, bevor das Hauptfenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="95001-142">Because the timer event handler retains a reference to the main window object, the timer event handler should be cleared (by passing **NULL** to **SetTimerEventHandler**) or the timer completely released before the main window is destroyed.</span></span>


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



<span data-ttu-id="95001-143">Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" im Windows Animation Sample [Timer-gesteuerte Animation](timer-driven-animation-sample.md). Weitere Informationen finden Sie unter der CMainWindow:: initializeanimation-Methode.</span><span class="sxs-lookup"><span data-stu-id="95001-143">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::InitializeAnimation method.</span></span> <span data-ttu-id="95001-144">Sie ruft die [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode für das Animation Manager-Objekt auf, um einen Zeiger auf [**iuianimationtimerupdatehandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler)zu erhalten, und verbindet dann die Objekte [**uianimationmanager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) und [**uianimationtimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) , indem der Animations-Manager mithilfe der [**iuianimationtimer**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)</span><span class="sxs-lookup"><span data-stu-id="95001-144">It calls the [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the animation manager object to get a pointer to [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), then connects the [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) and [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) objects by setting the animation manager as the timer's update handler using the [**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) method.</span></span> <span data-ttu-id="95001-145">Beachten Sie, dass es nicht erforderlich ist, diese Verbindung explizit zu löschen. die Verbindung wird sicher gelöscht, nachdem die Anwendung sowohl den Animations-Manager als auch den Animations Timer freigegeben hat.</span><span class="sxs-lookup"><span data-stu-id="95001-145">Note that it is not necessary to explicitly clear this connection; the connection is cleared safely after the application releases both the animation manager and the animation timer.</span></span>


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



<span data-ttu-id="95001-146">Wenn das **Verhalten der UI- \_ Animation im \_ Leerlauf \_ \_** nicht verwendet wird, ist es auch erforderlich, den Timer zu aktivieren, um ihn zu starten.</span><span class="sxs-lookup"><span data-stu-id="95001-146">If **UI\_ANIMATION\_IDLE\_BEHAVIOR\_DISABLE** is not used, it is also necessary to enable the timer to start it ticking.</span></span>

## <a name="previous-step"></a><span data-ttu-id="95001-147">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="95001-147">Previous Step</span></span>

<span data-ttu-id="95001-148">Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Erstellen von Animations Variablen](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="95001-148">Before starting this step, you should have completed this step: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="95001-149">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="95001-149">Next Step</span></span>

<span data-ttu-id="95001-150">Nachdem Sie diesen Schritt abgeschlossen haben, ist der nächste Schritt: [Lesen der Animations Variablen Werte](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="95001-150">After completing this step, the next step is: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95001-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95001-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95001-152">**Iuianimationmanager:: GetStatus**</span><span class="sxs-lookup"><span data-stu-id="95001-152">**IUIAnimationManager::GetStatus**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[<span data-ttu-id="95001-153">**Iuianimationmanager:: setmanagereventhandler**</span><span class="sxs-lookup"><span data-stu-id="95001-153">**IUIAnimationManager::SetManagerEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[<span data-ttu-id="95001-154">**Iuianimationmanager:: Update**</span><span class="sxs-lookup"><span data-stu-id="95001-154">**IUIAnimationManager::Update**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[<span data-ttu-id="95001-155">**Iuianimationtimer:: getTime**</span><span class="sxs-lookup"><span data-stu-id="95001-155">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="95001-156">**Iuianimationtimer:: lttimerupdatehandler**</span><span class="sxs-lookup"><span data-stu-id="95001-156">**IUIAnimationTimer::SetTimerUpdateHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

<span data-ttu-id="95001-157">[**Uianimationmanager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95001-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="95001-158">[**Uianimationtimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95001-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="95001-159">Übersicht über Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="95001-159">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 
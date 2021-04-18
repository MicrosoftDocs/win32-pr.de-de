---
description: Steuern eines externen Geräts
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: Steuern eines externen Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cb82de59877f2527c92da9123d8a9d5a59d41e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520723"
---
# <a name="controlling-an-external-device"></a><span data-ttu-id="cc54c-103">Steuern eines externen Geräts</span><span class="sxs-lookup"><span data-stu-id="cc54c-103">Controlling an External Device</span></span>

<span data-ttu-id="cc54c-104">Um ein Video Tape Recorder (VTR)-Gerät zu steuern, verwenden Sie die [**IAMExtTransport::p UT \_ Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) -Methode.</span><span class="sxs-lookup"><span data-stu-id="cc54c-104">To control a video tape recorder (VTR) device, use the [**IAMExtTransport::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) method.</span></span> <span data-ttu-id="cc54c-105">Geben Sie den neuen Status an, indem Sie eine der Konstanten verwenden, die im [Geräte Transport Status](device-transport-state.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cc54c-105">Specify the new state by using one of the constants listed in the [Device Transport State](device-transport-state.md).</span></span> <span data-ttu-id="cc54c-106">Um z. b. das Gerät anzuhalten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="cc54c-106">For example, to stop the device, use the following:</span></span>


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



<span data-ttu-id="cc54c-107">Da es sich bei VTR um ein physisches Gerät handelt, gibt es in der Regel eine Verzögerung zwischen der Ausgabe des Befehls und dem Abschluss des Befehls.</span><span class="sxs-lookup"><span data-stu-id="cc54c-107">Because the VTR is a physical device, there is typically a lag between issuing the command and when the command completes.</span></span> <span data-ttu-id="cc54c-108">Ihre Anwendung sollte einen zweiten Arbeits Thread erstellen, der auf den Abschluss des Befehls wartet.</span><span class="sxs-lookup"><span data-stu-id="cc54c-108">Your application should create a second worker thread that waits for the command to finish.</span></span> <span data-ttu-id="cc54c-109">Wenn der Befehl abgeschlossen ist, kann der Thread die Benutzeroberfläche aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cc54c-109">When the command finishes, the thread can update the user interface.</span></span> <span data-ttu-id="cc54c-110">Verwenden Sie einen kritischen Abschnitt, um die Statusänderung zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="cc54c-110">Use a critical section to serialize the state change.</span></span>

<span data-ttu-id="cc54c-111">Die Anwendung kann von einigen VTRs benachrichtigt werden, wenn sich der Transportzustand des Geräts geändert hat.</span><span class="sxs-lookup"><span data-stu-id="cc54c-111">Some VTRs can notify the application when the device's transport state has changed.</span></span> <span data-ttu-id="cc54c-112">Wenn das Gerät dieses Feature unterstützt, kann der Arbeits Thread auf die Benachrichtigung warten.</span><span class="sxs-lookup"><span data-stu-id="cc54c-112">If the device supports this feature, the worker thread can wait for the notification.</span></span> <span data-ttu-id="cc54c-113">Gemäß der "AV/C Tape Recorder/Player subunit Specification" der 1394-Handels Association ist der Befehl für die Transport Zustands Benachrichtigung jedoch optional, was bedeutet, dass Geräte diese nicht unterstützen müssen.</span><span class="sxs-lookup"><span data-stu-id="cc54c-113">According to the 1394 Trade Association's "AV/C Tape Recorder/Player Subunit Specification", however, the transport-state notification command is optional, meaning devices are not required to support it.</span></span> <span data-ttu-id="cc54c-114">Wenn eine Benachrichtigung von einem Gerät nicht unterstützt wird, sollten Sie das Gerät in regelmäßigen Abständen nach dem aktuellen Statusabfragen.</span><span class="sxs-lookup"><span data-stu-id="cc54c-114">If a device does not support notification, you should poll the device at periodic intervals for its current state.</span></span>

<span data-ttu-id="cc54c-115">In diesem Abschnitt wird zunächst der Benachrichtigungs Mechanismus beschrieben. Anschließend wird der Abruf von Geräten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cc54c-115">This section first describes the notification mechanism, and then describes device polling.</span></span>

<span data-ttu-id="cc54c-116">Verwenden der Transport Zustands Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="cc54c-116">Using Transport State Notification</span></span>

<span data-ttu-id="cc54c-117">Die Transport Zustands Benachrichtigung bewirkt, dass der Treiber ein Ereignis signalisiert, wenn der Transport in einen neuen Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="cc54c-117">Transport state notification works by having the driver signal an event when the transport switches to a new state.</span></span> <span data-ttu-id="cc54c-118">Deklarieren Sie in der Anwendung einen kritischen Abschnitt, ein Ereignis und ein Thread handle.</span><span class="sxs-lookup"><span data-stu-id="cc54c-118">In your application, declare a critical section, an event, and a thread handle.</span></span> <span data-ttu-id="cc54c-119">Der Abschnitt kritisch wird verwendet, um den Gerätezustand zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="cc54c-119">The critical section is used to synchronize the device state.</span></span> <span data-ttu-id="cc54c-120">Das-Ereignis wird verwendet, um den Arbeits Thread anzuhalten, wenn die Anwendung beendet wird:</span><span class="sxs-lookup"><span data-stu-id="cc54c-120">The event is used to halt the worker thread when the application exits:</span></span>


```C++
HANDLE hThread = 0;
HANDLE hThreadEnd = CreateEvent(NULL, TRUE, FALSE, NULL); 
if (hThreadEnd == NULL)
{
    // Handle error.
}
CRITICAL_SECTION csIssueCmd;
InitializeCriticalSection(&cdIssueCmd);
```



<span data-ttu-id="cc54c-121">Nachdem Sie eine Instanz des Erfassungs Filters erstellt haben, erstellen Sie den Arbeits Thread:</span><span class="sxs-lookup"><span data-stu-id="cc54c-121">After you create an instance of the capture filter, create the worker thread:</span></span>


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



<span data-ttu-id="cc54c-122">Starten Sie im Arbeits Thread, indem Sie die [**IAMExtTransport:: GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) -Methode mit dem Wert Ed \_ Notify \_ hevent \_ Get aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cc54c-122">In the worker thread, start by calling the [**IAMExtTransport::GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) method with the value ED\_NOTIFY\_HEVENT\_GET.</span></span> <span data-ttu-id="cc54c-123">Dieser Rückruf gibt ein Handle für ein Ereignis zurück, das signalisiert wird, wenn ein Vorgang abgeschlossen wird:</span><span class="sxs-lookup"><span data-stu-id="cc54c-123">This call returns a handle to an event that will be signaled when an operation completes:</span></span>


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



<span data-ttu-id="cc54c-124">Im nächsten Schritt wird **GetState** erneut aufgerufen, und der Wert für die \_ \_ Änderungs \_ Benachrichtigung im ED-Modus wird übergeben</span><span class="sxs-lookup"><span data-stu-id="cc54c-124">Next, call **GetState** again and pass the value ED\_MODE\_CHANGE\_NOTIFY:</span></span>


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



<span data-ttu-id="cc54c-125">Wenn das Gerät eine Benachrichtigung unterstützt, gibt die Methode den Wert E \_ Pending zurück.</span><span class="sxs-lookup"><span data-stu-id="cc54c-125">If the device supports notification, the method returns the value E\_PENDING.</span></span> <span data-ttu-id="cc54c-126">(Andernfalls müssen Sie das Gerät abrufen, wie im nächsten Abschnitt beschrieben.) Wenn das Gerät eine Benachrichtigung unterstützt, wird das Ereignis immer dann signalisiert, wenn sich der Status des VTR-Transports ändert.</span><span class="sxs-lookup"><span data-stu-id="cc54c-126">(Otherwise, you must poll device, as described in the next section.) Assuming the device supports notification, the event will be signaled whenever the state of the VTR transport changes.</span></span> <span data-ttu-id="cc54c-127">An diesem Punkt können Sie die Benutzeroberfläche aktualisieren, um den neuen Zustand widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="cc54c-127">At this point, you can update the user interface to reflect the new state.</span></span> <span data-ttu-id="cc54c-128">Wenn Sie die nächste Benachrichtigung abrufen möchten, setzen Sie das Ereignis Handle zurück, und wenden Sie erneut " **GetStatus** " auf " \_ \_ \_ Benachrichtigung Benachrichtigen".</span><span class="sxs-lookup"><span data-stu-id="cc54c-128">To get the next notification, reset the event handle and call **GetStatus** with ED\_MODE\_CHANGE\_NOTIFY again.</span></span>

<span data-ttu-id="cc54c-129">Bevor der Arbeits Thread beendet wird, geben Sie das Ereignis Handle frei, indem Sie **GetStatus** mit dem Flag Ed \_ Notification \_ hevent \_ Release und der Adresse des Handles aufrufen:</span><span class="sxs-lookup"><span data-stu-id="cc54c-129">Before the worker thread exits, release the event handle by calling **GetStatus** with the flag ED\_NOTIFY\_HEVENT\_RELEASE and the address of the handle:</span></span>


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



<span data-ttu-id="cc54c-130">Der folgende Code zeigt die gesamte Thread Prozedur.</span><span class="sxs-lookup"><span data-stu-id="cc54c-130">The following code shows the complete thread procedure.</span></span> <span data-ttu-id="cc54c-131">Es wird davon ausgegangen, dass die Funktion "updatetransportstate" eine Anwendungsfunktion ist, die die Benutzeroberfläche aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cc54c-131">The function UpdateTransportState is assumed to be an application function that updates the user interface.</span></span> <span data-ttu-id="cc54c-132">Beachten Sie, dass der Thread auf zwei Ereignisse wartet: das Benachrichtigungs Ereignis (*hnotify*) und das Thread Beendigungs Ereignis (*hthreadend*).</span><span class="sxs-lookup"><span data-stu-id="cc54c-132">Note that the thread waits for two events: the notification event (*hNotify*) and the thread-termination event (*hThreadEnd*).</span></span> <span data-ttu-id="cc54c-133">Beachten Sie auch, dass der kritische Abschnitt verwendet wird, um die Geräte Zustands Variable zu schützen.</span><span class="sxs-lookup"><span data-stu-id="cc54c-133">Also note where the critical section is used to protect the device state variable.</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    HANDLE  EventHandles[2];
    HANDLE  hNotify = NULL;
    DWORD   WaitStatus;
    LONG    State;

    // Get the notification event handle. This event will be signaled when
    // the next state-change operation completes.   
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);

    while (hThread && hNotify && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);
        // Ask the device to notify us when the state changes.
        hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
        LeaveCriticalSection(&csIssueCmd); 

        if(hr == E_PENDING)  // The device supports notification.
        {
            // Wait for the notification.
            EventHandles[0] = hNotify;
            EventHandles[1] = hThreadEnd;
            WaitStatus = WaitForMultipleObjects(2, EventHandles, FALSE, INFINITE);
            if(WAIT_OBJECT_0 == WaitStatus) 
            {
                // We got notified. Query for the new state.
                EnterCriticalSection(&csIssueCmd);  
                hr = m_pTransport->get_Mode(State);
                UpdateTransportState(State);  // Update the UI.
                LeaveCriticalSection(&m_csIssueCmd);
                ResetEvent(hNotify);
            } 
            else {
                break;  // End this thread.
            }
        } 
        else {          
            // The device does not support notification.
            PollDevice();        
        } 
    } // while

    // Cancel notification. 
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify);
    return 1; 
}
```



<span data-ttu-id="cc54c-134">Verwenden Sie außerdem den Abschnitt kritisch, wenn Sie Befehle an das Gerät ausgeben, wie im folgenden beschrieben:</span><span class="sxs-lookup"><span data-stu-id="cc54c-134">Also use the critical section when you issue commands to the device, as follows:</span></span>


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



<span data-ttu-id="cc54c-135">Bevor die Anwendung beendet wird, stoppen Sie den sekundären Thread, indem Sie das Thread-End-Ereignis festlegen:</span><span class="sxs-lookup"><span data-stu-id="cc54c-135">Before the application exits, halt the secondary thread by setting the thread-end event:</span></span>


```C++
if (hThread) 
{
    // Signaling this event will cause the thread to end.    
    if (SetEvent(hThreadEnd))
    {
        // Wait for it to end.
        WaitForSingleObjectEx(hThread, INFINITE, FALSE);
    }
}
CloseHandle(hThreadEnd);
CloseHandle(hThread);
```



<span data-ttu-id="cc54c-136">Abrufen des Transport Zustands</span><span class="sxs-lookup"><span data-stu-id="cc54c-136">Polling the Transport State</span></span>

<span data-ttu-id="cc54c-137">Wenn Sie **IAMExtTransport:: GetStatus** mit dem Flag zum \_ Benachrichtigen von Änderungen im ED-Modus aufrufen \_ \_ und der Rückgabewert nicht E \_ Pending ist, bedeutet dies, dass das Gerät keine Benachrichtigung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cc54c-137">If you call **IAMExtTransport::GetStatus** with the ED\_MODE\_CHANGE\_NOTIFY flag and the return value is not E\_PENDING, it means the device does not support notification.</span></span> <span data-ttu-id="cc54c-138">In diesem Fall müssen Sie das Gerät Abfragen, um seinen Status zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cc54c-138">In that case, you must poll the device to determine its state.</span></span> <span data-ttu-id="cc54c-139">Abruf *bedeutet einfach,* dass Sie in regelmäßigen Abständen den Abruf **\_ Modus** aufrufen, um den Transport Status zu überprüfen</span><span class="sxs-lookup"><span data-stu-id="cc54c-139">*Polling* simply means calling **get\_Mode** at regular intervals to check the transport state.</span></span> <span data-ttu-id="cc54c-140">Sie sollten weiterhin einen sekundären Thread und einen kritischen Abschnitt verwenden, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cc54c-140">You should still use a secondary thread and a critical section, as described earlier.</span></span> <span data-ttu-id="cc54c-141">Der Thread fragt das Gerät in regelmäßigen Abständen nach seinem Status ab.</span><span class="sxs-lookup"><span data-stu-id="cc54c-141">The thread queries the device for its state at a regular interval.</span></span> <span data-ttu-id="cc54c-142">Das folgende Beispiel zeigt eine Möglichkeit, den Thread zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="cc54c-142">The following example shows one way to implement the thread:</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    LONG State;
    DWORD WaitStatus;

    while (hThread && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);  
        State = 0;
        hr = pTransport->get_Mode(&State);
        LeaveCriticalSection(&csIssueCmd); 
        UpdateTransportState(State);

        // Wait for a while, or until the thread ends. 
        WaitStatus = WaitForSingleObjectEx(hThreadEnd, 200, FALSE); 
        if (WaitStatus == WAIT_OBJECT_0)
        {
            break; // Exit thread now. 
        }
        // Otherwise, the wait timed out. Time to poll again.
    }
    return 1;
}
```



## <a name="related-topics"></a><span data-ttu-id="cc54c-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc54c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc54c-144">Steuern eines DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="cc54c-144">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




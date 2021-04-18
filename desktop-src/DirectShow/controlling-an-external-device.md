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
# <a name="controlling-an-external-device"></a>Steuern eines externen Geräts

Um ein Video Tape Recorder (VTR)-Gerät zu steuern, verwenden Sie die [**IAMExtTransport::p UT \_ Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) -Methode. Geben Sie den neuen Status an, indem Sie eine der Konstanten verwenden, die im [Geräte Transport Status](device-transport-state.md)aufgeführt sind. Um z. b. das Gerät anzuhalten, verwenden Sie Folgendes:


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



Da es sich bei VTR um ein physisches Gerät handelt, gibt es in der Regel eine Verzögerung zwischen der Ausgabe des Befehls und dem Abschluss des Befehls. Ihre Anwendung sollte einen zweiten Arbeits Thread erstellen, der auf den Abschluss des Befehls wartet. Wenn der Befehl abgeschlossen ist, kann der Thread die Benutzeroberfläche aktualisieren. Verwenden Sie einen kritischen Abschnitt, um die Statusänderung zu serialisieren.

Die Anwendung kann von einigen VTRs benachrichtigt werden, wenn sich der Transportzustand des Geräts geändert hat. Wenn das Gerät dieses Feature unterstützt, kann der Arbeits Thread auf die Benachrichtigung warten. Gemäß der "AV/C Tape Recorder/Player subunit Specification" der 1394-Handels Association ist der Befehl für die Transport Zustands Benachrichtigung jedoch optional, was bedeutet, dass Geräte diese nicht unterstützen müssen. Wenn eine Benachrichtigung von einem Gerät nicht unterstützt wird, sollten Sie das Gerät in regelmäßigen Abständen nach dem aktuellen Statusabfragen.

In diesem Abschnitt wird zunächst der Benachrichtigungs Mechanismus beschrieben. Anschließend wird der Abruf von Geräten beschrieben.

Verwenden der Transport Zustands Benachrichtigung

Die Transport Zustands Benachrichtigung bewirkt, dass der Treiber ein Ereignis signalisiert, wenn der Transport in einen neuen Zustand wechselt. Deklarieren Sie in der Anwendung einen kritischen Abschnitt, ein Ereignis und ein Thread handle. Der Abschnitt kritisch wird verwendet, um den Gerätezustand zu synchronisieren. Das-Ereignis wird verwendet, um den Arbeits Thread anzuhalten, wenn die Anwendung beendet wird:


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



Nachdem Sie eine Instanz des Erfassungs Filters erstellt haben, erstellen Sie den Arbeits Thread:


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



Starten Sie im Arbeits Thread, indem Sie die [**IAMExtTransport:: GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) -Methode mit dem Wert Ed \_ Notify \_ hevent \_ Get aufrufen. Dieser Rückruf gibt ein Handle für ein Ereignis zurück, das signalisiert wird, wenn ein Vorgang abgeschlossen wird:


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



Im nächsten Schritt wird **GetState** erneut aufgerufen, und der Wert für die \_ \_ Änderungs \_ Benachrichtigung im ED-Modus wird übergeben


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



Wenn das Gerät eine Benachrichtigung unterstützt, gibt die Methode den Wert E \_ Pending zurück. (Andernfalls müssen Sie das Gerät abrufen, wie im nächsten Abschnitt beschrieben.) Wenn das Gerät eine Benachrichtigung unterstützt, wird das Ereignis immer dann signalisiert, wenn sich der Status des VTR-Transports ändert. An diesem Punkt können Sie die Benutzeroberfläche aktualisieren, um den neuen Zustand widerzuspiegeln. Wenn Sie die nächste Benachrichtigung abrufen möchten, setzen Sie das Ereignis Handle zurück, und wenden Sie erneut " **GetStatus** " auf " \_ \_ \_ Benachrichtigung Benachrichtigen".

Bevor der Arbeits Thread beendet wird, geben Sie das Ereignis Handle frei, indem Sie **GetStatus** mit dem Flag Ed \_ Notification \_ hevent \_ Release und der Adresse des Handles aufrufen:


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



Der folgende Code zeigt die gesamte Thread Prozedur. Es wird davon ausgegangen, dass die Funktion "updatetransportstate" eine Anwendungsfunktion ist, die die Benutzeroberfläche aktualisiert. Beachten Sie, dass der Thread auf zwei Ereignisse wartet: das Benachrichtigungs Ereignis (*hnotify*) und das Thread Beendigungs Ereignis (*hthreadend*). Beachten Sie auch, dass der kritische Abschnitt verwendet wird, um die Geräte Zustands Variable zu schützen.


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



Verwenden Sie außerdem den Abschnitt kritisch, wenn Sie Befehle an das Gerät ausgeben, wie im folgenden beschrieben:


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



Bevor die Anwendung beendet wird, stoppen Sie den sekundären Thread, indem Sie das Thread-End-Ereignis festlegen:


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



Abrufen des Transport Zustands

Wenn Sie **IAMExtTransport:: GetStatus** mit dem Flag zum \_ Benachrichtigen von Änderungen im ED-Modus aufrufen \_ \_ und der Rückgabewert nicht E \_ Pending ist, bedeutet dies, dass das Gerät keine Benachrichtigung unterstützt. In diesem Fall müssen Sie das Gerät Abfragen, um seinen Status zu ermitteln. Abruf *bedeutet einfach,* dass Sie in regelmäßigen Abständen den Abruf **\_ Modus** aufrufen, um den Transport Status zu überprüfen Sie sollten weiterhin einen sekundären Thread und einen kritischen Abschnitt verwenden, wie zuvor beschrieben. Der Thread fragt das Gerät in regelmäßigen Abständen nach seinem Status ab. Das folgende Beispiel zeigt eine Möglichkeit, den Thread zu implementieren:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




---
description: Steuern eines externen Geräts
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: Steuern eines externen Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f530bb48f35a6e35a0ab75d0559cc3c6770c4d0d1dfb2948f871982f70eb0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652130"
---
# <a name="controlling-an-external-device"></a>Steuern eines externen Geräts

Verwenden Sie zum Steuern eines VTR-Geräts (Video Tape Recorder) die [**IAMExtTransport::p ut \_ Mode-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) Geben Sie den neuen Zustand mithilfe einer der Konstanten an, die unter [Gerätetransportstatus](device-transport-state.md)aufgeführt sind. Verwenden Sie beispielsweise Folgendes, um das Gerät zu beenden:


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



Da es sich bei der VTR um ein physisches Gerät handelt, kommt es in der Regel zu einer Verzögerung zwischen der Ausgabe des Befehls und dem Abschluss des Befehls. Ihre Anwendung sollte einen zweiten Arbeitsthread erstellen, der auf den Abschluss des Befehls wartet. Wenn der Befehl abgeschlossen ist, kann der Thread die Benutzeroberfläche aktualisieren. Verwenden Sie einen kritischen Abschnitt, um die Zustandsänderung zu serialisieren.

Einige VTRs können die Anwendung benachrichtigen, wenn sich der Transportstatus des Geräts geändert hat. Wenn das Gerät dieses Feature unterstützt, kann der Arbeitsthread auf die Benachrichtigung warten. Gemäß der AV/C Tape Recorder/Player-Untereinheitsspezifikation der Trade Association von 1394 ist der Transportzustandsbenachrichtigungsbefehl jedoch optional, d.h. Geräte müssen ihn nicht unterstützen. Wenn ein Gerät keine Benachrichtigung unterstützt, sollten Sie das Gerät in regelmäßigen Abständen nach seinem aktuellen Zustand abfragen.

In diesem Abschnitt wird zunächst der Benachrichtigungsmechanismus und dann das Abfragen von Geräten beschrieben.

Verwenden von Transportstatusbenachrichtigungen

Die Transportzustandsbenachrichtigung funktioniert, indem der Treiber ein Ereignis signalisiert, wenn der Transport in einen neuen Zustand wechselt. Deklarieren Sie in Ihrer Anwendung einen kritischen Abschnitt, ein Ereignis und ein Threadhandle. Der kritische Abschnitt wird verwendet, um den Gerätezustand zu synchronisieren. Das -Ereignis wird verwendet, um den Arbeitsthread anzuhalten, wenn die Anwendung beendet wird:


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



Nachdem Sie eine Instanz des Erfassungsfilters erstellt haben, erstellen Sie den Arbeitsthread:


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



Rufen Sie im Arbeitsthread zunächst die [**IAMExtTransport::GetStatus-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) mit dem Wert ED \_ NOTIFY \_ HEVENT \_ GET auf. Dieser Aufruf gibt ein Handle für ein Ereignis zurück, das signalisiert wird, wenn ein Vorgang abgeschlossen ist:


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



Rufen Sie als Nächstes GetState erneut **auf,** und übergeben Sie den Wert ED \_ MODE CHANGE \_ \_ NOTIFY:


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



Wenn das Gerät Benachrichtigungen unterstützt, gibt die Methode den Wert E \_ PENDING zurück. (Andernfalls müssen Sie das Gerät wie im nächsten Abschnitt beschrieben abfragen.) Wenn das Gerät Benachrichtigungen unterstützt, wird das Ereignis immer dann signalisiert, wenn sich der Status des VTR-Transports ändert. An diesem Punkt können Sie die Benutzeroberfläche aktualisieren, um den neuen Zustand widerzuspiegeln. Um die nächste Benachrichtigung zu erhalten, setzen Sie das Ereignishandle zurück, und rufen **Sie GetStatus** mit ED \_ MODE CHANGE NOTIFY erneut \_ \_ auf.

Bevor der Arbeitsthread beendet wird, geben Sie das Ereignishandle frei, indem **Sie GetStatus** mit dem Flag ED \_ NOTIFY \_ HEVENT RELEASE und der Adresse des \_ Handles aufrufen:


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



Der folgende Code zeigt die vollständige Threadprozedur. Die Funktion UpdateTransportState wird als Anwendungsfunktion angenommen, die die Benutzeroberfläche aktualisiert. Beachten Sie, dass der Thread auf zwei Ereignisse wartet: das Benachrichtigungsereignis (*hNotify*) und das Threadbeendigungsereignis (*hThreadEnd*). Beachten Sie außerdem, wo der kritische Abschnitt verwendet wird, um die Gerätezustandsvariable zu schützen.


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



Verwenden Sie beim Ausführen von Befehlen für das Gerät auch den Abschnitt kritisch wie folgt:


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



Halten Sie den sekundären Thread an, bevor die Anwendung beendet wird, indem Sie das Thread-End-Ereignis festlegen:


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



Abfragen des Transportzustands

Wenn Sie **IAMExtTransport::GetStatus** mit dem \_ ED MODE \_ CHANGE NOTIFY-Flag aufrufen und der \_ Rückgabewert nicht E \_ PENDING lautet, bedeutet dies, dass das Gerät keine Benachrichtigung unterstützt. In diesem Fall müssen Sie das Gerät abfragen, um seinen Zustand zu bestimmen. *Abrufen* bedeutet einfach, dass **der \_ get-Modus** in regelmäßigen Abständen aufgerufen wird, um den Transportstatus zu überprüfen. Sie sollten weiterhin einen sekundären Thread und einen kritischen Abschnitt verwenden, wie zuvor beschrieben. Der Thread fragt das Gerät in regelmäßigen Abständen nach seinem Zustand ab. Das folgende Beispiel zeigt eine Möglichkeit, den Thread zu implementieren:


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

[Steuern eines DV-Dvds](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




---
description: Schreiben der Datei
ms.assetid: d3dbe6ab-810c-4798-a769-c3f00c52a93a
title: Schreiben der Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda23b144956ab5afca9dd733b29a6f9d639cddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360120"
---
# <a name="writing-the-file"></a>Schreiben der Datei

Um die Datei zu schreiben, führen Sie einfach das Filter Diagramm aus, indem Sie die [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) -Methode aufrufen. Warten Sie, bis die Wiedergabe vollständig ist, und beenden Sie das Diagramm explizit durch Aufrufen von [**IMediaControl:: beenden**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); Andernfalls wird die Datei nicht ordnungsgemäß geschrieben.

Um den Fortschritt des Datei Schreibvorgangs anzuzeigen, Fragen Sie den MUX-Filter nach der [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle ab. Rufen Sie die [**imediaseeking:: getduration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) -Methode auf, um die Dauer der Datei abzurufen. Wenn das Diagramm ausgeführt wird, rufen Sie die [**imediaseeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) -Methode regelmäßig auf, um die aktuelle Position des Diagramms im Stream abzurufen. Die aktuelle Position dividiert durch die Dauer gibt den Prozentsatz an.

> [!Note]  
> Eine Anwendung fragt in der Regel den Filter Graph-Manager nach **imediaseeking** ab, aber das Schreiben von Dateien stellt eine Ausnahme von dieser Regel dar. Der Filter Graph-Manager berechnet die aktuelle Position von der Startposition und die Ausführungsdauer des Diagramms, was für die Wiedergabe von Dateien, jedoch nicht für das Schreiben von Dateien, korrekt ist. Um ein genaues Ergebnis zu erhalten, sollten Sie daher die Position aus dem MUX-Filter abrufen.

 

Der folgende Code Ruft die Dauer der Datei ab, startet einen Timer, um die Benutzeroberfläche der Anwendung zu aktualisieren, und führt das Filter Diagramm aus. (Die Fehlerüberprüfung wird aus Gründen der Übersichtlichkeit ausgelassen.)


```C++
IMediaSeeking *pSeek = NULL;
IMediaEventEx *pEvent = NULL;
IMediaControl *pControl = NULL;
REFERENCE_TIME rtTotal;

// Query for interfaces. Remember to release them later.
hr = pMux->QueryInterface(IID_IMediaSeeking, (void**)&pSeek);
hr = pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEvent);
hr = pGraph->QueryInterface(IID_IMediaControl, (void**)&pControl);

// Error checking is omitted for clarity.

// Set the DirectShow event notification window.
hr = pEvent->SetNotifyWindow((OAHWND)hwnd, WM_GRAPHNOTIFY, 0);

// Set the range of the progress bar to the file length (in seconds).
hr = pSeek->GetDuration(&rtTotal);
SendDlgItemMessage(hwnd, IDC_PROGRESS1, PBM_SETRANGE, 0, 
   MAKELPARAM(0, rtTotal / 10000000));
// Start the timer.
UINT_PTR res = SetTimer(hwnd, nIDEvent, 100, NULL);
// Run the graph.
pControl->Run();
```



Wenn die Anwendung ein Timer-Ereignis empfängt, kann Sie die Benutzeroberfläche mit der aktuellen Position aktualisieren:


```C++
void OnTimer(HWND hDlg, IMediaSeeking *pSeek)
{
    REFERENCE_TIME rtNow;
    HRESULT hr = pSeek->GetCurrentPosition(&rtNow);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(hDlg, IDC_PROGRESS1, PBM_SETPOS, rtNow/10000000, 0);
    }
}
```



Wenn die Anwendung ein DirectShow-Abschluss Ereignis empfängt, sollte Sie das Diagramm beenden, wie im folgenden Code gezeigt:


```C++
// Application window procedure
LRESULT CALLBACK WndProc(HWND hDlg, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch (msg)
    {
    /*  ...  */
    case WM_GRAPHNOTIFY:
        DoHandleEvent();
        break;
    /*  ...  */
    }
}

void DoHandleEvent()
{
    long evCode, param1, param2;
    bool bComplete = false;
    if (!pEvent) return;

    // Get all the events, and see we're done.
    while (SUCCEEDED(pEvent->GetEvent(&evCode, &param1, &param2, 0))
    {
        pEvent->FreeEventParams(evCode, param1, param2);
        switch(evCode)
        {
            case EC_USERABORT:
            case EC_ERRORABORT:
            case EC_COMPLETE:
                bComplete = true;
                break;
        }
    }
    if (bComplete)
    {
        pControl->Stop(); // Important! You must stop the graph!

        // Turn off event notification.
        pEvent->SetNotifyWindow(NULL, 0, 0);
        pEvent->Release();
        pEvent = NULL;
        // Reset the progress bar to zero and get rid of the timer.
        SendDlgItemMessage(IDC_PROGRESS1, PBM_SETPOS, 0, 0);
        KillTimer(hwnd, nIDEvent);
    }
}
```



 

 




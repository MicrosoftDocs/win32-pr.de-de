---
description: Schreiben der Datei
ms.assetid: d3dbe6ab-810c-4798-a769-c3f00c52a93a
title: Schreiben der Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cabb5575f371c6525e58cc8ede7d05c2701acc31be325af46e3b00e6e2d8d20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051399"
---
# <a name="writing-the-file"></a>Schreiben der Datei

Um die Datei zu schreiben, führen Sie einfach das Filterdiagramm aus, indem Sie die [**IMediaControl::Run-Methode**](/windows/desktop/api/Control/nf-control-imediacontrol-run) aufrufen. Warten Sie, bis die Wiedergabe abgeschlossen ist, und beenden Sie den Graphen explizit, indem [**Sie IMediaControl::Stop aufrufen.**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) Andernfalls wird die Datei nicht ordnungsgemäß geschrieben.

Um den Fortschritt des Dateischreibens anzuzeigen, fragen Sie den Mux-Filter für die [**IMediaSeeking-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) ab. Rufen Sie [**die IMediaSeeking::GetDuration-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) auf, um die Dauer der Datei abzurufen. Rufen Sie während der Ausführung des Graphen regelmäßig die [**IMediaSeeking::GetCurrentPosition-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) auf, um die aktuelle Position des Graphen im Stream abzurufen. Die aktuelle Position dividiert durch die Dauer gibt den prozentsatz abgeschlossenen Prozentsatz an.

> [!Note]  
> Eine Anwendung fragt in der Regel den Filter Graph Manager für **IMediaSeeking** ab, aber das Schreiben von Dateien ist eine Ausnahme von dieser Regel. Der Filter Graph Manager berechnet die aktuelle Position von der Anfangsposition und die Ausführung des Graphen, was für die Dateiwiedergabe, aber nicht für das Schreiben von Dateien korrekt ist. Um ein genaues Ergebnis zu erhalten, sollten Sie daher die Position aus dem MUX-Filter abrufen.

 

Der folgende Code ruft die Dauer der Datei ab, startet einen Timer zum Aktualisieren der Anwendungsbenutzeroberfläche und führt das Filterdiagramm aus. (Die Fehlerüberprüfung wird aus Gründen der Übersichtlichkeit ausgelassen.)


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



Wenn die Anwendung ein Timerereignis empfängt, kann sie die Benutzeroberfläche mit der aktuellen Position aktualisieren:


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



Wenn die Anwendung ein DirectShow-Abschlussereignis empfängt, sollte sie das Diagramm beenden, wie im folgenden Code gezeigt:


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



 

 




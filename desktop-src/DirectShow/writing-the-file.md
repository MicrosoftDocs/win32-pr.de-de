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
# <a name="writing-the-file"></a><span data-ttu-id="d9a5c-103">Schreiben der Datei</span><span class="sxs-lookup"><span data-stu-id="d9a5c-103">Writing the File</span></span>

<span data-ttu-id="d9a5c-104">Um die Datei zu schreiben, führen Sie einfach das Filter Diagramm aus, indem Sie die [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d9a5c-104">To write the file, simply run the filter graph by calling the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method.</span></span> <span data-ttu-id="d9a5c-105">Warten Sie, bis die Wiedergabe vollständig ist, und beenden Sie das Diagramm explizit durch Aufrufen von [**IMediaControl:: beenden**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); Andernfalls wird die Datei nicht ordnungsgemäß geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d9a5c-105">Wait for playback to complete and explicitly stop the graph by calling [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); otherwise the file is not written correctly.</span></span>

<span data-ttu-id="d9a5c-106">Um den Fortschritt des Datei Schreibvorgangs anzuzeigen, Fragen Sie den MUX-Filter nach der [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="d9a5c-106">To display the progress of the file-writing operation, query the Mux filter for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="d9a5c-107">Rufen Sie die [**imediaseeking:: getduration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) -Methode auf, um die Dauer der Datei abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d9a5c-107">Call the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method to retrieve the duration of the file.</span></span> <span data-ttu-id="d9a5c-108">Wenn das Diagramm ausgeführt wird, rufen Sie die [**imediaseeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) -Methode regelmäßig auf, um die aktuelle Position des Diagramms im Stream abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d9a5c-108">Periodically while the graph is running, call the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method to retrieve the graph's current position in the stream.</span></span> <span data-ttu-id="d9a5c-109">Die aktuelle Position dividiert durch die Dauer gibt den Prozentsatz an.</span><span class="sxs-lookup"><span data-stu-id="d9a5c-109">Current position divided by duration gives the percentage complete.</span></span>

> [!Note]  
> <span data-ttu-id="d9a5c-110">Eine Anwendung fragt in der Regel den Filter Graph-Manager nach **imediaseeking** ab, aber das Schreiben von Dateien stellt eine Ausnahme von dieser Regel dar.</span><span class="sxs-lookup"><span data-stu-id="d9a5c-110">An application usually queries the Filter Graph Manager for **IMediaSeeking**, but file writing is an exception to this rule.</span></span> <span data-ttu-id="d9a5c-111">Der Filter Graph-Manager berechnet die aktuelle Position von der Startposition und die Ausführungsdauer des Diagramms, was für die Wiedergabe von Dateien, jedoch nicht für das Schreiben von Dateien, korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="d9a5c-111">The Filter Graph Manager calculates the current position from the starting position and how long the graph has been running, which is accurate for file playback but not for file writing.</span></span> <span data-ttu-id="d9a5c-112">Um ein genaues Ergebnis zu erhalten, sollten Sie daher die Position aus dem MUX-Filter abrufen.</span><span class="sxs-lookup"><span data-stu-id="d9a5c-112">Therefore, to get an accurate result, you should retrieve the position from the MUX filter.</span></span>

 

<span data-ttu-id="d9a5c-113">Der folgende Code Ruft die Dauer der Datei ab, startet einen Timer, um die Benutzeroberfläche der Anwendung zu aktualisieren, und führt das Filter Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="d9a5c-113">The following code gets the duration of the file, starts a timer to update the application UI, and runs the filter graph.</span></span> <span data-ttu-id="d9a5c-114">(Die Fehlerüberprüfung wird aus Gründen der Übersichtlichkeit ausgelassen.)</span><span class="sxs-lookup"><span data-stu-id="d9a5c-114">(Error checking is omitted for clarity.)</span></span>


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



<span data-ttu-id="d9a5c-115">Wenn die Anwendung ein Timer-Ereignis empfängt, kann Sie die Benutzeroberfläche mit der aktuellen Position aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="d9a5c-115">When the application receives a timer event, it can update the UI with the current position:</span></span>


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



<span data-ttu-id="d9a5c-116">Wenn die Anwendung ein DirectShow-Abschluss Ereignis empfängt, sollte Sie das Diagramm beenden, wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d9a5c-116">When the application receives a DirectShow completion event, it should stop the graph, as shown in the following code:</span></span>


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



 

 




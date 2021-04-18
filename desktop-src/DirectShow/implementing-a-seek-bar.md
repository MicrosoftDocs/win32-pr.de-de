---
description: Implementieren einer Suchleiste
ms.assetid: 384f0732-e0c5-4b1f-b590-195e0acf90e1
title: Implementieren einer Suchleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd3f2440c011267c792c79c8bc3550926c5767f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522211"
---
# <a name="implementing-a-seek-bar"></a><span data-ttu-id="3e62c-103">Implementieren einer Suchleiste</span><span class="sxs-lookup"><span data-stu-id="3e62c-103">Implementing a Seek Bar</span></span>

<span data-ttu-id="3e62c-104">In diesem Abschnitt wird beschrieben, wie eine Suchleiste für eine Media Player-Anwendung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="3e62c-104">This section describes how to implement a seek bar for a media-player application.</span></span> <span data-ttu-id="3e62c-105">Die Suchleiste wird als TrackBar-Steuerelement implementiert.</span><span class="sxs-lookup"><span data-stu-id="3e62c-105">The seek bar is implemented as a trackbar control.</span></span> <span data-ttu-id="3e62c-106">Eine Übersicht über die Suche in DirectShow finden Sie unter [Suchen des Filter Diagramms](seeking-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="3e62c-106">For an overview of seeking in DirectShow, see [Seeking the Filter Graph](seeking-the-filter-graph.md).</span></span>

<span data-ttu-id="3e62c-107">Wenn die Anwendung gestartet wird, initialisieren Sie die TrackBar:</span><span class="sxs-lookup"><span data-stu-id="3e62c-107">When the application starts, initialize the trackbar:</span></span>


```C++
void InitSlider(HWND hwnd) 
{
    // Initialize the trackbar range, but disable the 
    // control until the user opens a file.
    hScroll = GetDlgItem(hwnd, IDC_SLIDER1);
    EnableWindow(hScroll, FALSE);
    SendMessage(hScroll, TBM_SETRANGE, TRUE, MAKELONG(0, 100));
}
```



<span data-ttu-id="3e62c-108">Die TrackBar wird deaktiviert, bis der Benutzer eine Mediendatei öffnet.</span><span class="sxs-lookup"><span data-stu-id="3e62c-108">The trackbar is disabled until the user opens a media file.</span></span> <span data-ttu-id="3e62c-109">Der TrackBar-Bereich ist von 0 bis 100 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3e62c-109">The trackbar range is set from 0 to 100.</span></span> <span data-ttu-id="3e62c-110">Während der Wiedergabe der Datei wird die Wiedergabe Position von der Anwendung als Prozentsatz der Datei Dauer berechnet und die TrackBar entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3e62c-110">During file playback, the application will calculate the playback position as a percentage of the file duration, and update the trackbar accordingly.</span></span> <span data-ttu-id="3e62c-111">Die TrackBar-Position "50" entspricht z. b. immer der Mitte der Datei.</span><span class="sxs-lookup"><span data-stu-id="3e62c-111">For example, trackbar position "50" always corresponds to the middle of the file.</span></span>

<span data-ttu-id="3e62c-112">Wenn der Benutzer eine Datei öffnet, erstellen Sie mithilfe von **RenderFile** ein Diagramm zur Dateiwiedergabe.</span><span class="sxs-lookup"><span data-stu-id="3e62c-112">When the user opens a file, build a file-playback graph using **RenderFile**.</span></span> <span data-ttu-id="3e62c-113">Der Code dafür wird unter wieder [Gabe einer Datei](how-to-play-a-file.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3e62c-113">The code for this is shown in [How To Play a File](how-to-play-a-file.md).</span></span> <span data-ttu-id="3e62c-114">Fragen Sie anschließend den Filter Graph-Manager nach der **imediaseeking** -Schnittstelle ab, und speichern Sie den Schnittstellen Zeiger:</span><span class="sxs-lookup"><span data-stu-id="3e62c-114">Then query the Filter Graph Manager for the **IMediaSeeking** interface and store the interface pointer:</span></span>


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



<span data-ttu-id="3e62c-115">Um zu ermitteln, ob die Datei suchbar ist, rufen Sie entweder die [**imediaseeking:: Checkfunktionen**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) -Methode oder die [**imediaseeking:: getfunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3e62c-115">To determine whether the file is seekable, call either the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method or the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="3e62c-116">Diese Methoden sind fast identisch, ihre Semantik unterscheidet sich jedoch geringfügig.</span><span class="sxs-lookup"><span data-stu-id="3e62c-116">These methods do almost the same thing, but their semantics are slightly different.</span></span> <span data-ttu-id="3e62c-117">Im folgenden Beispiel werden **checkcapabilites** verwendet:</span><span class="sxs-lookup"><span data-stu-id="3e62c-117">The following example uses **CheckCapabilites**:</span></span>


```C++
// Determine if the source is seekable.
BOOL  bCanSeek = FALSE;
DWORD caps = AM_SEEKING_CanSeekAbsolute | AM_SEEKING_CanGetDuration; 
bCanSeek = (S_OK == pSeek->CheckCapabilities(&caps));
if (bCanSeek)
{
    // Enable the trackbar.
    EnableWindow(hScroll, TRUE);

    // Find the file duration.
    pSeek->GetDuration(&g_rtTotalTime);
}
```



<span data-ttu-id="3e62c-118">Das \_ Flag für die Suche nach \_ canseekabsolute überprüft, ob die Quelldatei suchbar ist, und das \_ gesuchte \_ cangetduration-Flag überprüft, ob die Dauer der Datei im Voraus festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3e62c-118">The AM\_SEEKING\_CanSeekAbsolute flag checks whether the source file is seekable, and the AM\_SEEKING\_CanGetDuration flag checks whether the duration of the file can be determined in advance.</span></span> <span data-ttu-id="3e62c-119">Wenn beide Funktionen unterstützt werden, aktiviert die Anwendung die TrackBar und ruft die Datei Dauer ab.</span><span class="sxs-lookup"><span data-stu-id="3e62c-119">If both of the capabilities are supported, the application enables the trackbar and retrieves the file duration.</span></span>

<span data-ttu-id="3e62c-120">Wenn das Diagramm suchbar ist, verwendet die Anwendung einen Timer, um die Position der TrackBar während der Wiedergabe zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3e62c-120">If the graph is seekable, the application will use a timer to update the trackbar position during playback.</span></span> <span data-ttu-id="3e62c-121">Wenn Sie das Filter Diagramm ausführen, um die Datei wiederzugeben, starten Sie das Timer-Ereignis, indem Sie eine der Windows-Timer-Funktionen aufrufen, **z. b**. "".</span><span class="sxs-lookup"><span data-stu-id="3e62c-121">When you run the filter graph to play the file, start the timer event by calling one of the Windows timer functions, such as **SetTimer**.</span></span> <span data-ttu-id="3e62c-122">Weitere Informationen zu Timern finden Sie im Thema "Timer" im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="3e62c-122">For more information about timers, see the topic "Timers" in the Platform SDK.</span></span>


```C++
void StartPlayback(HWND hwnd) 
{
    pControl->Run();
    if (bCanSeek)
    {
        StopTimer(); // Make sure an old timer is not still active.
        nTimerID = SetTimer(hwnd, IDT_TIMER1, TICK_FREQ, (TIMERPROC)NULL);
        if (nTimerID == 0)
        {
            /* Handle Error */
        }
    }
}

void StopTimer() 
{
    if (wTimerID != 0)
    {
        KillTimer(g_hwnd, wTimerID);
        wTimerID = 0;
    }
}
```



<span data-ttu-id="3e62c-123">Verwenden Sie das Timer-Ereignis, um die Position der TrackBar zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3e62c-123">Use the timer event to update the position of the trackbar.</span></span> <span data-ttu-id="3e62c-124">Rufen Sie [**imediaseeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) auf, um die Position der Currant-Wiedergabe abzurufen, und berechnen Sie dann die Position als Prozentsatz der Datei Dauer:</span><span class="sxs-lookup"><span data-stu-id="3e62c-124">Call [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) to retrieve the currant playback position, and then calculate the position as a percentage of the file duration:</span></span>


```C++
case WM_TIMER:
    if (wParam == IDT_TIMER1)
    {
        // Timer should not be running unless we really can seek.
        ASSERT(bCanSeek == TRUE);

        REFERENCE_TIME timeNow;
        if (SUCCEEDED(pSeek->GetCurrentPosition(&timeNow)))
        {
            long sliderTick = (long)((timeNow * 100) / g_rtTotalTime);
            SendMessage( hScroll, TBM_SETPOS, TRUE, sliderTick );
        }
    }
    break;
```



<span data-ttu-id="3e62c-125">Der Benutzer kann auch die TrackBar verschieben, um die Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="3e62c-125">The user can also move the trackbar to seek the file.</span></span> <span data-ttu-id="3e62c-126">Wenn der Benutzer auf das TrackBar-Steuerelement zieht oder klickt, empfängt die Anwendung ein "WM \_ HScroll"-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="3e62c-126">When the user drags or clicks the trackbar control, the application receives a WM\_HSCROLL event.</span></span> <span data-ttu-id="3e62c-127">Das niedrige Wort des *wParam* -Parameters ist die TrackBar-Benachrichtigungs Meldung.</span><span class="sxs-lookup"><span data-stu-id="3e62c-127">The low word of the *wParam* parameter is the trackbar notification message.</span></span> <span data-ttu-id="3e62c-128">Beispielsweise wird der TB \_ -EndTrack am Ende der TrackBar-Aktion gesendet, und der TB-Finger \_ Abdruck wird fortlaufend gesendet, während der Benutzer die TrackBar zieht.</span><span class="sxs-lookup"><span data-stu-id="3e62c-128">For example, TB\_ENDTRACK is sent at the end of the trackbar action, and TB\_THUMBTRACK is sent continuously while the user drags the trackbar.</span></span> <span data-ttu-id="3e62c-129">Der folgende Code zeigt eine Möglichkeit, die WM- \_ HScroll-Nachricht zu behandeln:</span><span class="sxs-lookup"><span data-stu-id="3e62c-129">The following code shows one way to handle the WM\_HSCROLL message:</span></span>


```C++
static OAFilterState state;
static BOOL bStartOfScroll = TRUE;

case WM_HSCROLL:
    short int userReq = LOWORD(wParam);
    if (userReq == TB_ENDTRACK || userReq == TB_THUMBTRACK)
    {
        DWORD dwPosition  = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
        // Pause when the scroll action begins.
        if (bStartOfScroll) 
        {
            pControl->GetState(10, &state);
            bStartOfScroll = FALSE;
            pControl->Pause();
        }
        // Update the position continuously.
        REFERENCE_TIME newTime = (g_rtTotalTime/100) * dwPosition;
        pSeek->SetPositions(&newTime, AM_SEEKING_AbsolutePositioning,
            NULL, AM_SEEKING_NoPositioning);

        // Restore the state at the end.
        if (userReq == TB_ENDTRACK)
        {
            if (state == State_Stopped)
                pControl->Stop();
            else if (state == State_Running) 
                pControl->Run();
            bStartOfScroll = TRUE;
        }
    }
}
```



<span data-ttu-id="3e62c-130">Wenn der Benutzer die TrackBar zieht, gibt die Anwendung eine Reihe von Seek-Befehlen aus, eine für jede \_ empfangene TB-Fingerabdruck Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3e62c-130">If the user drags the trackbar, the application issues a series of seek commands, one for each TB\_THUMBTRACK message that it receives.</span></span> <span data-ttu-id="3e62c-131">Um die Suchvorgänge so reibungslos wie möglich zu gestalten, hält die Anwendung das Diagramm an.</span><span class="sxs-lookup"><span data-stu-id="3e62c-131">To make the seek operations as smooth as possible, the application pauses the graph.</span></span> <span data-ttu-id="3e62c-132">Das Anhalten des Diagramms hält die Wiedergabe an, stellt jedoch sicher, dass das Videofenster aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="3e62c-132">Pausing the graph halts playback but ensures that the video window is updated.</span></span> <span data-ttu-id="3e62c-133">Wenn die Anwendung die TB- \_ EndTrack-Nachricht empfängt, stellt Sie den ursprünglichen Zustand des Diagramms wieder her.</span><span class="sxs-lookup"><span data-stu-id="3e62c-133">When the application receives the TB\_ENDTRACK message, it restores the graph to its original state.</span></span>

 

 




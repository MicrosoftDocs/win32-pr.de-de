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
# <a name="implementing-a-seek-bar"></a>Implementieren einer Suchleiste

In diesem Abschnitt wird beschrieben, wie eine Suchleiste für eine Media Player-Anwendung implementiert wird. Die Suchleiste wird als TrackBar-Steuerelement implementiert. Eine Übersicht über die Suche in DirectShow finden Sie unter [Suchen des Filter Diagramms](seeking-the-filter-graph.md).

Wenn die Anwendung gestartet wird, initialisieren Sie die TrackBar:


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



Die TrackBar wird deaktiviert, bis der Benutzer eine Mediendatei öffnet. Der TrackBar-Bereich ist von 0 bis 100 festgelegt. Während der Wiedergabe der Datei wird die Wiedergabe Position von der Anwendung als Prozentsatz der Datei Dauer berechnet und die TrackBar entsprechend aktualisiert. Die TrackBar-Position "50" entspricht z. b. immer der Mitte der Datei.

Wenn der Benutzer eine Datei öffnet, erstellen Sie mithilfe von **RenderFile** ein Diagramm zur Dateiwiedergabe. Der Code dafür wird unter wieder [Gabe einer Datei](how-to-play-a-file.md)gezeigt. Fragen Sie anschließend den Filter Graph-Manager nach der **imediaseeking** -Schnittstelle ab, und speichern Sie den Schnittstellen Zeiger:


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



Um zu ermitteln, ob die Datei suchbar ist, rufen Sie entweder die [**imediaseeking:: Checkfunktionen**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) -Methode oder die [**imediaseeking:: getfunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) -Methode auf. Diese Methoden sind fast identisch, ihre Semantik unterscheidet sich jedoch geringfügig. Im folgenden Beispiel werden **checkcapabilites** verwendet:


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



Das \_ Flag für die Suche nach \_ canseekabsolute überprüft, ob die Quelldatei suchbar ist, und das \_ gesuchte \_ cangetduration-Flag überprüft, ob die Dauer der Datei im Voraus festgelegt werden kann. Wenn beide Funktionen unterstützt werden, aktiviert die Anwendung die TrackBar und ruft die Datei Dauer ab.

Wenn das Diagramm suchbar ist, verwendet die Anwendung einen Timer, um die Position der TrackBar während der Wiedergabe zu aktualisieren. Wenn Sie das Filter Diagramm ausführen, um die Datei wiederzugeben, starten Sie das Timer-Ereignis, indem Sie eine der Windows-Timer-Funktionen aufrufen, **z. b**. "". Weitere Informationen zu Timern finden Sie im Thema "Timer" im Platform SDK.


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



Verwenden Sie das Timer-Ereignis, um die Position der TrackBar zu aktualisieren. Rufen Sie [**imediaseeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) auf, um die Position der Currant-Wiedergabe abzurufen, und berechnen Sie dann die Position als Prozentsatz der Datei Dauer:


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



Der Benutzer kann auch die TrackBar verschieben, um die Datei zu suchen. Wenn der Benutzer auf das TrackBar-Steuerelement zieht oder klickt, empfängt die Anwendung ein "WM \_ HScroll"-Ereignis. Das niedrige Wort des *wParam* -Parameters ist die TrackBar-Benachrichtigungs Meldung. Beispielsweise wird der TB \_ -EndTrack am Ende der TrackBar-Aktion gesendet, und der TB-Finger \_ Abdruck wird fortlaufend gesendet, während der Benutzer die TrackBar zieht. Der folgende Code zeigt eine Möglichkeit, die WM- \_ HScroll-Nachricht zu behandeln:


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



Wenn der Benutzer die TrackBar zieht, gibt die Anwendung eine Reihe von Seek-Befehlen aus, eine für jede \_ empfangene TB-Fingerabdruck Nachricht. Um die Suchvorgänge so reibungslos wie möglich zu gestalten, hält die Anwendung das Diagramm an. Das Anhalten des Diagramms hält die Wiedergabe an, stellt jedoch sicher, dass das Videofenster aktualisiert wird. Wenn die Anwendung die TB- \_ EndTrack-Nachricht empfängt, stellt Sie den ursprünglichen Zustand des Diagramms wieder her.

 

 




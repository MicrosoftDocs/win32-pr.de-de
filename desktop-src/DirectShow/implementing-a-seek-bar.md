---
description: Implementieren einer Suchleiste
ms.assetid: 384f0732-e0c5-4b1f-b590-195e0acf90e1
title: Implementieren einer Suchleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e86dc52f92a4800639a5dbb1659f70fbe1cfaca7cbc2f0d022df889f970ea5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015548"
---
# <a name="implementing-a-seek-bar"></a>Implementieren einer Suchleiste

In diesem Abschnitt wird beschrieben, wie Sie eine Suchleiste für eine Media Player-Anwendung implementieren. Die Suchleiste wird als Trackbar-Steuerelement implementiert. Eine Übersicht über die Suche in DirectShow finden Sie unter [Suchen des Filters Graph](seeking-the-filter-graph.md).

Initialisieren Sie beim Starten der Anwendung die Trackleiste:


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



Die Trackleiste ist deaktiviert, bis der Benutzer eine Mediendatei öffnet. Der Trackbarbereich wird von 0 bis 100 festgelegt. Während der Dateiwiedergabe berechnet die Anwendung die Wiedergabeposition als Prozentsatz der Dateidauer und aktualisiert die Trackleiste entsprechend. Die Trackbarposition "50" entspricht beispielsweise immer der Mitte der Datei.

Wenn der Benutzer eine Datei öffnet, erstellen Sie mithilfe von **RenderFile** ein Dateiwiedergabediagramm. Der Code dafür wird unter [Wiedergeben einer Datei](how-to-play-a-file.md)gezeigt. Fragen Sie dann den Filter Graph Manager für die **IMediaSeeking-Schnittstelle** ab, und speichern Sie den Schnittstellenzeiger:


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



Um zu bestimmen, ob die Datei gesucht werden kann, rufen Sie entweder die [**IMediaSeeking::CheckCapabilities-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) oder die [**IMediaSeeking::GetCapabilities-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) auf. Diese Methoden machen fast das gleiche, aber ihre Semantik unterscheidet sich geringfügig. Im folgenden Beispiel wird **CheckCapabilites** verwendet:


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



Das AM \_ SEEK \_ CanSeekAbsolute-Flag überprüft, ob die Quelldatei suchbar ist, und das AM \_ SEEK \_ CanGetDuration-Flag überprüft, ob die Dauer der Datei im Voraus bestimmt werden kann. Wenn beide Funktionen unterstützt werden, aktiviert die Anwendung die Trackleiste und ruft die Dateidauer ab.

Wenn das Diagramm gesucht werden kann, verwendet die Anwendung einen Timer, um die Position der Trackleiste während der Wiedergabe zu aktualisieren. Wenn Sie das Filterdiagramm ausführen, um die Datei wiederzuspielen, starten Sie das Timerereignis, indem Sie eine der Windows Timerfunktionen aufrufen, z. B. **SetTimer.** Weitere Informationen zu Timern finden Sie im Thema "Timer" im Plattform-SDK.


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



Verwenden Sie das Timerereignis, um die Position der Trackleiste zu aktualisieren. Rufen Sie [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) auf, um die Currant-Wiedergabeposition abzurufen, und berechnen Sie dann die Position als Prozentsatz der Dateidauer:


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



Der Benutzer kann auch die Trackleiste verschieben, um die Datei zu suchen. Wenn der Benutzer das Trackbar-Steuerelement zieht oder klickt, empfängt die Anwendung ein WM \_ HSCROLL-Ereignis. Das untere Wort des *wParam-Parameters* ist die Trackbarbenachrichtigungsmeldung. Beispielsweise wird TB \_ ENDTRACK am Ende der Trackbaraktion gesendet, und TB \_ THUMBTRACK wird kontinuierlich gesendet, während der Benutzer die Trackleiste zieht. Der folgende Code zeigt eine Möglichkeit, die \_ WM-HSCROLL-Meldung zu behandeln:


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



Wenn der Benutzer die Trackleiste zieht, gibt die Anwendung eine Reihe von Suchbefehlen aus, einen für jede \_ EMPFANGENe TB THUMBTRACK-Nachricht. Um die Suchvorgänge so reibungslos wie möglich zu gestalten, hält die Anwendung das Diagramm an. Durch Anhalten des Diagramms wird die Wiedergabe angehalten, aber es wird sichergestellt, dass das Videofenster aktualisiert wird. Wenn die Anwendung die \_ TB-ENDTRACK-Nachricht empfängt, stellt sie den ursprünglichen Zustand des Diagramms wieder her.

 

 




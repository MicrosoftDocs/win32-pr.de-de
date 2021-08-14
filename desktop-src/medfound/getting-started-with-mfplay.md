---
description: MFPlay ist eine API zum Erstellen von Medienwiedergabeanwendungen in C++.
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: Erste Schritte mit MFPlay
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2afb0b20189501530116c252a4d11a9b3e2d8d0dff07482b1998b73400071e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063493"
---
# <a name="getting-started-with-mfplay"></a>Erste Schritte mit MFPlay

\[MFPlay ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

MFPlay ist eine API zum Erstellen von Medienwiedergabeanwendungen in C++.

Dieses Thema enthält folgende Abschnitte:

-   [Requirements](#requirements)
-   [Informationen zu MFPlay](#about-mfplay)
-   [Wiedergeben einer Mediendatei](#playing-a-media-file)
-   [Steuern der Wiedergabe](#controlling-playback)
-   [Empfangen von Ereignissen vom Player](#receiving-events-from-the-player)
-   [Abrufen von Informationen zu einer Mediendatei](#getting-information-about-a-media-file)
-   [Verwalten der Videowiedergabe](#managing-video-playback)
-   [Einschränkungen von MFPlay](#limitations-of-mfplay)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen

MFPlay erfordert Windows 7.

## <a name="about-mfplay"></a>Informationen zu MFPlay

MFPlay verfügt über ein einfaches Programmiermodell und stellt gleichzeitig den Kernsatz von Features bereit, die die meisten Wiedergabeanwendungen benötigen. Eine Anwendung erstellt ein *Playerobjekt,* das die Wiedergabe steuert. Zum Wiedergeben einer Mediendatei erstellt das Playerobjekt ein *Medienelement,* das zum Abrufen von Informationen über den Inhalt der Mediendatei verwendet werden kann. Die Anwendung steuert die Wiedergabe über Methoden auf der [**IMFPMediaPlayer-Schnittstelle**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) des Playerobjekts. Optional kann die Anwendung Ereignisbenachrichtigungen über eine Rückrufschnittstelle abrufen. Das folgende Diagramm veranschaulicht diesen Prozess.

![Konzeptionelles Diagramm: Anwendung und Player zeigen aufeinander, beide zeigen auf Medienelement, das auf Mediendatei verweist](images/mfplay.png)

## <a name="playing-a-media-file"></a>Wiedergeben einer Mediendatei

Um eine Mediendatei wiederzugeben, rufen Sie die [**MFPCreateMediaPlayer-Funktion**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) auf.


```C++
// Global variables
IMFPMediaPlayer *g_pPlayer = NULL;

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

HRESULT PlayVideo(HWND hwnd, const WCHAR* sURL)
{
    // Create the player object and play a video file.

    return MFPCreateMediaPlayer(
        sURL,
        TRUE,   // Start playback automatically?
        0,      // Flags.
        NULL,   // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



Die [**MFPCreateMediaPlayer-Funktion**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) erstellt eine neue Instanz des MFPlay-Playerobjekts. Die Funktion verwendet die folgenden Parameter:

-   Der erste Parameter ist die URL der datei, die geöffnet werden soll. Dies kann eine lokale Datei oder eine Datei auf einem Medienserver sein.
-   Der zweite Parameter gibt an, ob die Wiedergabe automatisch gestartet wird. Durch Festlegen dieses Paremeters auf **TRUE** wird die Datei wiedergegeben, sobald MFPlay sie lädt.
-   Der dritte Parameter legt verschiedene Optionen fest. Übergeben Sie für die Standardoptionen 0 (null).
-   Der vierte Parameter ist ein Zeiger auf eine optionale Rückrufschnittstelle. Dieser Parameter kann **NULL** sein, wie gezeigt. Der Rückruf wird im Abschnitt [Empfangen von Ereignissen vom Player](#receiving-events-from-the-player)beschrieben.
-   Der fünfte Parameter ist ein Handle für das Anwendungsfenster. Wenn die Mediendatei einen Videostream enthält, wird das Video im Clientbereich dieses Fensters angezeigt. Für die ausschließliche Audiowiedergabe kann dieser Parameter **NULL** sein.

Der letzte Parameter empfängt einen Zeiger auf die [**IMFPMediaPlayer-Schnittstelle**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) des Playerobjekts.

Bevor die Anwendung heruntergefahren wird, stellen Sie sicher, dass Sie den [**IMFPMediaPlayer-Zeiger**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) freigeben. Sie können dies in Ihrem **WM CLOSE-Meldungshandler \_** tun.


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> In diesem Beispiel wird die [SafeRelease-Funktion](saferelease.md) verwendet, um Schnittstellenzeiger freizugeben.

 

Für die einfache Videowiedergabe ist dies der gesamte Code, den Sie benötigen. Im weiteren Verlauf dieses Tutorials erfahren Sie, wie Sie weitere Features hinzufügen, beginnend mit der Steuerung der Wiedergabe.

## <a name="controlling-playback"></a>Steuern der Wiedergabe

Der im vorherigen Abschnitt gezeigte Code gibt die Mediendatei wieder, bis sie das Ende der Datei erreicht. Sie können die Wiedergabe beenden und starten, indem Sie die folgenden Methoden auf der [**IMFPMediaPlayer-Schnittstelle**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) aufrufen:

-   [**IMFPMediaPlayer::P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) hält die Wiedergabe an. Während die Wiedergabe angehalten wird, wird der neueste Videoframe angezeigt, und die Audiodaten sind im Hintergrund.
-   [**IMFPMediaPlayer::Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) beendet die Wiedergabe. Es wird kein Video angezeigt, und die Wiedergabeposition wird auf den Anfang der Datei zurückgesetzt.
-   [**IMFPMediaPlayer::P lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) setzt die Wiedergabe nach dem Beenden oder Anhalten fort.

Der folgende Code hält die Wiedergabe an oder setzt die Wiedergabe fort, wenn Sie die **LEERTASTE** drücken.


```C++
//-------------------------------------------------------------------
// OnKeyDown
//
// Handles the WM_KEYDOWN message.
//-------------------------------------------------------------------

void OnKeyDown(HWND hwnd, UINT vk, BOOL fDown, int cRepeat, UINT flags)
{
    HRESULT hr = S_OK;

    switch (vk)
    {
    case VK_SPACE:

        // Toggle between playback and paused/stopped.
        if (g_pPlayer)
        {
            MFP_MEDIAPLAYER_STATE state = MFP_MEDIAPLAYER_STATE_EMPTY;
            
            g_pPlayer->GetState(&state);

            if (state == MFP_MEDIAPLAYER_STATE_PAUSED ||  
                state == MFP_MEDIAPLAYER_STATE_STOPPED)
            {
                g_pPlayer->Play();
            }
            else if (state == MFP_MEDIAPLAYER_STATE_PLAYING)
            {
                g_pPlayer->Pause();
            }
        }
        break;
    }
}
```



In diesem Beispiel wird die [**IMFPMediaPlayer::GetState-Methode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) zum Abrufen des aktuellen Wiedergabezustands (angehalten, angehalten oder wiedergegeben) und entsprechend angehalten oder fortgesetzt.

## <a name="receiving-events-from-the-player"></a>Empfangen von Ereignissen vom Player

MFPlay verwendet eine Rückrufschnittstelle, um Ereignisse an Ihre Anwendung zu senden. Es gibt zwei Gründe für diesen Rückruf:

-   Die Wiedergabe erfolgt in einem separaten Thread. Während der Wiedergabe können bestimmte Ereignisse auftreten, z. B. das Erreichen des Endes der Datei. MFPlay verwendet den Rückruf, um Ihre Anwendung über das Ereignis zu benachrichtigen.
-   Viele der [**IMFPMediaPlayer-Methoden**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) sind asynchron, d. h., sie geben zurück, bevor der Vorgang abgeschlossen ist. Mit asynchronen Methoden können Sie einen Vorgang über Ihren UI-Thread starten, der lange dauern kann, ohne dass dies zu einer Blockierung der Benutzeroberfläche führt. Nach Abschluss des Vorgangs signalisiert MFPlay den Rückruf.

Implementieren Sie zum Empfangen von Rückrufbenachrichtigungen die [**IMFPMediaPlayerCallback-Schnittstelle.**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) Diese Schnittstelle erbt **IUnknown** und definiert eine einzelne Methode, [**OnMediaPlayerEvent.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) Um den Rückruf einzurichten, übergeben Sie einen Zeiger auf Ihre **IMFPMediaPlayerCallback-Implementierung** im *pCallback-Parameter* der [**MFPCreateMediaPlayer-Funktion.**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)

Hier ist das erste Beispiel aus diesem Tutorial, das geändert wurde, um den Rückruf einzuschließt.


```
// Global variables.
IMFPMediaPlayer *g_pPlayer = NULL;
IMFPMediaPlayerCallback *g_pCallback = NULL;

// Call an application-defined function to create the callback object.
hr = CreateMyCallback(&g_pCallback);

// Create the player object and play a video file.

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

if (SUCCEEDED(hr))
{
    hr = MFPCreateMediaPlayer(
        sURL,
        TRUE,        // Start playback automatically?
        0,           // Flags.
        g_pCallback, // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



Die [**OnMediaPlayerEvent-Methode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) verfügt über einen einzelnen Parameter, der ein Zeiger auf die [**MFP \_ EVENT \_ HEADER-Struktur**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) ist. Der **eEventType-Member** dieser Struktur informiert Sie darüber, welches Ereignis aufgetreten ist. Wenn beispielsweise die Wiedergabe gestartet wird, sendet MFPlay das **MFP \_ EVENT TYPE \_ \_ PLAY-Ereignis.**

Jeder Ereignistyp verfügt über eine entsprechende Datenstruktur, die Informationen für dieses Ereignis enthält. Jede dieser Strukturen beginnt mit einer [**MFP \_ EVENT \_ HEADER-Struktur.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Stellen Sie in Ihrem Rückruf den **MFP \_ EVENT \_ HEADER-Zeiger** in die ereignisspezifische Datenstruktur um. Wenn der Ereignistyp beispielsweise **MFP \_ PLAY \_ EVENT** ist, ist die Datenstruktur [**MFP PLAY \_ \_ EVENT.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) Der folgende Code zeigt, wie dieses Ereignis im Rückruf behandelt wird.


```
void STDMETHODCALLTYPE MediaPlayerCallback::OnMediaPlayerEvent(
    MFP_EVENT_HEADER *pEventHeader
    )
{
    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_PLAY:
        OnPlay(MFP_GET_PLAY_EVENT(pEventHeader));
        break;

    // Other event types (not shown).

    }
}

// Function to handle the event.
void OnPlay(MFP_PLAY_EVENT *pEvent)
{
    if (FAILED(pEvent->header.hrEvent))
    {  
        // Error occurred during playback.
    }  
}
```



In diesem Beispiel wird das [**MFP \_ GET PLAY \_ \_ EVENT-Ereignis**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) verwendet, um den *pEventHeader-Zeiger* in eine [**MFP PLAY \_ \_ EVENT-Struktur**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) zu casten. Das **HRESULT** aus dem Vorgang, der das Ereignis ausgelöst hat, wird im **Feld hrEvent** der Struktur gespeichert.

Eine Liste aller Ereignistypen und der entsprechenden Datenstrukturen finden Sie unter [**MFP \_ EVENT \_ TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).

Hinweis zum Threading: Standardmäßig ruft MFPlay den Rückruf aus demselben Thread auf, der [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)aufgerufen hat. Dieser Thread muss über eine Meldungsschleife verfügen. Alternativ können Sie das **MFP \_ OPTION FREE \_ \_ THREADED \_ CALLBACK-Flag** im *parameter creationOptions* von **MFPCreateMediaPlayer** übergeben. Dieses Flag bewirkt, dass MFPlay Rückrufe aus einem separaten Thread aufruft. Beide Optionen haben Auswirkungen auf Ihre Anwendung. Die Standardoption bedeutet, dass Ihr Rückruf keine Aktionen ausführen kann, die auf ihre Nachrichtenschleife warten, z. B. das Warten auf eine UI-Aktion, da dadurch die Fensterprozedur blockiert wird. Die Freethreadoption bedeutet, dass Sie wichtige Abschnitte verwenden müssen, um alle Daten zu schützen, auf die Sie in Ihrem Rückruf zugreifen. In den meisten Fällen ist die Standardoption am einfachsten.

## <a name="getting-information-about-a-media-file"></a>Abrufen von Informationen zu einer Mediendatei

Wenn Sie eine Mediendatei in MFPlay öffnen, erstellt der Player ein Objekt namens *Medienelement,* das die Mediendatei darstellt. Dieses Objekt macht die [**IMFPMediaItem-Schnittstelle**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) verfügbar, mit der Sie Informationen zur Mediendatei abrufen können. Viele der MFPlay-Ereignisstrukturen enthalten einen Zeiger auf das aktuelle Medienelement. Sie können das aktuelle Medienelement auch abrufen, indem Sie [**IMFPMediaPlayer::GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) auf dem Player aufrufen.

Zwei besonders nützliche Methoden sind [**IMFPMediaItem::HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) und [**IMFPMediaItem::HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio). Diese Methoden fragen ab, ob die Medienquelle Video oder Audio enthält.

Der folgende Code testet beispielsweise, ob die aktuelle Mediendatei einen Videostream enthält.


```
IMFPMediaItem *pItem;
BOOL bHasVideo = FALSE;
BOOL bIsSelected = FALSE;

hr = g_pPlayer->GetMediaItem(TRUE, &pItem);
if (SUCCEEDED(hr))
{
    hr = pItem->HasVideo(&bHasVideo, &bIsSelected);
    pItem->Release();
}
```



Wenn die Quelldatei einen Videostream enthält, der für die Wiedergabe ausgewählt ist, werden *bHasVideo* und *bIsSelected* auf **TRUE** festgelegt.

## <a name="managing-video-playback"></a>Verwalten der Videowiedergabe

Wenn MFPlay eine Videodatei wiedergibt, wird das Video in dem Fenster geschaltet, das Sie in der [**MFPCreateMediaPlayer-Funktion**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) angegeben haben. Dies geschieht in einem separaten Thread, der sich im Besitz der Microsoft Media Foundation Wiedergabepipeline befindet. In den meisten Teilen muss Ihre Anwendung diesen Prozess nicht verwalten. Es gibt jedoch zwei Situationen, in denen die Anwendung MFPlay benachrichtigen muss, um das Video zu aktualisieren.

-   Wenn die Wiedergabe angehalten oder beendet wird, muss MFPlay benachrichtigt werden, sobald das Videofenster der Anwendung eine WM \_ PAINT-Nachricht empfängt. Dies ermöglicht MFPlay das erneute Anstrichen des Fensters.
-   Wenn die Größe des Fensters geändert wird, muss MFPlay benachrichtigt werden, damit das Video entsprechend der neuen Fenstergröße skaliert werden kann.

Die [**IMFPMediaPlayer::UpdateVideo-Methode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) behandelt beide Fälle. Rufen Sie diese Methode in den \_ WM PAINT- und WM \_ SIZE-Meldungshandlern für das Videofenster auf.

> [!IMPORTANT]
> Rufen Sie die GDI **BeginPaint-Funktion** auf, bevor [**Sie UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)aufrufen.

 


```
IMFPMediaPlayer *g_pPlayer;   // MFPlay player object

void OnSize(HWND hwnd, UINT state, int cx, int cy)
{
    HDC hdc;
    PAINTSTRUCT ps;

    if (g_pPlayer && (state == SIZE_RESTORED))
    {
        hdc = BeginPaint(hwnd, &ps);
        g_pPlayer->UpdateVideo();
         EndPaint(hwnd, &ps);
    }
}

void OnPaint(HWND hwnd)
{
    HDC hdc;
    PAINTSTRUCT ps;

    hdc = BeginPaint(hwnd, &ps);
    if (g_pPlayer)
    {
        g_pPlayer->UpdateVideo();
    }
      EndPaint(hwnd, &ps);
}
```



Sofern nicht anders angegeben, zeigt MFPlay das Video bei Bedarf mithilfe von Letterboxing im richtigen Seitenverhältnis an. Wenn Sie das Seitenverhältnis nicht beibehalten möchten, rufen Sie [**IMFPMediaPlayer::SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) mit dem **MfVideoARMode \_ None-Flag** auf. Dies führt dazu, dass MFPlay das Video gestreckt, um das gesamte Rechteck ohne Letterboxing auszufüllen. In der Regel sollten Sie die Standardeinstellung verwenden und MFPlay in das Video schreiben lassen. Die Standardmäßige Letterboxfarbe ist schwarz, aber Sie können dies ändern, indem Sie [**IMFPMediaPlayer::SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor)aufrufen.

## <a name="limitations-of-mfplay"></a>Einschränkungen von MFPlay

Die aktuelle Version von MFPlay weist die folgenden Einschränkungen auf:

-   MFPlay unterstützt keine DRM-geschützten Inhalte.
-   Standardmäßig unterstützt MFPlay keine Netzwerkstreamingprotokolle. Weitere Informationen finden Sie unter [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).
-   MFPlay unterstützt keine serverseitigen Wiedergabelisten (SSPLs) oder andere Quelltypen, die mehr als ein Segment wiedergeben. In technischer Hinsicht beendet MFPlay die Wiedergabe nach der ersten Präsentation und ignoriert alle [MENewPresentation-Ereignisse](menewpresentation.md) aus der Medienquelle.
-   MFPlay unterstützt keine nahtlosen Übergänge zwischen Medienquellen.
-   MFPlay unterstützt nicht das Mischen mehrerer Videostreams.
-   Nur Medienformate, die nativ in Media Foundation unterstützt werden, werden von MFPlay unterstützt. (Dies schließt Media Foundation Komponenten von Drittanbietern ein, die möglicherweise auf dem System installiert sind.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MFPlay für die Audio-/Videowiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 




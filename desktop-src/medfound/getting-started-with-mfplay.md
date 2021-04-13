---
description: MF Play ist eine API zum Erstellen von Medienwiedergabe Anwendungen in C++.
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: Ersten Einstieg in MF Play
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9e0405d3138a22e0d20e94849d416b29d62945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484062"
---
# <a name="getting-started-with-mfplay"></a>Ersten Einstieg in MF Play

\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

MF Play ist eine API zum Erstellen von Medienwiedergabe Anwendungen in C++.

Dieses Thema enthält folgende Abschnitte:

-   [Anforderungen](#requirements)
-   [Informationen zu MF Play](#about-mfplay)
-   [Wiedergeben einer Mediendatei](#playing-a-media-file)
-   [Steuern der Wiedergabe](#controlling-playback)
-   [Empfangen von Ereignissen vom Player](#receiving-events-from-the-player)
-   [Informationen zu einer Mediendatei](#getting-information-about-a-media-file)
-   [Verwalten der Video Wiedergabe](#managing-video-playback)
-   [Einschränkungen von MF Play](#limitations-of-mfplay)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen

MF Play erfordert Windows 7.

## <a name="about-mfplay"></a>Informationen zu MF Play

MF Play verfügt über ein einfaches Programmiermodell und bietet gleichzeitig den Kern Satz von Features, die für die meisten Wiedergabe Anwendungen benötigt werden. Eine Anwendung erstellt ein *Player* -Objekt zum Steuern der Wiedergabe. Zum Wiedergeben einer Mediendatei erstellt das Player-Objekt ein *Medien Element*, das zum erhalten von Informationen über den Inhalt der Mediendatei verwendet werden kann. Die Anwendung steuert die Wiedergabe über Methoden in der [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Schnittstelle des Player-Objekts. Optional kann die Anwendung Ereignis Benachrichtigungen über eine Rückruf Schnittstelle erhalten. das folgende Diagramm veranschaulicht diesen Prozess.

![Konzeptionelle Darstellung: die Anwendung und der Player zeigen aufeinander, beide zeigen auf das Medien Element, das auf die Mediendatei zeigt.](images/mfplay.png)

## <a name="playing-a-media-file"></a>Wiedergeben einer Mediendatei

Um eine Mediendatei wiederzugeben, müssen Sie die [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) -Funktion aufrufen.


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



Die [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) -Funktion erstellt eine neue Instanz des mfplay Player-Objekts. Die Funktion übernimmt die folgenden Parameter:

-   Der erste Parameter ist die URL der Datei, die geöffnet werden soll. Hierbei kann es sich um eine lokale Datei oder eine Datei auf einem Medienserver handeln.
-   Der zweite Parameter gibt an, ob die Wiedergabe automatisch startet. Durch Festlegen dieses Parameters auf " **true**" wird die Datei abgespielt, sobald Sie von mfplay geladen wird.
-   Der dritte Parameter legt verschiedene Optionen fest. Übergeben Sie für die Standardoptionen NULL (0).
-   Der vierte Parameter ist ein Zeiger auf eine optionale Rückruf Schnittstelle. Dieser Parameter kann **null** sein, wie hier gezeigt. Der Rückruf wird im Abschnitt [empfangen von Ereignissen vom Player](#receiving-events-from-the-player)beschrieben.
-   Der fünfte Parameter ist ein Handle für das Anwendungsfenster. Wenn die Mediendatei einen Videostream enthält, wird das Video im Client Bereich dieses Fensters angezeigt. Bei der reinen Audiowiedergabe kann dieser Parameter **null** sein.

Der letzte Parameter erhält einen Zeiger auf die [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Schnittstelle des Player Objekts.

Bevor die Anwendung heruntergefahren wird, stellen Sie sicher, dass Sie den [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Zeiger freigeben. Dies können Sie in Ihrem " **WM \_ Close** Message"-Handler tun.


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> In diesem Beispiel wird die Funktion " [saferelease](saferelease.md) " verwendet, um Schnittstellen Zeiger freizugeben.

 

Für eine einfache Videowiedergabe ist dies der gesamte Code, den Sie benötigen. Im weiteren Verlauf dieses Tutorials erfahren Sie, wie Sie weitere Features hinzufügen, beginnend mit dem Steuern der Wiedergabe.

## <a name="controlling-playback"></a>Steuern der Wiedergabe

Der im vorherigen Abschnitt gezeigte Code gibt die Mediendatei wieder, bis das Ende der Datei erreicht wird. Sie können die Wiedergabe starten, indem Sie die folgenden Methoden für die [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Schnittstelle aufrufen:

-   [**Imfpmediaplayer::P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) hält die Wiedergabe an. Während die Wiedergabe angehalten wird, wird der aktuelle Videoframe angezeigt, und Audiodaten werden automatisch angezeigt.
-   [**Imfpmediaplayer:: beenden**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) beendet die Wiedergabe. Es wird kein Video angezeigt, und die Wiedergabe Position wird auf den Anfang der Datei zurückgesetzt.
-   [**Imfpmediaplayer::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) setzt die Wiedergabe nach dem Beenden oder anhalten fort.

Der folgende Code hält die Wiedergabe an oder nimmt Sie wieder auf, wenn Sie die **LEERTASTE** drücken.


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



In diesem Beispiel wird die [**imfpmediaplayer:: GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) -Methode aufgerufen, um den aktuellen Wiedergabe Zustand (angehalten, angehalten oder wiederzugeben) zu erhalten und entsprechend anzuhalten oder fortzusetzen.

## <a name="receiving-events-from-the-player"></a>Empfangen von Ereignissen vom Player

Mfplay verwendet eine Rückruf Schnittstelle, um Ereignisse an Ihre Anwendung zu senden. Für diesen Rückruf gibt es zwei Gründe:

-   Die Wiedergabe erfolgt in einem separaten Thread. Während der Wiedergabe können bestimmte Ereignisse auftreten, z. b. das Erreichen des Datei Endes. Mfplay verwendet den Rückruf, um die Anwendung über das Ereignis zu benachrichtigen.
-   Viele der [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Methoden sind asynchron, d. h., Sie geben zurück, bevor der Vorgang abgeschlossen wird. Mithilfe von asynchronen Methoden können Sie einen Vorgang aus dem UI-Thread starten, der viel Zeit in Anspruch nimmt, ohne dass die Benutzeroberfläche blockiert wird. Nachdem der Vorgang abgeschlossen wurde, signalisiert MF Play den Rückruf.

Um Rückruf Benachrichtigungen zu empfangen, implementieren Sie die [**imfpmediaplayercallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) -Schnittstelle. Diese Schnittstelle erbt **IUnknown** und definiert eine einzelne Methode, [**onmediaplayerevent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent). Wenn Sie den Rückruf einrichten möchten, übergeben Sie einen Zeiger auf Ihre **imfpmediaplayercallback** -Implementierung im *pCallback* -Parameter der [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) -Funktion.

Im folgenden finden Sie das erste Beispiel aus diesem Tutorial, das so geändert wurde, dass es den Rückruf einschließt.


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



Die [**onmediaplayerevent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) -Methode verfügt über einen einzelnen Parameter, der ein Zeiger auf die [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Struktur ist. Der **eeventtype** -Member dieser Struktur gibt Aufschluss darüber, welches Ereignis aufgetreten ist. Wenn z. b. die Wiedergabe gestartet wird, sendet MF Play das Ereignis für den **MFP- \_ \_ Ereignistyp \_ Play** .

Jeder Ereignistyp verfügt über eine entsprechende Datenstruktur, die Informationen für dieses Ereignis enthält. Jede dieser Strukturen beginnt mit einer [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Struktur. Wandeln Sie in Ihrem Rückruf den **MFP- \_ Ereignis \_ Header** Zeiger in die ereignisspezifische Datenstruktur um. Wenn der Ereignistyp z. b. **MFP- \_ Wiedergabe \_ Ereignis** lautet, ist die Datenstruktur [**MFP- \_ Wiedergabe \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event). Der folgende Code zeigt, wie dieses Ereignis im Rückruf behandelt werden kann.


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



In diesem Beispiel wird das [**MFP \_ get \_ Play \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) -Ereignis Ereignis verwendet, um den *Peer Reader* -Zeiger in eine [**MFP- \_ Wiedergabe \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) Struktur umzuwandeln. Das **HRESULT** des Vorgangs, von dem das Ereignis ausgelöst wurde, wird im Feld " **hrevent** " der Struktur gespeichert.

Eine Liste aller Ereignis Typen und der entsprechenden Datenstrukturen finden Sie unter [**MFP- \_ \_ Ereignistyp**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).

Ein Hinweis zum Threading: Standardmäßig ruft mfplay den Rückruf von dem gleichen Thread auf, der " [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)" aufgerufen hat. Dieser Thread muss über eine Nachrichten Schleife verfügen. Alternativ dazu können Sie die **MFP- \_ Option " \_ Free \_ threaded \_ Callback** " im *Parameter "* " für den Parameter "" von " **mfpkreatemediaplayer**" übergeben. Dieses Flag bewirkt, dass mfplay Rückrufe von einem separaten Thread aufruft. Beide Optionen haben Auswirkungen auf Ihre Anwendung. Die Standardoption bedeutet, dass ihr Rückruf keine Aktionen ausführen kann, die auf Ihre Nachrichten Schleife warten, z. b. das warten auf eine UI-Aktion, da dadurch die Fenster Prozedur blockiert wird. Die Option "Free-Threaded" bedeutet, dass Sie kritische Abschnitte verwenden müssen, um alle Daten zu schützen, auf die Sie in Ihrem Rückruf zugreifen. In den meisten Fällen ist die Standardoption am einfachsten.

## <a name="getting-information-about-a-media-file"></a>Informationen zu einer Mediendatei

Wenn Sie eine Mediendatei in mfplay öffnen, erstellt der Player ein Objekt, das als *Medien Element* bezeichnet wird, das die Mediendatei darstellt. Dieses Objekt macht die [**imfpmediaitem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) -Schnittstelle verfügbar, die Sie verwenden können, um Informationen über die Mediendatei abzurufen. Viele der mfplay-Ereignis Strukturen enthalten einen Zeiger auf das aktuelle Medien Element. Sie können das aktuelle Medien Element auch abrufen, indem Sie [**imfpmediaplayer:: getmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) für den Player aufrufen.

Zwei besonders nützliche Methoden sind [**imfpmediaitem:: hasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) und [**imfpmediaitem:: HasAudio.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio) Mit diesen Methoden wird abgefragt, ob die Medienquelle Video-oder Audiodaten enthält.

Der folgende Code testet z. b., ob die aktuelle Mediendatei einen Videostream enthält.


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



Wenn die Quelldatei einen Videostream enthält, der für die Wiedergabe ausgewählt ist, werden *bhasvideo* und *bissselected* beide auf **true** festgelegt.

## <a name="managing-video-playback"></a>Verwalten der Video Wiedergabe

Wenn mfplay eine Videodatei wieder gibt, wird das Video in dem Fenster gezeichnet, das Sie in der Funktion [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) angegeben haben. Dies erfolgt in einem separaten Thread, der im Besitz der Microsoft Media Foundation Wiedergabe Pipeline ist. Die Anwendung muss diesen Prozess größtenteils nicht verwalten. Es gibt jedoch zwei Situationen, in denen die Anwendung mfplay Benachrichtigen muss, um das Video zu aktualisieren.

-   Wenn die Wiedergabe angehalten oder angehalten wird, muss MF Play benachrichtigt werden, wenn das Videofenster der Anwendung eine WM \_ Paint-Meldung empfängt. Dies ermöglicht es mfplay, das Fenster neu zu zeichnen.
-   Wenn die Größe des Fensters geändert wird, muss mfplay benachrichtigt werden, damit das Video so skaliert werden kann, dass es der neuen Fenstergröße entspricht.

Die [**imfpmediaplayer:: Updatevideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) -Methode behandelt beide Fälle. Ruft diese Methode in den Meldungs \_ Handlern "WM Paint" und "WM \_ size" für das Videofenster auf.

> [!IMPORTANT]
> Rufen Sie die GDI **BeginPaint** -Funktion vor dem Aufruf von [**Updatevideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)auf.

 


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



Wenn Sie nichts anderes angeben, zeigt MF Play das Video mit dem richtigen Seitenverhältnis an, bei Bedarf mithilfe von Letterbox. Wenn Sie das Seitenverhältnis nicht beibehalten möchten, wenden Sie [**imfpmediaplayer:: setaspectratiomode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) mit dem Flag " **mfvideoarmode \_ None** " an. Dadurch wird das Video durch "mfplay" gestreckt, um das gesamte Rechteck ohne Letterboxing auszufüllen. In der Regel sollten Sie die Standardeinstellung verwenden und das Video mit dem mfplay-Buchstaben versehen lassen. Die standardmäßige Letterbox-Farbe ist schwarz, Sie können diese jedoch ändern, indem Sie [**imfpmediaplayer:: setBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor)aufrufen.

## <a name="limitations-of-mfplay"></a>Einschränkungen von MF Play

Die aktuelle Version von MF Play weist die folgenden Einschränkungen auf:

-   Von MF Play werden von DRM geschützte Inhalte nicht unterstützt.
-   Standardmäßig unterstützt MF Play keine netzwerkstreamingprotokolle. Weitere Informationen finden Sie unter [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).
-   MF Play bietet keine Unterstützung für serverseitige Wiedergabelisten (sspls) oder andere Arten von Quellen, die mehr als ein Segment wiedergeben. In technischer Hinsicht stoppt MF Play die Wiedergabe nach der ersten Präsentation und ignoriert alle [menewpresentation](menewpresentation.md) -Ereignisse aus der Medienquelle.
-   MF Play unterstützt keine nahtlosen Übergänge zwischen Medienquellen.
-   MF Play unterstützt nicht das Mischen mehrerer Videostreams.
-   Nur Medienformate, die nativ in Media Foundation unterstützt werden, werden von MF Play unterstützt. (Hierzu gehören auch Media Foundation Komponenten von Drittanbietern, die möglicherweise auf dem System installiert sind.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 




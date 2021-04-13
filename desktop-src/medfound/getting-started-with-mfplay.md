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
# <a name="getting-started-with-mfplay"></a><span data-ttu-id="66bf5-103">Ersten Einstieg in MF Play</span><span class="sxs-lookup"><span data-stu-id="66bf5-103">Getting Started with MFPlay</span></span>

<span data-ttu-id="66bf5-104">\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="66bf5-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="66bf5-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="66bf5-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="66bf5-106">\]</span><span class="sxs-lookup"><span data-stu-id="66bf5-106">\]</span></span>

<span data-ttu-id="66bf5-107">MF Play ist eine API zum Erstellen von Medienwiedergabe Anwendungen in C++.</span><span class="sxs-lookup"><span data-stu-id="66bf5-107">MFPlay is an API for creating media playback applications in C++.</span></span>

<span data-ttu-id="66bf5-108">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="66bf5-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="66bf5-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66bf5-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="66bf5-110">Informationen zu MF Play</span><span class="sxs-lookup"><span data-stu-id="66bf5-110">About MFPlay</span></span>](#about-mfplay)
-   [<span data-ttu-id="66bf5-111">Wiedergeben einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="66bf5-111">Playing a Media File</span></span>](#playing-a-media-file)
-   [<span data-ttu-id="66bf5-112">Steuern der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="66bf5-112">Controlling Playback</span></span>](#controlling-playback)
-   [<span data-ttu-id="66bf5-113">Empfangen von Ereignissen vom Player</span><span class="sxs-lookup"><span data-stu-id="66bf5-113">Receiving Events From the Player</span></span>](#receiving-events-from-the-player)
-   [<span data-ttu-id="66bf5-114">Informationen zu einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="66bf5-114">Getting Information About a Media File</span></span>](#getting-information-about-a-media-file)
-   [<span data-ttu-id="66bf5-115">Verwalten der Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="66bf5-115">Managing Video Playback</span></span>](#managing-video-playback)
-   [<span data-ttu-id="66bf5-116">Einschränkungen von MF Play</span><span class="sxs-lookup"><span data-stu-id="66bf5-116">Limitations of MFPlay</span></span>](#limitations-of-mfplay)
-   [<span data-ttu-id="66bf5-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="66bf5-117">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="66bf5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66bf5-118">Requirements</span></span>

<span data-ttu-id="66bf5-119">MF Play erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="66bf5-119">MFPlay requires Windows 7.</span></span>

## <a name="about-mfplay"></a><span data-ttu-id="66bf5-120">Informationen zu MF Play</span><span class="sxs-lookup"><span data-stu-id="66bf5-120">About MFPlay</span></span>

<span data-ttu-id="66bf5-121">MF Play verfügt über ein einfaches Programmiermodell und bietet gleichzeitig den Kern Satz von Features, die für die meisten Wiedergabe Anwendungen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="66bf5-121">MFPlay has a simple programming model, while providing the core set of features that most playback applications need.</span></span> <span data-ttu-id="66bf5-122">Eine Anwendung erstellt ein *Player* -Objekt zum Steuern der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="66bf5-122">An application creates a *player* object that controls playback.</span></span> <span data-ttu-id="66bf5-123">Zum Wiedergeben einer Mediendatei erstellt das Player-Objekt ein *Medien Element*, das zum erhalten von Informationen über den Inhalt der Mediendatei verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="66bf5-123">To play a media file, the player object creates a *media item*, which can be used to get information about the contents of the media file.</span></span> <span data-ttu-id="66bf5-124">Die Anwendung steuert die Wiedergabe über Methoden in der [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Schnittstelle des Player-Objekts.</span><span class="sxs-lookup"><span data-stu-id="66bf5-124">The application controls playback through methods on the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="66bf5-125">Optional kann die Anwendung Ereignis Benachrichtigungen über eine Rückruf Schnittstelle erhalten. das folgende Diagramm veranschaulicht diesen Prozess.</span><span class="sxs-lookup"><span data-stu-id="66bf5-125">Optionally, the application can get event notifications through a callback interface The following diagram illustrates this process.</span></span>

![Konzeptionelle Darstellung: die Anwendung und der Player zeigen aufeinander, beide zeigen auf das Medien Element, das auf die Mediendatei zeigt.](images/mfplay.png)

## <a name="playing-a-media-file"></a><span data-ttu-id="66bf5-127">Wiedergeben einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="66bf5-127">Playing a Media File</span></span>

<span data-ttu-id="66bf5-128">Um eine Mediendatei wiederzugeben, müssen Sie die [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-128">To play a media file, call the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>


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



<span data-ttu-id="66bf5-129">Die [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) -Funktion erstellt eine neue Instanz des mfplay Player-Objekts.</span><span class="sxs-lookup"><span data-stu-id="66bf5-129">The [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function creates a new instance of the MFPlay player object.</span></span> <span data-ttu-id="66bf5-130">Die Funktion übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="66bf5-130">The function takes the following parameters:</span></span>

-   <span data-ttu-id="66bf5-131">Der erste Parameter ist die URL der Datei, die geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="66bf5-131">The first parameter is the URL of the file to open.</span></span> <span data-ttu-id="66bf5-132">Hierbei kann es sich um eine lokale Datei oder eine Datei auf einem Medienserver handeln.</span><span class="sxs-lookup"><span data-stu-id="66bf5-132">This can be a local file or a file on a media server.</span></span>
-   <span data-ttu-id="66bf5-133">Der zweite Parameter gibt an, ob die Wiedergabe automatisch startet.</span><span class="sxs-lookup"><span data-stu-id="66bf5-133">The second parameter specifies whether playback starts automatically.</span></span> <span data-ttu-id="66bf5-134">Durch Festlegen dieses Parameters auf " **true**" wird die Datei abgespielt, sobald Sie von mfplay geladen wird.</span><span class="sxs-lookup"><span data-stu-id="66bf5-134">By setting this paremeter to **TRUE**, the file will play as soon as MFPlay loads it.</span></span>
-   <span data-ttu-id="66bf5-135">Der dritte Parameter legt verschiedene Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="66bf5-135">The third parameter sets various options.</span></span> <span data-ttu-id="66bf5-136">Übergeben Sie für die Standardoptionen NULL (0).</span><span class="sxs-lookup"><span data-stu-id="66bf5-136">For the default options, pass zero (0).</span></span>
-   <span data-ttu-id="66bf5-137">Der vierte Parameter ist ein Zeiger auf eine optionale Rückruf Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="66bf5-137">The fourth parameter is a pointer to an optional callback interface.</span></span> <span data-ttu-id="66bf5-138">Dieser Parameter kann **null** sein, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="66bf5-138">This parameter can be **NULL**, as shown.</span></span> <span data-ttu-id="66bf5-139">Der Rückruf wird im Abschnitt [empfangen von Ereignissen vom Player](#receiving-events-from-the-player)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="66bf5-139">The callback is described in the section [Receiving Events From the Player](#receiving-events-from-the-player).</span></span>
-   <span data-ttu-id="66bf5-140">Der fünfte Parameter ist ein Handle für das Anwendungsfenster.</span><span class="sxs-lookup"><span data-stu-id="66bf5-140">The fifth parameter is a handle to the application window.</span></span> <span data-ttu-id="66bf5-141">Wenn die Mediendatei einen Videostream enthält, wird das Video im Client Bereich dieses Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="66bf5-141">If the media file contains a video stream, the video will appear inside the client area of this window.</span></span> <span data-ttu-id="66bf5-142">Bei der reinen Audiowiedergabe kann dieser Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="66bf5-142">For audio-only playback, this parameter can be **NULL**.</span></span>

<span data-ttu-id="66bf5-143">Der letzte Parameter erhält einen Zeiger auf die [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Schnittstelle des Player Objekts.</span><span class="sxs-lookup"><span data-stu-id="66bf5-143">The last parameter receives a pointer to the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span>

<span data-ttu-id="66bf5-144">Bevor die Anwendung heruntergefahren wird, stellen Sie sicher, dass Sie den [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Zeiger freigeben.</span><span class="sxs-lookup"><span data-stu-id="66bf5-144">Before the application shuts down, be sure to release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) pointer.</span></span> <span data-ttu-id="66bf5-145">Dies können Sie in Ihrem " **WM \_ Close** Message"-Handler tun.</span><span class="sxs-lookup"><span data-stu-id="66bf5-145">You can do this in your **WM\_CLOSE** message handler.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> <span data-ttu-id="66bf5-146">In diesem Beispiel wird die Funktion " [saferelease](saferelease.md) " verwendet, um Schnittstellen Zeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="66bf5-146">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="66bf5-147">Für eine einfache Videowiedergabe ist dies der gesamte Code, den Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-147">For simple video playback, that's all the code you need.</span></span> <span data-ttu-id="66bf5-148">Im weiteren Verlauf dieses Tutorials erfahren Sie, wie Sie weitere Features hinzufügen, beginnend mit dem Steuern der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="66bf5-148">The rest of this tutorial will show how to add more features, starting with how to control playback.</span></span>

## <a name="controlling-playback"></a><span data-ttu-id="66bf5-149">Steuern der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="66bf5-149">Controlling Playback</span></span>

<span data-ttu-id="66bf5-150">Der im vorherigen Abschnitt gezeigte Code gibt die Mediendatei wieder, bis das Ende der Datei erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="66bf5-150">The code shown in the previous section will play the media file until it reaches the end of the file.</span></span> <span data-ttu-id="66bf5-151">Sie können die Wiedergabe starten, indem Sie die folgenden Methoden für die [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Schnittstelle aufrufen:</span><span class="sxs-lookup"><span data-stu-id="66bf5-151">You can stop and start playback by calling the following methods on the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface:</span></span>

-   <span data-ttu-id="66bf5-152">[**Imfpmediaplayer::P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) hält die Wiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="66bf5-152">[**IMFPMediaPlayer::Pause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) pauses playback.</span></span> <span data-ttu-id="66bf5-153">Während die Wiedergabe angehalten wird, wird der aktuelle Videoframe angezeigt, und Audiodaten werden automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="66bf5-153">While playback is paused, the most recent video frame is displayed, and audio is silent.</span></span>
-   <span data-ttu-id="66bf5-154">[**Imfpmediaplayer:: beenden**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) beendet die Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="66bf5-154">[**IMFPMediaPlayer::Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) stops playback.</span></span> <span data-ttu-id="66bf5-155">Es wird kein Video angezeigt, und die Wiedergabe Position wird auf den Anfang der Datei zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="66bf5-155">No video is displayed, and the playback position resets to the start of the file.</span></span>
-   <span data-ttu-id="66bf5-156">[**Imfpmediaplayer::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) setzt die Wiedergabe nach dem Beenden oder anhalten fort.</span><span class="sxs-lookup"><span data-stu-id="66bf5-156">[**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) resumes playback after stopping or pausing.</span></span>

<span data-ttu-id="66bf5-157">Der folgende Code hält die Wiedergabe an oder nimmt Sie wieder auf, wenn Sie die **LEERTASTE** drücken.</span><span class="sxs-lookup"><span data-stu-id="66bf5-157">The following code pauses or resumes playback when you press the **SPACEBAR**.</span></span>


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



<span data-ttu-id="66bf5-158">In diesem Beispiel wird die [**imfpmediaplayer:: GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) -Methode aufgerufen, um den aktuellen Wiedergabe Zustand (angehalten, angehalten oder wiederzugeben) zu erhalten und entsprechend anzuhalten oder fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-158">This example calls the [**IMFPMediaPlayer::GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) method to get the current playback state (paused, stopped, or playing) and pauses or resumes accordingly.</span></span>

## <a name="receiving-events-from-the-player"></a><span data-ttu-id="66bf5-159">Empfangen von Ereignissen vom Player</span><span class="sxs-lookup"><span data-stu-id="66bf5-159">Receiving Events From the Player</span></span>

<span data-ttu-id="66bf5-160">Mfplay verwendet eine Rückruf Schnittstelle, um Ereignisse an Ihre Anwendung zu senden.</span><span class="sxs-lookup"><span data-stu-id="66bf5-160">MFPlay uses a callback interface to send events to your application.</span></span> <span data-ttu-id="66bf5-161">Für diesen Rückruf gibt es zwei Gründe:</span><span class="sxs-lookup"><span data-stu-id="66bf5-161">There are two reasons for this callback:</span></span>

-   <span data-ttu-id="66bf5-162">Die Wiedergabe erfolgt in einem separaten Thread.</span><span class="sxs-lookup"><span data-stu-id="66bf5-162">Playback occurs on a separate thread.</span></span> <span data-ttu-id="66bf5-163">Während der Wiedergabe können bestimmte Ereignisse auftreten, z. b. das Erreichen des Datei Endes.</span><span class="sxs-lookup"><span data-stu-id="66bf5-163">During playback, certain events might occur, such as reaching the end of the file.</span></span> <span data-ttu-id="66bf5-164">Mfplay verwendet den Rückruf, um die Anwendung über das Ereignis zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-164">MFPlay uses the callback to notify your application of the event.</span></span>
-   <span data-ttu-id="66bf5-165">Viele der [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Methoden sind asynchron, d. h., Sie geben zurück, bevor der Vorgang abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="66bf5-165">Many of the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) methods are asynchronous, meaning they return before the operation completes.</span></span> <span data-ttu-id="66bf5-166">Mithilfe von asynchronen Methoden können Sie einen Vorgang aus dem UI-Thread starten, der viel Zeit in Anspruch nimmt, ohne dass die Benutzeroberfläche blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="66bf5-166">Asynchronous methods let you start an operation from your UI thread that might take a long time to complete, without it causing your UI to block.</span></span> <span data-ttu-id="66bf5-167">Nachdem der Vorgang abgeschlossen wurde, signalisiert MF Play den Rückruf.</span><span class="sxs-lookup"><span data-stu-id="66bf5-167">After the operation completes, MFPlay signals the callback.</span></span>

<span data-ttu-id="66bf5-168">Um Rückruf Benachrichtigungen zu empfangen, implementieren Sie die [**imfpmediaplayercallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="66bf5-168">To receive callback notifications, implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="66bf5-169">Diese Schnittstelle erbt **IUnknown** und definiert eine einzelne Methode, [**onmediaplayerevent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="66bf5-169">This interface inherits **IUnknown** and defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="66bf5-170">Wenn Sie den Rückruf einrichten möchten, übergeben Sie einen Zeiger auf Ihre **imfpmediaplayercallback** -Implementierung im *pCallback* -Parameter der [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="66bf5-170">To set up the callback, pass a pointer to your **IMFPMediaPlayerCallback** implementation in the *pCallback* parameter of the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>

<span data-ttu-id="66bf5-171">Im folgenden finden Sie das erste Beispiel aus diesem Tutorial, das so geändert wurde, dass es den Rückruf einschließt.</span><span class="sxs-lookup"><span data-stu-id="66bf5-171">Here is the first example from this tutorial, modified to include the callback.</span></span>


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



<span data-ttu-id="66bf5-172">Die [**onmediaplayerevent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) -Methode verfügt über einen einzelnen Parameter, der ein Zeiger auf die [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="66bf5-172">The [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method has a single parameter, which is a pointer to the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="66bf5-173">Der **eeventtype** -Member dieser Struktur gibt Aufschluss darüber, welches Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="66bf5-173">The **eEventType** member of this structure tells you which event occurred.</span></span> <span data-ttu-id="66bf5-174">Wenn z. b. die Wiedergabe gestartet wird, sendet MF Play das Ereignis für den **MFP- \_ \_ Ereignistyp \_ Play** .</span><span class="sxs-lookup"><span data-stu-id="66bf5-174">For example, when playback starts, MFPlay sends the **MFP\_EVENT\_TYPE\_PLAY** event.</span></span>

<span data-ttu-id="66bf5-175">Jeder Ereignistyp verfügt über eine entsprechende Datenstruktur, die Informationen für dieses Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="66bf5-175">Each event type has a corresponding data structure that contains information for that event.</span></span> <span data-ttu-id="66bf5-176">Jede dieser Strukturen beginnt mit einer [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Struktur.</span><span class="sxs-lookup"><span data-stu-id="66bf5-176">Each of these structures starts with an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="66bf5-177">Wandeln Sie in Ihrem Rückruf den **MFP- \_ Ereignis \_ Header** Zeiger in die ereignisspezifische Datenstruktur um.</span><span class="sxs-lookup"><span data-stu-id="66bf5-177">In your callback, cast the **MFP\_EVENT\_HEADER** pointer to the event-specific data structure.</span></span> <span data-ttu-id="66bf5-178">Wenn der Ereignistyp z. b. **MFP- \_ Wiedergabe \_ Ereignis** lautet, ist die Datenstruktur [**MFP- \_ Wiedergabe \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span><span class="sxs-lookup"><span data-stu-id="66bf5-178">For example, if the event type is **MFP\_PLAY\_EVENT**, the data structure is [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span></span> <span data-ttu-id="66bf5-179">Der folgende Code zeigt, wie dieses Ereignis im Rückruf behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="66bf5-179">The following code shows how to handle this event in the callback.</span></span>


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



<span data-ttu-id="66bf5-180">In diesem Beispiel wird das [**MFP \_ get \_ Play \_**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) -Ereignis Ereignis verwendet, um den *Peer Reader* -Zeiger in eine [**MFP- \_ Wiedergabe \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) Struktur umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="66bf5-180">This example uses the [**MFP\_GET\_PLAY\_EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) event to cast the *pEventHeader* pointer to an [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) structure.</span></span> <span data-ttu-id="66bf5-181">Das **HRESULT** des Vorgangs, von dem das Ereignis ausgelöst wurde, wird im Feld " **hrevent** " der Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="66bf5-181">The **HRESULT** from the operation that triggered the event is stored in the **hrEvent** field of the structure.</span></span>

<span data-ttu-id="66bf5-182">Eine Liste aller Ereignis Typen und der entsprechenden Datenstrukturen finden Sie unter [**MFP- \_ \_ Ereignistyp**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span><span class="sxs-lookup"><span data-stu-id="66bf5-182">For a list of all the event types and the corresponding data structures, see [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span></span>

<span data-ttu-id="66bf5-183">Ein Hinweis zum Threading: Standardmäßig ruft mfplay den Rückruf von dem gleichen Thread auf, der " [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)" aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="66bf5-183">A note about threading: By default, MFPlay invokes the callback from the same thread that called [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span></span> <span data-ttu-id="66bf5-184">Dieser Thread muss über eine Nachrichten Schleife verfügen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-184">This thread must have a message loop.</span></span> <span data-ttu-id="66bf5-185">Alternativ dazu können Sie die **MFP- \_ Option " \_ Free \_ threaded \_ Callback** " im *Parameter "* " für den Parameter "" von " **mfpkreatemediaplayer**" übergeben.</span><span class="sxs-lookup"><span data-stu-id="66bf5-185">Alternatively, you can pass the **MFP\_OPTION\_FREE\_THREADED\_CALLBACK** flag in the *creationOptions* parameter of **MFPCreateMediaPlayer**.</span></span> <span data-ttu-id="66bf5-186">Dieses Flag bewirkt, dass mfplay Rückrufe von einem separaten Thread aufruft.</span><span class="sxs-lookup"><span data-stu-id="66bf5-186">This flag causes MFPlay to invoke callbacks from a separate thread.</span></span> <span data-ttu-id="66bf5-187">Beide Optionen haben Auswirkungen auf Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="66bf5-187">Either option has implications for your application.</span></span> <span data-ttu-id="66bf5-188">Die Standardoption bedeutet, dass ihr Rückruf keine Aktionen ausführen kann, die auf Ihre Nachrichten Schleife warten, z. b. das warten auf eine UI-Aktion, da dadurch die Fenster Prozedur blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="66bf5-188">The default option means your callback cannot do anything that waits on your message loop, such as waiting for a UI action, because that will block your window procedure.</span></span> <span data-ttu-id="66bf5-189">Die Option "Free-Threaded" bedeutet, dass Sie kritische Abschnitte verwenden müssen, um alle Daten zu schützen, auf die Sie in Ihrem Rückruf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-189">The free-threaded option means you need to use critical sections to protect any data that you access in your callback.</span></span> <span data-ttu-id="66bf5-190">In den meisten Fällen ist die Standardoption am einfachsten.</span><span class="sxs-lookup"><span data-stu-id="66bf5-190">In most cases, the default option is simplest.</span></span>

## <a name="getting-information-about-a-media-file"></a><span data-ttu-id="66bf5-191">Informationen zu einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="66bf5-191">Getting Information About a Media File</span></span>

<span data-ttu-id="66bf5-192">Wenn Sie eine Mediendatei in mfplay öffnen, erstellt der Player ein Objekt, das als *Medien Element* bezeichnet wird, das die Mediendatei darstellt.</span><span class="sxs-lookup"><span data-stu-id="66bf5-192">When you open a media file in MFPlay, the player creates an object called a *media item* that represents the media file.</span></span> <span data-ttu-id="66bf5-193">Dieses Objekt macht die [**imfpmediaitem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) -Schnittstelle verfügbar, die Sie verwenden können, um Informationen über die Mediendatei abzurufen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-193">This object exposes the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which you can use to get information about the media file.</span></span> <span data-ttu-id="66bf5-194">Viele der mfplay-Ereignis Strukturen enthalten einen Zeiger auf das aktuelle Medien Element.</span><span class="sxs-lookup"><span data-stu-id="66bf5-194">Many of the MFPlay event structures contain a pointer to the current media item.</span></span> <span data-ttu-id="66bf5-195">Sie können das aktuelle Medien Element auch abrufen, indem Sie [**imfpmediaplayer:: getmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) für den Player aufrufen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-195">You can also get the current media item by calling [**IMFPMediaPlayer::GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) on the player.</span></span>

<span data-ttu-id="66bf5-196">Zwei besonders nützliche Methoden sind [**imfpmediaitem:: hasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) und [**imfpmediaitem:: HasAudio.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio)</span><span class="sxs-lookup"><span data-stu-id="66bf5-196">Two particularly useful methods are [**IMFPMediaItem::HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) and [**IMFPMediaItem::HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span></span> <span data-ttu-id="66bf5-197">Mit diesen Methoden wird abgefragt, ob die Medienquelle Video-oder Audiodaten enthält.</span><span class="sxs-lookup"><span data-stu-id="66bf5-197">These methods query whether the media source contains video or audio.</span></span>

<span data-ttu-id="66bf5-198">Der folgende Code testet z. b., ob die aktuelle Mediendatei einen Videostream enthält.</span><span class="sxs-lookup"><span data-stu-id="66bf5-198">For example, the following code tests whether the current media file contains a video stream.</span></span>


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



<span data-ttu-id="66bf5-199">Wenn die Quelldatei einen Videostream enthält, der für die Wiedergabe ausgewählt ist, werden *bhasvideo* und *bissselected* beide auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="66bf5-199">If the source file contains a video stream that is selected for playback, *bHasVideo* and *bIsSelected* are both set to **TRUE**.</span></span>

## <a name="managing-video-playback"></a><span data-ttu-id="66bf5-200">Verwalten der Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="66bf5-200">Managing Video Playback</span></span>

<span data-ttu-id="66bf5-201">Wenn mfplay eine Videodatei wieder gibt, wird das Video in dem Fenster gezeichnet, das Sie in der Funktion [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="66bf5-201">When MFPlay plays a video file, it draws the video in the window that you specified in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span> <span data-ttu-id="66bf5-202">Dies erfolgt in einem separaten Thread, der im Besitz der Microsoft Media Foundation Wiedergabe Pipeline ist.</span><span class="sxs-lookup"><span data-stu-id="66bf5-202">This occurs on a separate thread owned by the Microsoft Media Foundation playback pipeline.</span></span> <span data-ttu-id="66bf5-203">Die Anwendung muss diesen Prozess größtenteils nicht verwalten.</span><span class="sxs-lookup"><span data-stu-id="66bf5-203">For the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="66bf5-204">Es gibt jedoch zwei Situationen, in denen die Anwendung mfplay Benachrichtigen muss, um das Video zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="66bf5-204">However, there are two situations where the application must notify MFPlay to update the video.</span></span>

-   <span data-ttu-id="66bf5-205">Wenn die Wiedergabe angehalten oder angehalten wird, muss MF Play benachrichtigt werden, wenn das Videofenster der Anwendung eine WM \_ Paint-Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="66bf5-205">If playback is paused or stopped, MFPlay must be notified whenever the application's video window receives a WM\_PAINT message.</span></span> <span data-ttu-id="66bf5-206">Dies ermöglicht es mfplay, das Fenster neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-206">This allows MFPlay to repaint the window.</span></span>
-   <span data-ttu-id="66bf5-207">Wenn die Größe des Fensters geändert wird, muss mfplay benachrichtigt werden, damit das Video so skaliert werden kann, dass es der neuen Fenstergröße entspricht.</span><span class="sxs-lookup"><span data-stu-id="66bf5-207">If the window is resized, MFPlay must be notified so that it can scale the video to match the new window size.</span></span>

<span data-ttu-id="66bf5-208">Die [**imfpmediaplayer:: Updatevideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) -Methode behandelt beide Fälle.</span><span class="sxs-lookup"><span data-stu-id="66bf5-208">The [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method handles both cases.</span></span> <span data-ttu-id="66bf5-209">Ruft diese Methode in den Meldungs \_ Handlern "WM Paint" und "WM \_ size" für das Videofenster auf.</span><span class="sxs-lookup"><span data-stu-id="66bf5-209">Call this method inside both the WM\_PAINT and WM\_SIZE message handlers for the video window.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66bf5-210">Rufen Sie die GDI **BeginPaint** -Funktion vor dem Aufruf von [**Updatevideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)auf.</span><span class="sxs-lookup"><span data-stu-id="66bf5-210">Call the GDI **BeginPaint** function before calling [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span>

 


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



<span data-ttu-id="66bf5-211">Wenn Sie nichts anderes angeben, zeigt MF Play das Video mit dem richtigen Seitenverhältnis an, bei Bedarf mithilfe von Letterbox.</span><span class="sxs-lookup"><span data-stu-id="66bf5-211">Unless you specify otherwise, MFPlay shows the video at the correct aspect ratio, using letterboxing if needed.</span></span> <span data-ttu-id="66bf5-212">Wenn Sie das Seitenverhältnis nicht beibehalten möchten, wenden Sie [**imfpmediaplayer:: setaspectratiomode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) mit dem Flag " **mfvideoarmode \_ None** " an.</span><span class="sxs-lookup"><span data-stu-id="66bf5-212">If you do not want to preserve the aspect ratio, call [**IMFPMediaPlayer::SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) with the **MFVideoARMode\_None** flag.</span></span> <span data-ttu-id="66bf5-213">Dadurch wird das Video durch "mfplay" gestreckt, um das gesamte Rechteck ohne Letterboxing auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-213">This will cause MFPlay to stretch the video to fill the entire rectangle, with no letterboxing.</span></span> <span data-ttu-id="66bf5-214">In der Regel sollten Sie die Standardeinstellung verwenden und das Video mit dem mfplay-Buchstaben versehen lassen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-214">Typically you should use the default setting and let MFPlay letterbox the video.</span></span> <span data-ttu-id="66bf5-215">Die standardmäßige Letterbox-Farbe ist schwarz, Sie können diese jedoch ändern, indem Sie [**imfpmediaplayer:: setBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-215">The default letterbox color is black, but you can change this by calling [**IMFPMediaPlayer::SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span></span>

## <a name="limitations-of-mfplay"></a><span data-ttu-id="66bf5-216">Einschränkungen von MF Play</span><span class="sxs-lookup"><span data-stu-id="66bf5-216">Limitations of MFPlay</span></span>

<span data-ttu-id="66bf5-217">Die aktuelle Version von MF Play weist die folgenden Einschränkungen auf:</span><span class="sxs-lookup"><span data-stu-id="66bf5-217">The current version of MFPlay has the following limitations:</span></span>

-   <span data-ttu-id="66bf5-218">Von MF Play werden von DRM geschützte Inhalte nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="66bf5-218">MFPlay does not support DRM-protected content.</span></span>
-   <span data-ttu-id="66bf5-219">Standardmäßig unterstützt MF Play keine netzwerkstreamingprotokolle.</span><span class="sxs-lookup"><span data-stu-id="66bf5-219">By default, MFPlay does not support network streaming protocols.</span></span> <span data-ttu-id="66bf5-220">Weitere Informationen finden Sie unter [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span><span class="sxs-lookup"><span data-stu-id="66bf5-220">For more information, see [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span>
-   <span data-ttu-id="66bf5-221">MF Play bietet keine Unterstützung für serverseitige Wiedergabelisten (sspls) oder andere Arten von Quellen, die mehr als ein Segment wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="66bf5-221">MFPlay does not support server-side playlists (SSPLs) or other types of source that play more than one segment.</span></span> <span data-ttu-id="66bf5-222">In technischer Hinsicht stoppt MF Play die Wiedergabe nach der ersten Präsentation und ignoriert alle [menewpresentation](menewpresentation.md) -Ereignisse aus der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="66bf5-222">In technical terms, MFPlay stops playback after the first presentation, and ignores any [MENewPresentation](menewpresentation.md) events from the media source.</span></span>
-   <span data-ttu-id="66bf5-223">MF Play unterstützt keine nahtlosen Übergänge zwischen Medienquellen.</span><span class="sxs-lookup"><span data-stu-id="66bf5-223">MFPlay does not support seamless transitions between media sources.</span></span>
-   <span data-ttu-id="66bf5-224">MF Play unterstützt nicht das Mischen mehrerer Videostreams.</span><span class="sxs-lookup"><span data-stu-id="66bf5-224">MFPlay does not support mixing multiple video streams.</span></span>
-   <span data-ttu-id="66bf5-225">Nur Medienformate, die nativ in Media Foundation unterstützt werden, werden von MF Play unterstützt.</span><span class="sxs-lookup"><span data-stu-id="66bf5-225">Only media formats supported natively in Media Foundation are supported by MFPlay.</span></span> <span data-ttu-id="66bf5-226">(Hierzu gehören auch Media Foundation Komponenten von Drittanbietern, die möglicherweise auf dem System installiert sind.)</span><span class="sxs-lookup"><span data-stu-id="66bf5-226">(This includes third-party Media Foundation components that might be installed on the system.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="66bf5-227">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="66bf5-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66bf5-228">Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="66bf5-228">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 




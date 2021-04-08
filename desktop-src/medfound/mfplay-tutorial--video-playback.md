---
description: Dieses Tutorial zeigt eine komplette Anwendung, die Videos mit MF Play wieder gibt.
ms.assetid: f72a7c1f-b059-474c-96f2-8fad3b1f7035
title: 'MF Play-Tutorial: Video Wiedergabe'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bbadae22e72799c64a42d09b6eed904b56a60d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755296"
---
# <a name="mfplay-tutorial-video-playback"></a><span data-ttu-id="d316a-103">MF Play-Tutorial: Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="d316a-103">MFPlay Tutorial: Video Playback</span></span>

<span data-ttu-id="d316a-104">\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d316a-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d316a-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d316a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d316a-106">\]</span><span class="sxs-lookup"><span data-stu-id="d316a-106">\]</span></span>

<span data-ttu-id="d316a-107">Dieses Tutorial zeigt eine komplette Anwendung, die Videos mit MF Play wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="d316a-107">This tutorial presents a complete application that plays video using MFPlay.</span></span> <span data-ttu-id="d316a-108">Es basiert auf dem [simpleplay](simpleplay-sample.md) SDK-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d316a-108">It is based on the [SimplePlay](simpleplay-sample.md) SDK sample.</span></span>

<span data-ttu-id="d316a-109">Dieses Tutorial enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="d316a-109">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="d316a-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d316a-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d316a-111">Header-und Bibliotheksdateien</span><span class="sxs-lookup"><span data-stu-id="d316a-111">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="d316a-112">Globale Variablen</span><span class="sxs-lookup"><span data-stu-id="d316a-112">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="d316a-113">Deklaration der Rückruf Klasse</span><span class="sxs-lookup"><span data-stu-id="d316a-113">Declare the Callback Class</span></span>](#declare-the-callback-class)
-   [<span data-ttu-id="d316a-114">Deklarieren der saferelease-Funktion</span><span class="sxs-lookup"><span data-stu-id="d316a-114">Declare the SafeRelease Function</span></span>](#declare-the-saferelease-function)
-   [<span data-ttu-id="d316a-115">Öffnen einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="d316a-115">Open a Media File</span></span>](#open-a-media-file)
-   [<span data-ttu-id="d316a-116">Fenster Meldungs Handler</span><span class="sxs-lookup"><span data-stu-id="d316a-116">Window Message Handlers</span></span>](#window-message-handlers)
-   [<span data-ttu-id="d316a-117">Implementieren der Rückruf Methode</span><span class="sxs-lookup"><span data-stu-id="d316a-117">Implement the Callback Method</span></span>](#implement-the-callback-method)
-   [<span data-ttu-id="d316a-118">Implementieren von WinMain</span><span class="sxs-lookup"><span data-stu-id="d316a-118">Implement WinMain</span></span>](#implement-winmain)
-   [<span data-ttu-id="d316a-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d316a-119">Related topics</span></span>](#related-topics)

<span data-ttu-id="d316a-120">Eine ausführlichere Erläuterung der MF Play-API finden Sie unter [Getting Started with MF](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="d316a-120">For a more detailed discussion of the MFPlay API, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d316a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d316a-121">Requirements</span></span>

<span data-ttu-id="d316a-122">MF Play erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d316a-122">MFPlay requires Windows 7.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="d316a-123">Header-und Bibliotheksdateien</span><span class="sxs-lookup"><span data-stu-id="d316a-123">Header and Library Files</span></span>

<span data-ttu-id="d316a-124">Fügen Sie die folgenden Header Dateien in das Projekt ein:</span><span class="sxs-lookup"><span data-stu-id="d316a-124">Include the following header files in your project:</span></span>


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <new>
#include <windows.h>
#include <windowsx.h>
#include <mfplay.h>
#include <mferror.h>
#include <shobjidl.h>   // defines IFileOpenDialog
#include <strsafe.h>
#include <Shlwapi.h>
```



<span data-ttu-id="d316a-125">Verknüpfung mit den folgenden Codebibliotheken:</span><span class="sxs-lookup"><span data-stu-id="d316a-125">Link to the following code libraries:</span></span>

-   <span data-ttu-id="d316a-126">MF Play. lib</span><span class="sxs-lookup"><span data-stu-id="d316a-126">mfplay.lib</span></span>
-   <span data-ttu-id="d316a-127">shlwapi. lib</span><span class="sxs-lookup"><span data-stu-id="d316a-127">shlwapi.lib</span></span>

## <a name="global-variables"></a><span data-ttu-id="d316a-128">Globale Variablen</span><span class="sxs-lookup"><span data-stu-id="d316a-128">Global Variables</span></span>

<span data-ttu-id="d316a-129">Deklarieren Sie die folgenden globalen Variablen:</span><span class="sxs-lookup"><span data-stu-id="d316a-129">Declare the following global variables:</span></span>


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



<span data-ttu-id="d316a-130">Diese Variablen werden wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="d316a-130">These variables will be used as follows:</span></span>

<dl> <dt>

<span data-ttu-id="d316a-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g \_ HWND*</span><span class="sxs-lookup"><span data-stu-id="d316a-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g\_hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="d316a-132">Ein Handle für das Anwendungsfenster.</span><span class="sxs-lookup"><span data-stu-id="d316a-132">A handle to the application window.</span></span>

</dd> <dt>

<span data-ttu-id="d316a-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ bvideo*</span><span class="sxs-lookup"><span data-stu-id="d316a-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g\_bVideo*</span></span>
</dt> <dd>

<span data-ttu-id="d316a-134">Ein boolescher Wert, der nachverfolgt, ob Videos abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="d316a-134">A Boolean value that tracks whether video is playing.</span></span>

</dd> <dt>

<span data-ttu-id="d316a-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ PPlayer*</span><span class="sxs-lookup"><span data-stu-id="d316a-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g\_pPlayer*</span></span>
</dt> <dd>

<span data-ttu-id="d316a-136">Ein Zeiger auf die [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d316a-136">A pointer to the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="d316a-137">Diese Schnittstelle wird zum Steuern der Wiedergabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="d316a-137">This interface is used to control playback.</span></span>

</dd> <dt>

<span data-ttu-id="d316a-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ pCallback*</span><span class="sxs-lookup"><span data-stu-id="d316a-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g\_pCallback*</span></span>
</dt> <dd>

<span data-ttu-id="d316a-139">Ein Zeiger auf die [**imfpmediaplayercallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d316a-139">A pointer to the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="d316a-140">Die Anwendung implementiert diese Rückruf Schnittstelle, um Benachrichtigungen vom Player-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d316a-140">The application implements this callback interface to get notifications from the player object.</span></span>

</dd> </dl>

## <a name="declare-the-callback-class"></a><span data-ttu-id="d316a-141">Deklaration der Rückruf Klasse</span><span class="sxs-lookup"><span data-stu-id="d316a-141">Declare the Callback Class</span></span>

<span data-ttu-id="d316a-142">Um Ereignis Benachrichtigungen aus dem Player-Objekt zu erhalten, muss die Anwendung die [**imfpmediaplayercallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="d316a-142">To get event notifications from the player object, the application must implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="d316a-143">Im folgenden Code wird eine Klasse deklariert, die die-Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="d316a-143">The following code declares a class that implements the interface.</span></span> <span data-ttu-id="d316a-144">Die einzige Member-Variable ist *m- \_ kref*, die den Verweis Zähler speichert.</span><span class="sxs-lookup"><span data-stu-id="d316a-144">The only member variable is *m\_cRef*, which stores the reference count.</span></span>

<span data-ttu-id="d316a-145">Die **IUnknown** -Methoden werden Inline implementiert.</span><span class="sxs-lookup"><span data-stu-id="d316a-145">The **IUnknown** methods are implemented inline.</span></span> <span data-ttu-id="d316a-146">Die Implementierung der [**imfpmediaplayercallback:: onmediaplayerevent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) -Methode wird später angezeigt. Weitere Informationen finden Sie [unter Implementieren der Rückruf Methode](#implement-the-callback-method).</span><span class="sxs-lookup"><span data-stu-id="d316a-146">The implementation of the [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is shown later; see [Implement the Callback Method](#implement-the-callback-method).</span></span>


```C++
// Implements the callback interface for MFPlay events.

class MediaPlayerCallback : public IMFPMediaPlayerCallback
{
    long m_cRef; // Reference count

public:

    MediaPlayerCallback() : m_cRef(1)
    {
    }

    IFACEMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(MediaPlayerCallback, IMFPMediaPlayerCallback),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    IFACEMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    IFACEMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    // IMFPMediaPlayerCallback methods
    IFACEMETHODIMP_(void) OnMediaPlayerEvent(MFP_EVENT_HEADER *pEventHeader);
};
```



## <a name="declare-the-saferelease-function"></a><span data-ttu-id="d316a-147">Deklarieren der saferelease-Funktion</span><span class="sxs-lookup"><span data-stu-id="d316a-147">Declare the SafeRelease Function</span></span>

<span data-ttu-id="d316a-148">In diesem Tutorial wird die [saferelease](saferelease.md) -Funktion verwendet, um Schnittstellen Zeiger freizugeben:</span><span class="sxs-lookup"><span data-stu-id="d316a-148">Throughout this tutorial, the [SafeRelease](saferelease.md) function is used to release interface pointers:</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="open-a-media-file"></a><span data-ttu-id="d316a-149">Öffnen einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="d316a-149">Open a Media File</span></span>

<span data-ttu-id="d316a-150">Die `PlayMediaFile` Funktion öffnet wie folgt eine Mediendatei:</span><span class="sxs-lookup"><span data-stu-id="d316a-150">The `PlayMediaFile` function opens a media file, as follows:</span></span>

1.  <span data-ttu-id="d316a-151">Wenn *g \_ PPlayer* **null** ist, ruft die Funktion [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) auf, um eine neue Instanz des Media Player-Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d316a-151">If *g\_pPlayer* is **NULL**, the function calls [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create a new instance of the media player object.</span></span> <span data-ttu-id="d316a-152">Die Eingabeparameter für **mfpkreatemediaplayer** enthalten einen Zeiger auf die Rückruf Schnittstelle und ein Handle für das Videofenster.</span><span class="sxs-lookup"><span data-stu-id="d316a-152">The input parameters to **MFPCreateMediaPlayer** include a pointer to the callback interface and a handle to the video window.</span></span>
2.  <span data-ttu-id="d316a-153">Um die Mediendatei zu öffnen, ruft die Funktion [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)auf und übergibt dabei die URL der Datei.</span><span class="sxs-lookup"><span data-stu-id="d316a-153">To open the media file, the function calls [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), passing in the URL of the file.</span></span> <span data-ttu-id="d316a-154">Diese Methode wird asynchron abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d316a-154">This method completes asynchronously.</span></span> <span data-ttu-id="d316a-155">Wenn der Vorgang abgeschlossen ist, wird die [**imfpmediaplayercallback:: onmediaplayerevent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) -Methode der Anwendung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d316a-155">When it completes, the application's [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is called.</span></span>


```C++
HRESULT PlayMediaFile(HWND hwnd, PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    // Create the MFPlayer object.
    if (g_pPlayer == NULL)
    {
        g_pPlayerCB = new (std::nothrow) MediaPlayerCallback();

        if (g_pPlayerCB == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFPCreateMediaPlayer(
            NULL,
            FALSE,          // Start playback automatically?
            0,              // Flags
            g_pPlayerCB,    // Callback pointer
            hwnd,           // Video window
            &g_pPlayer
            );
    }

    // Create a new media item for this URL.

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromURL(pszURL, FALSE, 0, NULL);
    }

    // The CreateMediaItemFromURL method completes asynchronously.
    // The application will receive an MFP_EVENT_TYPE_MEDIAITEM_CREATED
    // event. See MediaPlayerCallback::OnMediaPlayerEvent().

    return hr;
}
```



<span data-ttu-id="d316a-156">Die- `OnFileOpen` Funktion zeigt das allgemeine Datei Dialogfeld an, das es dem Benutzer ermöglicht, eine Datei für die Wiedergabe auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d316a-156">The `OnFileOpen` function displays the common file dialog, which enables the user to select a file for playback.</span></span> <span data-ttu-id="d316a-157">Die **IFileOpenDialog** -Schnittstelle wird verwendet, um das allgemeine Datei Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d316a-157">The **IFileOpenDialog** interface is used to display the common file dialog.</span></span> <span data-ttu-id="d316a-158">Diese Schnittstelle ist Teil der Windows Shell-APIs. Es wurde in Windows Vista als Ersatz für die ältere **GetOpenFileName** -Funktion eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d316a-158">This interface is part of the Windows Shell APIs; it was introduced in Windows Vista as a replacement for the older **GetOpenFileName** function.</span></span> <span data-ttu-id="d316a-159">Nachdem der Benutzer eine Datei ausgewählt hat, `OnFileOpen` ruft `PlayMediaFile` auf, um die Wiedergabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="d316a-159">After the user selects a file, `OnFileOpen` calls `PlayMediaFile` to start playback.</span></span>


```C++
void OnFileOpen(HWND hwnd)
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;
    PWSTR pwszFilePath = NULL;

    // Create the FileOpenDialog object.
    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL,
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->SetTitle(L"Select a File to Play");
    }

    // Show the file-open dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(hwnd);
    }

    if (hr == HRESULT_FROM_WIN32(ERROR_CANCELLED))
    {
        // User canceled.
        SafeRelease(&pFileOpen);
        return;
    }

    // Get the file name from the dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pItem->GetDisplayName(SIGDN_URL, &pwszFilePath);
    }

    // Open the media file.
    if (SUCCEEDED(hr))
    {
        hr = PlayMediaFile(hwnd, pwszFilePath);
    }

    if (FAILED(hr))
    {
        ShowErrorMessage(L"Could not open file.", hr);
    }

    CoTaskMemFree(pwszFilePath);

    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
}
```



## <a name="window-message-handlers"></a><span data-ttu-id="d316a-160">Fenster Meldungs Handler</span><span class="sxs-lookup"><span data-stu-id="d316a-160">Window Message Handlers</span></span>

<span data-ttu-id="d316a-161">Deklarieren Sie als nächstes Nachrichten Handler für die folgenden Fenster Meldungen:</span><span class="sxs-lookup"><span data-stu-id="d316a-161">Next, declare message handlers for the following window messages:</span></span>

-   <span data-ttu-id="d316a-162">**WM- \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="d316a-162">**WM\_PAINT**</span></span>
-   <span data-ttu-id="d316a-163">**WM- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="d316a-163">**WM\_SIZE**</span></span>
-   <span data-ttu-id="d316a-164">**WM \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="d316a-164">**WM\_CLOSE**</span></span>

<span data-ttu-id="d316a-165">Für die **WM \_** -Zeichnungs Nachricht müssen Sie nachverfolgen, ob das Video derzeit wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d316a-165">For the **WM\_PAINT** message, you must track whether video is currently playing.</span></span> <span data-ttu-id="d316a-166">Wenn dies der Fall ist, müssen Sie die [**imfpmediaplayer:: Updatevideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d316a-166">If so, call the [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method.</span></span> <span data-ttu-id="d316a-167">Diese Methode bewirkt, dass das Player-Objekt den neuesten Videorahmen neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="d316a-167">This method causes the player object to redraw the most recent video frame.</span></span>

<span data-ttu-id="d316a-168">Wenn kein Video vorhanden ist, ist die Anwendung dafür verantwortlich, das Fenster zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d316a-168">If there is no video, the application is responsible for painting the window.</span></span> <span data-ttu-id="d316a-169">In diesem Tutorial Ruft die Anwendung einfach die GDI **fillRect** -Funktion auf, um den gesamten Client Bereich auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="d316a-169">For this tutorial, the application simply calls the GDI **FillRect** function to fill the entire client area.</span></span>


```C++
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_bHasVideo)
    {
        // Playback has started and there is video.

        // Do not draw the window background, because the video
        // frame fills the entire client area.

        g_pPlayer->UpdateVideo();
    }
    else
    {
        // There is no video stream, or playback has not started.
        // Paint the entire client area.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
    }

    EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="d316a-170">Geben Sie für die Meldung **WM \_ size** den Wert [**imfpmediaplayer:: Updatevideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)ein.</span><span class="sxs-lookup"><span data-stu-id="d316a-170">For the **WM\_SIZE** message, call [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span> <span data-ttu-id="d316a-171">Diese Methode bewirkt, dass das Player-Objekt das Video mit der aktuellen Fenstergröße umpasst.</span><span class="sxs-lookup"><span data-stu-id="d316a-171">This method causes the player object to readjust the video to match the current size of the window.</span></span> <span data-ttu-id="d316a-172">Beachten Sie, dass **Updatevideo** sowohl für **WM \_ Paint** als auch für **WM \_ size** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d316a-172">Note that **UpdateVideo** is used for both **WM\_PAINT** and **WM\_SIZE**.</span></span>


```C++
void OnSize(HWND /*hwnd*/, UINT state, int /*cx*/, int /*cy*/)
{
    if (state == SIZE_RESTORED)
    {
        if (g_pPlayer)
        {
            // Resize the video.
            g_pPlayer->UpdateVideo();
        }
    }
}
```



<span data-ttu-id="d316a-173">Geben Sie für die Meldung zum **\_ Schließen der WM** den [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -und den [**imfpmediaplayercallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) -Zeiger frei.</span><span class="sxs-lookup"><span data-stu-id="d316a-173">For the **WM\_CLOSE** message, release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) and [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) pointers.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a><span data-ttu-id="d316a-174">Implementieren der Rückruf Methode</span><span class="sxs-lookup"><span data-stu-id="d316a-174">Implement the Callback Method</span></span>

<span data-ttu-id="d316a-175">Die [**imfpmediaplayercallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) -Schnittstelle definiert eine einzige Methode, [**onmediaplayerevent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="d316a-175">The [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="d316a-176">Diese Methode benachrichtigt die Anwendung immer dann, wenn während der Wiedergabe ein Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="d316a-176">This method notifies the application whenever an event occurs during playback.</span></span> <span data-ttu-id="d316a-177">Die-Methode nimmt einen Parameter an, einen Zeiger auf eine [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Struktur.</span><span class="sxs-lookup"><span data-stu-id="d316a-177">The method takes one parameter, a pointer to an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="d316a-178">Der **eeventtype** -Member der-Struktur gibt das Ereignis an, das aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d316a-178">The **eEventType** member of the structure specifies the event that occurred.</span></span>

<span data-ttu-id="d316a-179">Auf die [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Struktur folgen möglicherweise weitere Daten.</span><span class="sxs-lookup"><span data-stu-id="d316a-179">The [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure may be followed by additional data.</span></span> <span data-ttu-id="d316a-180">Für jeden Ereignistyp wird ein Makro definiert, das den **MFP- \_ Ereignis \_ Header** Zeiger in eine ereignisspezifische Struktur umwandelt.</span><span class="sxs-lookup"><span data-stu-id="d316a-180">For each event type, a macro is defined that casts the **MFP\_EVENT\_HEADER** pointer to an event-specific structure.</span></span> <span data-ttu-id="d316a-181">(Siehe [**MFP \_ - \_ Ereignistyp**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)</span><span class="sxs-lookup"><span data-stu-id="d316a-181">(See [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)</span></span>

<span data-ttu-id="d316a-182">Für dieses Tutorial sind zwei Ereignisse maßgeblich:</span><span class="sxs-lookup"><span data-stu-id="d316a-182">For this tutorial, two events are significant:</span></span>



| <span data-ttu-id="d316a-183">Ereignis</span><span class="sxs-lookup"><span data-stu-id="d316a-183">Event</span></span>                                    | <span data-ttu-id="d316a-184">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d316a-184">Description</span></span>                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d316a-185">**MFP \_ - \_ Ereignistyp \_ mediaitem \_ erstellt**</span><span class="sxs-lookup"><span data-stu-id="d316a-185">**MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED**</span></span> | <span data-ttu-id="d316a-186">Wird gesendet, wenn die " [**kreatemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) " abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d316a-186">Sent when the [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) completes.</span></span> |
| <span data-ttu-id="d316a-187">**MFP \_ - \_ Ereignistyp \_ mediaitem \_ festgelegt**</span><span class="sxs-lookup"><span data-stu-id="d316a-187">**MFP\_EVENT\_TYPE\_MEDIAITEM\_SET**</span></span>     | <span data-ttu-id="d316a-188">Wird gesendet, wenn [**setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d316a-188">Sent when [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) completes.</span></span>                         |



 

<span data-ttu-id="d316a-189">Der folgende Code zeigt, wie Sie den [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in die ereignisspezifische Struktur umwandeln.</span><span class="sxs-lookup"><span data-stu-id="d316a-189">The following code shows how to cast the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) pointer to the event-specific structure.</span></span>


```C++
void MediaPlayerCallback::OnMediaPlayerEvent(MFP_EVENT_HEADER * pEventHeader)
{
    if (FAILED(pEventHeader->hrEvent))
    {
        ShowErrorMessage(L"Playback error", pEventHeader->hrEvent);
        return;
    }

    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_MEDIAITEM_CREATED:
        OnMediaItemCreated(MFP_GET_MEDIAITEM_CREATED_EVENT(pEventHeader));
        break;

    case MFP_EVENT_TYPE_MEDIAITEM_SET:
        OnMediaItemSet(MFP_GET_MEDIAITEM_SET_EVENT(pEventHeader));
        break;
    }
}
```



<span data-ttu-id="d316a-190">Mit dem Ereignis **MFP- \_ \_ Ereignistyp \_ mediaitem \_ wurde** die Anwendung benachrichtigt, dass die [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) -Methode abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d316a-190">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event notifies the application that the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method has completed.</span></span> <span data-ttu-id="d316a-191">Die Ereignis Struktur enthält einen Zeiger auf die [**imfpmediaitem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) -Schnittstelle, die das aus der URL erstellte Medien Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="d316a-191">The event structure contains a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which represents the media item created from the URL.</span></span> <span data-ttu-id="d316a-192">Um das Element für die Wiedergabe in die Warteschlange zu stellen, übergeben Sie diesen Zeiger an die [**imfpmediaplayer:: setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) -Methode:</span><span class="sxs-lookup"><span data-stu-id="d316a-192">To queue the item for playback, pass this pointer to the [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method:</span></span>


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    // The media item was created successfully.

    if (g_pPlayer)
    {
        BOOL    bHasVideo = FALSE;
        BOOL    bIsSelected = FALSE;

        // Check if the media item contains video.
        HRESULT hr = pEvent->pMediaItem->HasVideo(&bHasVideo, &bIsSelected);
        if (SUCCEEDED(hr))
        {
            g_bHasVideo = bHasVideo && bIsSelected;

            // Set the media item on the player. This method completes
            // asynchronously.
            hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
        }

        if (FAILED(hr))
        {
            ShowErrorMessage(L"Error playing this file.", hr);
        }
   }
}
```



<span data-ttu-id="d316a-193">Der Ereignis Ereignis **\_ \_ \_ \_ Satz "mediaitem" vom MFP-Ereignistyp** benachrichtigt die Anwendung, dass [**setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d316a-193">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event notifies the application that [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) has completed.</span></span> <span data-ttu-id="d316a-194">[**Imfpmediaplayer wird aufgerufen::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , um die Wiedergabe zu starten:</span><span class="sxs-lookup"><span data-stu-id="d316a-194">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback:</span></span>


```C++
void OnMediaItemSet(MFP_MEDIAITEM_SET_EVENT * /*pEvent*/)
{
    HRESULT hr = g_pPlayer->Play();
    if (FAILED(hr))
    {
        ShowErrorMessage(L"IMFPMediaPlayer::Play failed.", hr);
    }
}
```



## <a name="implement-winmain"></a><span data-ttu-id="d316a-195">Implementieren von WinMain</span><span class="sxs-lookup"><span data-stu-id="d316a-195">Implement WinMain</span></span>

<span data-ttu-id="d316a-196">Im restlichen Teil dieses Tutorials gibt es keine Aufrufe von Media Foundation-APIs.</span><span class="sxs-lookup"><span data-stu-id="d316a-196">In the remainder of this tutorial, there are no calls to Media Foundation APIs.</span></span> <span data-ttu-id="d316a-197">Der folgende Code zeigt die Fenster Prozedur:</span><span class="sxs-lookup"><span data-stu-id="d316a-197">The following code shows the window procedure:</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        HANDLE_MSG(hwnd, WM_CLOSE,   OnClose);
        HANDLE_MSG(hwnd, WM_PAINT,   OnPaint);
        HANDLE_MSG(hwnd, WM_COMMAND, OnCommand);
        HANDLE_MSG(hwnd, WM_SIZE,    OnSize);

    case WM_ERASEBKGND:
        return 1;

    default:
        return DefWindowProc(hwnd, uMsg, wParam, lParam);
    }
}
```



<span data-ttu-id="d316a-198">Die `InitializeWindow` -Funktion registriert die Fenster Klasse der Anwendung und erstellt das Fenster.</span><span class="sxs-lookup"><span data-stu-id="d316a-198">The `InitializeWindow` function registers the application's window class and creates the window.</span></span>


```C++
BOOL InitializeWindow(HWND *pHwnd)
{
    const wchar_t CLASS_NAME[]  = L"MFPlay Window Class";
    const wchar_t WINDOW_NAME[] = L"MFPlay Sample Application";

    WNDCLASS wc = {};

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = GetModuleHandle(NULL);
    wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wc.lpszClassName = CLASS_NAME;
    wc.lpszMenuName  = MAKEINTRESOURCE(IDR_MENU1);

    RegisterClass(&wc);

    HWND hwnd = CreateWindow(
        CLASS_NAME, WINDOW_NAME, WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,
        NULL, NULL, GetModuleHandle(NULL), NULL);

    if (!hwnd)
    {
        return FALSE;
    }

    ShowWindow(hwnd, SW_SHOWDEFAULT);
    UpdateWindow(hwnd);

    *pHwnd = hwnd;

    return TRUE;
}
```



<span data-ttu-id="d316a-199">Implementieren Sie schließlich den Anwendungs Einstiegspunkt:</span><span class="sxs-lookup"><span data-stu-id="d316a-199">Finally, implement the application entry point:</span></span>


```C++
int WINAPI wWinMain(HINSTANCE, HINSTANCE, PWSTR, int)
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    HRESULT hr = CoInitializeEx(NULL,
        COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        return 0;
    }

    HWND hwnd = NULL;
    if (InitializeWindow(&hwnd))
    {
        // Message loop
        MSG msg = {};
        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }

        DestroyWindow(hwnd);
    }
    CoUninitialize();

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d316a-200">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d316a-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d316a-201">Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="d316a-201">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 




---
description: In diesem Tutorial wird eine vollständige Anwendung gezeigt, die Videos mithilfe von MFPlay abspielt.
ms.assetid: f72a7c1f-b059-474c-96f2-8fad3b1f7035
title: 'MFPlay-Tutorial: Videowiedergabe'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5b98de6cc845d121928fb18a33db055154f717e8fe583bcd1ad6ef8da32deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242007"
---
# <a name="mfplay-tutorial-video-playback"></a>MFPlay-Tutorial: Videowiedergabe

\[MFPlay steht für die Verwendung in den betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Tutorial wird eine vollständige Anwendung gezeigt, die Videos mithilfe von MFPlay abspielt. Sie basiert auf dem [SimplePlay SDK-Beispiel.](simpleplay-sample.md)

Dieses Tutorial enthält die folgenden Abschnitte:

-   [Anforderungen](#requirements)
-   [Header- und Bibliotheksdateien](#header-and-library-files)
-   [Globale Variablen](#global-variables)
-   [Deklarieren der Rückrufklasse](#declare-the-callback-class)
-   [Deklarieren der SafeRelease-Funktion](#declare-the-saferelease-function)
-   [Öffnen einer Mediendatei](#open-a-media-file)
-   [Fenstermeldungshandler](#window-message-handlers)
-   [Implementieren der Rückrufmethode](#implement-the-callback-method)
-   [Implementieren von WinMain](#implement-winmain)
-   [Zugehörige Themen](#related-topics)

Eine ausführlichere Erläuterung der MFPlay-API finden Sie unter Erste Schritte [mit MFPlay.](getting-started-with-mfplay.md)

## <a name="requirements"></a>Anforderungen

MFPlay erfordert Windows 7.

## <a name="header-and-library-files"></a>Header- und Bibliotheksdateien

Schließen Sie die folgenden Headerdateien in Ihr Projekt ein:


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



Link zu den folgenden Codebibliotheken:

-   mfplay.lib
-   shlwapi.lib

## <a name="global-variables"></a>Globale Variablen

Deklarieren Sie die folgenden globalen Variablen:


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



Diese Variablen werden wie folgt verwendet:

<dl> <dt>

<span id="g_hwnd"></span><span id="G_HWND"></span>*g \_ hwnd*
</dt> <dd>

Ein Handle für das Anwendungsfenster.

</dd> <dt>

<span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ bVideo*
</dt> <dd>

Ein boolescher Wert, der verfolgt, ob das Video abspielt.

</dd> <dt>

<span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ pPlayer*
</dt> <dd>

Ein Zeiger auf die [**IMFPMediaPlayer-Schnittstelle.**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) Diese Schnittstelle wird verwendet, um die Wiedergabe zu steuern.

</dd> <dt>

<span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ pCallback*
</dt> <dd>

Ein Zeiger auf die [**IMFPMediaPlayerCallback-Schnittstelle.**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) Die Anwendung implementiert diese Rückrufschnittstelle, um Benachrichtigungen vom Playerobjekt zu erhalten.

</dd> </dl>

## <a name="declare-the-callback-class"></a>Deklarieren der Rückrufklasse

Um Ereignisbenachrichtigungen vom Playerobjekt zu erhalten, muss die Anwendung die [**IMFPMediaPlayerCallback-Schnittstelle**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) implementieren. Der folgende Code deklariert eine Klasse, die die -Schnittstelle implementiert. Die einzige Membervariable ist *m \_ cRef,* in der die Verweisanzahl gespeichert wird.

Die **IUnknown-Methoden** werden inline implementiert. Die Implementierung der [**IMFPMediaPlayerCallback::OnMediaPlayerEvent-Methode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) wird später gezeigt. Siehe [Implementieren der Rückrufmethode](#implement-the-callback-method).


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



## <a name="declare-the-saferelease-function"></a>Deklarieren der SafeRelease-Funktion

In diesem Tutorial wird die [SafeRelease-Funktion](saferelease.md) verwendet, um Schnittstellenzeigen zu veröffentlichen:


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



## <a name="open-a-media-file"></a>Öffnen einer Mediendatei

Die `PlayMediaFile` Funktion öffnet wie folgt eine Mediendatei:

1.  Wenn *g \_ pPlayer* NULL **ist,** ruft die Funktion [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) auf, um eine neue Instanz des Media Player-Objekts zu erstellen. Die Eingabeparameter für **MFPCreateMediaPlayer** enthalten einen Zeiger auf die Rückrufschnittstelle und ein Handle für das Videofenster.
2.  Um die Mediendatei zu öffnen, ruft die Funktion [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)auf und über gibt die URL der Datei an. Diese Methode wird asynchron abgeschlossen. Nach Abschluss wird die [**IMFPMediaPlayerCallback::OnMediaPlayerEvent-Methode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) der Anwendung aufgerufen.


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



Die `OnFileOpen` Funktion zeigt das Allgemeine Dateidialogfeld an, mit dem der Benutzer eine Datei für die Wiedergabe auswählen kann. Die **IFileOpenDialog-Schnittstelle** wird verwendet, um das Allgemeine Dateidialogfeld anzuzeigen. Diese Schnittstelle ist Teil der Windows Shell-APIs. es wurde in Windows Vista als Ersatz für die ältere **GetOpenFileName-Funktion** eingeführt. Nachdem der Benutzer eine Datei ausgewählt hat, ruft `OnFileOpen` auf, `PlayMediaFile` um die Wiedergabe zu starten.


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



## <a name="window-message-handlers"></a>Fenstermeldungshandler

Deklarieren Sie als Nächstes Meldungshandler für die folgenden Fenstermeldungen:

-   **WM \_ PAINT**
-   **WM \_ SIZE**
-   **WM \_ CLOSE**

Für die **WM \_ PAINT-Nachricht** müssen Sie nachverfolgen, ob das Video gerade abspielt. Wenn ja, rufen Sie die [**IMFPMediaPlayer::UpdateVideo-Methode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) auf. Diese Methode bewirkt, dass das Player-Objekt den letzten Videoframe neu gezeichnet hat.

Wenn kein Video angezeigt wird, ist die Anwendung für das Malen des Fensters verantwortlich. In diesem Tutorial ruft die Anwendung einfach die GDI **FillRect-Funktion** auf, um den gesamten Clientbereich zu füllen.


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



Rufen Sie **für die \_ WM SIZE-Meldung** [**IMFPMediaPlayer::UpdateVideo auf.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) Diese Methode bewirkt, dass das Player-Objekt das Video an die aktuelle Größe des Fensters anpasst. Beachten **Sie, dass UpdateVideo** sowohl für **WM \_ PAINT** als auch **für WM SIZE verwendet \_ wird.**


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



Geben Sie **für die \_ WM CLOSE-Nachricht** die [**Zeiger IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) und [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) frei.


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a>Implementieren der Rückrufmethode

Die [**IMFPMediaPlayerCallback-Schnittstelle**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) definiert eine einzelne Methode, [**OnMediaPlayerEvent.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) Diese Methode benachrichtigt die Anwendung, wenn während der Wiedergabe ein Ereignis auftritt. Die -Methode akzeptiert einen Parameter, einen Zeiger auf eine [**MFP \_ EVENT \_ HEADER-Struktur.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Der **eEventType-Member** der -Struktur gibt das aufgetretene Ereignis an.

Auf [**die MFP \_ EVENT \_ HEADER-Struktur**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) können zusätzliche Daten folgen. Für jeden Ereignistyp wird ein Makro definiert, das den **MFP \_ EVENT \_ HEADER-Zeiger** in eine ereignisspezifische Struktur umformt. (Siehe [**\_ MFP-EREIGNISTYP \_**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)

Für dieses Tutorial sind zwei Ereignisse von Bedeutung:



| Ereignis                                    | BESCHREIBUNG                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| **\_ \_ MFP-EREIGNISTYP \_ MEDIAITEM \_ ERSTELLT** | Wird gesendet, [**wenn CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) abgeschlossen ist. |
| **\_ \_ MFP-EREIGNISTYP \_ MEDIAITEM \_ SET**     | Wird [**gesendet, wenn SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) abgeschlossen ist.                         |



 

Der folgende Code zeigt, wie der [**MFP \_ EVENT \_ HEADER-Zeiger**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) in die ereignisspezifische Struktur umgeformt wird.


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



Das **MFP \_ EVENT TYPE \_ \_ MEDIAITEM \_ CREATED-Ereignis** benachrichtigt die Anwendung, dass die [**IMFPMediaPlayer::CreateMediaItemFromURL-Methode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) abgeschlossen wurde. Die Ereignisstruktur enthält einen Zeiger auf die [**IMFPMediaItem-Schnittstelle,**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) die das aus der URL erstellte Medienelement darstellt. Um das Element für die Wiedergabe in die Warteschlange zu stellen, übergeben Sie diesen Zeiger an die [**IMFPMediaPlayer::SetMediaItem-Methode:**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem)


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



Das **MFP \_ EVENT TYPE \_ \_ MEDIAITEM \_ SET-Ereignis** benachrichtigt die Anwendung, dass [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) abgeschlossen wurde. Rufen [**Sie IMFPMediaPlayer::P lay auf,**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) um die Wiedergabe zu starten:


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



## <a name="implement-winmain"></a>Implementieren von WinMain

Im weiteren Verlauf dieses Tutorials werden keine Aufrufe Media Foundation APIs. Der folgende Code zeigt die Fensterprozedur:


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



Die `InitializeWindow` -Funktion registriert die Fensterklasse der Anwendung und erstellt das Fenster.


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



Implementieren Sie abschließend den Anwendungseinstiegspunkt:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MFPlay für die Audio-/Videowiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 




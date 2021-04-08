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
# <a name="mfplay-tutorial-video-playback"></a>MF Play-Tutorial: Video Wiedergabe

\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

Dieses Tutorial zeigt eine komplette Anwendung, die Videos mit MF Play wieder gibt. Es basiert auf dem [simpleplay](simpleplay-sample.md) SDK-Beispiel.

Dieses Tutorial enthält die folgenden Abschnitte:

-   [Anforderungen](#requirements)
-   [Header-und Bibliotheksdateien](#header-and-library-files)
-   [Globale Variablen](#global-variables)
-   [Deklaration der Rückruf Klasse](#declare-the-callback-class)
-   [Deklarieren der saferelease-Funktion](#declare-the-saferelease-function)
-   [Öffnen einer Mediendatei](#open-a-media-file)
-   [Fenster Meldungs Handler](#window-message-handlers)
-   [Implementieren der Rückruf Methode](#implement-the-callback-method)
-   [Implementieren von WinMain](#implement-winmain)
-   [Zugehörige Themen](#related-topics)

Eine ausführlichere Erläuterung der MF Play-API finden Sie unter [Getting Started with MF](getting-started-with-mfplay.md).

## <a name="requirements"></a>Anforderungen

MF Play erfordert Windows 7.

## <a name="header-and-library-files"></a>Header-und Bibliotheksdateien

Fügen Sie die folgenden Header Dateien in das Projekt ein:


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



Verknüpfung mit den folgenden Codebibliotheken:

-   MF Play. lib
-   shlwapi. lib

## <a name="global-variables"></a>Globale Variablen

Deklarieren Sie die folgenden globalen Variablen:


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



Diese Variablen werden wie folgt verwendet:

<dl> <dt>

<span id="g_hwnd"></span><span id="G_HWND"></span>*g \_ HWND*
</dt> <dd>

Ein Handle für das Anwendungsfenster.

</dd> <dt>

<span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ bvideo*
</dt> <dd>

Ein boolescher Wert, der nachverfolgt, ob Videos abgespielt werden.

</dd> <dt>

<span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ PPlayer*
</dt> <dd>

Ein Zeiger auf die [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -Schnittstelle. Diese Schnittstelle wird zum Steuern der Wiedergabe verwendet.

</dd> <dt>

<span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ pCallback*
</dt> <dd>

Ein Zeiger auf die [**imfpmediaplayercallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) -Schnittstelle. Die Anwendung implementiert diese Rückruf Schnittstelle, um Benachrichtigungen vom Player-Objekt zu erhalten.

</dd> </dl>

## <a name="declare-the-callback-class"></a>Deklaration der Rückruf Klasse

Um Ereignis Benachrichtigungen aus dem Player-Objekt zu erhalten, muss die Anwendung die [**imfpmediaplayercallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) -Schnittstelle implementieren. Im folgenden Code wird eine Klasse deklariert, die die-Schnittstelle implementiert. Die einzige Member-Variable ist *m- \_ kref*, die den Verweis Zähler speichert.

Die **IUnknown** -Methoden werden Inline implementiert. Die Implementierung der [**imfpmediaplayercallback:: onmediaplayerevent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) -Methode wird später angezeigt. Weitere Informationen finden Sie [unter Implementieren der Rückruf Methode](#implement-the-callback-method).


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



## <a name="declare-the-saferelease-function"></a>Deklarieren der saferelease-Funktion

In diesem Tutorial wird die [saferelease](saferelease.md) -Funktion verwendet, um Schnittstellen Zeiger freizugeben:


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

1.  Wenn *g \_ PPlayer* **null** ist, ruft die Funktion [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) auf, um eine neue Instanz des Media Player-Objekts zu erstellen. Die Eingabeparameter für **mfpkreatemediaplayer** enthalten einen Zeiger auf die Rückruf Schnittstelle und ein Handle für das Videofenster.
2.  Um die Mediendatei zu öffnen, ruft die Funktion [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)auf und übergibt dabei die URL der Datei. Diese Methode wird asynchron abgeschlossen. Wenn der Vorgang abgeschlossen ist, wird die [**imfpmediaplayercallback:: onmediaplayerevent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) -Methode der Anwendung aufgerufen.


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



Die- `OnFileOpen` Funktion zeigt das allgemeine Datei Dialogfeld an, das es dem Benutzer ermöglicht, eine Datei für die Wiedergabe auszuwählen. Die **IFileOpenDialog** -Schnittstelle wird verwendet, um das allgemeine Datei Dialogfeld anzuzeigen. Diese Schnittstelle ist Teil der Windows Shell-APIs. Es wurde in Windows Vista als Ersatz für die ältere **GetOpenFileName** -Funktion eingeführt. Nachdem der Benutzer eine Datei ausgewählt hat, `OnFileOpen` ruft `PlayMediaFile` auf, um die Wiedergabe zu starten.


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



## <a name="window-message-handlers"></a>Fenster Meldungs Handler

Deklarieren Sie als nächstes Nachrichten Handler für die folgenden Fenster Meldungen:

-   **WM- \_ Paint**
-   **WM- \_ Größe**
-   **WM \_ Schließen**

Für die **WM \_** -Zeichnungs Nachricht müssen Sie nachverfolgen, ob das Video derzeit wiedergegeben wird. Wenn dies der Fall ist, müssen Sie die [**imfpmediaplayer:: Updatevideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) -Methode aufrufen. Diese Methode bewirkt, dass das Player-Objekt den neuesten Videorahmen neu zeichnet.

Wenn kein Video vorhanden ist, ist die Anwendung dafür verantwortlich, das Fenster zu zeichnen. In diesem Tutorial Ruft die Anwendung einfach die GDI **fillRect** -Funktion auf, um den gesamten Client Bereich auszufüllen.


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



Geben Sie für die Meldung **WM \_ size** den Wert [**imfpmediaplayer:: Updatevideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)ein. Diese Methode bewirkt, dass das Player-Objekt das Video mit der aktuellen Fenstergröße umpasst. Beachten Sie, dass **Updatevideo** sowohl für **WM \_ Paint** als auch für **WM \_ size** verwendet wird.


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



Geben Sie für die Meldung zum **\_ Schließen der WM** den [**imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) -und den [**imfpmediaplayercallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) -Zeiger frei.


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a>Implementieren der Rückruf Methode

Die [**imfpmediaplayercallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) -Schnittstelle definiert eine einzige Methode, [**onmediaplayerevent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent). Diese Methode benachrichtigt die Anwendung immer dann, wenn während der Wiedergabe ein Ereignis auftritt. Die-Methode nimmt einen Parameter an, einen Zeiger auf eine [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Struktur. Der **eeventtype** -Member der-Struktur gibt das Ereignis an, das aufgetreten ist.

Auf die [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Struktur folgen möglicherweise weitere Daten. Für jeden Ereignistyp wird ein Makro definiert, das den **MFP- \_ Ereignis \_ Header** Zeiger in eine ereignisspezifische Struktur umwandelt. (Siehe [**MFP \_ - \_ Ereignistyp**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)

Für dieses Tutorial sind zwei Ereignisse maßgeblich:



| Ereignis                                    | BESCHREIBUNG                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| **MFP \_ - \_ Ereignistyp \_ mediaitem \_ erstellt** | Wird gesendet, wenn die " [**kreatemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) " abgeschlossen ist. |
| **MFP \_ - \_ Ereignistyp \_ mediaitem \_ festgelegt**     | Wird gesendet, wenn [**setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) abgeschlossen ist.                         |



 

Der folgende Code zeigt, wie Sie den [**MFP- \_ Ereignis \_ Header**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) Zeiger in die ereignisspezifische Struktur umwandeln.


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



Mit dem Ereignis **MFP- \_ \_ Ereignistyp \_ mediaitem \_ wurde** die Anwendung benachrichtigt, dass die [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) -Methode abgeschlossen wurde. Die Ereignis Struktur enthält einen Zeiger auf die [**imfpmediaitem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) -Schnittstelle, die das aus der URL erstellte Medien Element darstellt. Um das Element für die Wiedergabe in die Warteschlange zu stellen, übergeben Sie diesen Zeiger an die [**imfpmediaplayer:: setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) -Methode:


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



Der Ereignis Ereignis **\_ \_ \_ \_ Satz "mediaitem" vom MFP-Ereignistyp** benachrichtigt die Anwendung, dass [**setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) abgeschlossen wurde. [**Imfpmediaplayer wird aufgerufen::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , um die Wiedergabe zu starten:


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

Im restlichen Teil dieses Tutorials gibt es keine Aufrufe von Media Foundation-APIs. Der folgende Code zeigt die Fenster Prozedur:


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



Die `InitializeWindow` -Funktion registriert die Fenster Klasse der Anwendung und erstellt das Fenster.


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



Implementieren Sie schließlich den Anwendungs Einstiegspunkt:


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

[Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 




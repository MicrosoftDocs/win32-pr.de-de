---
description: Dieses Thema ist Schritt 1 des Tutorials Audio-/Videowiedergabe in DirectShow.
ms.assetid: 3ccd201d-e60d-40bf-a602-6d42df03b36b
title: 'Schritt 1: Deklarieren der dshowplayer-Klasse'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22ff36a76be8017f7b468815cf572514900f8d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356263"
---
# <a name="step-1-declare-the-dshowplayer-class"></a>Schritt 1: Deklarieren der dshowplayer-Klasse

Dieses Thema ist Schritt 1 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md). Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.

In diesem Tutorial verwaltet die- `DShowPlayer` Klasse alle DirectShow-Funktionen. Diese Klasse wird als folows deklariert.


```C++
#include <new>
#include <windows.h>
#include <dshow.h>


enum PlaybackState
{
    STATE_NO_GRAPH,
    STATE_RUNNING,
    STATE_PAUSED,
    STATE_STOPPED,
};

const UINT WM_GRAPH_EVENT = WM_APP + 1;

typedef void (CALLBACK *GraphEventFN)(HWND hwnd, long eventCode, LONG_PTR param1, LONG_PTR param2);

class DShowPlayer
{
public:
    DShowPlayer(HWND hwnd);
    ~DShowPlayer();

    PlaybackState State() const { return m_state; }

    HRESULT OpenFile(PCWSTR pszFileName);
    
    HRESULT Play();
    HRESULT Pause();
    HRESULT Stop();

    BOOL    HasVideo() const;
    HRESULT UpdateVideoWindow(const LPRECT prc);
    HRESULT Repaint(HDC hdc);
    HRESULT DisplayModeChanged();

    HRESULT HandleGraphEvent(GraphEventFN pfnOnGraphEvent);

private:
    HRESULT InitializeGraph();
    void    TearDownGraph();
    HRESULT CreateVideoRenderer();
    HRESULT RenderStreams(IBaseFilter *pSource);

    PlaybackState   m_state;

    HWND m_hwnd; // Video window. This window also receives graph events.

    IGraphBuilder   *m_pGraph;
    IMediaControl   *m_pControl;
    IMediaEventEx   *m_pEvent;
    CVideoRenderer  *m_pVideo;
};
```





Hinweise:

-   Die- `PlaybackState` Enumeration beschreibt den aktuellen Status des- `DShowPlayer` Objekts.
-   Das Ereignis für die gleich-WM- \_ Diagramm Definition \_ definiert eine private Fenster Meldung. Diese Meldung wird verwendet, um die Anwendung über Filter Diagramm Ereignisse zu benachrichtigen. Weitere Informationen finden Sie unter [Step 6: handle Graph Events](step-6--handle-graph-events.md).
-   `GraphEventFN` ist ein Zeiger auf eine Rückruffunktion zum Verarbeiten von Filter Diagramm Ereignissen. Die Anwendung implementiert diese Rückruffunktion.
-   Die *m \_ pvideo* -Member-Variable stellt einen Wrapper für die verschiedenen DirectShow-Videorenderer bereit. Weitere Informationen finden Sie unter [Step 2: Declare cvideorenderer und abgeleitete Klassen](step-2--declare-cvideorenderer-and-derived-classes.md).
-   In diesem Tutorial wird die [saferelease](../medfound/saferelease.md) -Funktion verwendet, um COM-Schnittstellen Zeiger freizugeben.

Weiter: [Schritt 2: Deklarieren von cvideorenderer und abgeleiteten Klassen](step-2--declare-cvideorenderer-and-derived-classes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiowiedergabe und Video Wiedergabe in DirectShow](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 

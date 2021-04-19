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
# <a name="step-1-declare-the-dshowplayer-class"></a><span data-ttu-id="766a4-103">Schritt 1: Deklarieren der dshowplayer-Klasse</span><span class="sxs-lookup"><span data-stu-id="766a4-103">Step 1: Declare the DShowPlayer Class</span></span>

<span data-ttu-id="766a4-104">Dieses Thema ist Schritt 1 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="766a4-104">This topic is step 1 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="766a4-105">Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="766a4-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="766a4-106">In diesem Tutorial verwaltet die- `DShowPlayer` Klasse alle DirectShow-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="766a4-106">In this tutorial, the `DShowPlayer` class manages all DirectShow functionality.</span></span> <span data-ttu-id="766a4-107">Diese Klasse wird als folows deklariert.</span><span class="sxs-lookup"><span data-stu-id="766a4-107">This class is declared as folows.</span></span>


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





<span data-ttu-id="766a4-108">Hinweise:</span><span class="sxs-lookup"><span data-stu-id="766a4-108">Notes:</span></span>

-   <span data-ttu-id="766a4-109">Die- `PlaybackState` Enumeration beschreibt den aktuellen Status des- `DShowPlayer` Objekts.</span><span class="sxs-lookup"><span data-stu-id="766a4-109">The `PlaybackState` enumeration describes the current state of the `DShowPlayer` object.</span></span>
-   <span data-ttu-id="766a4-110">Das Ereignis für die gleich-WM- \_ Diagramm Definition \_ definiert eine private Fenster Meldung.</span><span class="sxs-lookup"><span data-stu-id="766a4-110">The constant WM\_GRAPH\_EVENT defines a private window message.</span></span> <span data-ttu-id="766a4-111">Diese Meldung wird verwendet, um die Anwendung über Filter Diagramm Ereignisse zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="766a4-111">This message is used to notify the application about filter graph events.</span></span> <span data-ttu-id="766a4-112">Weitere Informationen finden Sie unter [Step 6: handle Graph Events](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="766a4-112">See [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>
-   <span data-ttu-id="766a4-113">`GraphEventFN` ist ein Zeiger auf eine Rückruffunktion zum Verarbeiten von Filter Diagramm Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="766a4-113">`GraphEventFN` is a pointer to a callback function for handling filter graph events.</span></span> <span data-ttu-id="766a4-114">Die Anwendung implementiert diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="766a4-114">The application implements this callback function.</span></span>
-   <span data-ttu-id="766a4-115">Die *m \_ pvideo* -Member-Variable stellt einen Wrapper für die verschiedenen DirectShow-Videorenderer bereit.</span><span class="sxs-lookup"><span data-stu-id="766a4-115">The *m\_pVideo* member variable provides a wrapper for the various DirectShow video renderers.</span></span> <span data-ttu-id="766a4-116">Weitere Informationen finden Sie unter [Step 2: Declare cvideorenderer und abgeleitete Klassen](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="766a4-116">See [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>
-   <span data-ttu-id="766a4-117">In diesem Tutorial wird die [saferelease](../medfound/saferelease.md) -Funktion verwendet, um COM-Schnittstellen Zeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="766a4-117">Throughout this tutorial, the [SafeRelease](../medfound/saferelease.md) function is used to release COM interface pointers.</span></span>

<span data-ttu-id="766a4-118">Weiter: [Schritt 2: Deklarieren von cvideorenderer und abgeleiteten Klassen](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="766a4-118">Next: [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="766a4-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="766a4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="766a4-120">Audiowiedergabe und Video Wiedergabe in DirectShow</span><span class="sxs-lookup"><span data-stu-id="766a4-120">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> </dl>

 

 

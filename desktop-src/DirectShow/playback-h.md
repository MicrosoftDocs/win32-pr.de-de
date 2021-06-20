---
description: Dieser Artikel enthält Code für die Datei playback.h für das Tutorial Audio-/Videowiedergabe in DirectShow.
ms.assetid: 8cf0f281-3680-4329-80d0-8282d1051c1a
title: playback.h
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52dc50cd14b26bcd26284a62c96400706d8aa8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405113"
---
# <a name="playbackh"></a><span data-ttu-id="5e030-103">playback.h</span><span class="sxs-lookup"><span data-stu-id="5e030-103">playback.h</span></span>

<span data-ttu-id="5e030-104">Dieses Thema enthält Code für das Tutorial [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="5e030-104">This topic contains code for the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved.

#pragma once

class CVideoRenderer;

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



## <a name="related-topics"></a><span data-ttu-id="5e030-105">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e030-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e030-106">Audio-/Videowiedergabe in DirectShow</span><span class="sxs-lookup"><span data-stu-id="5e030-106">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="5e030-107">Beispiel für DirectShow-Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="5e030-107">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> </dl>

 

 




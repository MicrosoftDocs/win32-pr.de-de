---
description: Dieses Thema ist Schritt 7 des Tutorials Audio-/Videowiedergabe in DirectShow.
ms.assetid: 2e542a2d-fc71-41d5-9abd-0dfa70719c0f
title: 'Schritt 7: Transport Steuerelemente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b974ccc8c186b1915d2a6564870a0b177073544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351436"
---
# <a name="step-7-transport-controls"></a><span data-ttu-id="d53b8-103">Schritt 7: Transport Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d53b8-103">Step 7: Transport Controls</span></span>

<span data-ttu-id="d53b8-104">Dieses Thema ist Schritt 7 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="d53b8-104">This topic is step 7 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="d53b8-105">Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d53b8-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="d53b8-106">Der letzte Schritt besteht darin, Transport Steuerelemente hinzuzufügen (Wiedergabe, anhalten und anhalten).</span><span class="sxs-lookup"><span data-stu-id="d53b8-106">The last step is to add transport controls (play, pause, and stop).</span></span> <span data-ttu-id="d53b8-107">Um die Datei wiederzugeben, nennen Sie [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span><span class="sxs-lookup"><span data-stu-id="d53b8-107">To play the file, call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run).</span></span>


```C++
HRESULT DShowPlayer::Play()
{
    if (m_state != STATE_PAUSED && m_state != STATE_STOPPED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Run();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_RUNNING;
    }
    return hr;
}
```



<span data-ttu-id="d53b8-108">Um anzuhalten, nennen Sie [**IMediaControl::P ause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).</span><span class="sxs-lookup"><span data-stu-id="d53b8-108">To pause, call [**IMediaControl::Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause).</span></span>


```C++
HRESULT DShowPlayer::Pause()
{
    if (m_state != STATE_RUNNING)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_PAUSED;
    }
    return hr;
}
```



<span data-ttu-id="d53b8-109">Um den Vorgang zu unterbinden, nennen Sie [**IMediaControl:: Beendigung**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="d53b8-109">To stop, call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>


```C++
HRESULT DShowPlayer::Stop()
{
    if (m_state != STATE_RUNNING && m_state != STATE_PAUSED)
    {
        return VFW_E_WRONG_STATE;
    }

    HRESULT hr = m_pControl->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = STATE_STOPPED;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d53b8-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d53b8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d53b8-111">Audiowiedergabe und Video Wiedergabe in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d53b8-111">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="d53b8-112">Beispiel zur DirectShow-Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="d53b8-112">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="d53b8-113">Filter Zustände</span><span class="sxs-lookup"><span data-stu-id="d53b8-113">Filter States</span></span>](filter-states.md)
</dt> </dl>

 

 




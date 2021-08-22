---
description: Dieses Thema ist Schritt 7 des Tutorials Audio-/Videowiedergabe in DirectShow.
ms.assetid: 2e542a2d-fc71-41d5-9abd-0dfa70719c0f
title: 'Schritt 7: Transportsteuerelemente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8253efab566f5dc14a0d0210a26e84cb0a50113389d54b7a871d818a17296ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072414"
---
# <a name="step-7-transport-controls"></a>Schritt 7: Transportsteuerelemente

Dieses Thema ist Schritt 7 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md). Der vollständige Code wird im Thema [DirectShow Playback Example (DirectShow-Wiedergabebeispiel)](directshow-playback-example.md)gezeigt.

Der letzte Schritt ist das Hinzufügen von Transportsteuerelementen (Wiedergeben, Anhalten und Beenden). Rufen Sie [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run)auf, um die Datei wiederzuspielen.


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



Rufen Sie zum Anhalten [**IMediaControl::P ause auf.**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)


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



Rufen Sie zum Beenden [**IMediaControl::Stop auf.**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Beispiel für DirectShow-Wiedergabe](directshow-playback-example.md)
</dt> <dt>

[Filterzustände](filter-states.md)
</dt> </dl>

 

 




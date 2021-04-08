---
description: Dieses Thema ist Schritt 3 des Tutorials zum Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 'Schritt 3: Öffnen einer Mediendatei'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b50f036b84806f96e4349f77a3f06e02e08764
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104050702"
---
# <a name="step-3-open-a-media-file"></a><span data-ttu-id="172dc-103">Schritt 3: Öffnen einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="172dc-103">Step 3: Open a Media File</span></span>

<span data-ttu-id="172dc-104">Dieses Thema ist Schritt 3 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="172dc-104">This topic is step 3 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="172dc-105">Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="172dc-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="172dc-106">Die- `CPlayer::OpenURL` Methode öffnet eine Mediendatei aus einer URL.</span><span class="sxs-lookup"><span data-stu-id="172dc-106">The `CPlayer::OpenURL` method opens a media file from a URL.</span></span>


```C++
//  Open a URL for playback.
HRESULT CPlayer::OpenURL(const WCHAR *sURL)
{
    // 1. Create a new media session.
    // 2. Create the media source.
    // 3. Create the topology.
    // 4. Queue the topology [asynchronous]
    // 5. Start playback [asynchronous - does not happen in this method.]

    IMFTopology *pTopology = NULL;
    IMFPresentationDescriptor* pSourcePD = NULL;

    // Create the media session.
    HRESULT hr = CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the media source.
    hr = CreateMediaSource(sURL, &m_pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the presentation descriptor for the media source.
    hr = m_pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pSourcePD, m_hwndVideo, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

    // If SetTopology succeeds, the media session will queue an 
    // MESessionTopologySet event.

done:
    if (FAILED(hr))
    {
        m_state = Closed;
    }

    SafeRelease(&pSourcePD);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="172dc-107">Diese Methode führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="172dc-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="172dc-108">Ruft **cplayer:: kreatesession** auf, um eine neue Instanz der Medien Sitzung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="172dc-108">Calls **CPlayer::CreateSession** to create a new instance of the Media Session.</span></span> <span data-ttu-id="172dc-109">Weitere Informationen finden Sie [unterschritt 4: Erstellen der Medien Sitzung](step-4--create-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="172dc-109">See [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span>
2.  <span data-ttu-id="172dc-110">Erstellt eine Medienquelle aus der URL.</span><span class="sxs-lookup"><span data-stu-id="172dc-110">Creates a media source from the URL.</span></span> <span data-ttu-id="172dc-111">Den gesamten Code für diesen Schritt finden Sie im Thema [using the Source Resolver](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="172dc-111">The complete code for this step is shown in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>
3.  <span data-ttu-id="172dc-112">Ruft [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) auf, um den Präsentations Deskriptor der Medienquelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="172dc-112">Calls [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span> <span data-ttu-id="172dc-113">Der Präsentations Deskriptor beschreibt die einzelnen Streams in der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="172dc-113">The presentation descriptor describes each streams in the source file.</span></span>
4.  <span data-ttu-id="172dc-114">Erstellt die Wiedergabe Topologie.</span><span class="sxs-lookup"><span data-stu-id="172dc-114">Creates the playback topology.</span></span> <span data-ttu-id="172dc-115">Code für diesen Schritt finden Sie im Thema [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="172dc-115">Code for this step is shown in the topic [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="172dc-116">Ruft [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) auf, um die Topologie für die Medien Sitzung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="172dc-116">Calls [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>

<span data-ttu-id="172dc-117">Die [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Methode wird asynchron abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="172dc-117">The [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="172dc-118">Wenn der Vorgang abgeschlossen ist, wird die [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Methode des cplayer-Objekts aufgerufen. Weitere Informationen finden Sie unter [Step 5: handle Media Session Events](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="172dc-118">When it completes, the CPlayer object's [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called; see [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>

<span data-ttu-id="172dc-119">Nächste [Schritte: Schritt 4: Erstellen der Medien Sitzung](step-4--create-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="172dc-119">Next: [Step 4: Create the Media Session](step-4--create-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="172dc-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="172dc-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="172dc-121">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="172dc-121">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="172dc-122">Wiedergeben von Mediendateien mit Media Foundation</span><span class="sxs-lookup"><span data-stu-id="172dc-122">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 




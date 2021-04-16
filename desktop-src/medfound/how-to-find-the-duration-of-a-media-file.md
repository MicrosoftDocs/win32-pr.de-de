---
description: So ermitteln Sie die Dauer einer Mediendatei
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: So finden Sie die Dauer einer Mediendatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8915e52e97a4532b1d174166ec2863e26d18e34a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530503"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a><span data-ttu-id="fecb5-103">So finden Sie die Dauer einer Mediendatei</span><span class="sxs-lookup"><span data-stu-id="fecb5-103">How to Find the Duration of a Media File</span></span>

<span data-ttu-id="fecb5-104">Führen Sie die folgenden Schritte aus, um die Dauer einer Mediendatei zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="fecb5-104">To find the duration of a media file, perform the following steps:</span></span>

1.  <span data-ttu-id="fecb5-105">Verwenden Sie den [quellresolver](source-resolver.md) , um eine Medienquelle zu erstellen, mit der die Mediendatei analysiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fecb5-105">Use the [Source Resolver](source-resolver.md) to create a media source that can parse the media file.</span></span>
2.  <span data-ttu-id="fecb5-106">Aufrufen von [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) für die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="fecb5-106">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source.</span></span> <span data-ttu-id="fecb5-107">Diese Methode gibt einen Präsentations Deskriptor zurück, der den Inhalt der Mediendatei beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fecb5-107">This method returns presentation descriptor that describes the contents of the media file.</span></span>
3.  <span data-ttu-id="fecb5-108">Fragen Sie den Präsentations Deskriptor für das [MF \_ PD \_ Duration](mf-pd-duration-attribute.md) -Attribut ab, indem Sie die [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fecb5-108">Query the presentation descriptor for the [MF\_PD\_DURATION](mf-pd-duration-attribute.md) attribute by calling the [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) method.</span></span> <span data-ttu-id="fecb5-109">Der Wert des-Attributs, falls vorhanden, ist die Datei Dauer in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="fecb5-109">The value of the attribute, if present, is the file duration in 100-nanosecond units.</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="fecb5-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fecb5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fecb5-111">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="fecb5-111">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 




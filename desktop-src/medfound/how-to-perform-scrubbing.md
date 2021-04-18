---
description: Vorgehensweise beim Ausführen von Scrubbing
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Vorgehensweise beim Ausführen von Scrubbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527686"
---
# <a name="how-to-perform-scrubbing"></a><span data-ttu-id="8424c-103">Vorgehensweise beim Ausführen von Scrubbing</span><span class="sxs-lookup"><span data-stu-id="8424c-103">How to Perform Scrubbing</span></span>

<span data-ttu-id="8424c-104">Das Scrubbing wird ausgeführt, um sofort bestimmte Punkte in einer Datei zu suchen, indem Sie mit einer visuellen Darstellung der Zeit interagieren, z. b. einer Scrollleiste.</span><span class="sxs-lookup"><span data-stu-id="8424c-104">Scrubbing is performed to instantaneously seek to specific points within a file by interacting with a visual representation of time, such as a scrollbar.</span></span> <span data-ttu-id="8424c-105">In Media Foundation bedeutet Bereinigungs, eine Datei zu suchen und einen aktualisierten Frame zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8424c-105">In Media Foundation, scrubbing means seeking on a file and getting one updated frame.</span></span>

<span data-ttu-id="8424c-106">Informationen zum Bereinigen finden Sie unter Informationen [zur Raten Kontrolle](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="8424c-106">For information about scrubbing, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-perform-scrubbing"></a><span data-ttu-id="8424c-107">So führen Sie Bereinigungs aus</span><span class="sxs-lookup"><span data-stu-id="8424c-107">To perform scrubbing</span></span>

1.  <span data-ttu-id="8424c-108">Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) zum Abrufen der [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstelle aus der [Medien Sitzung](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="8424c-108">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the [Media Session](media-session.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="8424c-109">Die [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstelle kann nicht aus der Medienquelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8424c-109">Do not get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the media source.</span></span> <span data-ttu-id="8424c-110">Die Schnittstelle immer aus der Medien Sitzung erhalten.</span><span class="sxs-lookup"><span data-stu-id="8424c-110">Always get the interface from the Media Session.</span></span>

     

2.  <span data-ttu-id="8424c-111">Greifen Sie [**imfratecontrol:: setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) an, um die Wiedergabe Rate auf NULL festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8424c-111">Call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) to set the playback rate to zero.</span></span> <span data-ttu-id="8424c-112">Weitere Informationen zum Aufrufen dieser Methode finden Sie unter [Festlegen der Wiedergabe Rate für die Medien Sitzung](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="8424c-112">For more information about calling this method, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>
3.  <span data-ttu-id="8424c-113">Erstellen Sie eine Suchposition in einer **PROPVARIANT** , indem Sie die Darstellungs Zeit in einem **mftime** -Typ angeben.</span><span class="sxs-lookup"><span data-stu-id="8424c-113">Create a seek position in a **PROPVARIANT** by specifying the presentation time to seek to in a **MFTIME** type.</span></span>
4.  <span data-ttu-id="8424c-114">Geben Sie [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) mit der Suchposition an, um die Wiedergabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="8424c-114">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the seek position to start playback.</span></span>
5.  <span data-ttu-id="8424c-115">Wenn der Bereinigungsvorgang beendet ist, sendet die Medien Sitzung ein [mesessionscrubsamplecomplete](mesessionscrubsamplecomplete.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8424c-115">When the scrub operation is complete, the Media Session sends an [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event.</span></span> <span data-ttu-id="8424c-116">Warten Sie auf dieses Ereignis, bevor Sie erneut [**starten**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) , um einen weiteren Bereinigungs Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8424c-116">Wait for this event before calling [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) again for another scrubbing operation.</span></span>

## <a name="example"></a><span data-ttu-id="8424c-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8424c-117">Example</span></span>

<span data-ttu-id="8424c-118">Im folgenden Codebeispiel wird gezeigt, wie ein Scrubbing durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8424c-118">The following code example shows how to perform scrubbing.</span></span>


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



<span data-ttu-id="8424c-119">Bei einem erfolgreichen Bereinigungs Vorgang wird das Ereignis [mesessionscrubsamplecomplete](mesessionscrubsamplecomplete.md) generiert, nachdem alle streamsenken mit dem neuen Frame aktualisiert wurden und der Bereinigungs Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8424c-119">A successful scrubbing operation generates the [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event after all the stream sinks are updated with the new frame and the scrubbing operation completes successfully.</span></span> <span data-ttu-id="8424c-120">Beim Bereinigen einer Videodatei wird der Frame angezeigt, zu dem das Seeding erfolgt ist, aber es wird keine Audioausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="8424c-120">Scrubbing a video file displays the frame that was seeked to, but does not generate an audio output.</span></span>

<span data-ttu-id="8424c-121">Die Anwendung kann Frame-Stepping durchführen, indem die Wiedergabe Rate auf NULL festgelegt wird und dann eine **PROPVARIANT** , die auf **VT \_ empty** festgelegt ist, im [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)-Befehl übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8424c-121">The application can perform frame stepping by setting the playback rate to zero and then passing a **PROPVARIANT** that is set to **VT\_EMPTY** in the call to [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8424c-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8424c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8424c-123">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="8424c-123">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="8424c-124">Raten Steuerung</span><span class="sxs-lookup"><span data-stu-id="8424c-124">Rate Control</span></span>](rate-control.md)
</dt> </dl>

 

 




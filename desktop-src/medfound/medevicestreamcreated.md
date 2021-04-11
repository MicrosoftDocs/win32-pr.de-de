---
description: Medevicestreamcreated ist ein erweiterter Medien Ereignistyp, der vom Geräte-MFT mit einem meunknown-Medienereignis generiert wurde.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Mede vicestreamcreated-Ereignis (MF Transform. h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 632ebc305473cd596656a21f562be25d53c2bace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214888"
---
# <a name="medevicestreamcreated-event"></a><span data-ttu-id="3018b-103">Mede vicestreamcreated-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3018b-103">MEDeviceStreamCreated event</span></span>

<span data-ttu-id="3018b-104">Medevicestreamcreated ist ein erweiterter Medien Ereignistyp, der vom Geräte-MFT mit einem meunknown-Medienereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3018b-104">MEDeviceStreamCreated is an extended media event type generated with an MEUnknown media event by the Device MFT.</span></span>

<span data-ttu-id="3018b-105">Dieser erweiterte Medien Ereignistyp hat keine Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="3018b-105">This extended media event type has no payload.</span></span>  <span data-ttu-id="3018b-106">Ein entsprechendes HRESULT sollte über die [**imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) -Methode bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3018b-106">Appropriate HRESULT should be provided via the [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) method.</span></span>




## <a name="remarks"></a><span data-ttu-id="3018b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3018b-107">Remarks</span></span>

<span data-ttu-id="3018b-108">Dieses erweiterte Medienereignis muss von der MFT des Geräts als Teil der Medientyp Auswahl im Ausgabestream der DMFT gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="3018b-108">This extended media event must be sent by the Device MFT as a part of the media type selection on the output stream of the DMFT.</span></span>  <span data-ttu-id="3018b-109">Wenn setoutputstreamstate auf der imfdevicetransform-Schnittstelle aufgerufen wird, ist die DMFT für das signalisieren der Änderung in den erforderlichen eingabestreamzuständen mit dem [metransforminputstreamstatechanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) -Medienereignis verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="3018b-109">When the SetOutputStreamState is invoked on the IMFDeviceTransform interface, the DMFT is responsible for signaling the change in the required input stream states with the [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) media event.</span></span> <span data-ttu-id="3018b-110">Wenn die eingabestreamstatusänderung von der Pipeline mit dem Aufrufs von "endputstreamstate" der DMFT bestätigt wurde, ist die DMFT dafür zuständig, die interne Zustands Konfiguration abzuschließen und den Ereignis Typ " **medevicestreamcreated** Extended Media" zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="3018b-110">When the input stream state change has been acknowledged by the pipeline with the call into SetInputStreamState of the DMFT, the DMFT is responsible for completing its internal state configuration and raising the **MEDeviceStreamCreated** extended media event type.</span></span>

<span data-ttu-id="3018b-111">Wenn dieser erweiterte Medien Ereignistyp nicht ausgelöst wird, stellt der geräteregistrierungs-Manager keine Eingabe Frames für die DMFT bereit.</span><span class="sxs-lookup"><span data-stu-id="3018b-111">If this extended media event type is not raised, the Device Transform Manager will not deliver any input frames to the DMFT.</span></span>
<span data-ttu-id="3018b-112">Der Extended Media-Ereignistyp muss auch als Attribut von IMF Media Event festgelegt werden, der Ausgabestream-ID unter Verwendung des **MF_EVENT_MFT_INPUT_STREAM_ID** -Attributs.</span><span class="sxs-lookup"><span data-stu-id="3018b-112">The extended media event type must also set as an attribute of the IMFMediaEvent, the output stream ID using the **MF_EVENT_MFT_INPUT_STREAM_ID** attribute.</span></span>

```cpp
IMFMediaEvent* pMediaEvent = nullptr;

hr = MFCreateMediaEvent (MEUnknown,
                         MEDeviceStreamCreated,
                         S_OK,
                         nullptr,
                         &pMediaEvent);
if (SUCCEEDED(hr))
{
    hr = pMediaEvent->SetUINT32(MF_EVENT_MFT_INPUT_STREAM_ID, GetOutputStreamId());
}

if (SUCCEEDED(hr))
{
    hr = m_pEventQueue->QueueEvent(pMediaEvent);
}

if (nullptr != pMediaEvent)
{
    pMediaEvent->Release();
    pMediaEvent = nullptr;
}

return hr;
```

## <a name="requirements"></a><span data-ttu-id="3018b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3018b-113">Requirements</span></span>



| <span data-ttu-id="3018b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3018b-114">Requirement</span></span> | <span data-ttu-id="3018b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3018b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3018b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3018b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3018b-117">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3018b-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3018b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3018b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3018b-119">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3018b-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3018b-120">Header</span><span class="sxs-lookup"><span data-stu-id="3018b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3018b-121"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3018b-121"><dt>mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3018b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3018b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3018b-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3018b-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="3018b-124">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="3018b-124">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 

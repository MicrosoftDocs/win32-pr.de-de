---
description: Wird von einem asynchronen Media Foundation Transform (MFT) gesendet, um ein neues Eingabe Beispiel anzufordern.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Metransformneedinput-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbdea648e4dc7d90b1321958eebb6c544ebb88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129805"
---
# <a name="metransformneedinput-event"></a><span data-ttu-id="3d7f3-103">Metransformneedinput-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3d7f3-103">METransformNeedInput event</span></span>

<span data-ttu-id="3d7f3-104">Wird von einem asynchronen Media Foundation Transform (MFT) gesendet, um ein neues Eingabe Beispiel anzufordern.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-104">Sent by an asynchronous Media Foundation transform (MFT) to request a new input sample.</span></span>

## <a name="event-values"></a><span data-ttu-id="3d7f3-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="3d7f3-105">Event values</span></span>

<span data-ttu-id="3d7f3-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3d7f3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3d7f3-107">VARTYPE</span></span>              | <span data-ttu-id="3d7f3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d7f3-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="3d7f3-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="3d7f3-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="3d7f3-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="3d7f3-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="3d7f3-111">Attributes</span></span>

<span data-ttu-id="3d7f3-112">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="3d7f3-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="3d7f3-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="3d7f3-113">Attribute</span></span>                                                                        | <span data-ttu-id="3d7f3-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d7f3-114">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d7f3-115">\_ \_ MFT- \_ Eingabedaten \_ Strom- \_ ID des MF-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="3d7f3-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="3d7f3-116">Der Bezeichner des Streams, der Eingabedaten benötigt.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-116">The identifier of the stream that needs input data.</span></span><br/><span data-ttu-id="3d7f3-117">*Benötigten*</span><span class="sxs-lookup"><span data-stu-id="3d7f3-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3d7f3-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d7f3-118">Remarks</span></span>

<span data-ttu-id="3d7f3-119">Asynchrone MFTs Senden dieses Ereignis über die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="3d7f3-120">Dieses Ereignis wird von synchronen MFTs niemals gesendet.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="3d7f3-121">Wenn der Client der MFT dieses Ereignis empfängt, sollte er [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) aufrufen, um das nächste Beispiel bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-121">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) to deliver the next sample.</span></span> <span data-ttu-id="3d7f3-122">Das [MF- \_ Ereignis \_ MFT-Eingabedaten Strom- \_ \_ \_ ID](mf-event-mft-input-stream-id.md) -Attribut des Ereignis Objekts gibt an, welcher Eingabedaten Strom Daten erfordert.</span><span class="sxs-lookup"><span data-stu-id="3d7f3-122">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event object specifies which input stream requires data.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d7f3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d7f3-123">Requirements</span></span>



| <span data-ttu-id="3d7f3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d7f3-124">Requirement</span></span> | <span data-ttu-id="3d7f3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3d7f3-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7f3-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d7f3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3d7f3-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d7f3-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="3d7f3-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d7f3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3d7f3-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d7f3-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="3d7f3-130">Header</span><span class="sxs-lookup"><span data-stu-id="3d7f3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d7f3-131"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d7f3-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d7f3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d7f3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d7f3-133">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d7f3-133">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="3d7f3-134">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="3d7f3-134">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 





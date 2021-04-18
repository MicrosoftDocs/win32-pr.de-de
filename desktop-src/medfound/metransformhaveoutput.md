---
description: Wird von einem asynchronen Media Foundation Transform (MFT) gesendet, wenn neue Ausgabedaten aus dem MFT verfügbar sind.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Metransformhaveoutput-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345148"
---
# <a name="metransformhaveoutput-event"></a><span data-ttu-id="3d4e1-103">Metransformhaveoutput-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3d4e1-103">METransformHaveOutput event</span></span>

<span data-ttu-id="3d4e1-104">Wird von einem asynchronen Media Foundation Transform (MFT) gesendet, wenn neue Ausgabedaten aus dem MFT verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-104">Sent by an asynchronous Media Foundation transform (MFT) when new output data is available from the MFT.</span></span>

## <a name="event-values"></a><span data-ttu-id="3d4e1-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="3d4e1-105">Event values</span></span>

<span data-ttu-id="3d4e1-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3d4e1-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3d4e1-107">VARTYPE</span></span>              | <span data-ttu-id="3d4e1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d4e1-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="3d4e1-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="3d4e1-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="3d4e1-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="3d4e1-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="3d4e1-111">Attributes</span></span>

<span data-ttu-id="3d4e1-112">Für dieses Ereignis sind keine Attribute definiert.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-112">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d4e1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d4e1-113">Remarks</span></span>

<span data-ttu-id="3d4e1-114">Asynchrone MFTs Senden dieses Ereignis über die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-114">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="3d4e1-115">Dieses Ereignis wird von synchronen MFTs niemals gesendet.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-115">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="3d4e1-116">Wenn der Client der MFT dieses Ereignis empfängt, sollte er [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) zum Abrufen der Ausgabe abrufen.</span><span class="sxs-lookup"><span data-stu-id="3d4e1-116">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get the output.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d4e1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d4e1-117">Requirements</span></span>



| <span data-ttu-id="3d4e1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d4e1-118">Requirement</span></span> | <span data-ttu-id="3d4e1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3d4e1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d4e1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d4e1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3d4e1-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d4e1-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="3d4e1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d4e1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3d4e1-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d4e1-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="3d4e1-124">Header</span><span class="sxs-lookup"><span data-stu-id="3d4e1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d4e1-125"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d4e1-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d4e1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d4e1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4e1-127">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d4e1-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="3d4e1-128">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="3d4e1-128">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 





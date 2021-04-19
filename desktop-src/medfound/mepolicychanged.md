---
description: Wird von einer Pipeline Komponente ausgelöst, wenn die Ausgabe Richtlinie für den Stream geändert wird. Dieses Ereignis gilt nur für geschützte Inhalte.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Mepolicychanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6827c44958e2df016365a8caa9a66f1aad9a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350556"
---
# <a name="mepolicychanged-event"></a><span data-ttu-id="5d0bd-104">Mepolicychanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5d0bd-104">MEPolicyChanged event</span></span>

<span data-ttu-id="5d0bd-105">Wird von einer Pipeline Komponente ausgelöst, wenn die Ausgabe Richtlinie für den Stream geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5d0bd-105">Raised by a pipeline component when the output policy for the stream changes.</span></span> <span data-ttu-id="5d0bd-106">Dieses Ereignis gilt nur für geschützte Inhalte.</span><span class="sxs-lookup"><span data-stu-id="5d0bd-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="5d0bd-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="5d0bd-107">Event values</span></span>

<span data-ttu-id="5d0bd-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="5d0bd-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5d0bd-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5d0bd-109">VARTYPE</span></span>                | <span data-ttu-id="5d0bd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d0bd-110">Description</span></span>                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d0bd-111">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="5d0bd-111">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="5d0bd-112">Ein Zeiger auf die [**imfoutputpolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) -Schnittstelle der neuen Richtlinie für den Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="5d0bd-112">Pointer to the [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) interface of the new policy for the stream.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5d0bd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d0bd-113">Remarks</span></span>

<span data-ttu-id="5d0bd-114">Alle vertrauenswürdigen Ausgaben müssen dieses Ereignis behandeln.</span><span class="sxs-lookup"><span data-stu-id="5d0bd-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="5d0bd-115">Media Foundation Transformationen (MFTs) empfangen dieses Ereignis über die [**IMF Transform::P rocesabvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5d0bd-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="5d0bd-116">Medien senken empfangen dieses Ereignis über die [**IMF streamsink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5d0bd-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="5d0bd-117">Die vertrauenswürdige Ausgabe muss die neue Richtlinie anwenden oder die Fehlercode-MF- \_ E- \_ Richtlinie \_ nicht unterstützt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5d0bd-117">The trusted output must apply the new policy or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d0bd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d0bd-118">Requirements</span></span>



| <span data-ttu-id="5d0bd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d0bd-119">Requirement</span></span> | <span data-ttu-id="5d0bd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5d0bd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d0bd-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d0bd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5d0bd-122">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5d0bd-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="5d0bd-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d0bd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5d0bd-124">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5d0bd-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="5d0bd-125">Header</span><span class="sxs-lookup"><span data-stu-id="5d0bd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d0bd-126"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d0bd-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d0bd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d0bd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d0bd-128">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5d0bd-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





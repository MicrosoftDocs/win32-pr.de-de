---
description: Wird von einer Pipeline Komponente ausgelöst, wenn sich die Konfiguration für eines der Ausgabe Schutz Schemas ändert. Dieses Ereignis gilt nur für geschützte Inhalte.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Mecontentschutzmessage-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f96ac75711559881232ced4cec6bfca2bc030c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753184"
---
# <a name="mecontentprotectionmessage-event"></a><span data-ttu-id="3a500-104">Mecontentschutzmessage-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3a500-104">MEContentProtectionMessage event</span></span>

<span data-ttu-id="3a500-105">Wird von einer Pipeline Komponente ausgelöst, wenn sich die Konfiguration für eines der Ausgabe Schutz Schemas ändert.</span><span class="sxs-lookup"><span data-stu-id="3a500-105">Raised by a pipeline component when the configuration changes for one of the output protection schemes.</span></span> <span data-ttu-id="3a500-106">Dieses Ereignis gilt nur für geschützte Inhalte.</span><span class="sxs-lookup"><span data-stu-id="3a500-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="3a500-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="3a500-107">Event values</span></span>

<span data-ttu-id="3a500-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="3a500-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3a500-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3a500-109">VARTYPE</span></span>              | <span data-ttu-id="3a500-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a500-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="3a500-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="3a500-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="3a500-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="3a500-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3a500-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a500-113">Remarks</span></span>

<span data-ttu-id="3a500-114">Alle vertrauenswürdigen Ausgaben müssen dieses Ereignis behandeln.</span><span class="sxs-lookup"><span data-stu-id="3a500-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="3a500-115">Media Foundation Transformationen (MFTs) empfangen dieses Ereignis über die [**IMF Transform::P rocesabvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3a500-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="3a500-116">Medien senken empfangen dieses Ereignis über die [**IMF streamsink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3a500-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="3a500-117">Die vertrauenswürdige Ausgabe muss die Richtlinien Änderungen anwenden oder die Fehlercode-MF- \_ E- \_ Richtlinie \_ nicht unterstützt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3a500-117">The trusted output must apply the policy changes or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

<span data-ttu-id="3a500-118">Die Ereignisdaten und Attribute sind vom verwendeten Inhalts Schutzsystem abhängig.</span><span class="sxs-lookup"><span data-stu-id="3a500-118">The event data and attributes depend on the content protection system in use.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a500-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a500-119">Requirements</span></span>



| <span data-ttu-id="3a500-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a500-120">Requirement</span></span> | <span data-ttu-id="3a500-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3a500-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a500-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a500-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3a500-123">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="3a500-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="3a500-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a500-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3a500-125">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="3a500-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="3a500-126">Header</span><span class="sxs-lookup"><span data-stu-id="3a500-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a500-127"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a500-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a500-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a500-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a500-129">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a500-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 





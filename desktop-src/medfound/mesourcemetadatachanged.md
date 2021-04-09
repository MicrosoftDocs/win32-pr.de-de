---
description: Wird von einer Medienquelle ausgelöst, wenn die Metadaten aktualisiert werden.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: MESourceMetadataChanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959052"
---
# <a name="mesourcemetadatachanged-event"></a><span data-ttu-id="1e264-103">MESourceMetadataChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="1e264-103">MESourceMetadataChanged event</span></span>

<span data-ttu-id="1e264-104">Wird von einer Medienquelle ausgelöst, wenn die Metadaten aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1e264-104">Raised by a media source when it updates its metadata.</span></span>

## <a name="event-values"></a><span data-ttu-id="1e264-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="1e264-105">Event values</span></span>

<span data-ttu-id="1e264-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="1e264-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1e264-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1e264-107">VARTYPE</span></span>              | <span data-ttu-id="1e264-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e264-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="1e264-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="1e264-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="1e264-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="1e264-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1e264-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e264-111">Remarks</span></span>

<span data-ttu-id="1e264-112">Wenn die Medienquelle nicht alle Metadaten bereitstellen kann, wenn die Quelle erstmalig erstellt wird, sollte dieses Ereignis ausgelöst werden, nachdem die Metadaten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1e264-112">If the media source cannot provide all of the metadata when the source is first created, it should raise this event after the metadata is available.</span></span>

<span data-ttu-id="1e264-113">Von der Medienquelle sollte ein neuer Präsentations Deskriptor erstellt werden, und alle Attribute aus dem Präsentations Deskriptor (PD) werden in das Ereignis Objekt kopiert.</span><span class="sxs-lookup"><span data-stu-id="1e264-113">The media source should create a new presentation descriptor and copy all of the attributes from the presentation descriptor (PD) to the event object.</span></span> <span data-ttu-id="1e264-114">Die Anwendung kann das Ereignis Objekt zum Auflisten der neuen PD-Attribute verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e264-114">The application can use the event object to enumerate the new PD attributes.</span></span> <span data-ttu-id="1e264-115">Insbesondere sind die Werte für die Dateigröße von [MF \_ PD \_ ](mf-pd-duration-attribute.md) und die [ \_ \_ gesamte \_ Datei \_ Größe von MF PD](mf-pd-total-file-size-attribute.md) möglicherweise unbekannt, bis die Datei vollständig heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="1e264-115">In particular, the values for [MF\_PD\_DURATION](mf-pd-duration-attribute.md) and [MF\_PD\_TOTAL\_FILE\_SIZE](mf-pd-total-file-size-attribute.md) might be unknown until the file is completely downloaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e264-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e264-116">Requirements</span></span>



| <span data-ttu-id="1e264-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e264-117">Requirement</span></span> | <span data-ttu-id="1e264-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1e264-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e264-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e264-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1e264-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e264-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1e264-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e264-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1e264-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e264-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1e264-123">Header</span><span class="sxs-lookup"><span data-stu-id="1e264-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e264-124"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e264-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e264-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e264-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e264-126">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e264-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="1e264-127">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="1e264-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





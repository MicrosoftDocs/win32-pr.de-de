---
description: Präsentationszeit für ein Beispiel, das beim Scrubbing gerendert wurde.
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: MF_EVENT_SCRUBSAMPLE_TIME-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7c4fb1a8015367fa3d48edb066cdb135983926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959292"
---
# <a name="mf_event_scrubsample_time-attribute"></a><span data-ttu-id="e8200-103">\_ \_ Scrubsample- \_ Zeit Attribut für MF-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e8200-103">MF\_EVENT\_SCRUBSAMPLE\_TIME attribute</span></span>

<span data-ttu-id="e8200-104">Präsentationszeit für ein Beispiel, das beim Scrubbing gerendert wurde.</span><span class="sxs-lookup"><span data-stu-id="e8200-104">Presentation time for a sample that was rendered while scrubbing.</span></span>

## <a name="data-type"></a><span data-ttu-id="e8200-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e8200-105">Data type</span></span>

<span data-ttu-id="e8200-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="e8200-106">**UINT64**</span></span>

<span data-ttu-id="e8200-107">Als **Longlong** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="e8200-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8200-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8200-108">Remarks</span></span>

<span data-ttu-id="e8200-109">Dieses Attribut wird mit dem [mestreamsinkscrubsamplecomplete](mestreamsinkscrubsamplecomplete.md) -Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8200-109">This attribute is used with the [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) event.</span></span>

<span data-ttu-id="e8200-110">Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e8200-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="e8200-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="e8200-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8200-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8200-112">Requirements</span></span>



| <span data-ttu-id="e8200-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8200-113">Requirement</span></span> | <span data-ttu-id="e8200-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e8200-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8200-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8200-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e8200-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8200-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e8200-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8200-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e8200-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8200-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e8200-119">Header</span><span class="sxs-lookup"><span data-stu-id="e8200-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8200-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8200-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8200-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8200-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8200-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e8200-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e8200-123">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="e8200-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="e8200-124">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="e8200-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="e8200-125">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="e8200-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 





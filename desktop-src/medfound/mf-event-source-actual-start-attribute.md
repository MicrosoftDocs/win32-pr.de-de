---
description: Enthält die Startzeit, bei der eine Medienquelle von Ihrer aktuellen Position neu gestartet wird.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: MF_EVENT_SOURCE_ACTUAL_START-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393557"
---
# <a name="mf_event_source_actual_start-attribute"></a><span data-ttu-id="1ae6e-103">Das \_ \_ \_ tatsächliche \_ Start Attribut der MF-Ereignis Quelle</span><span class="sxs-lookup"><span data-stu-id="1ae6e-103">MF\_EVENT\_SOURCE\_ACTUAL\_START attribute</span></span>

<span data-ttu-id="1ae6e-104">Enthält die Startzeit, bei der eine Medienquelle von Ihrer aktuellen Position neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-104">Contains the start time at which a media source restarts from its current position.</span></span>

## <a name="data-type"></a><span data-ttu-id="1ae6e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1ae6e-105">Data type</span></span>

<span data-ttu-id="1ae6e-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1ae6e-106">**UINT64**</span></span>

<span data-ttu-id="1ae6e-107">Als **Longlong** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ae6e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ae6e-108">Remarks</span></span>

<span data-ttu-id="1ae6e-109">Dieses Attribut wird mit dem [mesourcestarted](mesourcestarted.md) -Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="1ae6e-110">Das-Attribut ist relevant, wenn die Ereignisdaten leer sind (**VT \_ empty**), was darauf hinweist, dass die Medienquelle von der aktuellen Wiedergabe Position gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-110">The attribute is relevant when the event data is empty (**VT\_EMPTY**), which indicates that the media source started from the current playback position.</span></span> <span data-ttu-id="1ae6e-111">In diesem Fall gibt das **\_ \_ \_ tatsächliche \_ Start Attribut der MF-Ereignis Quelle** die tatsächliche Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-111">In that case, the **MF\_EVENT\_SOURCE\_ACTUAL\_START** attribute specifies the actual starting time.</span></span> <span data-ttu-id="1ae6e-112">Wenn die Ereignisdaten **VT \_ empty** sind und dieses Attribut nicht festgelegt ist, wird für die Startzeit der Wert 0 (null) angenommen.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-112">If the event data is **VT\_EMPTY** and this attribute is not set, the starting time is assumed to be zero.</span></span>

<span data-ttu-id="1ae6e-113">Wenn die [mesourcestarted](mesourcestarted.md) -Ereignisdaten die Startzeit (**VT \_ I8**) enthalten, sollte dieses Attribut nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-113">When the [MESourceStarted](mesourcestarted.md) event data contains the start time (**VT\_I8**), this attribute should not be set.</span></span>

<span data-ttu-id="1ae6e-114">Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-114">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="1ae6e-115">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="1ae6e-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae6e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ae6e-116">Requirements</span></span>



| <span data-ttu-id="1ae6e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ae6e-117">Requirement</span></span> | <span data-ttu-id="1ae6e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1ae6e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae6e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ae6e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1ae6e-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ae6e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1ae6e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ae6e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1ae6e-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ae6e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1ae6e-123">Header</span><span class="sxs-lookup"><span data-stu-id="1ae6e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ae6e-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ae6e-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ae6e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ae6e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae6e-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="1ae6e-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ae6e-127">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="1ae6e-127">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ae6e-128">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="1ae6e-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="1ae6e-129">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="1ae6e-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 





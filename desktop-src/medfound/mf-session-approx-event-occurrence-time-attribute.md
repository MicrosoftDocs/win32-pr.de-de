---
description: Der ungefähre Zeitpunkt, zu dem die Medien Sitzung ein Ereignis ausgelöst hat.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a31b1970c2c9d86384c12c50777a8cee55e3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364077"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a><span data-ttu-id="d9923-103">MF- \_ Sitzung \_ ca. \_ Ereignis \_ vorkommen \_ Zeit Attribut</span><span class="sxs-lookup"><span data-stu-id="d9923-103">MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME attribute</span></span>

<span data-ttu-id="d9923-104">Der ungefähre Zeitpunkt, zu dem die Medien Sitzung ein Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="d9923-104">The approximate time when the Media Session raised an event.</span></span>

## <a name="data-type"></a><span data-ttu-id="d9923-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d9923-105">Data type</span></span>

<span data-ttu-id="d9923-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="d9923-106">**UINT64**</span></span>

<span data-ttu-id="d9923-107">Als **Longlong** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="d9923-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9923-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9923-108">Remarks</span></span>

<span data-ttu-id="d9923-109">Einige Ereignisse aus der Medien Sitzung verfügen über dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="d9923-109">Some events from the Media Session have this attribute.</span></span> <span data-ttu-id="d9923-110">Der-Wert gibt die ungefähre Präsentationszeit an, zu der das-Ereignis ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="d9923-110">The value gives the approximate presentation time when the event was raised.</span></span>

<span data-ttu-id="d9923-111">Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="d9923-111">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="d9923-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="d9923-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9923-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9923-113">Requirements</span></span>



| <span data-ttu-id="d9923-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9923-114">Requirement</span></span> | <span data-ttu-id="d9923-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d9923-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9923-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9923-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d9923-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9923-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d9923-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9923-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d9923-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9923-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d9923-120">Header</span><span class="sxs-lookup"><span data-stu-id="d9923-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9923-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9923-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9923-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9923-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9923-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="d9923-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d9923-124">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="d9923-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="d9923-125">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="d9923-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="d9923-126">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="d9923-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 





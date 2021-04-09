---
description: Offset zwischen der Präsentationszeit und den Medienquellen-Zeitstempeln.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: MF_EVENT_PRESENTATION_TIME_OFFSET-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862959"
---
# <a name="mf_event_presentation_time_offset-attribute"></a><span data-ttu-id="7e139-103">\_ \_ \_ Zeit \_ Offset Attribut der MF-Ereignis Präsentation</span><span class="sxs-lookup"><span data-stu-id="7e139-103">MF\_EVENT\_PRESENTATION\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="7e139-104">Offset zwischen der Präsentationszeit und den Zeitstempeln der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="7e139-104">Offset between the presentation time and the media source's time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e139-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7e139-105">Data type</span></span>

<span data-ttu-id="7e139-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="7e139-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="7e139-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e139-107">Remarks</span></span>

<span data-ttu-id="7e139-108">Der Offset wird wie folgt berechnet: Offset = Präsentationszeit-Quell Zeit.</span><span class="sxs-lookup"><span data-stu-id="7e139-108">The offset is calculated as follows: offset = presentation time − source time.</span></span> <span data-ttu-id="7e139-109">Dieses Attribut wird mit den folgenden Ereignissen verwendet:</span><span class="sxs-lookup"><span data-stu-id="7e139-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="7e139-110">Mesessionnotifypresentationtime</span><span class="sxs-lookup"><span data-stu-id="7e139-110">MESessionNotifyPresentationTime</span></span>](mesessionnotifypresentationtime.md)
-   [<span data-ttu-id="7e139-111">Mesessionstarted</span><span class="sxs-lookup"><span data-stu-id="7e139-111">MESessionStarted</span></span>](mesessionstarted.md)

<span data-ttu-id="7e139-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="7e139-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e139-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e139-113">Requirements</span></span>



| <span data-ttu-id="7e139-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e139-114">Requirement</span></span> | <span data-ttu-id="7e139-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7e139-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e139-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e139-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7e139-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e139-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7e139-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e139-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7e139-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e139-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7e139-120">Header</span><span class="sxs-lookup"><span data-stu-id="7e139-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e139-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e139-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e139-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e139-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e139-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7e139-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7e139-124">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="7e139-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="7e139-125">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="7e139-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="7e139-126">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="7e139-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 





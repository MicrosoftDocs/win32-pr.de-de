---
description: Die Startzeit für die Präsentation in 100-Nanosecond-Einheiten, gemessen an der Präsentations Uhr.
ms.assetid: d19d851c-ab4a-4a9d-bcc4-8dd4e993fa2c
title: MF_EVENT_START_PRESENTATION_TIME-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65bf6142ce12a7bf921fd26373ea5d10ab384560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050611"
---
# <a name="mf_event_start_presentation_time-attribute"></a><span data-ttu-id="f3c50-103">Zeit Attribut der MF- \_ Ereignis \_ Start \_ Präsentation \_</span><span class="sxs-lookup"><span data-stu-id="f3c50-103">MF\_EVENT\_START\_PRESENTATION\_TIME attribute</span></span>

<span data-ttu-id="f3c50-104">Die Startzeit für die Präsentation in 100-Nanosecond-Einheiten, gemessen an der Präsentations Uhr.</span><span class="sxs-lookup"><span data-stu-id="f3c50-104">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>

## <a name="data-type"></a><span data-ttu-id="f3c50-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f3c50-105">Data type</span></span>

<span data-ttu-id="f3c50-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f3c50-106">**UINT64**</span></span>

<span data-ttu-id="f3c50-107">Als **Longlong** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="f3c50-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3c50-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3c50-108">Remarks</span></span>

<span data-ttu-id="f3c50-109">Dieses Attribut wird mit dem [mesessionnotifypresentationtime](mesessionnotifypresentationtime.md) -Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3c50-109">This attribute is used with the [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) event.</span></span>

<span data-ttu-id="f3c50-110">Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="f3c50-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="f3c50-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="f3c50-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3c50-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3c50-112">Requirements</span></span>



| <span data-ttu-id="f3c50-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3c50-113">Requirement</span></span> | <span data-ttu-id="f3c50-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f3c50-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c50-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3c50-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c50-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3c50-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f3c50-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3c50-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c50-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3c50-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f3c50-119">Header</span><span class="sxs-lookup"><span data-stu-id="f3c50-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3c50-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3c50-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3c50-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3c50-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c50-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="f3c50-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3c50-123">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="f3c50-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3c50-124">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="f3c50-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="f3c50-125">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="f3c50-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 





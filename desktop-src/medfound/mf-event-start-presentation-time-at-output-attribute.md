---
description: Die Präsentationszeit, zu der die Medien senken das erste Beispiel der neuen Topologie Rendering.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a588bc6604deed6c6865cd8283390d28e3ffd49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866188"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a><span data-ttu-id="48034-103">\_ \_ \_ Zeitpunkt der Präsentation des MF-Ereignisses \_ \_ beim \_ Ausgabe Attribut</span><span class="sxs-lookup"><span data-stu-id="48034-103">MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT attribute</span></span>

<span data-ttu-id="48034-104">Die Präsentationszeit, zu der die Medien senken das erste Beispiel der neuen Topologie Rendering.</span><span class="sxs-lookup"><span data-stu-id="48034-104">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="48034-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="48034-105">Data type</span></span>

<span data-ttu-id="48034-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="48034-106">**UINT64**</span></span>

<span data-ttu-id="48034-107">Als **Longlong** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="48034-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48034-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48034-108">Remarks</span></span>

<span data-ttu-id="48034-109">Wenn alle Pipeline Objekte in der vorherigen Topologie Daten gepuffert haben, ist dieser Wert etwas niedriger als der Wert im [**\_ \_ \_ Zeit \_ Offset Attribut der MF-Ereignis Präsentation**](mf-event-presentation-time-offset-attribute.md) , da die senken die gepufferten Daten renderten müssen.</span><span class="sxs-lookup"><span data-stu-id="48034-109">If any pipeline objects in the previous topology buffered data, this value will be slightly less than the value in the [**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**](mf-event-presentation-time-offset-attribute.md) attribute, because the sinks must render the buffered data.</span></span>

<span data-ttu-id="48034-110">Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="48034-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="48034-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="48034-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="48034-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48034-112">Requirements</span></span>



| <span data-ttu-id="48034-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48034-113">Requirement</span></span> | <span data-ttu-id="48034-114">Wert</span><span class="sxs-lookup"><span data-stu-id="48034-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="48034-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48034-115">Minimum supported client</span></span><br/> | <span data-ttu-id="48034-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48034-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="48034-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48034-117">Minimum supported server</span></span><br/> | <span data-ttu-id="48034-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48034-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="48034-119">Header</span><span class="sxs-lookup"><span data-stu-id="48034-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="48034-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="48034-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48034-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48034-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48034-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="48034-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="48034-123">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="48034-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="48034-124">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="48034-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="48034-125">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="48034-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 





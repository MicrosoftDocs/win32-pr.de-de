---
description: Gibt die Startzeit für Präsentationen an, die nach der ersten Präsentation in die Warteschlange eingereiht werden.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355530"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a><span data-ttu-id="3c726-103">\_Start Zeitpunkt der MF-Topologie \_ \_ \_ bei \_ Presentation Switch- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="3c726-103">MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute</span></span>

<span data-ttu-id="3c726-104">Gibt die Startzeit für Präsentationen an, die nach der ersten Präsentation in die Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="3c726-104">Specifies the start time for presentations that are queued after the first presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="3c726-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3c726-105">Data type</span></span>

<span data-ttu-id="3c726-106">**Int64** als **UINT64** gespeichert</span><span class="sxs-lookup"><span data-stu-id="3c726-106">**INT64** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="3c726-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="3c726-107">Get/set</span></span>

<span data-ttu-id="3c726-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="3c726-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="3c726-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="3c726-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3c726-110">Gilt für</span><span class="sxs-lookup"><span data-stu-id="3c726-110">Applies To</span></span>

[<span data-ttu-id="3c726-111">**Imftopology**</span><span class="sxs-lookup"><span data-stu-id="3c726-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="3c726-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c726-112">Remarks</span></span>

<span data-ttu-id="3c726-113">Wenn die Anwendung die erste Präsentation in der Medien Sitzung in die Warteschlange eingereiht, gibt die Anwendung die Startzeit im *pvarstartposition* -Parameter der [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) -Methode an.</span><span class="sxs-lookup"><span data-stu-id="3c726-113">When the application queues the first presentation on the Media Session, the application specifies the start time in the *pvarStartPosition* parameter of the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method.</span></span> <span data-ttu-id="3c726-114">Bei allen nachfolgenden Präsentationen wird die Startzeit jedoch durch die Start Zeit der MF- \_ Topologie für \_ \_ \_ \_ \_ das Präsentations switchattribut in der Topologie angegeben.</span><span class="sxs-lookup"><span data-stu-id="3c726-114">For any subsequent presentations, however, the start time is given by the MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute on the topology.</span></span> <span data-ttu-id="3c726-115">Die Startzeit wird in 100-Nanosecond-Einheiten relativ zum Anfang der Präsentation angegeben.</span><span class="sxs-lookup"><span data-stu-id="3c726-115">The start time is specified in 100-nanosecond units, relative to the beginning of the presentation.</span></span> <span data-ttu-id="3c726-116">Wenn der Wert z. b. 50 Millionen ist, startet die Wiedergabe 5 Sekunden in der Präsentation.</span><span class="sxs-lookup"><span data-stu-id="3c726-116">For example, if the value is 50000000, playback starts 5 seconds into the presentation.</span></span> <span data-ttu-id="3c726-117">Wenn dieses Attribut nicht festgelegt ist, ist die Standard Startzeit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3c726-117">If this attribute is not set, the default start time is zero.</span></span>

<span data-ttu-id="3c726-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="3c726-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c726-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c726-119">Requirements</span></span>



| <span data-ttu-id="3c726-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c726-120">Requirement</span></span> | <span data-ttu-id="3c726-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3c726-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c726-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c726-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3c726-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c726-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3c726-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c726-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3c726-125">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c726-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3c726-126">Header</span><span class="sxs-lookup"><span data-stu-id="3c726-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c726-127"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c726-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c726-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c726-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c726-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="3c726-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3c726-130">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="3c726-130">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 





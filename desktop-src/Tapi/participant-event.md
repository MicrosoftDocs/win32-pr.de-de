---
description: Die Teilnehmer Ereignis-Aufzählung \_ beschreibt Teilnehmer Ereignisse.
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: PARTICIPANT_EVENT-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370666"
---
# <a name="participant_event-enumeration"></a><span data-ttu-id="04214-103">Teilnehmer \_ ereignisenumeration</span><span class="sxs-lookup"><span data-stu-id="04214-103">PARTICIPANT\_EVENT enumeration</span></span>

<span data-ttu-id="04214-104">\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="04214-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="04214-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="04214-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="04214-106">Die **Teilnehmer \_ Ereignis** -Aufzählung beschreibt Teilnehmer Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="04214-106">The **PARTICIPANT\_EVENT** enum describes participant events.</span></span> <span data-ttu-id="04214-107">Die [**itparticipvorgänger Vent:: get- \_ Ereignis**](itparticipantevent-get-event.md) Methode gibt einen Member dieser Enumeration zurück, um den Typ des aufgetretenen Konferenzteilnehmer Ereignisses anzugeben.</span><span class="sxs-lookup"><span data-stu-id="04214-107">The [**ITParticipantEvent::get\_Event**](itparticipantevent-get-event.md) method returns a member of this enum to indicate the type of conference participant event that occurred.</span></span> <span data-ttu-id="04214-108">Diese Enumeration wird von Anwendungen verwendet, die auf die [ipconf-MSP](ipconf-msp.md)zugreifen.</span><span class="sxs-lookup"><span data-stu-id="04214-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="04214-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="04214-109">Syntax</span></span>


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a><span data-ttu-id="04214-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="04214-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="04214-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_neuen \_ Teilnehmer PE**</span><span class="sxs-lookup"><span data-stu-id="04214-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**PE\_NEW\_PARTICIPANT**</span></span>
</dt> <dd>

<span data-ttu-id="04214-112">Der Konferenz wurde ein neuer Teilnehmer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="04214-112">A new participant has been added to the conference.</span></span>

</dd> <dt>

<span data-ttu-id="04214-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**PE- \_ Informations \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="04214-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**PE\_INFO\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="04214-114">Die Informationen zu einem Teilnehmer wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="04214-114">Information on a participant has changed.</span></span>

</dd> <dt>

<span data-ttu-id="04214-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE- \_ Teilnehmer \_ verlassen**</span><span class="sxs-lookup"><span data-stu-id="04214-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE\_PARTICIPANT\_LEAVE**</span></span>
</dt> <dd>

<span data-ttu-id="04214-116">Ein Teilnehmer hat die Konferenz verlassen.</span><span class="sxs-lookup"><span data-stu-id="04214-116">A participant has left the conference.</span></span>

</dd> <dt>

<span data-ttu-id="04214-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**\_neuen \_ substream PE**</span><span class="sxs-lookup"><span data-stu-id="04214-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**PE\_NEW\_SUBSTREAM**</span></span>
</dt> <dd>

<span data-ttu-id="04214-118">Dem Teilnehmer wurde ein neuer untergeordneter Stream hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="04214-118">A new substream has been added to the participant.</span></span>

</dd> <dt>

<span data-ttu-id="04214-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**PE- \_ substrom \_ entfernt**</span><span class="sxs-lookup"><span data-stu-id="04214-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**PE\_SUBSTREAM\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="04214-120">Ein neuer teilstream wurde aus dem Teilnehmer entfernt.</span><span class="sxs-lookup"><span data-stu-id="04214-120">A new substream has been removed from the participant.</span></span>

</dd> <dt>

<span data-ttu-id="04214-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**zugeordneter PE- \_ substream \_**</span><span class="sxs-lookup"><span data-stu-id="04214-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**PE\_SUBSTREAM\_MAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="04214-122">Ein Teilnehmer wurde einem substream zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="04214-122">A participant has been mapped to a substream.</span></span>

</dd> <dt>

<span data-ttu-id="04214-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE- \_ substream \_ nicht zugeordnet**</span><span class="sxs-lookup"><span data-stu-id="04214-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE\_SUBSTREAM\_UNMAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="04214-124">Die Zuordnung eines Teilnehmers zu einem substream wurde aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="04214-124">A participant has been unmapped from a substream.</span></span>

</dd> <dt>

<span data-ttu-id="04214-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**Timeout für PE- \_ Teilnehmer \_**</span><span class="sxs-lookup"><span data-stu-id="04214-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**PE\_PARTICIPANT\_TIMEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="04214-126">Ein Teilnehmer wurde aufgrund eines Timeouts aus der Konferenz entfernt.</span><span class="sxs-lookup"><span data-stu-id="04214-126">A participant has been removed from the conference due to a timeout.</span></span>

</dd> <dt>

<span data-ttu-id="04214-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**PE- \_ Teilnehmer \_ wieder hergestellt**</span><span class="sxs-lookup"><span data-stu-id="04214-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**PE\_PARTICIPANT\_RECOVERED**</span></span>
</dt> <dd>

<span data-ttu-id="04214-128">Ein entfernter Teilnehmer ist wieder sichtbar.</span><span class="sxs-lookup"><span data-stu-id="04214-128">A removed participant is again visible.</span></span> <span data-ttu-id="04214-129">Normalerweise ist dies ein Teilnehmer, der abgelaufen ist, aber Signale empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="04214-129">Usually, this is a participant who timed out but signals are now being received.</span></span>

</dd> <dt>

<span data-ttu-id="04214-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**aktiver PE- \_ Teilnehmer \_**</span><span class="sxs-lookup"><span data-stu-id="04214-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**PE\_PARTICIPANT\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="04214-131">Der Teilnehmer ist in der Konferenz aktiv geworden.</span><span class="sxs-lookup"><span data-stu-id="04214-131">The participant has become active in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="04214-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE- \_ Teilnehmer \_ inaktiv**</span><span class="sxs-lookup"><span data-stu-id="04214-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE\_PARTICIPANT\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="04214-133">Der Teilnehmer ist in der Konferenz inaktiv geworden.</span><span class="sxs-lookup"><span data-stu-id="04214-133">The participant has become inactive in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="04214-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**lokales PE- \_ \_ Gespräch**</span><span class="sxs-lookup"><span data-stu-id="04214-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**PE\_LOCAL\_TALKING**</span></span>
</dt> <dd>

<span data-ttu-id="04214-135">Der lokale Teilnehmer hat mit der Diskussion begonnen.</span><span class="sxs-lookup"><span data-stu-id="04214-135">The local participant has started to talk.</span></span>

</dd> <dt>

<span data-ttu-id="04214-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**lokale PE-unbeaufsichtigte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="04214-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE\_LOCAL\_SILENT**</span></span>
</dt> <dd>

<span data-ttu-id="04214-137">Der lokale Teilnehmer ist in der Konferenz unbeaufsichtigt.</span><span class="sxs-lookup"><span data-stu-id="04214-137">The local participant has become silent in the conference.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04214-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04214-138">Requirements</span></span>



| <span data-ttu-id="04214-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04214-139">Requirement</span></span> | <span data-ttu-id="04214-140">Wert</span><span class="sxs-lookup"><span data-stu-id="04214-140">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04214-141">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="04214-141">TAPI version</span></span><br/> | <span data-ttu-id="04214-142">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="04214-142">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="04214-143">Header</span><span class="sxs-lookup"><span data-stu-id="04214-143">Header</span></span><br/>       | <dl> <span data-ttu-id="04214-144"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="04214-144"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04214-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04214-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04214-146">**Itparticipvorgänger Vent:: get- \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="04214-146">**ITParticipantEvent::get\_Event**</span></span>](itparticipantevent-get-event.md)
</dt> <dt>

[<span data-ttu-id="04214-147">Ipconf-msp</span><span class="sxs-lookup"><span data-stu-id="04214-147">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="04214-148">Ipconf-MSP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="04214-148">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 





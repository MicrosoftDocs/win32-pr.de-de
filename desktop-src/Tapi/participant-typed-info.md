---
description: 'Die Member der typisierten Info-Enumeration für den Teilnehmer \_ \_ identifizieren den Typ der Teilnehmer Informationen, die von der itparticipants:: get- \_ Methode "participanttypdinfo" abgerufen werden. Diese Enumeration wird von Anwendungen verwendet, die auf die ipconf-MSP zugreifen.'
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: PARTICIPANT_TYPED_INFO-Enumeration (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370665"
---
# <a name="participant_typed_info-enumeration"></a><span data-ttu-id="3420d-104">Teilnehmer mit \_ typisierter \_ Enumeration</span><span class="sxs-lookup"><span data-stu-id="3420d-104">PARTICIPANT\_TYPED\_INFO enumeration</span></span>

<span data-ttu-id="3420d-105">\[**Teilnehmer \_ Typisierte \_ Informationen** sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3420d-105">\[**PARTICIPANT\_TYPED\_INFO** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3420d-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="3420d-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3420d-107">Die Member der **\_ typisierten \_ Info** -Enumeration für den Teilnehmer identifizieren den Typ der Teilnehmer Informationen, die von der [**itparticipants:: Get-Methode " \_ participanttypdinfo**](itparticipant-get-participanttypedinfo.md) " abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3420d-107">The members of the **PARTICIPANT\_TYPED\_INFO** enum identify the type of participant information being retrieved by the [**ITParticipant::get\_ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) method.</span></span> <span data-ttu-id="3420d-108">Diese Enumeration wird von Anwendungen verwendet, die auf die [ipconf-MSP](ipconf-msp.md)zugreifen.</span><span class="sxs-lookup"><span data-stu-id="3420d-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3420d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3420d-109">Syntax</span></span>


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a><span data-ttu-id="3420d-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3420d-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3420d-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI \_ CanonicalName**</span><span class="sxs-lookup"><span data-stu-id="3420d-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI\_CANONICALNAME**</span></span>
</dt> <dd>

<span data-ttu-id="3420d-112">Kanonischer Name des Teilnehmers, z someone@example.com . b..</span><span class="sxs-lookup"><span data-stu-id="3420d-112">Canonical name of participant, such as someone@example.com.</span></span>

</dd> <dt>

<span data-ttu-id="3420d-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**PTI- \_ Name**</span><span class="sxs-lookup"><span data-stu-id="3420d-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**PTI\_NAME**</span></span>
</dt> <dd>

<span data-ttu-id="3420d-114">Anzeigbarer Name des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="3420d-114">Displayable name of participant.</span></span>

</dd> <dt>

<span data-ttu-id="3420d-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI \_ EmailAddress**</span><span class="sxs-lookup"><span data-stu-id="3420d-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI\_EMAILADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="3420d-116">E-Mail-Adresse des Teilnehmers</span><span class="sxs-lookup"><span data-stu-id="3420d-116">Participant's email address.</span></span>

</dd> <dt>

<span data-ttu-id="3420d-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI- \_ PhoneNumber**</span><span class="sxs-lookup"><span data-stu-id="3420d-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI\_PHONENUMBER**</span></span>
</dt> <dd>

<span data-ttu-id="3420d-118">Telefon Adresse des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="3420d-118">Participant's phone address.</span></span>

</dd> <dt>

<span data-ttu-id="3420d-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**PTI- \_ Speicherort**</span><span class="sxs-lookup"><span data-stu-id="3420d-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**PTI\_LOCATION**</span></span>
</dt> <dd>

<span data-ttu-id="3420d-120">Geografische Adresse des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="3420d-120">Participant's geographical address.</span></span>

</dd> <dt>

<span data-ttu-id="3420d-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**PTI- \_ Tool**</span><span class="sxs-lookup"><span data-stu-id="3420d-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**PTI\_TOOL**</span></span>
</dt> <dd>

<span data-ttu-id="3420d-122">Die Anwendung des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="3420d-122">Participant's application.</span></span>

</dd> <dt>

<span data-ttu-id="3420d-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI- \_ Notizen**</span><span class="sxs-lookup"><span data-stu-id="3420d-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI\_NOTES**</span></span>
</dt> <dd>

<span data-ttu-id="3420d-124">Hinweise zum Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="3420d-124">Notes concerning participant.</span></span>

</dd> <dt>

<span data-ttu-id="3420d-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ Privat**</span><span class="sxs-lookup"><span data-stu-id="3420d-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="3420d-126">Definiert eine experimentelle oder anwendungsspezifische Erweiterung der Quell Beschreibung (SDES).</span><span class="sxs-lookup"><span data-stu-id="3420d-126">Defines an experimental or application-specific Source Description (SDES) extension.</span></span> <span data-ttu-id="3420d-127">Weitere Informationen finden Sie in RFC 1889.</span><span class="sxs-lookup"><span data-stu-id="3420d-127">See RFC 1889 for details.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3420d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3420d-128">Requirements</span></span>



| <span data-ttu-id="3420d-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3420d-129">Requirement</span></span> | <span data-ttu-id="3420d-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3420d-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3420d-131">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="3420d-131">TAPI version</span></span><br/> | <span data-ttu-id="3420d-132">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3420d-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3420d-133">Header</span><span class="sxs-lookup"><span data-stu-id="3420d-133">Header</span></span><br/>       | <dl> <span data-ttu-id="3420d-134"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3420d-134"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3420d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3420d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3420d-136">**Itteilnehmer:: get \_ participanttypdinfo**</span><span class="sxs-lookup"><span data-stu-id="3420d-136">**ITParticipant::get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[<span data-ttu-id="3420d-137">Ipconf-msp</span><span class="sxs-lookup"><span data-stu-id="3420d-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="3420d-138">Ipconf-MSP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3420d-138">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 





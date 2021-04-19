---
description: Die \_ Bitflag-Konstanten von linecallpartyid beschreiben die Art der Informationen, die über die an einem-Befehl beteiligten Parteien verfügbar sind.
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: LINECALLPARTYID_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370826"
---
# <a name="linecallpartyid_-constants"></a><span data-ttu-id="f23e6-103">Linecallpartyid- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="f23e6-103">LINECALLPARTYID\_ Constants</span></span>

<span data-ttu-id="f23e6-104">Die Bitflag-Konstanten von **linecallpartyid \_** beschreiben die Art der Informationen, die über die an einem-Befehl beteiligten Parteien verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f23e6-104">The **LINECALLPARTYID\_** bit-flag constants describe the nature of the information available about the parties involved in a call.</span></span>

<dl> <dt>

<span data-ttu-id="f23e6-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**linecallpartyid- \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="f23e6-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**LINECALLPARTYID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f23e6-106">Informationen zu Partei Bezeichnern bestehen aus der Adresse der Partei im kanonischen Adressformat oder im Format der ausführbaren Adresse.</span><span class="sxs-lookup"><span data-stu-id="f23e6-106">Party identifier information consists of the party's address in either canonical address format or dialable address format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f23e6-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**die linecallpartyid ist \_ blockiert.**</span><span class="sxs-lookup"><span data-stu-id="f23e6-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f23e6-108">Die Informationen zur Partei Kennung sind nicht verfügbar, da Sie von der Remote Partei blockiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f23e6-108">Party identifier information is not available because it has been blocked by the remote party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f23e6-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**Name der linecallpartyid \_**</span><span class="sxs-lookup"><span data-stu-id="f23e6-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**LINECALLPARTYID\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f23e6-110">Die Informationen zur Partei Kennung bestehen aus dem Namen der Partei (z. b. aus einem Verzeichnis, das im Switch aufbewahrt wird).</span><span class="sxs-lookup"><span data-stu-id="f23e6-110">Party identifier information consists of the party's name (as, for example, from a directory kept inside the switch).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f23e6-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**linecallpartyid- \_ outof-Bereich**</span><span class="sxs-lookup"><span data-stu-id="f23e6-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID\_OUTOFAREA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f23e6-112">Aufrufer-ID-Informationen für den Aufruf sind nicht verfügbar, da Sie nicht auf die gesamte Weise vom Netzwerk weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f23e6-112">Caller ID information for the call is not available because it is not propagated all the way by the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f23e6-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**linecallpartyid \_ partiell**</span><span class="sxs-lookup"><span data-stu-id="f23e6-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f23e6-114">Die Informationen zu Partei Bezeichnern sind gültig, sind jedoch nur auf partielle Informationen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f23e6-114">Party identifier information is valid but it is limited to partial information only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f23e6-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**linecallpartyid ist \_ nicht erreichbar.**</span><span class="sxs-lookup"><span data-stu-id="f23e6-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f23e6-116">Die Informationen zur Partei Kennung sind nicht verfügbar und werden später nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f23e6-116">Party identifier information is not available and will not become available later.</span></span> <span data-ttu-id="f23e6-117">Informationen sind aus unbekannten Gründen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f23e6-117">Information may be unavailable for unspecified reasons.</span></span> <span data-ttu-id="f23e6-118">Beispielsweise wurden die Informationen nicht vom Netzwerk übermittelt, Sie wurden vom Dienstanbieter ignoriert usw.</span><span class="sxs-lookup"><span data-stu-id="f23e6-118">For example, the information was not delivered by the network, it was ignored by the service provider, and so forth.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f23e6-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**linecallpartyid \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="f23e6-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f23e6-120">Informationen zu Partei Bezeichnern sind zurzeit unbekannt, werden aber später möglicherweise bekannt sein.</span><span class="sxs-lookup"><span data-stu-id="f23e6-120">Party identifier information is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f23e6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f23e6-121">Remarks</span></span>

<span data-ttu-id="f23e6-122">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="f23e6-122">No extensibility.</span></span> <span data-ttu-id="f23e6-123">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="f23e6-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="f23e6-124">Für jede der möglichen Parteien, die an einem-Befehl beteiligt sind, beschreiben die **linecallpartyid \_** -Konstanten, wie die Partei-Bezeichnerinformationen formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="f23e6-124">For each of the possible parties involved in a call, the **LINECALLPARTYID\_** constants describe how the party identifier information is formatted.</span></span> <span data-ttu-id="f23e6-125">Diese Informationen werden in der [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) -Datenstruktur bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f23e6-125">This information is supplied in the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f23e6-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f23e6-126">Requirements</span></span>



| <span data-ttu-id="f23e6-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f23e6-127">Requirement</span></span> | <span data-ttu-id="f23e6-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f23e6-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f23e6-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="f23e6-129">TAPI version</span></span><br/> | <span data-ttu-id="f23e6-130">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f23e6-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f23e6-131">Header</span><span class="sxs-lookup"><span data-stu-id="f23e6-131">Header</span></span><br/>       | <dl> <span data-ttu-id="f23e6-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f23e6-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 





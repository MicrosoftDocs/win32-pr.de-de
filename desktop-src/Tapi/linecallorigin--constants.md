---
description: Die linecallorigin- \_ Konstanten beschreiben den Ursprung eines Aufrufes.
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: LINECALLORIGIN_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351262"
---
# <a name="linecallorigin_-constants"></a><span data-ttu-id="c364d-103">Linecallorigin- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="c364d-103">LINECALLORIGIN\_ Constants</span></span>

<span data-ttu-id="c364d-104">Die **linecallorigin \_** -Konstanten beschreiben den Ursprung eines Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="c364d-104">The **LINECALLORIGIN\_** constants describe the origin of a call.</span></span>

<dl> <dt>

<span data-ttu-id="c364d-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**linecallorigin- \_ Konferenz**</span><span class="sxs-lookup"><span data-stu-id="c364d-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**LINECALLORIGIN\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c364d-106">Das Telefon Handle ist ein Konferenzgespräch, d. h., es handelt sich um die Verbindung der Anwendung mit der Konferenzbrücke im Switch.</span><span class="sxs-lookup"><span data-stu-id="c364d-106">The call handle is for a conference call, that is, it is the application's connection to the conference bridge in the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c364d-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**linecallorigin \_ extern**</span><span class="sxs-lookup"><span data-stu-id="c364d-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c364d-108">Der-Befehl stammt als eingehender-Rückruf für eine externe Zeile.</span><span class="sxs-lookup"><span data-stu-id="c364d-108">The call originated as an incoming call on an external line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c364d-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**linecallorigin \_ eingehend**</span><span class="sxs-lookup"><span data-stu-id="c364d-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN\_INBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c364d-110">Der-Befehl stammt als eingehender-Rückruf, aber der Dienstanbieter kann nicht ermitteln, ob er von einer anderen Station desselben Switches oder von einer externen Zeile stammt.</span><span class="sxs-lookup"><span data-stu-id="c364d-110">The call originated as an incoming call, but the service provider is unable to determine whether it came from another station on the same switch or from an external line.</span></span> <span data-ttu-id="c364d-111">Dienstanbieter können diese Konstante nur verwenden, wenn TAPI-Version 1,4 oder höher ausgehandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="c364d-111">Service providers can use this constant only when TAPI version 1.4 or later has been negotiated.</span></span> <span data-ttu-id="c364d-112">Andernfalls kann der Dienstanbieter den "linecallorigin"- \_ nicht Gebrauch ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c364d-112">Otherwise, the service provider can substitute LINECALLORIGIN\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c364d-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**linecallorigin ( \_ intern)**</span><span class="sxs-lookup"><span data-stu-id="c364d-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c364d-114">Der-Befehl stammt als eingehender aufrufungsort an einer Station, die sich intern in derselben Wechsel Umgebung befand.</span><span class="sxs-lookup"><span data-stu-id="c364d-114">The call originated as an incoming call at a station internal to the same switching environment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c364d-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**linecallorigin \_ ausgehend**</span><span class="sxs-lookup"><span data-stu-id="c364d-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN\_OUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c364d-116">Der-Befehl stammt von dieser Station als ausgehender-Befehl.</span><span class="sxs-lookup"><span data-stu-id="c364d-116">The call originated from this station as an outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c364d-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**linecallorigin ist \_ nicht erreichbar.**</span><span class="sxs-lookup"><span data-stu-id="c364d-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c364d-118">Der Ursprungs Ursprung ist nicht verfügbar und wird für diesen-Befehl nie bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="c364d-118">The call origin is not available and will never become known for this call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c364d-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**linecallorigin \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="c364d-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c364d-120">Der Ursprungs Ursprung ist derzeit unbekannt, kann aber später bekannt werden.</span><span class="sxs-lookup"><span data-stu-id="c364d-120">The call origin is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c364d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c364d-121">Remarks</span></span>

<span data-ttu-id="c364d-122">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="c364d-122">No extensibility.</span></span> <span data-ttu-id="c364d-123">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="c364d-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="c364d-124">Der Ursprung eines Aufrufes wird im Member **dwOrigin** der [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) -Struktur des Aufrufes gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c364d-124">The origin of a call is stored in the **dwOrigin** member of the call's [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c364d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c364d-125">Requirements</span></span>



| <span data-ttu-id="c364d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c364d-126">Requirement</span></span> | <span data-ttu-id="c364d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c364d-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c364d-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="c364d-128">TAPI version</span></span><br/> | <span data-ttu-id="c364d-129">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c364d-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c364d-130">Header</span><span class="sxs-lookup"><span data-stu-id="c364d-130">Header</span></span><br/>       | <dl> <span data-ttu-id="c364d-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c364d-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 





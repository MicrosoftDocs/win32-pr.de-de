---
description: Die lineofferingmode \_ -bitflagkonstanten (TAPI-Versionen 1,4 und höher) beschreiben verschiedene Unterzustände eines Angebots Aufrufes.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: LINEOFFERINGMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361406"
---
# <a name="lineofferingmode_-constants"></a><span data-ttu-id="ac38a-103">Lineofferingmode- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="ac38a-103">LINEOFFERINGMODE\_ Constants</span></span>

<span data-ttu-id="ac38a-104">Die **lineofferingmode \_** -bitflagkonstanten (TAPI-Versionen 1,4 und höher) beschreiben verschiedene Unterzustände eines Angebots Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="ac38a-104">The **LINEOFFERINGMODE\_** bit-flag constants (TAPI versions 1.4 and later) describe different substates of an offering call.</span></span> <span data-ttu-id="ac38a-105">Ein Modus ist als Aufruf Status für die Anwendung nach den Aufrufen State-trdansitionen für Angebot und innerhalb der [**line \_ CallState**](line-callstate.md) -Meldung verfügbar, die angibt, dass der Aufruf im linecallstate- \_ Angebot vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ac38a-105">A mode is available as call status to the application after the call state trdansitions to offering, and within the [**LINE\_CALLSTATE**](line-callstate.md) message indicating the call is in LINECALLSTATE\_OFFERING.</span></span> <span data-ttu-id="ac38a-106">Diese Werte werden verwendet, wenn der Aufruf einer freigegebenen Adresse mit anderen Stationen (siehe [**lineaddresssharing- \_ Konstanten**](lineaddresssharing--constants.md)), primär elektronischer Schlüsselsysteme, erfolgt.</span><span class="sxs-lookup"><span data-stu-id="ac38a-106">These values are used when the call is on an address that is shared (bridged) with other stations (see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span>

<dl> <dt>

<span data-ttu-id="ac38a-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**lineofferingmode \_ aktiv**</span><span class="sxs-lookup"><span data-stu-id="ac38a-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac38a-108">Gibt an, dass der Anruf an der aktuellen Station warnt (wird von linedevstate \_ -Klingel Meldungen begleitet), und wenn eine Anwendung für die automatische Beantwortung eingerichtet ist, kann Sie dies tun.</span><span class="sxs-lookup"><span data-stu-id="ac38a-108">Indicates that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="ac38a-109">Wenn der aufrufstatusmodus 0 (null) ist, sollte die Anwendung davon ausgehen, dass der Wert aktiv ist (Dies wäre die Situation bei einer nicht überbrücken Adresse).</span><span class="sxs-lookup"><span data-stu-id="ac38a-109">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="ac38a-110">(TAPI-Versionen 1,4 und höher)</span><span class="sxs-lookup"><span data-stu-id="ac38a-110">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac38a-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**lineofferingmode \_ inaktiv**</span><span class="sxs-lookup"><span data-stu-id="ac38a-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac38a-112">Gibt an, dass der-Befehl an mehr als einer Station angeboten wird, aber die aktuelle Station hat keine Warnung (z. b. kann es sich um eine Aufsichts Station handeln, bei der der Angebots Status "Advisory" ist, z. b. blinkende eines Lichts); die Software auf der Stations Gruppe für die automatische Beantwortung sollte den Anruf vorzugsweise nicht beantworten, da dies das Vorrecht an der primären (Warnungs-) Station sein sollte, aber [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) kann verwendet werden, um den Anruf zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="ac38a-112">Indicates that the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) may be used to connect the call.</span></span> <span data-ttu-id="ac38a-113">(TAPI-Versionen 1,4 und höher)</span><span class="sxs-lookup"><span data-stu-id="ac38a-113">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac38a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac38a-114">Remarks</span></span>

<span data-ttu-id="ac38a-115">Nicht erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="ac38a-115">Not extensible.</span></span> <span data-ttu-id="ac38a-116">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="ac38a-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="ac38a-117">Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version in der Zeile zu untersuchen und diese lineofferingmode-Werte nicht zu verwenden, \_ Wenn Sie von der ausgehandelten Version nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ac38a-117">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEOFFERINGMODE\_ values if they are not supported on the negotiated version.</span></span> <span data-ttu-id="ac38a-118">Anwendungen, die nicht von lineofferingmode erkannt werden, \_ nehmen wahrscheinlich an, dass sich ein im linecallstate-Angebot vorgegander Vorgang \_ im lineofferingmode-Modus befindet \_ .</span><span class="sxs-lookup"><span data-stu-id="ac38a-118">Applications that are not cognizant of LINEOFFERINGMODE\_ will most likely assume that a call that is in LINECALLSTATE\_OFFERING is in LINEOFFERINGMODE\_ACTIVE.</span></span>

<span data-ttu-id="ac38a-119">Die inaktiven Werte für "lineofferingmode" \_ und "lineofferingmode" \_ werden verwendet, wenn sich der Aufruf auf einer Adresse befindet, die mit anderen Stationen gemeinsam genutzt wird (überbrückt; siehe [lineaddresssharing- \_ Konstanten](lineaddresssharing--constants.md)), primär mit elektronischen Schlüssel Systemen.</span><span class="sxs-lookup"><span data-stu-id="ac38a-119">The LINEOFFERINGMODE\_ACTIVE and LINEOFFERINGMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [LINEADDRESSSHARING\_ Constants](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="ac38a-120">Wenn der Anruf Zustands Modus des Angebots "aktiv" ist, bedeutet dies, dass der Anruf an der aktuellen Station warnt (wird von linedevstate \_ -Nachrichten begleitet), und wenn eine Anwendung für die automatische Beantwortung eingerichtet ist, kann Sie dies tun.</span><span class="sxs-lookup"><span data-stu-id="ac38a-120">If the offering call state mode is "active," it means that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="ac38a-121">Wenn der CallState-Modus "inaktiv" ist, wird der-Befehl auf mehreren Stationen angeboten, aber die aktuelle Station hat keine Warnung (es kann sich z. b. um eine Aufsichts Station handeln, bei der der Angebots Status "Advisory" ist, wie z. b. das Blinken eines Lichts). die Software auf der Stations Gruppe für die automatische Beantwortung sollte den Anruf vorzugsweise nicht beantworten, da dies das Vorrecht an der primären (Warnungs-) Station sein sollte, aber [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) kann verwendet werden, um den Anruf zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="ac38a-121">If the call state mode is "inactive," the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) can be used to connect the call.</span></span> <span data-ttu-id="ac38a-122">Wenn der aufrufstatusmodus 0 (null) ist, sollte die Anwendung davon ausgehen, dass der Wert aktiv ist (Dies wäre die Situation bei einer nicht überbrücken Adresse).</span><span class="sxs-lookup"><span data-stu-id="ac38a-122">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac38a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac38a-123">Requirements</span></span>



| <span data-ttu-id="ac38a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac38a-124">Requirement</span></span> | <span data-ttu-id="ac38a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ac38a-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac38a-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="ac38a-126">TAPI version</span></span><br/> | <span data-ttu-id="ac38a-127">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ac38a-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ac38a-128">Header</span><span class="sxs-lookup"><span data-stu-id="ac38a-128">Header</span></span><br/>       | <dl> <span data-ttu-id="ac38a-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac38a-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 





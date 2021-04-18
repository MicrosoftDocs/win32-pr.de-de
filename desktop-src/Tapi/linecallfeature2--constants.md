---
description: Die LINECALLFEATURE2 \_ -Konstanten Listen die ergänzenden Features auf, die für Konferenz-, Übertragungs-und Park Anrufe verfügbar sind.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: LINECALLFEATURE2_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977e71f722fba34da6b2ecbd6a3e914c34a0aae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357671"
---
# <a name="linecallfeature2_-constants"></a><span data-ttu-id="251b7-103">LINECALLFEATURE2- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="251b7-103">LINECALLFEATURE2\_ Constants</span></span>

<span data-ttu-id="251b7-104">Die **LINECALLFEATURE2 \_** -Konstanten Listen die ergänzenden Features auf, die für Konferenz-, Übertragungs-und Park Anrufe verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="251b7-104">The **LINECALLFEATURE2\_** constants list the supplemental features available for conferencing, transferring, and parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="251b7-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ complcallback**</span><span class="sxs-lookup"><span data-stu-id="251b7-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2\_COMPLCALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="251b7-106">Wenn dieses Bit aktiviert ist, kann das "Callback"-Feature mithilfe der linecomplmode- \_ Rückrufoption mit [**linecompletecallaufgerufen**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)werden.</span><span class="sxs-lookup"><span data-stu-id="251b7-106">If this bit is on, the "callback" feature can be invoked by using the LINECOMPLMODE\_CALLBACK option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="251b7-107">Das \_ completecallbit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.</span><span class="sxs-lookup"><span data-stu-id="251b7-107">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="251b7-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ complcampon**</span><span class="sxs-lookup"><span data-stu-id="251b7-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2\_COMPLCAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="251b7-109">Wenn dieses Bit aktiviert ist, kann das Feature "Camp on" mithilfe der Option "-Option für linecomplmode" \_ mit [**linecompletecallaufgerufen**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)werden.</span><span class="sxs-lookup"><span data-stu-id="251b7-109">If this bit is on, the "camp on" feature can be invoked by using the LINECOMPLMODE\_CAMPON option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="251b7-110">Das \_ completecallbit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.</span><span class="sxs-lookup"><span data-stu-id="251b7-110">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="251b7-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ complintrude**</span><span class="sxs-lookup"><span data-stu-id="251b7-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2\_COMPLINTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="251b7-112">Wenn dieses Bit aktiviert ist, kann das "Intrude"-Feature mithilfe der Option linecomplmode \_ Intrude mit [**linecompletecallaufgerufen**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)werden.</span><span class="sxs-lookup"><span data-stu-id="251b7-112">If this bit is on, the "intrude" feature can be invoked by using the LINECOMPLMODE\_INTRUDE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="251b7-113">Das \_ completecallbit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.</span><span class="sxs-lookup"><span data-stu-id="251b7-113">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="251b7-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ complmessage**</span><span class="sxs-lookup"><span data-stu-id="251b7-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2\_COMPLMESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="251b7-115">Wenn dieses Bit aktiviert ist, kann die Funktion "Nachricht verlassen" mithilfe der Option "linecomplmode \_ Message" mit [**linecompletecallaufgerufen**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)werden.</span><span class="sxs-lookup"><span data-stu-id="251b7-115">If this bit is on, the "leave message" feature can be invoked by using the LINECOMPLMODE\_MESSAGE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="251b7-116">Das \_ completecallbit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.</span><span class="sxs-lookup"><span data-stu-id="251b7-116">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="251b7-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ noholdconference**</span><span class="sxs-lookup"><span data-stu-id="251b7-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="251b7-118">Wenn dieses Bit aktiviert ist, kann eine "keine Hold-Konferenz" mithilfe der Option "linecallparamflags \_ noholdconference" mit [**linesetupconference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="251b7-118">If this bit is on, a "no hold conference" can be created by using the LINECALLPARAMFLAGS\_NOHOLDCONFERENCE option with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference).</span></span> <span data-ttu-id="251b7-119">Das linecallfeature \_ setupconf-Bit wird auch im **dwcallfeatures** -Member aktiviert.</span><span class="sxs-lookup"><span data-stu-id="251b7-119">The LINECALLFEATURE\_SETUPCONF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="251b7-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ onesteptransfer**</span><span class="sxs-lookup"><span data-stu-id="251b7-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="251b7-121">Wenn dieses Bit aktiviert ist, kann "One Step Transfer" mithilfe der linecallparamflags \_ onesteptransfer-Option mit [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="251b7-121">If this bit is on, "one step transfer" can be created by using the LINECALLPARAMFLAGS\_ONESTEPTRANSFER option with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="251b7-122">Das linecallfeature \_ setuptransfer-Bit wird auch im **dwcallfeatures** -Member aktiviert.</span><span class="sxs-lookup"><span data-stu-id="251b7-122">The LINECALLFEATURE\_SETUPTRANSFER bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="251b7-123">Wenn keines der compl-Bits im **dwCallFeatures2** -Member in [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) angegeben ist, aber linecallfeature \_ completecallfest gelegt ist, ist es möglich, dass jeder dieser Komponenten funktioniert, aber der Dienstanbieter hat nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="251b7-123">If none of the "COMPL" bits is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETECALL is specified, then it is possible that any of them will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="251b7-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ transferconf**</span><span class="sxs-lookup"><span data-stu-id="251b7-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2\_TRANSFERCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="251b7-125">Wenn dieses Bit ist, kann die Funktion [**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) verwendet werden, um die Übertragung als drei-Wege-Konferenz aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="251b7-125">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a three-way conference.</span></span> <span data-ttu-id="251b7-126">Das \_ completetransf-Bit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.</span><span class="sxs-lookup"><span data-stu-id="251b7-126">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="251b7-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ transfernorm**</span><span class="sxs-lookup"><span data-stu-id="251b7-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2\_TRANSFERNORM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="251b7-128">Wenn dieses Bit ist, kann die Funktion [**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) verwendet werden, um die Übertragung als normale Übertragung zu beheben.</span><span class="sxs-lookup"><span data-stu-id="251b7-128">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a normal transfer.</span></span> <span data-ttu-id="251b7-129">Das \_ completetransf-Bit linecallfeature wird auch im **dwcallfeatures** -Member aktiviert.</span><span class="sxs-lookup"><span data-stu-id="251b7-129">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="251b7-130">Wenn weder transfernorm noch transferconf im **dwCallFeatures2** -Member in [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) angegeben ist, aber linecallfeature \_ completetransf angegeben ist, ist es möglich, dass entweder funktioniert, aber der Dienstanbieter hat nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="251b7-130">If neither TRANSFERNORM nor TRANSFERCONF is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETETRANSF is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="251b7-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ Park Direct**</span><span class="sxs-lookup"><span data-stu-id="251b7-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2\_PARKDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="251b7-132">Wenn dieses Bit aktiviert ist, kann das "gesteuerte Park"-Feature mithilfe der linepark Mode- \_ Option mit [**linepark**](/windows/desktop/api/Tapi/nf-tapi-linepark)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="251b7-132">If this bit is on, the "directed park" feature can be invoked by using the LINEPARKMODE\_DIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="251b7-133">Das linecallfeature- \_ Park Bit befindet sich auch im **dwcallfeatures** -Member.</span><span class="sxs-lookup"><span data-stu-id="251b7-133">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="251b7-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 " \_ Parser"**</span><span class="sxs-lookup"><span data-stu-id="251b7-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2\_PARKNONDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="251b7-135">Wenn dieses Bit aktiviert ist, kann die "nicht gesteuerte Park"-Funktion mithilfe der nicht gesteuerten Option linepark Mode \_ mit [**linepark**](/windows/desktop/api/Tapi/nf-tapi-linepark)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="251b7-135">If this bit is on, the "non-directed park" feature can be invoked by using the LINEPARKMODE\_NONDIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="251b7-136">Das linecallfeature- \_ Park Bit befindet sich auch im **dwcallfeatures** -Member.</span><span class="sxs-lookup"><span data-stu-id="251b7-136">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="251b7-137">Wenn weder Park Direct noch parknondirect im **dwCallFeatures2** -Member in [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) angegeben ist, aber linecallfeature \_ Park angegeben ist, ist es möglich, dass entweder funktioniert, aber der Dienstanbieter hat nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="251b7-137">If neither PARKDIRECT nor PARKNONDIRECT is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_PARK is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="251b7-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="251b7-138">Requirements</span></span>



| <span data-ttu-id="251b7-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="251b7-139">Requirement</span></span> | <span data-ttu-id="251b7-140">Wert</span><span class="sxs-lookup"><span data-stu-id="251b7-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="251b7-141">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="251b7-141">TAPI version</span></span><br/> | <span data-ttu-id="251b7-142">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="251b7-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="251b7-143">Header</span><span class="sxs-lookup"><span data-stu-id="251b7-143">Header</span></span><br/>       | <dl> <span data-ttu-id="251b7-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="251b7-144"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="251b7-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="251b7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="251b7-146">**Linecallstatus**</span><span class="sxs-lookup"><span data-stu-id="251b7-146">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="251b7-147">**linecompletecall**</span><span class="sxs-lookup"><span data-stu-id="251b7-147">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="251b7-148">**linecompletetransfer**</span><span class="sxs-lookup"><span data-stu-id="251b7-148">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="251b7-149">**linepark**</span><span class="sxs-lookup"><span data-stu-id="251b7-149">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[<span data-ttu-id="251b7-150">**linesetupconference**</span><span class="sxs-lookup"><span data-stu-id="251b7-150">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="251b7-151">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="251b7-151">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 





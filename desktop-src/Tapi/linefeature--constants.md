---
description: Die linefeature- \_ Konstanten Listen die Vorgänge auf, die mithilfe dieser API in einer Zeile aufgerufen werden können.
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: LINEFEATURE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365828"
---
# <a name="linefeature_-constants"></a><span data-ttu-id="e8b7e-103">Linefeature- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="e8b7e-103">LINEFEATURE\_ Constants</span></span>

<span data-ttu-id="e8b7e-104">Die **linefeature- \_ Konstanten** Listen die Vorgänge auf, die mithilfe dieser API in einer Zeile aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-104">The **LINEFEATURE\_ constants** list the operations that can be invoked on a line using this API.</span></span>

<dl> <dt>

<span data-ttu-id="e8b7e-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**linefeature \_ DevSpecific**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8b7e-106">Gerätespezifische Vorgänge können in der Zeile verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-106">Device-specific operations can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8b7e-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**linefeature \_ devspecificfeat**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE\_DEVSPECIFICFEAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8b7e-108">Gerätespezifische Features können in der Zeile verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-108">Device-specific features can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8b7e-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**linefeature \_ Vorwärts**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8b7e-110">Die Weiterleitung aller Adressen kann in der Zeile verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-110">Forwarding of all addresses can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8b7e-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**linefeature \_ forwarddnd**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8b7e-112">Die [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) -Funktion (mit einer leeren Zieladresse) kann verwendet werden, um die Funktion "nicht stören" für alle Adressen in der Zeile zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-112">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on all addresses on the line.</span></span> <span data-ttu-id="e8b7e-113">Linefeature \_ Forward wird ebenfalls festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-113">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="e8b7e-114">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-114">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8b7e-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**linefeature \_ forwardfwd**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8b7e-116">Die [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) -Funktion kann verwendet werden, um Aufrufe an allen Adressen an der Zeile an andere Zahlen weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-116">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on all address on the line to other numbers.</span></span> <span data-ttu-id="e8b7e-117">Linefeature \_ Forward wird ebenfalls festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-117">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="e8b7e-118">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-118">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8b7e-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**linefeature \_ MakeCall**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8b7e-120">Ein ausgehender Anruf kann mithilfe einer nicht angegebenen Adresse in dieser Zeile platziert werden.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-120">An outgoing call can be placed on this line using an unspecified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8b7e-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**linefeature \_ setdevstatus**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE\_SETDEVSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8b7e-122">Die [**linesetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) -Funktion kann auf dem liniengerät aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-122">The [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) function can be invoked on the line device.</span></span> <span data-ttu-id="e8b7e-123">Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-123">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8b7e-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**linefeature \_ setmediacontrol**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8b7e-125">Ein mediensteuer Element kann in dieser Zeile festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-125">Media control can be set on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8b7e-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**linefeature \_ setterminal**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8b7e-127">Terminal Modi für diese Zeile können festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-127">Terminal modes for this line can be set.</span></span>

> [!Note]  
> <span data-ttu-id="e8b7e-128">Wenn keines der neuen geänderten "Forward"-Bits im **dwlinefeatures** -Member in [**linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) festgelegt ist, aber das linefeature- \_ Forward-Bit festgelegt ist, kann jeder der vorwärts Modi funktionieren. der Dienstanbieter hat einfach nicht angegeben, welche Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-128">If neither of the new modified "FORWARD" bits is set in the **dwLineFeatures** member in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) but the LINEFEATURE\_FORWARD bit is set, then any of the forward modes can work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8b7e-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8b7e-129">Remarks</span></span>

<span data-ttu-id="e8b7e-130">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-130">No extensibility.</span></span> <span data-ttu-id="e8b7e-131">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-131">All 32 bits are reserved.</span></span>

<span data-ttu-id="e8b7e-132">Die linefeature- \_ Konstanten werden in [**linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) verwendet (von [**linegetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)zurückgegeben).</span><span class="sxs-lookup"><span data-stu-id="e8b7e-132">The LINEFEATURE\_ constants are used in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (returned by [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span></span> <span data-ttu-id="e8b7e-133">[**Linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) -Berichte für eine bestimmte Zeile, welche Zeilen Features tatsächlich aufgerufen werden können, während sich die Zeile im aktuellen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) reports, for a given line, which line features can actually be invoked while the line is in the current state.</span></span> <span data-ttu-id="e8b7e-134">Eine Anwendung würde diese Bestimmung nach Zeilen Statusänderungen dynamisch machen, was in der Regel durch Adressen-oder aufrufaktivitäten in der Zeile verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="e8b7e-134">An application would make this determination dynamically after line state changes, typically caused by address or call-related activities on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8b7e-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8b7e-135">Requirements</span></span>



| <span data-ttu-id="e8b7e-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8b7e-136">Requirement</span></span> | <span data-ttu-id="e8b7e-137">Wert</span><span class="sxs-lookup"><span data-stu-id="e8b7e-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e8b7e-138">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e8b7e-138">TAPI version</span></span><br/> | <span data-ttu-id="e8b7e-139">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e8b7e-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e8b7e-140">Header</span><span class="sxs-lookup"><span data-stu-id="e8b7e-140">Header</span></span><br/>       | <dl> <span data-ttu-id="e8b7e-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8b7e-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8b7e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8b7e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b7e-143">**Linedevstatus**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-143">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="e8b7e-144">**lineforward**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-144">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="e8b7e-145">**linegetlinedevstatus**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-145">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="e8b7e-146">**linesetlinedevstatus**</span><span class="sxs-lookup"><span data-stu-id="e8b7e-146">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 





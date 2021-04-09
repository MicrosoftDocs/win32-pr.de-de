---
title: IP_SPECIFIC_DATA Struktur (RTM. h)
description: Die IP \_ -spezifische Datenstruktur enthält IP-spezifische Daten.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- IP_SPECIFIC_DATA Struktur-RAS
- PIP_SPECIFIC_DATA-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104678"
---
# <a name="ip_specific_data-structure"></a><span data-ttu-id="109e6-105">IP- \_ spezifische \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="109e6-105">IP\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="109e6-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="109e6-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="109e6-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="109e6-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="109e6-108">Die **IP- \_ spezifische Daten** Struktur enthält IP-spezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="109e6-108">The **IP\_SPECIFIC DATA** structure contains IP-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="109e6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="109e6-109">Syntax</span></span>


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="109e6-110">Member</span><span class="sxs-lookup"><span data-stu-id="109e6-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="109e6-111">**Typ " \_ Typ"**</span><span class="sxs-lookup"><span data-stu-id="109e6-111">**FSD\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="109e6-112">Gibt den Routentyp an, wie in [RFC 1354](routing-protocols-request-for-comments.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="109e6-112">Specifies the route type as defined in [RFC 1354](routing-protocols-request-for-comments.md).</span></span> <span data-ttu-id="109e6-113">In der folgenden Tabelle werden die möglichen Werte für diesen Member angezeigt.</span><span class="sxs-lookup"><span data-stu-id="109e6-113">The following table shows the possible values for this member.</span></span>



| <span data-ttu-id="109e6-114">Member</span><span class="sxs-lookup"><span data-stu-id="109e6-114">Member</span></span>                                                                                               | <span data-ttu-id="109e6-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="109e6-115">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="109e6-116"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="109e6-116"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="109e6-117">Der Routentyp wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="109e6-117">The route type is not specified.</span></span> <span data-ttu-id="109e6-118">Der-Typ unterscheidet sich von den hier aufgeführten.</span><span class="sxs-lookup"><span data-stu-id="109e6-118">The type is different from those listed here.</span></span><br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <span data-ttu-id="109e6-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="109e6-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="109e6-120">Die Route ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="109e6-120">The route is invalid.</span></span> <span data-ttu-id="109e6-121">Normalerweise wird dieser Wert verwendet, um eine Route für ungültig zu erklären.</span><span class="sxs-lookup"><span data-stu-id="109e6-121">Normally, this value is used to invalidate a route.</span></span> <span data-ttu-id="109e6-122">Da die Invalidierung vom Routing Tabellen-Manager jedoch nicht unterstützt wird, wird die Route weiterhin in den Best-Route-Berechnungen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="109e6-122">However, since invalidation is not supported by the routing table manager, the route is still considered in best-route computations.</span></span> <span data-ttu-id="109e6-123">Daher sollten Routing Protokolle diesen Wert nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="109e6-123">Therefore, routing protocols should not use this value.</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="109e6-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="109e6-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="109e6-125">Die Route ist eine lokale Route, d. h., der nächste Hop ist das endgültige Ziel.</span><span class="sxs-lookup"><span data-stu-id="109e6-125">The route is a local route, that is, the next hop is the final destination.</span></span><br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <span data-ttu-id="109e6-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="109e6-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="109e6-127">Die Route ist eine Remote Route, d. h., der nächste Hop ist nicht das endgültige Ziel.</span><span class="sxs-lookup"><span data-stu-id="109e6-127">The route is a remote route, that is, the next hop is not the final destination.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="109e6-128">**F- \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="109e6-128">**FSD\_Policy**</span></span>
</dt> <dd>

<span data-ttu-id="109e6-129">Gibt den Satz von Bedingungen an, die die Auswahl einer multipfadroute bewirken würden.</span><span class="sxs-lookup"><span data-stu-id="109e6-129">Specifies the set of conditions that would cause the selection of a multi-path route.</span></span> <span data-ttu-id="109e6-130">Dieser Member befindet sich in der Regel im IP-Adressformat.</span><span class="sxs-lookup"><span data-stu-id="109e6-130">This member is typically in IP TOS format.</span></span> <span data-ttu-id="109e6-131">Weitere Informationen finden Sie unter [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="109e6-131">For more information, see [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="109e6-132">**F// \_ nexthopas**</span><span class="sxs-lookup"><span data-stu-id="109e6-132">**FSD\_NextHopAS**</span></span>
</dt> <dd>

<span data-ttu-id="109e6-133">Gibt die autonome System Nummer des nächsten Hops an.</span><span class="sxs-lookup"><span data-stu-id="109e6-133">Specifies the autonomous system number of the next hop.</span></span>

</dd> <dt>

<span data-ttu-id="109e6-134">**F- \_ Priorität**</span><span class="sxs-lookup"><span data-stu-id="109e6-134">**FSD\_Priority**</span></span>
</dt> <dd>

<span data-ttu-id="109e6-135">Gibt einen Metrikwert an.</span><span class="sxs-lookup"><span data-stu-id="109e6-135">Specifies a metric value.</span></span> <span data-ttu-id="109e6-136">Der Routing Tabellen-Manager verwendet diesen Wert, um diesen Routen Eintrag mit Routen Einträgen zu vergleichen, die aus anderen Routing Protokollen abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="109e6-136">The routing table manager uses this value to compare this route entry to route entries obtained from other routing protocols.</span></span> <span data-ttu-id="109e6-137">Der Wert dieses Members wird vom Routing Tabellen-Manager festgelegt.</span><span class="sxs-lookup"><span data-stu-id="109e6-137">The value of this member is set by the routing table manager.</span></span>

</dd> <dt>

<span data-ttu-id="109e6-138">**F- \_ Metrik**</span><span class="sxs-lookup"><span data-stu-id="109e6-138">**FSD\_Metric**</span></span>
</dt> <dd>

<span data-ttu-id="109e6-139">Gibt einen Metrikwert an.</span><span class="sxs-lookup"><span data-stu-id="109e6-139">Specifies a metric value.</span></span> <span data-ttu-id="109e6-140">Der Routing Tabellen-Manager verwendet diesen Wert, um diesen Routen Eintrag mit anderen Routen Einträgen zu vergleichen, die aus demselben Routing Protokoll abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="109e6-140">The routing table manager uses this value to compare this route entry to other route entries obtained from the same routing protocol.</span></span> <span data-ttu-id="109e6-141">Der Wert dieses Members wird durch das Routing Protokoll festgelegt.</span><span class="sxs-lookup"><span data-stu-id="109e6-141">The value of this member is set by the routing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="109e6-142">**\_Metric1**</span><span class="sxs-lookup"><span data-stu-id="109e6-142">**FSD\_Metric1**</span></span>
</dt> <dd>

<span data-ttu-id="109e6-143">Gibt einen Routing Protokoll spezifischen Metrikwert an.</span><span class="sxs-lookup"><span data-stu-id="109e6-143">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="109e6-144">Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="109e6-144">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="109e6-145">**\_Metric2**</span><span class="sxs-lookup"><span data-stu-id="109e6-145">**FSD\_Metric2**</span></span>
</dt> <dd>

<span data-ttu-id="109e6-146">Gibt einen Routing Protokoll spezifischen Metrikwert an.</span><span class="sxs-lookup"><span data-stu-id="109e6-146">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="109e6-147">Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="109e6-147">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="109e6-148">**\_Metric3**</span><span class="sxs-lookup"><span data-stu-id="109e6-148">**FSD\_Metric3**</span></span>
</dt> <dd>

<span data-ttu-id="109e6-149">Gibt einen Routing Protokoll spezifischen Metrikwert an.</span><span class="sxs-lookup"><span data-stu-id="109e6-149">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="109e6-150">Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="109e6-150">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="109e6-151">**\_Metric4**</span><span class="sxs-lookup"><span data-stu-id="109e6-151">**FSD\_Metric4**</span></span>
</dt> <dd>

<span data-ttu-id="109e6-152">Gibt einen Routing Protokoll spezifischen Metrikwert an.</span><span class="sxs-lookup"><span data-stu-id="109e6-152">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="109e6-153">Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="109e6-153">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="109e6-154">**\_Metric5**</span><span class="sxs-lookup"><span data-stu-id="109e6-154">**FSD\_Metric5**</span></span>
</dt> <dd>

<span data-ttu-id="109e6-155">Gibt einen Routing Protokoll spezifischen Metrikwert an.</span><span class="sxs-lookup"><span data-stu-id="109e6-155">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="109e6-156">Dieser Metrikwert ist in [RFC 1354](routing-protocols-request-for-comments.md)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="109e6-156">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="109e6-157">**F- \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="109e6-157">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="109e6-158">Gibt an, ob die Route gültig ist.</span><span class="sxs-lookup"><span data-stu-id="109e6-158">Specifies whether the route is valid.</span></span> <span data-ttu-id="109e6-159">Das Routing Protokoll sollte diese Flags zuerst löschen und dann die Route als gültig oder ungültig festlegen.</span><span class="sxs-lookup"><span data-stu-id="109e6-159">The routing protocol should first clear these flags, then set the route as either valid or invalid.</span></span> <span data-ttu-id="109e6-160">Das Routing Protokoll sollte zum Durchführen dieser Vorgänge die Makros **clearrouteflags ()** **, "", "**", "", "", "", "", "", " **", "** "</span><span class="sxs-lookup"><span data-stu-id="109e6-160">The routing protocol should use the macros **ClearRouteFlags()**, **SetRouteValid()**, and **ClearRouteValid()** to perform these operations.</span></span> <span data-ttu-id="109e6-161">Diese Makros sind in RTM. h definiert.</span><span class="sxs-lookup"><span data-stu-id="109e6-161">These macros are defined in Rtm.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="109e6-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="109e6-162">Remarks</span></span>

<span data-ttu-id="109e6-163">Der Routing Tabellen-Manager verwendet die **FSD- \_ Priorität** und die **FSD- \_ metrikelemente** , um die beste Route zu einem bestimmten Zielnetzwerk zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="109e6-163">The routing table manager uses the **FSD\_Priority** and **FSD\_Metric** members to compute the best route to a particular destination network.</span></span>

<span data-ttu-id="109e6-164">Die **FSD- \_ Metrik \[ 1-5 \]** -Elemente sind für die MIB II-Konformität vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="109e6-164">The **FSD\_Metric\[1-5\]** members are for MIB II conformance.</span></span> <span data-ttu-id="109e6-165">In MIB II-Agents werden nur diese Metrikwerte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="109e6-165">MIB II agents display only these metric values.</span></span> <span data-ttu-id="109e6-166">Der Wert der **SSD \_** -Metrik wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="109e6-166">They do not display the **FSD\_Metric** metric value.</span></span> <span data-ttu-id="109e6-167">Damit die **FSD- \_ Metrik** angezeigt wird, sollte das Routing Protokoll auch den Wert in einem der **FSD- \_ Metrik \[ 1-5 \]** -Elemente speichern.</span><span class="sxs-lookup"><span data-stu-id="109e6-167">To have the **FSD\_Metric** displayed, the routing protocol should also store the value in one of the **FSD\_Metric\[1-5\]** members.</span></span>

<span data-ttu-id="109e6-168">Der Routing Tabellen-Manager verwendet die Metrikwerte in den **FSD- \_ Metrik \[ 1-5 \]** -Membern nicht, wenn die beste Route zu einem Zielnetzwerk berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="109e6-168">The routing table manager does not use the metric values in the **FSD\_Metric\[1-5\]** members when computing the best route to a destination network.</span></span> <span data-ttu-id="109e6-169">Daher sollte das Routing Protokoll sicherstellen, dass das **FSD- \_ metrikelement** über einen entsprechenden Metrikwert verfügt.</span><span class="sxs-lookup"><span data-stu-id="109e6-169">Therefore, the routing protocol should ensure that the **FSD\_Metric** member has an appropriate metric value.</span></span>

<span data-ttu-id="109e6-170">Ein Routing Protokoll könnte mithilfe der **FSD- \_ Flags** eine Route als ungültig markieren, wenn die Route nicht von anderen Routing Protokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="109e6-170">A routing protocol could use the **FSD\_Flags** to mark a route as invalid, if the route should not be used by other routing protocols.</span></span>

## <a name="requirements"></a><span data-ttu-id="109e6-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="109e6-171">Requirements</span></span>



| <span data-ttu-id="109e6-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="109e6-172">Requirement</span></span> | <span data-ttu-id="109e6-173">Wert</span><span class="sxs-lookup"><span data-stu-id="109e6-173">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="109e6-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="109e6-174">Minimum supported client</span></span><br/> | <span data-ttu-id="109e6-175">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="109e6-175">None supported</span></span><br/>                                                        |
| <span data-ttu-id="109e6-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="109e6-176">Minimum supported server</span></span><br/> | <span data-ttu-id="109e6-177">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="109e6-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="109e6-178">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="109e6-178">End of server support</span></span><br/>    | <span data-ttu-id="109e6-179">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="109e6-179">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="109e6-180">Header</span><span class="sxs-lookup"><span data-stu-id="109e6-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="109e6-181"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="109e6-181"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="109e6-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="109e6-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="109e6-183">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="109e6-183">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="109e6-184">Routing Tabellen-Manager, Version 1, Strukturen</span><span class="sxs-lookup"><span data-stu-id="109e6-184">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="109e6-185">**RTM \_ -IP- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="109e6-185">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 






---
description: Gibt die virtuelle Schutz Ebene für einen angegebenen Schutzmechanismus zurück.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347860"
---
# <a name="opm_get_virtual_protection_level"></a><span data-ttu-id="cfbb6-103">OPM \_ - \_ Ebene zum virtuellen \_ Schutz \_</span><span class="sxs-lookup"><span data-stu-id="cfbb6-103">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="cfbb6-104">Gibt die virtuelle Schutz Ebene für einen angegebenen Schutzmechanismus zurück.</span><span class="sxs-lookup"><span data-stu-id="cfbb6-104">Returns the virtual protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="cfbb6-105">Die *virtuelle* Schutz Ebene ist die Ebene, die von der Anwendung während der aktuellen Output Protection Manager-Sitzung (OPM) angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="cfbb6-105">The *virtual* protection level is the level requested by the application during the current Output Protection Manager (OPM) session.</span></span> <span data-ttu-id="cfbb6-106">Der Treiber kann aufgrund von Ereignissen außerhalb dieser OPM-Sitzung eine höhere Ebene anwenden.</span><span class="sxs-lookup"><span data-stu-id="cfbb6-106">The driver might apply a higher level, due to events outside of this OPM session.</span></span> <span data-ttu-id="cfbb6-107">Um die tatsächliche Sicherheitsstufe zu ermitteln, die wirksam ist, senden Sie die OPM-Abfrage zum Abrufen der [**\_ \_ tatsächlichen \_ Schutz \_ Ebene**](opm-get-actual-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="cfbb6-107">To find the actual protection level that is in effect, send the [**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**](opm-get-actual-protection-level.md) query.</span></span>



| <span data-ttu-id="cfbb6-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfbb6-108">Requirement</span></span> | <span data-ttu-id="cfbb6-109">Wert</span><span class="sxs-lookup"><span data-stu-id="cfbb6-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb6-110">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="cfbb6-110">Request GUID</span></span> | <span data-ttu-id="cfbb6-111">OPM \_ - \_ Ebene zum virtuellen \_ Schutz \_</span><span class="sxs-lookup"><span data-stu-id="cfbb6-111">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                          |
| <span data-ttu-id="cfbb6-112">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="cfbb6-112">Input data</span></span>   | <span data-ttu-id="cfbb6-113">Der abzufragende Schutzmechanismus, der als 32-Bit-Ganzzahl angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cfbb6-113">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="cfbb6-114">Der Wert wird als Member der [**OPM-Schutztyp Flags**](opm-protection-type-flags.md)interpretiert.</span><span class="sxs-lookup"><span data-stu-id="cfbb6-114">The value is interpreted as a member of the [**OPM Protection Type Flags**](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="cfbb6-115">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="cfbb6-115">Return data</span></span>  | <span data-ttu-id="cfbb6-116">Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur</span><span class="sxs-lookup"><span data-stu-id="cfbb6-116">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="cfbb6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfbb6-117">Remarks</span></span>

<span data-ttu-id="cfbb6-118">Die Schutz Ebene wird im **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cfbb6-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="cfbb6-119">Die Bedeutung dieses Werts hängt von dem abgefragten Schutzmechanismus ab.</span><span class="sxs-lookup"><span data-stu-id="cfbb6-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="cfbb6-120">Für jeden Schutzmechanismus ist der Wert von **ulinformation** ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cfbb6-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="cfbb6-121">Schutzmechanismus</span><span class="sxs-lookup"><span data-stu-id="cfbb6-121">Protection mechanism</span></span> | <span data-ttu-id="cfbb6-122">Enumeration</span><span class="sxs-lookup"><span data-stu-id="cfbb6-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cfbb6-123">ACP</span><span class="sxs-lookup"><span data-stu-id="cfbb6-123">ACP</span></span>                  | [<span data-ttu-id="cfbb6-124">**OPM \_ -ACP- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="cfbb6-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="cfbb6-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="cfbb6-125">CGMS-A</span></span>               | [<span data-ttu-id="cfbb6-126">**CGMS-A-Schutzflags**</span><span class="sxs-lookup"><span data-stu-id="cfbb6-126">**CGMS-A Protection Flags**</span></span>](cgms-a-protection-flags.md)        |
| <span data-ttu-id="cfbb6-127">Dpcp</span><span class="sxs-lookup"><span data-stu-id="cfbb6-127">DPCP</span></span>                 | [<span data-ttu-id="cfbb6-128">**OPM \_ dpcp- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="cfbb6-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="cfbb6-129">HDCP</span><span class="sxs-lookup"><span data-stu-id="cfbb6-129">HDCP</span></span>                 | [<span data-ttu-id="cfbb6-130">**OPM- \_ HDCP- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="cfbb6-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="cfbb6-131">Diese Abfrage entspricht der DXVA- \_ Abfrage "coppquerylocalschutzlevel", die im Certified Output Protection Protocol (COPP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cfbb6-131">This query is equivalent to the DXVA\_COPPQueryLocalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbb6-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfbb6-132">Requirements</span></span>



| <span data-ttu-id="cfbb6-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfbb6-133">Requirement</span></span> | <span data-ttu-id="cfbb6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="cfbb6-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb6-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfbb6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cfbb6-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfbb6-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cfbb6-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfbb6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cfbb6-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfbb6-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cfbb6-139">Header</span><span class="sxs-lookup"><span data-stu-id="cfbb6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfbb6-140"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfbb6-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbb6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfbb6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbb6-142">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="cfbb6-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="cfbb6-143">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="cfbb6-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="cfbb6-144">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfbb6-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 





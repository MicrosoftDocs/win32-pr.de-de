---
description: Gibt die globale Schutz Ebene für einen angegebenen Schutzmechanismus zurück.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041903"
---
# <a name="opm_get_actual_protection_level"></a><span data-ttu-id="37fb9-103">OPM \_ get \_ Actual \_ Protection \_ Level</span><span class="sxs-lookup"><span data-stu-id="37fb9-103">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="37fb9-104">Gibt die globale Schutz Ebene für einen angegebenen Schutzmechanismus zurück.</span><span class="sxs-lookup"><span data-stu-id="37fb9-104">Returns the global protection level for a specified protection mechanism.</span></span>



| <span data-ttu-id="37fb9-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37fb9-105">Requirement</span></span> | <span data-ttu-id="37fb9-106">Wert</span><span class="sxs-lookup"><span data-stu-id="37fb9-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37fb9-107">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="37fb9-107">Request GUID</span></span> | <span data-ttu-id="37fb9-108">OPM \_ get \_ Actual \_ Protection \_ Level</span><span class="sxs-lookup"><span data-stu-id="37fb9-108">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                       |
| <span data-ttu-id="37fb9-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="37fb9-109">Input data</span></span>   | <span data-ttu-id="37fb9-110">Der abzufragende Schutzmechanismus, der als 32-Bit-Ganzzahl angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="37fb9-110">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="37fb9-111">Der Wert wird als Member der [OPM-Schutztyp Flags](opm-protection-type-flags.md)interpretiert.</span><span class="sxs-lookup"><span data-stu-id="37fb9-111">The value is interpreted as a member of the [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="37fb9-112">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="37fb9-112">Return data</span></span>  | <span data-ttu-id="37fb9-113">Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur</span><span class="sxs-lookup"><span data-stu-id="37fb9-113">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="37fb9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37fb9-114">Remarks</span></span>

<span data-ttu-id="37fb9-115">Die globale Schutz Ebene ist die Schutz Ebene, die zurzeit auf den Connector angewendet wird, unabhängig davon, wie der Grafiktreiber angewiesen wurde, den Schutz anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="37fb9-115">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="37fb9-116">Beispielsweise kann eine Anwendung die ACP-Schutz Ebene durch Aufrufen der **changedisplaysettingsex** -Funktion festlegen.</span><span class="sxs-lookup"><span data-stu-id="37fb9-116">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="37fb9-117">In diesem Fall würde die globale Schutz Ebene diese Einstellung widerspiegeln, auch wenn Sie nicht durch Output Protection Manager (OPM) angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="37fb9-117">In that case, the global protection level would reflect this setting, even though it was not requested through Output Protection Manager (OPM).</span></span>

<span data-ttu-id="37fb9-118">Die Schutz Ebene wird im **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37fb9-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="37fb9-119">Die Bedeutung dieses Werts hängt von dem abgefragten Schutzmechanismus ab.</span><span class="sxs-lookup"><span data-stu-id="37fb9-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="37fb9-120">Für jeden Schutzmechanismus ist der Wert von **ulinformation** ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="37fb9-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="37fb9-121">Schutzmechanismus</span><span class="sxs-lookup"><span data-stu-id="37fb9-121">Protection mechanism</span></span> | <span data-ttu-id="37fb9-122">Enumeration</span><span class="sxs-lookup"><span data-stu-id="37fb9-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="37fb9-123">ACP</span><span class="sxs-lookup"><span data-stu-id="37fb9-123">ACP</span></span>                  | [<span data-ttu-id="37fb9-124">**OPM \_ -ACP- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="37fb9-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="37fb9-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="37fb9-125">CGMS-A</span></span>               | [<span data-ttu-id="37fb9-126">CGMS-A-Schutzflags</span><span class="sxs-lookup"><span data-stu-id="37fb9-126">CGMS-A Protection Flags</span></span>](cgms-a-protection-flags.md)            |
| <span data-ttu-id="37fb9-127">Dpcp</span><span class="sxs-lookup"><span data-stu-id="37fb9-127">DPCP</span></span>                 | [<span data-ttu-id="37fb9-128">**OPM \_ dpcp- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="37fb9-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="37fb9-129">HDCP</span><span class="sxs-lookup"><span data-stu-id="37fb9-129">HDCP</span></span>                 | [<span data-ttu-id="37fb9-130">**OPM- \_ HDCP- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="37fb9-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="37fb9-131">Diese Abfrage entspricht der DXVA- \_ Abfrage "coppqueryglobalschutzlevel", die im Certified Output Protection Protocol (COPP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37fb9-131">This query is equivalent to the DXVA\_COPPQueryGlobalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="37fb9-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37fb9-132">Requirements</span></span>



| <span data-ttu-id="37fb9-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37fb9-133">Requirement</span></span> | <span data-ttu-id="37fb9-134">Wert</span><span class="sxs-lookup"><span data-stu-id="37fb9-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="37fb9-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37fb9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="37fb9-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37fb9-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="37fb9-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37fb9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="37fb9-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37fb9-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="37fb9-139">Header</span><span class="sxs-lookup"><span data-stu-id="37fb9-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="37fb9-140"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="37fb9-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37fb9-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37fb9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37fb9-142">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="37fb9-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="37fb9-143">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="37fb9-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="37fb9-144">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37fb9-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 





---
description: 'Weitere Informationen finden Sie hier: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355566"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a><span data-ttu-id="a182a-103">OPM \_ get \_ ACP \_ und \_ cgmsa- \_ Signalisierung</span><span class="sxs-lookup"><span data-stu-id="a182a-103">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="a182a-104">Gibt die folgenden Informationen zu einer Videoausgabe zurück:</span><span class="sxs-lookup"><span data-stu-id="a182a-104">Returns the following information about a video output:</span></span>

-   <span data-ttu-id="a182a-105">Eine Liste der vom Treiber unterstützten TV-Schutzstandards.</span><span class="sxs-lookup"><span data-stu-id="a182a-105">A list of television protection standards supported by the driver.</span></span>
-   <span data-ttu-id="a182a-106">Der Standard, der derzeit aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="a182a-106">The standard that is currently active.</span></span>
-   <span data-ttu-id="a182a-107">Das aktuelle Seitenverhältnis oder andere Signalisierungs Daten.</span><span class="sxs-lookup"><span data-stu-id="a182a-107">The current aspect ratio or other signaling data.</span></span>



| <span data-ttu-id="a182a-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a182a-108">Requirement</span></span> | <span data-ttu-id="a182a-109">Wert</span><span class="sxs-lookup"><span data-stu-id="a182a-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a182a-110">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="a182a-110">Request GUID</span></span> | <span data-ttu-id="a182a-111">OPM \_ get \_ ACP \_ und \_ cgmsa- \_ Signalisierung</span><span class="sxs-lookup"><span data-stu-id="a182a-111">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                |
| <span data-ttu-id="a182a-112">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="a182a-112">Input data</span></span>   | <span data-ttu-id="a182a-113">Keine</span><span class="sxs-lookup"><span data-stu-id="a182a-113">None</span></span>                                                                                |
| <span data-ttu-id="a182a-114">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="a182a-114">Return data</span></span>  | <span data-ttu-id="a182a-115">Eine [**OPM \_ -ACP- \_ und \_ cgmsa- \_ Signal**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) Struktur</span><span class="sxs-lookup"><span data-stu-id="a182a-115">An [**OPM\_ACP\_AND\_CGMSA\_SIGNALING**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a182a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a182a-116">Remarks</span></span>

<span data-ttu-id="a182a-117">Diese Abfrage entspricht der DXVA-Option " \_ coppquerysigna", die im Certified Output Protection Protocol (COPP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a182a-117">This query is equivalent to the DXVA\_COPPQuerySignaling query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="a182a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a182a-118">Requirements</span></span>



| <span data-ttu-id="a182a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a182a-119">Requirement</span></span> | <span data-ttu-id="a182a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a182a-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a182a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a182a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a182a-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a182a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a182a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a182a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a182a-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a182a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a182a-125">Header</span><span class="sxs-lookup"><span data-stu-id="a182a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a182a-126"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a182a-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a182a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a182a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a182a-128">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="a182a-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="a182a-129">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="a182a-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="a182a-130">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a182a-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 





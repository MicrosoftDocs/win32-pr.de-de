---
description: Gibt die Liste der Schutzmechanismen zurück, die vom Connector unterstützt werden.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc79b33673e34d00914b84165d915baa0d8f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959233"
---
# <a name="opm_get_supported_protection_types"></a><span data-ttu-id="cbe19-103">OPM \_ - \_ unterstützte \_ Schutz \_ Typen erhalten</span><span class="sxs-lookup"><span data-stu-id="cbe19-103">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>

<span data-ttu-id="cbe19-104">Gibt die Liste der Schutzmechanismen zurück, die vom Connector unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cbe19-104">Returns the list of protection mechanisms that are supported by the connector.</span></span>



| <span data-ttu-id="cbe19-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbe19-105">Requirement</span></span> | <span data-ttu-id="cbe19-106">Wert</span><span class="sxs-lookup"><span data-stu-id="cbe19-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="cbe19-107">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="cbe19-107">Request GUID</span></span> | <span data-ttu-id="cbe19-108">OPM \_ - \_ unterstützte \_ Schutz \_ Typen erhalten</span><span class="sxs-lookup"><span data-stu-id="cbe19-108">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>                                      |
| <span data-ttu-id="cbe19-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="cbe19-109">Input data</span></span>   | <span data-ttu-id="cbe19-110">Keine</span><span class="sxs-lookup"><span data-stu-id="cbe19-110">None</span></span>                                                                        |
| <span data-ttu-id="cbe19-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="cbe19-111">Return data</span></span>  | <span data-ttu-id="cbe19-112">Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur</span><span class="sxs-lookup"><span data-stu-id="cbe19-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cbe19-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbe19-113">Remarks</span></span>

<span data-ttu-id="cbe19-114">Die Schutzmechanismen werden im **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbe19-114">The protection mechanisms are returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="cbe19-115">Der Wert ist ein bitweiser **or** - [Typ von OPM-Schutztyp Flags](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="cbe19-115">The value is a bitwise **OR** of [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span>

<span data-ttu-id="cbe19-116">Diese Abfrage entspricht der DXVA- \_ Abfrage "coppqueryschutztype", die im Certified Output Protection Protocol (COPP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cbe19-116">This query is equivalent to the DXVA\_COPPQueryProtectionType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbe19-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbe19-117">Requirements</span></span>



| <span data-ttu-id="cbe19-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbe19-118">Requirement</span></span> | <span data-ttu-id="cbe19-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cbe19-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe19-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbe19-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cbe19-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbe19-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cbe19-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbe19-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cbe19-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbe19-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cbe19-124">Header</span><span class="sxs-lookup"><span data-stu-id="cbe19-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbe19-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbe19-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbe19-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbe19-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe19-127">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="cbe19-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="cbe19-128">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="cbe19-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="cbe19-129">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbe19-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 





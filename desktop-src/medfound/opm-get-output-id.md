---
description: Gibt den eindeutigen Bezeichner des Monitors zurück, der mit dieser Videoausgabe verknüpft ist.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347031"
---
# <a name="opm_get_output_id"></a><span data-ttu-id="22721-103">OPM \_ - \_ Ausgabe- \_ ID erhalten</span><span class="sxs-lookup"><span data-stu-id="22721-103">OPM\_GET\_OUTPUT\_ID</span></span>

<span data-ttu-id="22721-104">Gibt den eindeutigen Bezeichner des Monitors zurück, der mit dieser Videoausgabe verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="22721-104">Returns the unique identifier of the monitor associated with this video output.</span></span>



| <span data-ttu-id="22721-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22721-105">Requirement</span></span> | <span data-ttu-id="22721-106">Wert</span><span class="sxs-lookup"><span data-stu-id="22721-106">Value</span></span> |
|--------------|------------------------------------------------------------------|
| <span data-ttu-id="22721-107">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="22721-107">Request GUID</span></span> | <span data-ttu-id="22721-108">OPM \_ - \_ Ausgabe- \_ ID erhalten</span><span class="sxs-lookup"><span data-stu-id="22721-108">OPM\_GET\_OUTPUT\_ID</span></span>                                             |
| <span data-ttu-id="22721-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="22721-109">Input data</span></span>   | <span data-ttu-id="22721-110">Keine</span><span class="sxs-lookup"><span data-stu-id="22721-110">None</span></span>                                                             |
| <span data-ttu-id="22721-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="22721-111">Return data</span></span>  | <span data-ttu-id="22721-112">Eine [**OPM- \_ Ausgabe- \_ ID- \_ Daten**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) Struktur</span><span class="sxs-lookup"><span data-stu-id="22721-112">An [**OPM\_OUTPUT\_ID\_DATA**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="22721-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22721-113">Remarks</span></span>

<span data-ttu-id="22721-114">Der Videotreiber weist jedem Monitor einen eindeutigen Bezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="22721-114">The video driver assigns a unique identifier to each monitor.</span></span> <span data-ttu-id="22721-115">Diese Abfrage gibt den Bezeichner für den Monitor zurück, der dem aktuellen [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Zeiger zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="22721-115">This query returns the identifier for the monitor that is associated with the current [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="22721-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22721-116">Requirements</span></span>



| <span data-ttu-id="22721-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22721-117">Requirement</span></span> | <span data-ttu-id="22721-118">Wert</span><span class="sxs-lookup"><span data-stu-id="22721-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="22721-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22721-119">Minimum supported client</span></span><br/> | <span data-ttu-id="22721-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22721-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="22721-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22721-121">Minimum supported server</span></span><br/> | <span data-ttu-id="22721-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22721-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="22721-123">Header</span><span class="sxs-lookup"><span data-stu-id="22721-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="22721-124"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="22721-124"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22721-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22721-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22721-126">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="22721-126">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="22721-127">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22721-127">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 





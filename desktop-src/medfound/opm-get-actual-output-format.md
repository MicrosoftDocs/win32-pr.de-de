---
description: Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344419"
---
# <a name="opm_get_actual_output_format"></a><span data-ttu-id="048a8-103">OPM \_ get \_ tatsächliches \_ Ausgabe \_ Format</span><span class="sxs-lookup"><span data-stu-id="048a8-103">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>

<span data-ttu-id="048a8-104">Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="048a8-104">Returns a description of the video signal that is being transmitted over the connector.</span></span>



| <span data-ttu-id="048a8-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="048a8-105">Requirement</span></span> | <span data-ttu-id="048a8-106">Wert</span><span class="sxs-lookup"><span data-stu-id="048a8-106">Value</span></span> |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="048a8-107">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="048a8-107">Request GUID</span></span> | <span data-ttu-id="048a8-108">OPM \_ get \_ tatsächliches \_ Ausgabe \_ Format</span><span class="sxs-lookup"><span data-stu-id="048a8-108">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>                                             |
| <span data-ttu-id="048a8-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="048a8-109">Input data</span></span>   | <span data-ttu-id="048a8-110">Keine</span><span class="sxs-lookup"><span data-stu-id="048a8-110">None</span></span>                                                                         |
| <span data-ttu-id="048a8-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="048a8-111">Return data</span></span>  | <span data-ttu-id="048a8-112">Eine [**tatsächliche OPM- \_ \_ Ausgabe \_ Format**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) Struktur</span><span class="sxs-lookup"><span data-stu-id="048a8-112">An [**OPM\_ACTUAL\_OUTPUT\_FORMAT**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="048a8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="048a8-113">Remarks</span></span>

<span data-ttu-id="048a8-114">Das über den Connector übertragene Videosignal weist nicht notwendigerweise dasselbe Format wie der Desktop Anzeigemodus auf.</span><span class="sxs-lookup"><span data-stu-id="048a8-114">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="048a8-115">Beispielsweise kann der Desktop Anzeigemodus 1024 x 768 Pixel bei 85 Hz sein, während der Connector ein S-Video-Connector sein kann, der ein Videosignal mit 720 x 480 Pixel, 60/1.01 Hz-Zeilen Sprung überträgt.</span><span class="sxs-lookup"><span data-stu-id="048a8-115">For example, the desktop display mode might be 1024 x 768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720 x 480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="048a8-116">In diesem Fall würde der Treiber die Auflösung des S-Video Signals und nicht die Desktop Auflösung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="048a8-116">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

<span data-ttu-id="048a8-117">Diese Abfrage entspricht der DXVA- \_ Abfrage "coppquerydisplaydata", die im Certified Output Protection Protocol (COPP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="048a8-117">This query is equivalent to the DXVA\_COPPQueryDisplayData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="048a8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="048a8-118">Requirements</span></span>



| <span data-ttu-id="048a8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="048a8-119">Requirement</span></span> | <span data-ttu-id="048a8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="048a8-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="048a8-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="048a8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="048a8-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="048a8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="048a8-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="048a8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="048a8-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="048a8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="048a8-125">Header</span><span class="sxs-lookup"><span data-stu-id="048a8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="048a8-126"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="048a8-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="048a8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="048a8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="048a8-128">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="048a8-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="048a8-129">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="048a8-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="048a8-130">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="048a8-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 





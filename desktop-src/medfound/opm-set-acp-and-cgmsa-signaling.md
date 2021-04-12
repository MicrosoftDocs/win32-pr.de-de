---
description: Gibt Informationen über das Videosignal außer der Schutz Ebene an.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527875"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a><span data-ttu-id="b5121-103">OPM \_ Set \_ ACP \_ und \_ cgmsa \_ Signalisierung</span><span class="sxs-lookup"><span data-stu-id="b5121-103">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="b5121-104">Gibt Informationen über das Videosignal außer der Schutz Ebene an.</span><span class="sxs-lookup"><span data-stu-id="b5121-104">Specifies information about the video signal, other than the protection level.</span></span>



| <span data-ttu-id="b5121-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5121-105">Requirement</span></span> | <span data-ttu-id="b5121-106">Wert</span><span class="sxs-lookup"><span data-stu-id="b5121-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5121-107">Befehls-GUID</span><span class="sxs-lookup"><span data-stu-id="b5121-107">Command GUID</span></span> | <span data-ttu-id="b5121-108">OPM \_ Set \_ ACP \_ und \_ cgmsa \_ Signalisierung</span><span class="sxs-lookup"><span data-stu-id="b5121-108">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                                                |
| <span data-ttu-id="b5121-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="b5121-109">Input data</span></span>   | <span data-ttu-id="b5121-110">Eine [**OPM \_ \_ -Set ACP- \_ und \_ cgmsa- \_ Signalisierungs \_ Parameter-**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) Struktur</span><span class="sxs-lookup"><span data-stu-id="b5121-110">An [**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b5121-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5121-111">Remarks</span></span>

<span data-ttu-id="b5121-112">Dieser Befehl entspricht dem DXVA-Befehl "", der \_ im Certified Output Protection Protocol (COPP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b5121-112">This command is equivalent to the DXVA\_COPPSetSignaling command used in Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="b5121-113">Für CGMS-a erfordern bestimmte Schutzstandards, dass das Fernsehsignal Informationen in denselben VBI-Wellenform-Paketen wie die CGMS-a-Bits enthält.</span><span class="sxs-lookup"><span data-stu-id="b5121-113">For CGMS-A, certain protection standards require that the television signal contain information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="b5121-114">Unter anderem umfasst diese Informationen das Seitenverhältnis des Bilds.</span><span class="sxs-lookup"><span data-stu-id="b5121-114">Among other things, this information includes the picture aspect ratio.</span></span> <span data-ttu-id="b5121-115">Fernsehgeräte können schlecht angezeigt werden, wenn die Seitenverhältnis Informationen nicht mit dem Videostream konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="b5121-115">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="b5121-116">Die Anwendung kann diesen Befehl verwenden, um das Seitenverhältnis anzugeben, damit der Grafiktreiber die richtigen VBI-Pakete generieren kann.</span><span class="sxs-lookup"><span data-stu-id="b5121-116">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5121-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5121-117">Requirements</span></span>



| <span data-ttu-id="b5121-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5121-118">Requirement</span></span> | <span data-ttu-id="b5121-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b5121-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b5121-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5121-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b5121-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5121-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b5121-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5121-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b5121-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5121-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b5121-124">Header</span><span class="sxs-lookup"><span data-stu-id="b5121-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5121-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5121-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5121-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5121-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5121-127">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="b5121-127">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="b5121-128">OPM-Befehle</span><span class="sxs-lookup"><span data-stu-id="b5121-128">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 





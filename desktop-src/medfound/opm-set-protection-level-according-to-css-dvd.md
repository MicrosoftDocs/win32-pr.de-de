---
description: Legt die HDCP-Schutz Ebene für die DVD-Wiedergabe fest, und zwar gemäß den DVD-Inhalts Regeln für das Scramble-System
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130493"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a><span data-ttu-id="33f70-103">OPM \_ Festlegen der \_ Schutz \_ Ebene \_ gemäß CSS- \_ \_ \_ DVD</span><span class="sxs-lookup"><span data-stu-id="33f70-103">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>

<span data-ttu-id="33f70-104">Legt die HDCP-Schutz Ebene für die DVD-Wiedergabe fest, und zwar gemäß den DVD-Inhalts Regeln für das Scramble-System</span><span class="sxs-lookup"><span data-stu-id="33f70-104">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span>



| <span data-ttu-id="33f70-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33f70-105">Requirement</span></span> | <span data-ttu-id="33f70-106">Wert</span><span class="sxs-lookup"><span data-stu-id="33f70-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33f70-107">Befehls-GUID</span><span class="sxs-lookup"><span data-stu-id="33f70-107">Command GUID</span></span> | <span data-ttu-id="33f70-108">OPM \_ Festlegen der \_ Schutz \_ Ebene \_ gemäß CSS- \_ \_ \_ DVD</span><span class="sxs-lookup"><span data-stu-id="33f70-108">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>                                                |
| <span data-ttu-id="33f70-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="33f70-109">Input data</span></span>   | <span data-ttu-id="33f70-110">Eine [**OPM-Parameter Struktur zum \_ Festlegen der \_ Schutz \_ Ebenen \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="33f70-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="33f70-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33f70-111">Remarks</span></span>

<span data-ttu-id="33f70-112">Dieser Befehl wird verwendet, um bei der Wiedergabe von Standard-DVDs High-Bandwidth Digital Content Protection (HDCP) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="33f70-112">This command is used to set High-Bandwidth Digital Content Protection (HDCP) when playing standard DVDs.</span></span> <span data-ttu-id="33f70-113">Anders als beim OPM-Befehl zum [**\_ Festlegen der \_ Schutz \_ Ebene**](opm-set-protection-level.md) , wenn HDCP aus irgendeinem Grund nicht festgelegt werden kann, wird die Wiedergabe durch diesen Befehl nicht beendet.</span><span class="sxs-lookup"><span data-stu-id="33f70-113">Unlike the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command, if HDCP cannot be set for some reason, this command does not stop playback.</span></span> <span data-ttu-id="33f70-114">(DVD-CSS-Regeln enthalten eine "bestmögliche" Bereitstellung für Player.) Andernfalls ist dieser Befehl mit dem OPM-Befehl zum **\_ Festlegen der \_ Schutz \_ Ebene** identisch.</span><span class="sxs-lookup"><span data-stu-id="33f70-114">(DVD CSS rules contain a "best effort" provision for players.) Otherwise, this command is identical to the **OPM\_SET\_PROTECTION\_LEVEL** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="33f70-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33f70-115">Requirements</span></span>



| <span data-ttu-id="33f70-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33f70-116">Requirement</span></span> | <span data-ttu-id="33f70-117">Wert</span><span class="sxs-lookup"><span data-stu-id="33f70-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="33f70-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33f70-118">Minimum supported client</span></span><br/> | <span data-ttu-id="33f70-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33f70-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="33f70-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33f70-120">Minimum supported server</span></span><br/> | <span data-ttu-id="33f70-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33f70-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="33f70-122">Header</span><span class="sxs-lookup"><span data-stu-id="33f70-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="33f70-123"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="33f70-123"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33f70-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33f70-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f70-125">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="33f70-125">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="33f70-126">OPM-Befehle</span><span class="sxs-lookup"><span data-stu-id="33f70-126">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 





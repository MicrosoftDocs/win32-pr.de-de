---
description: Legt die Schutz Ebene für einen ausgabeschutzmechanismus fest.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM_SET_PROTECTION_LEVEL (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348259"
---
# <a name="opm_set_protection_level"></a><span data-ttu-id="6b4de-103">OPM \_ - \_ Schutz \_ Ebene festlegen</span><span class="sxs-lookup"><span data-stu-id="6b4de-103">OPM\_SET\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="6b4de-104">Legt die Schutz Ebene für einen ausgabeschutzmechanismus fest.</span><span class="sxs-lookup"><span data-stu-id="6b4de-104">Sets the protection level for an output protection mechanism.</span></span>



| <span data-ttu-id="6b4de-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b4de-105">Requirement</span></span> | <span data-ttu-id="6b4de-106">Wert</span><span class="sxs-lookup"><span data-stu-id="6b4de-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b4de-107">Befehls-GUID</span><span class="sxs-lookup"><span data-stu-id="6b4de-107">Command GUID</span></span> | <span data-ttu-id="6b4de-108">OPM \_ - \_ Schutz \_ Ebene festlegen</span><span class="sxs-lookup"><span data-stu-id="6b4de-108">OPM\_SET\_PROTECTION\_LEVEL</span></span>                                                                         |
| <span data-ttu-id="6b4de-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="6b4de-109">Input data</span></span>   | <span data-ttu-id="6b4de-110">Eine [**OPM-Parameter Struktur zum \_ Festlegen der \_ Schutz \_ Ebenen \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="6b4de-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6b4de-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b4de-111">Remarks</span></span>

<span data-ttu-id="6b4de-112">Einige Connectors können mehrere Schutzmechanismen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6b4de-112">Some connectors can support multiple protection mechanisms.</span></span> <span data-ttu-id="6b4de-113">Mit diesem Verbindungstyp können Sie mehrere Schutzmechanismen auf denselben Connector anwenden, wobei jeweils jeweils jeweils eine Einstellung unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="6b4de-113">With that type of connector, you can apply several protection mechanisms to the same connector, with different settings for each.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b4de-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b4de-114">Requirements</span></span>



| <span data-ttu-id="6b4de-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b4de-115">Requirement</span></span> | <span data-ttu-id="6b4de-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6b4de-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6b4de-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b4de-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6b4de-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b4de-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6b4de-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b4de-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6b4de-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b4de-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6b4de-121">Header</span><span class="sxs-lookup"><span data-stu-id="6b4de-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b4de-122"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b4de-122"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b4de-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b4de-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b4de-124">**IOPMVideoOutput:: Configure**</span><span class="sxs-lookup"><span data-stu-id="6b4de-124">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="6b4de-125">OPM-Befehle</span><span class="sxs-lookup"><span data-stu-id="6b4de-125">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 





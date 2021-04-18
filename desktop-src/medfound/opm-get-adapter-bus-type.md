---
description: Gibt den Typ des e/a-Busses zurück, der von der Videoausgabe verwendet wird.
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: OPM_GET_ADAPTER_BUS_TYPE (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde3611eb00977670c59c4326f793c1cb9037fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347272"
---
# <a name="opm_get_adapter_bus_type"></a><span data-ttu-id="953c6-103">OPM \_ get \_ Adapter \_ \_ Bustyp</span><span class="sxs-lookup"><span data-stu-id="953c6-103">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>

<span data-ttu-id="953c6-104">Gibt den Typ des e/a-Busses zurück, der von der Videoausgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="953c6-104">Returns the type of I/O bus used by the video output.</span></span>



| <span data-ttu-id="953c6-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="953c6-105">Requirement</span></span> | <span data-ttu-id="953c6-106">Wert</span><span class="sxs-lookup"><span data-stu-id="953c6-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="953c6-107">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="953c6-107">Request GUID</span></span> | <span data-ttu-id="953c6-108">OPM \_ get \_ Adapter \_ \_ Bustyp</span><span class="sxs-lookup"><span data-stu-id="953c6-108">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>                                                |
| <span data-ttu-id="953c6-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="953c6-109">Input data</span></span>   | <span data-ttu-id="953c6-110">Keine</span><span class="sxs-lookup"><span data-stu-id="953c6-110">None</span></span>                                                                        |
| <span data-ttu-id="953c6-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="953c6-111">Return data</span></span>  | <span data-ttu-id="953c6-112">Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur</span><span class="sxs-lookup"><span data-stu-id="953c6-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="953c6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="953c6-113">Remarks</span></span>

<span data-ttu-id="953c6-114">Der Bustyp wird im **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="953c6-114">The bus type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="953c6-115">Der Wert ist ein bitweises **or** von [**OPM-bustyps**](opm-bus-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="953c6-115">The value is a bitwise **OR** of [**OPM Bus Type Flags**](opm-bus-type-flags.md).</span></span>

<span data-ttu-id="953c6-116">Diese Abfrage entspricht der DXVA- \_ Abfrage "coppquerybusdata", die im Certified Output Protection Protocol (COPP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="953c6-116">This query is equivalent to the DXVA\_COPPQueryBusData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="953c6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="953c6-117">Requirements</span></span>



| <span data-ttu-id="953c6-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="953c6-118">Requirement</span></span> | <span data-ttu-id="953c6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="953c6-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="953c6-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="953c6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="953c6-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="953c6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="953c6-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="953c6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="953c6-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="953c6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="953c6-124">Header</span><span class="sxs-lookup"><span data-stu-id="953c6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="953c6-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="953c6-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="953c6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="953c6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="953c6-127">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="953c6-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="953c6-128">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="953c6-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="953c6-129">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="953c6-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 





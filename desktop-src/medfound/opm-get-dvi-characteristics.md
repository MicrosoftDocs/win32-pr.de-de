---
description: Fragt ab, ob ein DVI-Connector (Digital Video Interface) die DVI-Version 1,1 oder höher unterstützt.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041901"
---
# <a name="opm_get_dvi_characteristics"></a><span data-ttu-id="c52f1-103">OPM- \_ get- \_ DVI- \_ Merkmale</span><span class="sxs-lookup"><span data-stu-id="c52f1-103">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>

<span data-ttu-id="c52f1-104">Fragt ab, ob ein DVI-Connector (Digital Video Interface) die DVI-Version 1,1 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c52f1-104">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>



| <span data-ttu-id="c52f1-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c52f1-105">Requirement</span></span> | <span data-ttu-id="c52f1-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c52f1-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="c52f1-107">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="c52f1-107">Request GUID</span></span> | <span data-ttu-id="c52f1-108">OPM- \_ get- \_ DVI- \_ Merkmale</span><span class="sxs-lookup"><span data-stu-id="c52f1-108">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>                                              |
| <span data-ttu-id="c52f1-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="c52f1-109">Input data</span></span>   | <span data-ttu-id="c52f1-110">Keine</span><span class="sxs-lookup"><span data-stu-id="c52f1-110">None</span></span>                                                                        |
| <span data-ttu-id="c52f1-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="c52f1-111">Return data</span></span>  | <span data-ttu-id="c52f1-112">Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur</span><span class="sxs-lookup"><span data-stu-id="c52f1-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c52f1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c52f1-113">Remarks</span></span>

<span data-ttu-id="c52f1-114">Wenn diese Abfrage erfolgreich ist, enthält der **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="c52f1-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains one of the following values.</span></span>



| <span data-ttu-id="c52f1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c52f1-115">Value</span></span>                                     | <span data-ttu-id="c52f1-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c52f1-116">Description</span></span>               |
|-------------------------------------------|---------------------------|
| <span data-ttu-id="c52f1-117">OPM- \_ DVI- \_ Merkmal \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c52f1-117">OPM\_DVI\_CHARACTERISTIC\_1\_0</span></span>            | <span data-ttu-id="c52f1-118">DVI-Version 1,0.</span><span class="sxs-lookup"><span data-stu-id="c52f1-118">DVI version 1.0.</span></span>          |
| <span data-ttu-id="c52f1-119">OPM- \_ DVI- \_ Merkmal \_ 1 \_ 1 \_ oder \_ höher</span><span class="sxs-lookup"><span data-stu-id="c52f1-119">OPM\_DVI\_CHARACTERISTIC\_1\_1\_OR\_ABOVE</span></span> | <span data-ttu-id="c52f1-120">DVI-Version 1,1 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c52f1-120">DVI version 1.1 or later.</span></span> |



 

<span data-ttu-id="c52f1-121">Diese Abfrage wird nur unterstützt, wenn der Typ des physischen Connector der OPM- \_ Connector ist \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c52f1-121">This query is supported only when the physical connector type is OPM\_CONNECTOR\_TYPE\_DVI.</span></span> <span data-ttu-id="c52f1-122">Um den Verbindungstyp zu erhalten, senden Sie die Abfrage " [**OPM \_ get \_ Connector \_ Type**](opm-get-connector-type.md) ".</span><span class="sxs-lookup"><span data-stu-id="c52f1-122">To get the connector type, send the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) query.</span></span>

## <a name="requirements"></a><span data-ttu-id="c52f1-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c52f1-123">Requirements</span></span>



| <span data-ttu-id="c52f1-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c52f1-124">Requirement</span></span> | <span data-ttu-id="c52f1-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c52f1-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c52f1-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c52f1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c52f1-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c52f1-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c52f1-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c52f1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c52f1-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c52f1-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c52f1-130">Header</span><span class="sxs-lookup"><span data-stu-id="c52f1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c52f1-131"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c52f1-131"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c52f1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c52f1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c52f1-133">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="c52f1-133">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="c52f1-134">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c52f1-134">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 





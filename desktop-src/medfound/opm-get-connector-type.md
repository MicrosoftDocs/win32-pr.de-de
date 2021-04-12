---
description: Gibt den physischen Verbindungstyp der Videoausgabe zurück.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215027"
---
# <a name="opm_get_connector_type"></a><span data-ttu-id="5e768-103">OPM \_ get \_ Connector- \_ Typ</span><span class="sxs-lookup"><span data-stu-id="5e768-103">OPM\_GET\_CONNECTOR\_TYPE</span></span>

<span data-ttu-id="5e768-104">Gibt den physischen Verbindungstyp der Videoausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="5e768-104">Returns the physical connector type of the video output.</span></span>



| <span data-ttu-id="5e768-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e768-105">Requirement</span></span> | <span data-ttu-id="5e768-106">Wert</span><span class="sxs-lookup"><span data-stu-id="5e768-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5e768-107">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="5e768-107">Request GUID</span></span> | <span data-ttu-id="5e768-108">OPM \_ get \_ Connector- \_ Typ</span><span class="sxs-lookup"><span data-stu-id="5e768-108">OPM\_GET\_CONNECTOR\_TYPE</span></span>                                                   |
| <span data-ttu-id="5e768-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="5e768-109">Input data</span></span>   | <span data-ttu-id="5e768-110">Keine</span><span class="sxs-lookup"><span data-stu-id="5e768-110">None</span></span>                                                                        |
| <span data-ttu-id="5e768-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="5e768-111">Return data</span></span>  | <span data-ttu-id="5e768-112">Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur</span><span class="sxs-lookup"><span data-stu-id="5e768-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5e768-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e768-113">Remarks</span></span>

<span data-ttu-id="5e768-114">Der Verbindungstyp wird im **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e768-114">The connector type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="5e768-115">Der Wert von **ulinformation** ist gleich einem der Connector-Typen, die in [**OPM-Connector-Typflags**](opm-connector-type-flags.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5e768-115">The value of **ulInformation** is equal to one of the connector types listed in [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="5e768-116">Im COPP-Emulations Modus kann der Verbindungstyp mit dem **internen OPM- \_ \_ \_ \_ Kopiertyp \_** -Flag kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="5e768-116">In COPP emulation mode, the connector type might be combined with the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="5e768-117">Verwenden Sie ein bitweises **and-** Element, um den Verbindungstyp zu extrahieren:</span><span class="sxs-lookup"><span data-stu-id="5e768-117">Use a bitwise **AND** to extract the connector type:</span></span>

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

<span data-ttu-id="5e768-118">Anwendungen sollten das interne Flag " **OPM \_ COPP \_ Compatible \_ Connector \_ Type \_** " ignorieren.</span><span class="sxs-lookup"><span data-stu-id="5e768-118">Applications should ignore the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="5e768-119">Weitere Informationen finden Sie im Abschnitt "Hinweise" der [**OPM-Connector-Typflags**](opm-connector-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5e768-119">For more information, see the Remarks section of [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="5e768-120">Diese Abfrage entspricht der DXVA- \_ Abfrage "coppqueryconnector Type", die im Certified Output Protection Protocol (COPP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e768-120">This query is equivalent to the DXVA\_COPPQueryConnectorType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e768-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e768-121">Requirements</span></span>



| <span data-ttu-id="5e768-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e768-122">Requirement</span></span> | <span data-ttu-id="5e768-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5e768-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5e768-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e768-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5e768-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e768-125">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5e768-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e768-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5e768-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e768-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5e768-128">Header</span><span class="sxs-lookup"><span data-stu-id="5e768-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e768-129"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e768-129"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e768-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e768-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e768-131">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="5e768-131">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="5e768-132">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="5e768-132">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="5e768-133">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e768-133">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 





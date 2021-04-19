---
description: Gibt die Versionsnummer der von der Videoausgabe verwendeten SRM (System erneuerbarkeits Meldung) zurück.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372917"
---
# <a name="opm_get_current_hdcp_srm_version"></a><span data-ttu-id="ed7aa-103">OPM \_ get \_ Current \_ HDCP \_ SRM- \_ Version</span><span class="sxs-lookup"><span data-stu-id="ed7aa-103">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>

<span data-ttu-id="ed7aa-104">Gibt die Versionsnummer der von der Videoausgabe verwendeten SRM (System erneuerbarkeits Meldung) zurück.</span><span class="sxs-lookup"><span data-stu-id="ed7aa-104">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>



| <span data-ttu-id="ed7aa-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed7aa-105">Requirement</span></span> | <span data-ttu-id="ed7aa-106">Wert</span><span class="sxs-lookup"><span data-stu-id="ed7aa-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="ed7aa-107">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="ed7aa-107">Request GUID</span></span> | <span data-ttu-id="ed7aa-108">OPM \_ get \_ Current \_ HDCP \_ SRM- \_ Version</span><span class="sxs-lookup"><span data-stu-id="ed7aa-108">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>                                       |
| <span data-ttu-id="ed7aa-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="ed7aa-109">Input data</span></span>   | <span data-ttu-id="ed7aa-110">Keine</span><span class="sxs-lookup"><span data-stu-id="ed7aa-110">None</span></span>                                                                        |
| <span data-ttu-id="ed7aa-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="ed7aa-111">Return data</span></span>  | <span data-ttu-id="ed7aa-112">Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur</span><span class="sxs-lookup"><span data-stu-id="ed7aa-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ed7aa-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed7aa-113">Remarks</span></span>

<span data-ttu-id="ed7aa-114">Wenn diese Abfrage erfolgreich ist, enthält der **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur die SRM-Versionsnummer im Little-Endian-Format.</span><span class="sxs-lookup"><span data-stu-id="ed7aa-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains the SRM version number, in little-endian format.</span></span>

<span data-ttu-id="ed7aa-115">Mithilfe von SRMs wird die Liste der gesperrten HDCP-Geräte (High-Bandwidth Digital Content Protection) aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ed7aa-115">SRMs are used to update the list of revoked High-Bandwidth Digital Content Protection (HDCP) devices.</span></span> <span data-ttu-id="ed7aa-116">SRMs werden mit dem Videoinhalt geliefert.</span><span class="sxs-lookup"><span data-stu-id="ed7aa-116">SRMs are delivered with the video content.</span></span> <span data-ttu-id="ed7aa-117">Um den SRM festzulegen, senden Sie den Befehl [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .</span><span class="sxs-lookup"><span data-stu-id="ed7aa-117">To set the SRM, send the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="ed7aa-118">Diese Abfrage kann bewirken, dass die [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) -Methode einen der folgenden Fehlercodes zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ed7aa-118">This query can cause the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method to return any of the following error codes.</span></span>



| <span data-ttu-id="ed7aa-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ed7aa-119">Return code</span></span>                                            | <span data-ttu-id="ed7aa-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed7aa-120">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="ed7aa-121">Fehler \_ Grafik \_ OPM \_ HDCP \_ SRM \_ nie \_ festgelegt</span><span class="sxs-lookup"><span data-stu-id="ed7aa-121">ERROR\_GRAPHICS\_OPM\_HDCP\_SRM\_NEVER\_SET</span></span>            | <span data-ttu-id="ed7aa-122">Die Anwendung hat keinen SRM festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ed7aa-122">The application did not set an SRM.</span></span>     |
| <span data-ttu-id="ed7aa-123">Fehler \_ Grafik- \_ OPM- \_ Ausgabe \_ \_ \_ unterstützt \_ HDCP nicht</span><span class="sxs-lookup"><span data-stu-id="ed7aa-123">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="ed7aa-124">HDCP wird von der Videoausgabe nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed7aa-124">The video output does not support HDCP.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ed7aa-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed7aa-125">Requirements</span></span>



| <span data-ttu-id="ed7aa-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed7aa-126">Requirement</span></span> | <span data-ttu-id="ed7aa-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ed7aa-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7aa-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed7aa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ed7aa-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed7aa-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ed7aa-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed7aa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ed7aa-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed7aa-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ed7aa-132">Header</span><span class="sxs-lookup"><span data-stu-id="ed7aa-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed7aa-133"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed7aa-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed7aa-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed7aa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed7aa-135">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="ed7aa-135">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="ed7aa-136">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed7aa-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 





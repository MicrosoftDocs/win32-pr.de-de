---
description: OPM-Statusanforderungen
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: OPM-Statusanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf7338fe1309feb49fd191e3f4a1a22f3639b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120175"
---
# <a name="opm-status-requests"></a><span data-ttu-id="cd4dc-103">OPM-Statusanforderungen</span><span class="sxs-lookup"><span data-stu-id="cd4dc-103">OPM Status Requests</span></span>

<span data-ttu-id="cd4dc-104">In diesem Abschnitt werden die verfügbaren Statusanforderungen für [Output Protection Manager](output-protection-manager.md) (OPM) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="cd4dc-105">Um eine OPM-Statusanforderung zu senden, rufen Sie [**IOPMVideoOutput::GetInformation auf.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)</span><span class="sxs-lookup"><span data-stu-id="cd4dc-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="cd4dc-106">Für jede Anforderung werden die folgenden Informationen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-106">For each request, the following information is listed.</span></span>



| <span data-ttu-id="cd4dc-107">Wert</span><span class="sxs-lookup"><span data-stu-id="cd4dc-107">Value</span></span>             | <span data-ttu-id="cd4dc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd4dc-108">Description</span></span>                                                                                                                                                           |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd4dc-109">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="cd4dc-109">Request GUID</span></span> | <span data-ttu-id="cd4dc-110">Identifiziert die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-110">Identifies the request.</span></span> <span data-ttu-id="cd4dc-111">Legen Sie **den guidSetting-Member** der [**OPM \_ GET INFO \_ \_ PARAMETERS-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) auf diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-111">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="cd4dc-112">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="cd4dc-112">Input data</span></span>   | <span data-ttu-id="cd4dc-113">Gibt an, wie das **abParameters-Array** in der [**OPM \_ GET INFO \_ \_ PARAMETERS-Struktur interpretiert**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) wird.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-113">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="cd4dc-114">Ausgabedaten</span><span class="sxs-lookup"><span data-stu-id="cd4dc-114">Output data</span></span>  | <span data-ttu-id="cd4dc-115">Gibt an, wie das **abRequestedInformation-Array** in der [**OPM \_ REQUESTED \_ INFORMATION-Struktur interpretiert**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) wird.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-115">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="cd4dc-116">Die folgenden Statusanforderungen werden definiert:</span><span class="sxs-lookup"><span data-stu-id="cd4dc-116">The following status requests are defined:</span></span>



| <span data-ttu-id="cd4dc-117">Statusanforderung</span><span class="sxs-lookup"><span data-stu-id="cd4dc-117">Status request</span></span>                                                                                      | <span data-ttu-id="cd4dc-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd4dc-118">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd4dc-119">**OPM \_ GET ACP AND CGMSA SIGNALING (OPM GET \_ \_ ACP- UND \_ CGMSA-SIGNALISIERUNG) \_**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-119">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="cd4dc-120">Gibt die folgenden Informationen zu einer Videoausgabe zurück:</span><span class="sxs-lookup"><span data-stu-id="cd4dc-120">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="cd4dc-121">**OPM \_ GET \_ ACTUAL \_ OUTPUT \_ FORMAT**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-121">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="cd4dc-122">Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-122">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="cd4dc-123">**OPM \_ GET \_ ACTUAL \_ PROTECTION \_ LEVEL**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-123">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="cd4dc-124">Gibt die globale Schutzebene für einen angegebenen Schutzmechanismus zurück.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-124">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="cd4dc-125">**OPM \_ GET \_ ADAPTER \_ BUS \_ TYPE**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-125">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="cd4dc-126">Gibt den Typ des E/A-Bus zurück, der von der Videoausgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-126">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="cd4dc-127">**OPM \_ GET \_ CODEC \_ INFO**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-127">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="cd4dc-128">Ruft den Wert eines Hardwarecodecs ab.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-128">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="cd4dc-129">**OPM \_ GET \_ CONNECTED \_ HDCP \_ DEVICE \_ INFORMATION**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-129">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="cd4dc-130">Ruft Informationen zu einem High-Bandwidth Digital Content Protection (HDCP) ab, das an die Videoausgabe angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-130">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="cd4dc-131">Die folgenden Informationen werden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="cd4dc-131">The following information is returned:</span></span> |
| [<span data-ttu-id="cd4dc-132">**OPM \_ GET \_ CONNECTOR \_ TYPE**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-132">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="cd4dc-133">Gibt den physischen Connectortyp der Videoausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-133">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="cd4dc-134">**OPM \_ GET \_ CURRENT \_ HDCP \_ SRM \_ VERSION**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-134">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="cd4dc-135">Gibt die Versionsnummer der Systemerneuerbarkeitsmeldung (SRM) zurück, die derzeit von der Videoausgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-135">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="cd4dc-136">**OPM \_ GET \_ DVI \_ CHARACTERISTICS**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-136">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="cd4dc-137">Fragt ab, ob ein DVI-Connector (Digital Video Interface) DVI Version 1.1 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-137">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="cd4dc-138">**OPM \_ GET \_ OUTPUT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-138">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="cd4dc-139">Gibt den eindeutigen Bezeichner des Monitors zurück, der dieser Videoausgabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-139">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="cd4dc-140">**OPM \_ GET \_ SUPPORTED \_ PROTECTION \_ TYPES**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-140">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="cd4dc-141">Gibt die Liste der Schutzmechanismen zurück, die vom Connector unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-141">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="cd4dc-142">**OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL**</span><span class="sxs-lookup"><span data-stu-id="cd4dc-142">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="cd4dc-143">Gibt die virtuelle Schutzebene für einen angegebenen Schutzmechanismus zurück.</span><span class="sxs-lookup"><span data-stu-id="cd4dc-143">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="cd4dc-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd4dc-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd4dc-145">OPM-Programmierreferenz</span><span class="sxs-lookup"><span data-stu-id="cd4dc-145">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="cd4dc-146">Ausgabeschutz-Manager</span><span class="sxs-lookup"><span data-stu-id="cd4dc-146">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 




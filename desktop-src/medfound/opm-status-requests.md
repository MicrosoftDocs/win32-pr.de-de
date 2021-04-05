---
description: OPM-Status Anforderungen
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: OPM-Status Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd994d7cb8d43db23fe59352dba830e741b74b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753913"
---
# <a name="opm-status-requests"></a><span data-ttu-id="9eece-103">OPM-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9eece-103">OPM Status Requests</span></span>

<span data-ttu-id="9eece-104">In diesem Abschnitt werden die verfügbaren Status Anforderungen für den [Output Protection Manager](output-protection-manager.md) (OPM) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9eece-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="9eece-105">Um eine OPM-Status Anforderung zu senden, nennen Sie [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span><span class="sxs-lookup"><span data-stu-id="9eece-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="9eece-106">Für jede Anforderung werden die folgenden Informationen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9eece-106">For each request, the following information is listed.</span></span>



|              |                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eece-107">Anforderungs-GUID</span><span class="sxs-lookup"><span data-stu-id="9eece-107">Request GUID</span></span> | <span data-ttu-id="9eece-108">Gibt die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="9eece-108">Identifies the request.</span></span> <span data-ttu-id="9eece-109">Legen Sie den **guidsetting** -Member der [**OPM-Struktur \_ get \_ Info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) auf diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="9eece-109">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="9eece-110">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="9eece-110">Input data</span></span>   | <span data-ttu-id="9eece-111">Gibt an, wie das **abparameter** -Array in der [**OPM-Struktur \_ get \_ Info \_ Parameters interpretiert werden**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) soll.</span><span class="sxs-lookup"><span data-stu-id="9eece-111">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="9eece-112">Ausgabedaten</span><span class="sxs-lookup"><span data-stu-id="9eece-112">Output data</span></span>  | <span data-ttu-id="9eece-113">Gibt an, wie das **abrequestedinformation** -Array in der von [**OPM \_ angeforderten \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) Struktur interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9eece-113">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="9eece-114">Die folgenden Status Anforderungen sind definiert:</span><span class="sxs-lookup"><span data-stu-id="9eece-114">The following status requests are defined:</span></span>



| <span data-ttu-id="9eece-115">Status Anforderung</span><span class="sxs-lookup"><span data-stu-id="9eece-115">Status request</span></span>                                                                                      | <span data-ttu-id="9eece-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9eece-116">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eece-117">**OPM \_ get \_ ACP \_ und \_ cgmsa- \_ Signalisierung**</span><span class="sxs-lookup"><span data-stu-id="9eece-117">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="9eece-118">Gibt die folgenden Informationen zu einer Videoausgabe zurück:</span><span class="sxs-lookup"><span data-stu-id="9eece-118">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="9eece-119">**OPM \_ get \_ tatsächliches \_ Ausgabe \_ Format**</span><span class="sxs-lookup"><span data-stu-id="9eece-119">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="9eece-120">Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="9eece-120">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="9eece-121">**OPM \_ get \_ Actual \_ Protection \_ Level**</span><span class="sxs-lookup"><span data-stu-id="9eece-121">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="9eece-122">Gibt die globale Schutz Ebene für einen angegebenen Schutzmechanismus zurück.</span><span class="sxs-lookup"><span data-stu-id="9eece-122">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="9eece-123">**OPM \_ get \_ Adapter \_ \_ Bustyp**</span><span class="sxs-lookup"><span data-stu-id="9eece-123">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="9eece-124">Gibt den Typ des e/a-Busses zurück, der von der Videoausgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9eece-124">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="9eece-125">**OPM- \_ get- \_ Codec- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="9eece-125">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="9eece-126">Ruft den Verdienst Wert eines Hardware Codecs ab.</span><span class="sxs-lookup"><span data-stu-id="9eece-126">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="9eece-127">**OPM \_ get \_ Connected \_ HDCP- \_ Geräte \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="9eece-127">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="9eece-128">Ruft Informationen zu einem HDCP-Gerät (High-Bandwidth Digital Content Protection) ab, das an die Videoausgabe angehängt ist.</span><span class="sxs-lookup"><span data-stu-id="9eece-128">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="9eece-129">Die folgenden Informationen werden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="9eece-129">The following information is returned:</span></span> |
| [<span data-ttu-id="9eece-130">**OPM \_ get \_ Connector- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="9eece-130">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="9eece-131">Gibt den physischen Verbindungstyp der Videoausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="9eece-131">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="9eece-132">**OPM \_ get \_ Current \_ HDCP \_ SRM- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="9eece-132">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="9eece-133">Gibt die Versionsnummer der von der Videoausgabe verwendeten SRM (System erneuerbarkeits Meldung) zurück.</span><span class="sxs-lookup"><span data-stu-id="9eece-133">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="9eece-134">**OPM- \_ get- \_ DVI- \_ Merkmale**</span><span class="sxs-lookup"><span data-stu-id="9eece-134">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="9eece-135">Fragt ab, ob ein DVI-Connector (Digital Video Interface) die DVI-Version 1,1 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9eece-135">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="9eece-136">**OPM \_ - \_ Ausgabe- \_ ID erhalten**</span><span class="sxs-lookup"><span data-stu-id="9eece-136">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="9eece-137">Gibt den eindeutigen Bezeichner des Monitors zurück, der mit dieser Videoausgabe verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="9eece-137">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="9eece-138">**OPM \_ - \_ unterstützte \_ Schutz \_ Typen erhalten**</span><span class="sxs-lookup"><span data-stu-id="9eece-138">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="9eece-139">Gibt die Liste der Schutzmechanismen zurück, die vom Connector unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9eece-139">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="9eece-140">**OPM \_ - \_ Ebene zum virtuellen \_ Schutz \_**</span><span class="sxs-lookup"><span data-stu-id="9eece-140">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="9eece-141">Gibt die virtuelle Schutz Ebene für einen angegebenen Schutzmechanismus zurück.</span><span class="sxs-lookup"><span data-stu-id="9eece-141">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="9eece-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9eece-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eece-143">OPM-Programmier Referenz</span><span class="sxs-lookup"><span data-stu-id="9eece-143">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="9eece-144">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="9eece-144">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 




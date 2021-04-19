---
description: OPM-Befehle
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: OPM-Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa14026123656b26e978bc179d65c3b61913c62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372918"
---
# <a name="opm-commands"></a><span data-ttu-id="d81e8-103">OPM-Befehle</span><span class="sxs-lookup"><span data-stu-id="d81e8-103">OPM Commands</span></span>

<span data-ttu-id="d81e8-104">In diesem Abschnitt werden die verfügbaren Befehle für den [Output Protection Manager](output-protection-manager.md) (OPM) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d81e8-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="d81e8-105">Um einen OPM-Befehl zu senden, nennen Sie [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="d81e8-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="d81e8-106">Die folgenden Informationen sind für jeden Befehl aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d81e8-106">For each command, the following information is listed.</span></span>



|              |                                                                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d81e8-107">Befehls-GUID</span><span class="sxs-lookup"><span data-stu-id="d81e8-107">Command GUID</span></span> | <span data-ttu-id="d81e8-108">Identifiziert den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="d81e8-108">Identifies the command.</span></span> <span data-ttu-id="d81e8-109">Legen Sie den **guidsetting** -Member der [**OPM-Struktur \_ configure \_ Parameters**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) auf diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="d81e8-109">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="d81e8-110">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="d81e8-110">Input data</span></span>   | <span data-ttu-id="d81e8-111">Gibt an, wie das **abparameter** -Array in der OPM-Struktur " [**\_ configure \_ Parameters**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) " interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="d81e8-111">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="d81e8-112">Die folgenden Befehle sind definiert:</span><span class="sxs-lookup"><span data-stu-id="d81e8-112">The following commands are defined:</span></span>



| <span data-ttu-id="d81e8-113">Get-Help</span><span class="sxs-lookup"><span data-stu-id="d81e8-113">Command</span></span>                                                                                                       | <span data-ttu-id="d81e8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d81e8-114">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d81e8-115">**OPM \_ Set \_ ACP \_ und \_ cgmsa \_ Signalisierung**</span><span class="sxs-lookup"><span data-stu-id="d81e8-115">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="d81e8-116">Gibt Informationen über das Videosignal außer der Schutz Ebene an.</span><span class="sxs-lookup"><span data-stu-id="d81e8-116">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="d81e8-117">**OPM \_ Set \_ HDCP \_ SRM**</span><span class="sxs-lookup"><span data-stu-id="d81e8-117">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="d81e8-118">Aktualisiert die System-erneuerbarkeits Meldung (SRM) für High-Bandwidth Digital Content Protection (HDCP).</span><span class="sxs-lookup"><span data-stu-id="d81e8-118">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="d81e8-119">**OPM \_ - \_ Schutz \_ Ebene festlegen**</span><span class="sxs-lookup"><span data-stu-id="d81e8-119">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="d81e8-120">Legt die Schutz Ebene für einen ausgabeschutzmechanismus fest.</span><span class="sxs-lookup"><span data-stu-id="d81e8-120">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="d81e8-121">**OPM \_ Festlegen der \_ Schutz \_ Ebene \_ gemäß CSS- \_ \_ \_ DVD**</span><span class="sxs-lookup"><span data-stu-id="d81e8-121">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="d81e8-122">Legt die HDCP-Schutz Ebene für die DVD-Wiedergabe fest, und zwar gemäß den DVD-Inhalts Regeln für das Scramble-System</span><span class="sxs-lookup"><span data-stu-id="d81e8-122">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d81e8-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d81e8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d81e8-124">OPM-Programmier Referenz</span><span class="sxs-lookup"><span data-stu-id="d81e8-124">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="d81e8-125">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="d81e8-125">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 




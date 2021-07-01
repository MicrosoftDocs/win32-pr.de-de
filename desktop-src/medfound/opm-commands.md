---
description: OPM-Befehle
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: OPM-Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b00240925c28322b911ab55a0e4f026f051d6ec
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119145"
---
# <a name="opm-commands"></a><span data-ttu-id="26d2c-103">OPM-Befehle</span><span class="sxs-lookup"><span data-stu-id="26d2c-103">OPM Commands</span></span>

<span data-ttu-id="26d2c-104">In diesem Abschnitt werden die verfügbaren Befehle für [Output Protection Manager](output-protection-manager.md) (OPM) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="26d2c-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="26d2c-105">Um einen OPM-Befehl zu senden, rufen Sie [**IOPMVideoOutput::Configure auf.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)</span><span class="sxs-lookup"><span data-stu-id="26d2c-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="26d2c-106">Für jeden Befehl werden die folgenden Informationen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="26d2c-106">For each command, the following information is listed.</span></span>



| <span data-ttu-id="26d2c-107">Wert</span><span class="sxs-lookup"><span data-stu-id="26d2c-107">Value</span></span>             | <span data-ttu-id="26d2c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26d2c-108">Description</span></span>                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26d2c-109">Befehls-GUID</span><span class="sxs-lookup"><span data-stu-id="26d2c-109">Command GUID</span></span> | <span data-ttu-id="26d2c-110">Identifiziert den Befehl.</span><span class="sxs-lookup"><span data-stu-id="26d2c-110">Identifies the command.</span></span> <span data-ttu-id="26d2c-111">Legen Sie **den guidSetting-Member** der [**OPM \_ CONFIGURE \_ PARAMETERS-Struktur**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) auf diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="26d2c-111">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="26d2c-112">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="26d2c-112">Input data</span></span>   | <span data-ttu-id="26d2c-113">Gibt an, wie das **abParameters-Array** in der [**OPM \_ CONFIGURE \_ PARAMETERS-Struktur interpretiert**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) wird.</span><span class="sxs-lookup"><span data-stu-id="26d2c-113">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="26d2c-114">Die folgenden Befehle sind definiert:</span><span class="sxs-lookup"><span data-stu-id="26d2c-114">The following commands are defined:</span></span>



| <span data-ttu-id="26d2c-115">Befehl</span><span class="sxs-lookup"><span data-stu-id="26d2c-115">Command</span></span>                                                                                                       | <span data-ttu-id="26d2c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26d2c-116">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26d2c-117">**OPM \_ SET \_ \_ ACP- UND \_ CGMSA-SIGNALISIERUNG \_**</span><span class="sxs-lookup"><span data-stu-id="26d2c-117">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="26d2c-118">Gibt Informationen über das Videosignal an, die nicht die Schutzebene sind.</span><span class="sxs-lookup"><span data-stu-id="26d2c-118">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="26d2c-119">**OPM \_ SET \_ HDCP \_ SRM**</span><span class="sxs-lookup"><span data-stu-id="26d2c-119">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="26d2c-120">Aktualisiert die Systemerneuerbarkeitsmeldung (SRM) für High-Bandwidth Digital Content Protection (HDCP).</span><span class="sxs-lookup"><span data-stu-id="26d2c-120">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="26d2c-121">**OPM \_ SET \_ PROTECTION \_ LEVEL**</span><span class="sxs-lookup"><span data-stu-id="26d2c-121">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="26d2c-122">Legt die Schutzebene für einen Ausgabeschutzmechanismus fest.</span><span class="sxs-lookup"><span data-stu-id="26d2c-122">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="26d2c-123">**\_OPM: \_ FESTLEGEN DER \_ \_ SCHUTZEBENE GEMÄß \_ \_ \_ CSS-DVD**</span><span class="sxs-lookup"><span data-stu-id="26d2c-123">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="26d2c-124">Legt die HDCP-Schutzebene für die DVD-Wiedergabe fest, die den CSS-Regeln (DVD Content Scramble System) folgt.</span><span class="sxs-lookup"><span data-stu-id="26d2c-124">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="26d2c-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26d2c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26d2c-126">OPM-Programmierreferenz</span><span class="sxs-lookup"><span data-stu-id="26d2c-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="26d2c-127">Ausgabeschutz-Manager</span><span class="sxs-lookup"><span data-stu-id="26d2c-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 




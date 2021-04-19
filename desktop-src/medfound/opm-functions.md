---
description: Die folgenden Funktionen werden mit dem Output Protection Manager (OPM) verwendet.
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: OPM-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345816"
---
# <a name="opm-functions"></a><span data-ttu-id="84346-103">OPM-Funktionen</span><span class="sxs-lookup"><span data-stu-id="84346-103">OPM Functions</span></span>

<span data-ttu-id="84346-104">Die folgenden Funktionen werden mit dem [Output Protection Manager](output-protection-manager.md) (OPM) verwendet.</span><span class="sxs-lookup"><span data-stu-id="84346-104">The following functions are used with [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>



| <span data-ttu-id="84346-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="84346-105">Function</span></span>                                                                                             | <span data-ttu-id="84346-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84346-106">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84346-107">**Opmgetvideooutputfortarget**</span><span class="sxs-lookup"><span data-stu-id="84346-107">**OPMGetVideoOutputForTarget**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | <span data-ttu-id="84346-108">Gibt ein Videoausgabe Objekt für das VidPN-Ziel auf dem angegebenen Adapter zurück.</span><span class="sxs-lookup"><span data-stu-id="84346-108">Returns a video output object for the VidPN target on the specified adapter.</span></span>                                                          |
| [<span data-ttu-id="84346-109">**Opmgetvideooutputsfromhmonitor**</span><span class="sxs-lookup"><span data-stu-id="84346-109">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | <span data-ttu-id="84346-110">Erstellt ein OPM-Objekt (Output Protection Manager) für jeden physischen Monitor, der einem bestimmten **Hmonitor** -Handle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="84346-110">Creates an Output Protection Manager (OPM) object for each physical monitor that is associated with a particular **HMONITOR** handle.</span></span> |
| [<span data-ttu-id="84346-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="84346-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | <span data-ttu-id="84346-112">Erstellt ein OPM-Objekt für jeden physischen Monitor, der einem bestimmten Direct3D-Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="84346-112">Creates an OPM object for each physical monitor that is associated with a particular Direct3D device.</span></span>                                 |



 

<span data-ttu-id="84346-113">Die folgenden Funktionen werden von OPM verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="84346-113">The following functions are used by OPM to access functionality in the display driver.</span></span> <span data-ttu-id="84346-114">Anwendungen sollten diese Funktionen nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="84346-114">Applications should not call these functions.</span></span>

-   [<span data-ttu-id="84346-115">**Konfiguration von reopmprotectedoutput**</span><span class="sxs-lookup"><span data-stu-id="84346-115">**ConfigureOPMProtectedOutput**</span></span>](configureopmprotectedoutput.md)
-   [<span data-ttu-id="84346-116">**"Kreateopmprotectedoutputs"**</span><span class="sxs-lookup"><span data-stu-id="84346-116">**CreateOPMProtectedOutputs**</span></span>](createopmprotectedoutputs.md)
-   [<span data-ttu-id="84346-117">**Destroyopmprotectedoutput**</span><span class="sxs-lookup"><span data-stu-id="84346-117">**DestroyOPMProtectedOutput**</span></span>](destroyopmprotectedoutput.md)
-   [<span data-ttu-id="84346-118">**Von GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="84346-118">**GetCertificate**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [<span data-ttu-id="84346-119">**Getcertifialisiesize**</span><span class="sxs-lookup"><span data-stu-id="84346-119">**GetCertificateSize**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [<span data-ttu-id="84346-120">**Getcoppcompatibleopminformation**</span><span class="sxs-lookup"><span data-stu-id="84346-120">**GetCOPPCompatibleOPMInformation**</span></span>](getcoppcompatibleopminformation.md)
-   [<span data-ttu-id="84346-121">**Getopminformation**</span><span class="sxs-lookup"><span data-stu-id="84346-121">**GetOPMInformation**</span></span>](getopminformation.md)
-   [<span data-ttu-id="84346-122">**Getopmrandomnumber**</span><span class="sxs-lookup"><span data-stu-id="84346-122">**GetOPMRandomNumber**</span></span>](getopmrandomnumber.md)
-   [<span data-ttu-id="84346-123">**Getvorschlags stedopmprotectedoutputarraysize**</span><span class="sxs-lookup"><span data-stu-id="84346-123">**GetSuggestedOPMProtectedOutputArraySize**</span></span>](getsuggestedopmprotectedoutputarraysize.md)
-   [<span data-ttu-id="84346-124">**"Setup" für "Setup keyandsequencenumbers"**</span><span class="sxs-lookup"><span data-stu-id="84346-124">**SetOPMSigningKeyAndSequenceNumbers**</span></span>](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a><span data-ttu-id="84346-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="84346-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84346-126">OPM-Programmier Referenz</span><span class="sxs-lookup"><span data-stu-id="84346-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="84346-127">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="84346-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 




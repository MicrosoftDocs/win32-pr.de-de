---
title: DWM-Strukturen
description: Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager-Strukturen (DWM).
ms.assetid: 26b36617-54c2-405a-9a7d-bd86fefa94b6
keywords:
- Desktopfenster-Manager (DWM), Referenz
- Dwm (Desktopfenster-Manager), Referenz
- Desktopfenster-Manager (DWM), Strukturen
- Dwm (Desktopfenster-Manager), Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f212d248c0f70cfd51e6e47b2d37c89d24f630b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036994"
---
# <a name="dwm-structures"></a><span data-ttu-id="85532-107">DWM-Strukturen</span><span class="sxs-lookup"><span data-stu-id="85532-107">DWM Structures</span></span>

<span data-ttu-id="85532-108">Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager-Strukturen (DWM).</span><span class="sxs-lookup"><span data-stu-id="85532-108">This section contains information about the Desktop Window Manager (DWM) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="85532-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="85532-109">In this section</span></span>



| <span data-ttu-id="85532-110">Thema</span><span class="sxs-lookup"><span data-stu-id="85532-110">Topic</span></span>                                                                     | <span data-ttu-id="85532-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85532-111">Description</span></span>                                                                                                                                               |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85532-112">**DWM- \_ blurbehind**</span><span class="sxs-lookup"><span data-stu-id="85532-112">**DWM\_BLURBEHIND**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)<br/>                      | <span data-ttu-id="85532-113">Gibt DWM-weich-Behind-Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="85532-113">Specifies DWM blur-behind properties.</span></span> <span data-ttu-id="85532-114">Wird von der [**dwmenableblurabledwindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="85532-114">Used by the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function.</span></span><br/>                     |
| [<span data-ttu-id="85532-115">**DWM \_ - \_ Parameter vorhanden**</span><span class="sxs-lookup"><span data-stu-id="85532-115">**DWM\_PRESENT\_PARAMETERS**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_present_parameters)<br/>     | <span data-ttu-id="85532-116">Gibt die DWM-Video Frame Parameter für die Frame Komposition an.</span><span class="sxs-lookup"><span data-stu-id="85532-116">Specifies DWM video frame parameters for frame composition.</span></span> <span data-ttu-id="85532-117">Wird von der Funktion [**dwmsetpresentparameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) verwendet.</span><span class="sxs-lookup"><span data-stu-id="85532-117">Used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function.</span></span><br/>   |
| [<span data-ttu-id="85532-118">**Eigenschaften der DWM- \_ Miniaturansicht \_**</span><span class="sxs-lookup"><span data-stu-id="85532-118">**DWM\_THUMBNAIL\_PROPERTIES**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties)<br/> | <span data-ttu-id="85532-119">Gibt DWM-Miniatur Ansichts Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="85532-119">Specifies DWM thumbnail properties.</span></span> <span data-ttu-id="85532-120">Wird von der Funktion " [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="85532-120">Used by the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function.</span></span><br/>                 |
| [<span data-ttu-id="85532-121">**DWM- \_ Zeit Steuerungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="85532-121">**DWM\_TIMING\_INFO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_timing_info)<br/>                   | <span data-ttu-id="85532-122">Gibt DWM-Kompositions Zeit Steuerungsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="85532-122">Specifies DWM composition timing information.</span></span> <span data-ttu-id="85532-123">Wird von der Funktion " [**dwmgetcompositiontiminginfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="85532-123">Used by the [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) function.</span></span><br/>         |
| [<span data-ttu-id="85532-124">**MilMatrix3x2D**</span><span class="sxs-lookup"><span data-stu-id="85532-124">**MilMatrix3x2D**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-milmatrix3x2d)<br/>                         | <span data-ttu-id="85532-125">Gibt eine 3 x 2-Matrix an, die eine Transformation beschreibt.</span><span class="sxs-lookup"><span data-stu-id="85532-125">Specifies a 3x2 matrix that describes a transform.</span></span> <br/>                                                                                            |
| [<span data-ttu-id="85532-126">**unsigned- \_ Verhältnis**</span><span class="sxs-lookup"><span data-stu-id="85532-126">**UNSIGNED\_RATIO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-unsigned_ratio)<br/>                      | <span data-ttu-id="85532-127">Definiert einen Datentyp, der von den DWM-APIs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="85532-127">Defines a data type used by the DWM APIs.</span></span> <span data-ttu-id="85532-128">Es stellt ein allgemeines Verhältnis dar und wird für unterschiedliche Zwecke und Einheiten auch innerhalb einer einzigen API verwendet.</span><span class="sxs-lookup"><span data-stu-id="85532-128">It represents a generic ratio and is used for different purposes and units even within a single API.</span></span><br/> |



 

 

 






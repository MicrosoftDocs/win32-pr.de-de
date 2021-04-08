---
title: DWM-Konstanten und-Enumerationen
description: Dieser Abschnitt enthält Informationen zu den Konstanten und Enumerationen, die in den Desktopfenster-Manager-APIs (DWM) verwendet werden.
ms.assetid: b01f620d-ac87-4e93-88ab-f4297d8cf1d5
keywords:
- Desktopfenster-Manager (DWM), Referenz
- Dwm (Desktopfenster-Manager), Referenz
- Desktopfenster-Manager (DWM), Konstanten
- Dwm (Desktopfenster-Manager), Konstanten
- Desktopfenster-Manager (DWM), Enumerationen
- Dwm (Desktopfenster-Manager), Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280fff527f95176b47fc99f88d09453dbf579f38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711184"
---
# <a name="dwm-constants-and-enumerations"></a><span data-ttu-id="0a3e5-109">DWM-Konstanten und-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="0a3e5-109">DWM Constants and Enumerations</span></span>

<span data-ttu-id="0a3e5-110">Dieser Abschnitt enthält Informationen zu den Konstanten und Enumerationen, die in den Desktopfenster-Manager-APIs (DWM) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a3e5-110">This section contains information about the constants and enumerations used in the Desktop Window Manager (DWM) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0a3e5-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0a3e5-111">In this section</span></span>



| <span data-ttu-id="0a3e5-112">Thema</span><span class="sxs-lookup"><span data-stu-id="0a3e5-112">Topic</span></span>                                                                                     | <span data-ttu-id="0a3e5-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a3e5-113">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a3e5-114">**DWM-weich-hinter Konstanten**</span><span class="sxs-lookup"><span data-stu-id="0a3e5-114">**DWM Blur Behind Constants**</span></span>](dwm-bb-constants.md)<br/>                          | <span data-ttu-id="0a3e5-115">Flags, die von der [**DWM- \_ blurbehind**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) -Struktur verwendet werden, um anzugeben, welche der Member gültige Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0a3e5-115">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span><br/>                                                                    |
| [<span data-ttu-id="0a3e5-116">**DWM-Kompositions Konstanten aktivieren**</span><span class="sxs-lookup"><span data-stu-id="0a3e5-116">**DWM Enable Composition Constants**</span></span>](dwm-ec-constants.md)<br/>                   | <span data-ttu-id="0a3e5-117">Flags, die von der [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  -Funktion verwendet werden, um den Zustand der DWM-Komposition zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0a3e5-117">Flags used by the [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  function to change the state of DWM composition.</span></span><br/>                                                                             |
| [<span data-ttu-id="0a3e5-118">**DWM \_ - \_ Quellframe- \_ Sampling**</span><span class="sxs-lookup"><span data-stu-id="0a3e5-118">**DWM\_SOURCE\_FRAME\_SAMPLING**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwm_source_frame_sampling)<br/>              | <span data-ttu-id="0a3e5-119">Flags, die von der Funktion [**dwmsetpresentparameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) zum Angeben des Frame-Samplings verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a3e5-119">Flags used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function to specify the frame sampling type.</span></span><br/>                                                                            |
| [<span data-ttu-id="0a3e5-120">**Anforderungen an das \_ Windows-Registerkarten \_ Fenster \_**</span><span class="sxs-lookup"><span data-stu-id="0a3e5-120">**DWM\_TAB\_WINDOW\_REQUIREMENTS**</span></span>](/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements)<br/>          | <span data-ttu-id="0a3e5-121">Wird von dwmgetunmettabrequirements zurückgegeben, um die Anforderungen anzugeben, die für ein Fenster zum Platzieren von Registerkarten in der Titelleiste der Anwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0a3e5-121">Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar.</span></span><br/>                                                                    |
| [<span data-ttu-id="0a3e5-122">**DWM- \_ TNP-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="0a3e5-122">**DWM\_TNP Constants**</span></span>](dwm-tnp-constants.md)<br/>                                | <span data-ttu-id="0a3e5-123">Flags, die von der Eigenschaften Struktur der [**DWM- \_ Miniaturansicht \_**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) verwendet werden, um anzugeben, welche der Member gültige Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0a3e5-123">Flags used by the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) structure to indicate which of its members contain valid information.</span></span><br/>                                               |
| [<span data-ttu-id="0a3e5-124">**DWMFLIP3DWINDOWPOLICY**</span><span class="sxs-lookup"><span data-stu-id="0a3e5-124">**DWMFLIP3DWINDOWPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmflip3dwindowpolicy)<br/>                         | <span data-ttu-id="0a3e5-125">Flags, die von der [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) -Funktion verwendet werden, um die Flip3D-Fenster Richtlinie anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0a3e5-125">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the Flip3D window policy.</span></span><br/>                                                                               |
| [<span data-ttu-id="0a3e5-126">**Dwmncrenderingpolicy**</span><span class="sxs-lookup"><span data-stu-id="0a3e5-126">**DWMNCRENDERINGPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmncrenderingpolicy)<br/>                           | <span data-ttu-id="0a3e5-127">Flags, die von der [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) -Funktion verwendet werden, um die nicht-Client Bereichs-renderingrichtlinie anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0a3e5-127">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the non-client area rendering policy.</span></span><br/>                                                                   |
| [<span data-ttu-id="0a3e5-128">**dwmtransition \_ ownedWindow- \_ Ziel**</span><span class="sxs-lookup"><span data-stu-id="0a3e5-128">**DWMTRANSITION\_OWNEDWINDOW\_TARGET**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmtransition_ownedwindow_target)<br/> | <span data-ttu-id="0a3e5-129">Identifiziert das Ziel.</span><span class="sxs-lookup"><span data-stu-id="0a3e5-129">Identifies the target.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="0a3e5-130">**DWMWINDOWATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="0a3e5-130">**DWMWINDOWATTRIBUTE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)<br/>                               | <span data-ttu-id="0a3e5-131">Flags, die von den Funktionen [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) und [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) zum Angeben von Fenster Attributen für nicht-Client Rendering verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a3e5-131">Flags used by the [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions to specify window attributes for non-client rendering.</span></span><br/> |
| [<span data-ttu-id="0a3e5-132">**Gesten- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="0a3e5-132">**GESTURE\_TYPE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-gesture_type)<br/>                                          | <span data-ttu-id="0a3e5-133">Identifiziert den in [**dwmrendergeste**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture)angegebenen Gesten-Typ.</span><span class="sxs-lookup"><span data-stu-id="0a3e5-133">Identifies the gesture type specified in [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span></span><br/>                                                                                                               |



 

 

 






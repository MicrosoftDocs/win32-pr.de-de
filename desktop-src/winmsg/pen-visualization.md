---
description: Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn eine der aufgelisteten Stift Gesten erkannt wird.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Stift Visualisierung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529162"
---
# <a name="pen-visualization"></a><span data-ttu-id="9470a-103">Stift Visualisierung</span><span class="sxs-lookup"><span data-stu-id="9470a-103">Pen Visualization</span></span>

<span data-ttu-id="9470a-104">Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn eine der aufgelisteten Stift Gesten erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="9470a-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed pen gestures is detected.</span></span>

<span data-ttu-id="9470a-105">Diese Konstanten werden mit den Parametern für die **SPI \_ getpvisualisierung** und **SPI \_ setpvisualisierungen** und der [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="9470a-105">These constants are used with the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="9470a-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**"pvisualisierung" \_ aus**</span><span class="sxs-lookup"><span data-stu-id="9470a-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9470a-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="9470a-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="9470a-108">Gibt an, dass das UI-Feedback für alle Stift Gesten deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9470a-108">Specifies that UI feedback for all pen gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9470a-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**pvisualisierung \_ am**</span><span class="sxs-lookup"><span data-stu-id="9470a-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9470a-110">0x0023</span><span class="sxs-lookup"><span data-stu-id="9470a-110">0x0023</span></span>
</dt> <dt>



<span data-ttu-id="9470a-111">Gibt an, dass das UI-Feedback für alle Stift Gesten eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="9470a-111">Specifies that UI feedback for all pen gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9470a-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**pvisualisierung \_ tippen**</span><span class="sxs-lookup"><span data-stu-id="9470a-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9470a-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="9470a-113">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="9470a-114">Gibt das UI-Feedback für eine Stift Abzweigung an.</span><span class="sxs-lookup"><span data-stu-id="9470a-114">Specifies UI feedback for a pen tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9470a-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**\_tavisualisierungs-Double Tap**</span><span class="sxs-lookup"><span data-stu-id="9470a-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9470a-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="9470a-116">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="9470a-117">Gibt das Benutzeroberflächen Feedback für eine Stift-Doppel tippen an.</span><span class="sxs-lookup"><span data-stu-id="9470a-117">Specifies UI feedback for a pen double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9470a-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**pvisualisierung- \_ Cursor**</span><span class="sxs-lookup"><span data-stu-id="9470a-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**PENVISUALIZATION\_CURSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9470a-119">0x0020</span><span class="sxs-lookup"><span data-stu-id="9470a-119">0x0020</span></span>
</dt> <dt>



<span data-ttu-id="9470a-120">Gibt das UI-Feedback für den Stift Cursor an.</span><span class="sxs-lookup"><span data-stu-id="9470a-120">Specifies UI feedback for the pen cursor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9470a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9470a-121">Requirements</span></span>



| <span data-ttu-id="9470a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9470a-122">Requirement</span></span> | <span data-ttu-id="9470a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9470a-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9470a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9470a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9470a-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9470a-125">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9470a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9470a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9470a-127">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9470a-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9470a-128">Header</span><span class="sxs-lookup"><span data-stu-id="9470a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9470a-129"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="9470a-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9470a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9470a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9470a-131">Konfigurations Konstanten</span><span class="sxs-lookup"><span data-stu-id="9470a-131">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="9470a-132">**Kontakt Visualisierung**</span><span class="sxs-lookup"><span data-stu-id="9470a-132">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="9470a-133">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="9470a-133">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="9470a-134">Eingabe-Feedback-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="9470a-134">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 


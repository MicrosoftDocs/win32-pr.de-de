---
description: Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn eine der aufgelisteten Gesten erkannt wird.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Gesten Visualisierung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351042"
---
# <a name="gesture-visualization"></a><span data-ttu-id="ee540-103">Gesten Visualisierung</span><span class="sxs-lookup"><span data-stu-id="ee540-103">Gesture Visualization</span></span>

<span data-ttu-id="ee540-104">Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn eine der aufgelisteten Gesten erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="ee540-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed gestures is detected.</span></span>

<span data-ttu-id="ee540-105">Diese Konstanten werden mit den **SPI \_ getgesturevisualisierungs** -und **SPI \_ setgesturevisualisierungs** -Parametern und der [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee540-105">These constants are used with the **SPI\_GETGESTUREVISUALIZATION** and **SPI\_SETGESTUREVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="ee540-106">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="ee540-106">**Note**</span></span>  

<span data-ttu-id="ee540-107">Zum Abrufen oder Festlegen von Pen-Visualisierungs Informationen wird empfohlen, dass Sie die **SPI \_ getpenvisualisierungs** -und **SPI \_ setpenvisualisierungs** Parameter und die in [**Pen-Visualisierung**](pen-visualization.md)aufgeführten Konstanten verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee540-107">For retrieving or setting pen visualization info, we recommend that you use the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the constants listed in [**Pen Visualization**](pen-visualization.md).</span></span>

<dl> <dt>

<span data-ttu-id="ee540-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**gesturevisualisierungen \_ aus**</span><span class="sxs-lookup"><span data-stu-id="ee540-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee540-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="ee540-109">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="ee540-110">Gibt an, dass das UI-Feedback für alle Gesten deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ee540-110">Specifies that UI feedback for all gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee540-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**gesturevisualisierung \_ in**</span><span class="sxs-lookup"><span data-stu-id="ee540-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee540-112">0x001F</span><span class="sxs-lookup"><span data-stu-id="ee540-112">0x001F</span></span>
</dt> <dt>



<span data-ttu-id="ee540-113">Gibt an, dass Benutzeroberflächen Feedback für alle Gesten auf ON festgelegt ist</span><span class="sxs-lookup"><span data-stu-id="ee540-113">Specifies that UI feedback for all gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee540-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**gesturevisualisierungs \_ tippen**</span><span class="sxs-lookup"><span data-stu-id="ee540-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee540-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="ee540-115">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="ee540-116">Gibt das UI-Feedback für eine Tap an.</span><span class="sxs-lookup"><span data-stu-id="ee540-116">Specifies UI feedback for a tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee540-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**gesturevisualisierungs- \_ Double Tap**</span><span class="sxs-lookup"><span data-stu-id="ee540-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee540-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="ee540-118">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="ee540-119">Gibt das UI-Feedback für eine doppelte Tap an.</span><span class="sxs-lookup"><span data-stu-id="ee540-119">Specifies UI feedback for a double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee540-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**gesturevisualisierungs- \_ pressandtap**</span><span class="sxs-lookup"><span data-stu-id="ee540-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION\_PRESSANDTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee540-121">0x0004</span><span class="sxs-lookup"><span data-stu-id="ee540-121">0x0004</span></span>
</dt> <dt>



<span data-ttu-id="ee540-122">Gibt das UI-Feedback für ein drücken und tippen an.</span><span class="sxs-lookup"><span data-stu-id="ee540-122">Specifies UI feedback for a press and tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee540-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**gesturevisualisierungs- \_ pressandhold**</span><span class="sxs-lookup"><span data-stu-id="ee540-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION\_PRESSANDHOLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee540-124">0x0008</span><span class="sxs-lookup"><span data-stu-id="ee540-124">0x0008</span></span>
</dt> <dt>



<span data-ttu-id="ee540-125">Gibt das Benutzeroberflächen Feedback für einen Press-und-Halt an.</span><span class="sxs-lookup"><span data-stu-id="ee540-125">Specifies UI feedback for a press and hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee540-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**gesturevisualisierungs- \_ RightTap**</span><span class="sxs-lookup"><span data-stu-id="ee540-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION\_RIGHTTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee540-127">0x0010</span><span class="sxs-lookup"><span data-stu-id="ee540-127">0x0010</span></span>
</dt> <dt>



<span data-ttu-id="ee540-128">Gibt das UI-Feedback für einen richtigen Tap an.</span><span class="sxs-lookup"><span data-stu-id="ee540-128">Specifies UI feedback for a right tap.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee540-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee540-129">Requirements</span></span>



| <span data-ttu-id="ee540-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee540-130">Requirement</span></span> | <span data-ttu-id="ee540-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ee540-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ee540-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee540-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ee540-133">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee540-133">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ee540-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee540-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ee540-135">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee540-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ee540-136">Header</span><span class="sxs-lookup"><span data-stu-id="ee540-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee540-137"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee540-137"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee540-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee540-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee540-139">Konfigurations Konstanten</span><span class="sxs-lookup"><span data-stu-id="ee540-139">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="ee540-140">**Kontakt Visualisierung**</span><span class="sxs-lookup"><span data-stu-id="ee540-140">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="ee540-141">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="ee540-141">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="ee540-142">Eingabe-Feedback-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ee540-142">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 


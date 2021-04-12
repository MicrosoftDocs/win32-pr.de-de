---
description: Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn ein Eingabe Kontakt erkannt wird.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Kontakt Visualisierung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348189"
---
# <a name="contact-visualization"></a><span data-ttu-id="98ef6-103">Kontakt Visualisierung</span><span class="sxs-lookup"><span data-stu-id="98ef6-103">Contact Visualization</span></span>

<span data-ttu-id="98ef6-104">Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn ein Eingabe Kontakt erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="98ef6-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when an input contact is detected.</span></span>

<span data-ttu-id="98ef6-105">Diese Konstanten werden mit den Parametern **SPI \_ getcontactvisuand** **SPI \_ setcontactvisuund** der Funktion [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) verwendet.</span><span class="sxs-lookup"><span data-stu-id="98ef6-105">These constants are used with the **SPI\_GETCONTACTVISUALIZATION** and **SPI\_SETCONTACTVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="98ef6-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**contactvisualisierung \_ aus**</span><span class="sxs-lookup"><span data-stu-id="98ef6-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ef6-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="98ef6-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="98ef6-108">Gibt an, dass das UI-Feedback für alle Kontakte deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="98ef6-108">Specifies UI feedback for all contacts is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98ef6-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**contactvisualisierung \_ in**</span><span class="sxs-lookup"><span data-stu-id="98ef6-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ef6-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="98ef6-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="98ef6-111">Gibt an, dass das UI-Feedback für alle Kontakte on ist.</span><span class="sxs-lookup"><span data-stu-id="98ef6-111">Specifies UI feedback for all contacts is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98ef6-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**"contactvisualisierung" ( \_ presentationmode)**</span><span class="sxs-lookup"><span data-stu-id="98ef6-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION\_PRESENTATIONMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98ef6-113">0x0002</span><span class="sxs-lookup"><span data-stu-id="98ef6-113">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="98ef6-114">Gibt an, dass Benutzeroberflächen Feedback für alle Kontakte mit visuellen Darstellung im Präsentationsmodus angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="98ef6-114">Specifies UI feedback for all contacts is on with presentation mode visuals.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98ef6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98ef6-115">Requirements</span></span>



| <span data-ttu-id="98ef6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98ef6-116">Requirement</span></span> | <span data-ttu-id="98ef6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="98ef6-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="98ef6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98ef6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="98ef6-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98ef6-119">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="98ef6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98ef6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="98ef6-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98ef6-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="98ef6-122">Header</span><span class="sxs-lookup"><span data-stu-id="98ef6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="98ef6-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="98ef6-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98ef6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98ef6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ef6-125">Konfigurations Konstanten</span><span class="sxs-lookup"><span data-stu-id="98ef6-125">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="98ef6-126">**Gesten Visualisierung**</span><span class="sxs-lookup"><span data-stu-id="98ef6-126">**Gesture Visualization**</span></span>](gesture-visualization.md)
</dt> <dt>

[<span data-ttu-id="98ef6-127">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="98ef6-127">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="98ef6-128">Eingabe-Feedback-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="98ef6-128">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 


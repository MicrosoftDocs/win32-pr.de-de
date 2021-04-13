---
title: Schieberegler (Windows Multimedia)
description: Schieberegler
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Schieberegler
- Mischungen, Steuerelemente
- Mixer, Schieberegler
- Schieberegler-Steuerelemente
- MIXERCONTROLDETAILS_SIGNED Struktur
- Pan-Steuerelement
- QSound Pan-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391398"
---
# <a name="sliders-windows-multimedia"></a><span data-ttu-id="1cda8-111">Schieberegler (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="1cda8-111">Sliders (Windows Multimedia)</span></span>

<span data-ttu-id="1cda8-112">Die Schieberegler-Steuerelemente sind in der Regel horizontale Steuerelemente, die nach links oder rechts angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="1cda8-112">The slider controls are typically horizontal controls that can be adjusted to the left or right.</span></span> <span data-ttu-id="1cda8-113">Diese Steuerelemente verwenden die [**\_ signierte "mixercontroldetails**](/previous-versions//dd757297(v=vs.85)) "-Struktur zum Abrufen und Festlegen von Steuerelement Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1cda8-113">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="1cda8-114">In der folgenden Tabelle werden die Typen von Schiebereglern beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1cda8-114">The following table describes the types of sliders.</span></span>



| <span data-ttu-id="1cda8-115">Control</span><span class="sxs-lookup"><span data-stu-id="1cda8-115">Control</span></span>    | <span data-ttu-id="1cda8-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1cda8-116">Description</span></span>                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cda8-117">Schieberegler</span><span class="sxs-lookup"><span data-stu-id="1cda8-117">Slider</span></span>     | <span data-ttu-id="1cda8-118">Hat einen Bereich von – 32.768 bis 32.767.</span><span class="sxs-lookup"><span data-stu-id="1cda8-118">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="1cda8-119">Der mischertreibers definiert die Begrenzungen dieses Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="1cda8-119">The mixer driver defines the limits of this control.</span></span>                               |
| <span data-ttu-id="1cda8-120">Schwenken</span><span class="sxs-lookup"><span data-stu-id="1cda8-120">Pan</span></span>        | <span data-ttu-id="1cda8-121">Hat einen Bereich von – 32.768 bis 32.767.</span><span class="sxs-lookup"><span data-stu-id="1cda8-121">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="1cda8-122">Der mischertreibers definiert die Begrenzungen dieses Steuer Elements mit 0 als Wert für Midrange.</span><span class="sxs-lookup"><span data-stu-id="1cda8-122">The mixer driver defines the limits of this control, with 0 as the midrange value.</span></span> |
| <span data-ttu-id="1cda8-123">QSound schwenken</span><span class="sxs-lookup"><span data-stu-id="1cda8-123">QSound Pan</span></span> | <span data-ttu-id="1cda8-124">Bietet erweiterte Soundsteuerung durch QSound.</span><span class="sxs-lookup"><span data-stu-id="1cda8-124">Provides expanded sound control through QSound.</span></span> <span data-ttu-id="1cda8-125">Dieses Steuerelement hat einen Bereich von – 15 bis 15.</span><span class="sxs-lookup"><span data-stu-id="1cda8-125">This control has a range of –15 through 15.</span></span>                               |



 

 

 

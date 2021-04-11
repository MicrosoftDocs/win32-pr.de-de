---
title: Subview-Element
description: Subview-Element
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Windows Media Player Skins, subview-Element
- Skins, subview-Element
- Subview-Element
- Verweis für Skins, subview-Element
- Elemente, unter Ansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310971"
---
# <a name="subview-element"></a><span data-ttu-id="65630-108">Subview-Element</span><span class="sxs-lookup"><span data-stu-id="65630-108">SUBVIEW Element</span></span>

<span data-ttu-id="65630-109">Das **subview** -Element bietet eine Möglichkeit, einen Teil einer Skin zu bearbeiten, um z. b. eine Systemsteuerung bereitzustellen, die ausgeblendet werden kann, wenn Sie nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65630-109">The **SUBVIEW** element provides a way to manipulate a portion of a skin, for example, to provide a control panel that can be hidden when it is not being used.</span></span> <span data-ttu-id="65630-110">**Subview** -Elemente sind immer untergeordnete Elemente von übergeordneten **Ansichts** Elementen und können ein anderes Skin-Element enthalten, mit Ausnahme der Elemente **View**, **Theme** und other **subview** .</span><span class="sxs-lookup"><span data-stu-id="65630-110">**SUBVIEW** elements are always children of parent **VIEW** elements, and can contain other skin element except for **VIEW**, **THEME**, and other **SUBVIEW** elements.</span></span>

<span data-ttu-id="65630-111">Das **subview** -Element unterstützt die folgenden Attribute, die unter dem **View** -Element definiert sind.</span><span class="sxs-lookup"><span data-stu-id="65630-111">The **SUBVIEW** element supports the following attributes, which are defined under the **VIEW** element.</span></span>



| <span data-ttu-id="65630-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="65630-112">Attribute</span></span>                                                       | <span data-ttu-id="65630-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65630-113">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65630-114">Background Color</span><span class="sxs-lookup"><span data-stu-id="65630-114">backgroundColor</span></span>](view-backgroundcolor.md)                     | <span data-ttu-id="65630-115">Gibt die Hintergrundfarbe des **unter Ansicht** -Steuer Elements an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="65630-115">Specifies or retrieves the background color of the **SUBVIEW** control.</span></span> <span data-ttu-id="65630-116">Der Standardwert ist "None".</span><span class="sxs-lookup"><span data-stu-id="65630-116">The default value is "none".</span></span>        |
| [<span data-ttu-id="65630-117">backgroundImage</span><span class="sxs-lookup"><span data-stu-id="65630-117">backgroundImage</span></span>](view-backgroundimage.md)                     | <span data-ttu-id="65630-118">Gibt das Hintergrundbild des **unter Ansicht** -Steuer Elements an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="65630-118">Specifies or retrieves the background image of the **SUBVIEW** control.</span></span>                                     |
| [<span data-ttu-id="65630-119">backgroundimagehueshift</span><span class="sxs-lookup"><span data-stu-id="65630-119">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="65630-120">Gibt den Betrag an, um den der Farbton des Hintergrund Bilds verschoben wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="65630-120">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                      |
| [<span data-ttu-id="65630-121">backgroundimagesationations</span><span class="sxs-lookup"><span data-stu-id="65630-121">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="65630-122">Gibt den Sättigungswert des Hintergrund Bilds an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="65630-122">Specifies or retrieves the saturation value of the background image.</span></span>                                        |
| [<span data-ttu-id="65630-123">backgroundkacheln</span><span class="sxs-lookup"><span data-stu-id="65630-123">backgroundTiled</span></span>](view-backgroundtiled.md)                     | <span data-ttu-id="65630-124">Gibt einen Wert an, der angibt, ob das Hintergrundbild des **unter Ansicht** -Steuer Elements angezeigt wird, oder ruft diesen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="65630-124">Specifies or retrieves a value indicating whether the background image of the **SUBVIEW** control is tiled.</span></span> |
| [<span data-ttu-id="65630-125">resizebackgroundimage</span><span class="sxs-lookup"><span data-stu-id="65630-125">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="65630-126">Gibt einen Wert an oder ruft ihn ab, der angibt, ob die Größe des Hintergrund Bilds geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="65630-126">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                      |
| [<span data-ttu-id="65630-127">transparendcolor</span><span class="sxs-lookup"><span data-stu-id="65630-127">transparencyColor</span></span>](view-transparencycolor.md)                 | <span data-ttu-id="65630-128">Gibt die Transparenz Farbe des Hintergrund Bilds an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="65630-128">Specifies or retrieves the transparency color of the background image.</span></span>                                      |



 

<span data-ttu-id="65630-129">Das **subview** -Element unterstützt die Ambient-Attribute, sofern nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="65630-129">The **SUBVIEW** element supports the ambient attributes, except where noted.</span></span> <span data-ttu-id="65630-130">Weitere Informationen finden Sie unter [Ambient-Attribute](ambient-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="65630-130">For more information, see [Ambient Attributes](ambient-attributes.md).</span></span>

<span data-ttu-id="65630-131">Das **subview** -Element kann die folgenden Ambient-Ereignishandler implementieren: [onendmove](onendmove.md) und [OnResize](onresize.md).</span><span class="sxs-lookup"><span data-stu-id="65630-131">The **SUBVIEW** element can implement the following ambient event handlers: [onendmove](onendmove.md) and [onresize](onresize.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="65630-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="65630-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65630-133">**Referenz zur Skin-Programmierung**</span><span class="sxs-lookup"><span data-stu-id="65630-133">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="65630-134">**View-Element**</span><span class="sxs-lookup"><span data-stu-id="65630-134">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





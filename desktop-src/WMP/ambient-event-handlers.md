---
title: Ambient-Ereignishandler
description: Ambient-Ereignishandler
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Windows Media Player Skins, Ambient-Ereignishandler
- Skins, Ambient-Ereignishandler
- Referenz für Skins, Ambient-Ereignishandler
- Ambient-Ereignishandler
- Ereignisse, Ambient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388086"
---
# <a name="ambient-event-handlers"></a><span data-ttu-id="71b01-108">Ambient-Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="71b01-108">Ambient Event Handlers</span></span>

<span data-ttu-id="71b01-109">Die folgenden Ereignishandler können für die meisten Skin-Elemente implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="71b01-109">The following event handlers can be implemented for most skin elements.</span></span> <span data-ttu-id="71b01-110">Die Ambient-Ereignis Attribute, auf die mit dem **Ereignis** Schlüsselwort zugegriffen wird, können innerhalb eines Ereignis Handlers verwendet werden, um den Zustand der Tastatur und der Maus zum Zeitpunkt des Ereignisses zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="71b01-110">The ambient event attributes accessed with the **event** keyword can be used within an event handler to determine the state of the keyboard and mouse at the time of the event.</span></span>



| <span data-ttu-id="71b01-111">Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="71b01-111">Event handler</span></span>                                   | <span data-ttu-id="71b01-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71b01-112">Description</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71b01-113">*Attribut* \_ OnChange</span><span class="sxs-lookup"><span data-stu-id="71b01-113">*attribute*\_onchange</span></span>](attribute-onchange.md) | <span data-ttu-id="71b01-114">Wenn ein Skin-Attribut den Wert ändert, tritt ein Ereignis auf, das von einem Ereignishandler behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="71b01-114">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="71b01-115">Der Name des Ereignis Handlers ist der Name des Attributs, gefolgt von einem Unterstrich und "OnChange", z. b. "Value \_ OnChange".</span><span class="sxs-lookup"><span data-stu-id="71b01-115">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span> |
| [<span data-ttu-id="71b01-116">onblur</span><span class="sxs-lookup"><span data-stu-id="71b01-116">onblur</span></span>](onblur.md)                            | <span data-ttu-id="71b01-117">Behandelt ein Ereignis, das auftritt, wenn das Element den Tastaturfokus verliert.</span><span class="sxs-lookup"><span data-stu-id="71b01-117">Handles an event that occurs when the element loses the keyboard focus.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="71b01-118">OnClick</span><span class="sxs-lookup"><span data-stu-id="71b01-118">onclick</span></span>](onclick.md)                          | <span data-ttu-id="71b01-119">Behandelt ein Ereignis, das auftritt, wenn der Benutzer auf das Element klickt.</span><span class="sxs-lookup"><span data-stu-id="71b01-119">Handles an event that occurs when the user clicks the element.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="71b01-120">ondblclick</span><span class="sxs-lookup"><span data-stu-id="71b01-120">ondblclick</span></span>](ondblclick.md)                    | <span data-ttu-id="71b01-121">Behandelt ein Ereignis, das auftritt, wenn der Benutzer auf das Element doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="71b01-121">Handles an event that occurs when the user double-clicks the element.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="71b01-122">onendalphablend</span><span class="sxs-lookup"><span data-stu-id="71b01-122">onendalphablend</span></span>](onendalphablend.md)          | <span data-ttu-id="71b01-123">Behandelt ein Ereignis, das auftritt, wenn ein Element einen **alphablendto** -Vorgang abschließt.</span><span class="sxs-lookup"><span data-stu-id="71b01-123">Handles an event that occurs when an element completes an **alphaBlendTo** operation.</span></span>                                                                                                                                         |
| [<span data-ttu-id="71b01-124">onendmove</span><span class="sxs-lookup"><span data-stu-id="71b01-124">onendmove</span></span>](onendmove.md)                      | <span data-ttu-id="71b01-125">Behandelt ein Ereignis, das auftritt, **Wenn ein Element einen Vorgang vom** Typ "Vorgang" abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="71b01-125">Handles an event that occurs when an element completes a **moveTo** operation.</span></span>                                                                                                                                                |
| [<span data-ttu-id="71b01-126">onfocus</span><span class="sxs-lookup"><span data-stu-id="71b01-126">onfocus</span></span>](onfocus.md)                          | <span data-ttu-id="71b01-127">Behandelt ein Ereignis, das auftritt, wenn das Element den Tastaturfokus erhält.</span><span class="sxs-lookup"><span data-stu-id="71b01-127">Handles an event that occurs when the element receives the keyboard focus.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="71b01-128">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="71b01-128">onkeydown</span></span>](onkeydown.md)                      | <span data-ttu-id="71b01-129">Behandelt ein Ereignis, das auftritt, wenn eine Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="71b01-129">Handles an event that occurs when a key is pressed.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="71b01-130">OnKeyPress</span><span class="sxs-lookup"><span data-stu-id="71b01-130">onkeypress</span></span>](onkeypress.md)                    | <span data-ttu-id="71b01-131">Behandelt ein Ereignis, das auftritt, wenn der Benutzer einen alphanumerischen Schlüssel drückt.</span><span class="sxs-lookup"><span data-stu-id="71b01-131">Handles an event that occurs when the user presses an alphanumeric key.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="71b01-132">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="71b01-132">onkeyup</span></span>](onkeyup.md)                          | <span data-ttu-id="71b01-133">Behandelt ein Ereignis, das auftritt, wenn eine Taste losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="71b01-133">Handles an event that occurs when a key is released.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="71b01-134">"OnMouseDown"</span><span class="sxs-lookup"><span data-stu-id="71b01-134">onmousedown</span></span>](onmousedown.md)                  | <span data-ttu-id="71b01-135">Behandelt ein Ereignis, das auftritt, wenn der Benutzer auf eine Maustaste klickt.</span><span class="sxs-lookup"><span data-stu-id="71b01-135">Handles an event that occurs when the user clicks a mouse button.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="71b01-136">OnMouseMove</span><span class="sxs-lookup"><span data-stu-id="71b01-136">onmousemove</span></span>](onmousemove.md)                  | <span data-ttu-id="71b01-137">Behandelt ein Ereignis, das auftritt, wenn der Benutzer den Mauszeiger bewegt, während er sich über einem Element befindet.</span><span class="sxs-lookup"><span data-stu-id="71b01-137">Handles an event that occurs when the user moves the mouse pointer while it is over an element.</span></span>                                                                                                                               |
| [<span data-ttu-id="71b01-138">onmouout</span><span class="sxs-lookup"><span data-stu-id="71b01-138">onmouseout</span></span>](onmouseout.md)                    | <span data-ttu-id="71b01-139">Behandelt ein Ereignis, das auftritt, wenn der Benutzer den Mauszeiger vom Element bewegt.</span><span class="sxs-lookup"><span data-stu-id="71b01-139">Handles an event that occurs when the user moves the pointer off the element.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="71b01-140">"onmouseover</span><span class="sxs-lookup"><span data-stu-id="71b01-140">onmouseover</span></span>](onmouseover.md)                  | <span data-ttu-id="71b01-141">Behandelt ein Ereignis, das auftritt, wenn der Benutzer den Mauszeiger über das Element platziert.</span><span class="sxs-lookup"><span data-stu-id="71b01-141">Handles an event that occurs when the user first places the pointer over the element.</span></span>                                                                                                                                         |
| [<span data-ttu-id="71b01-142">OnMouseUp</span><span class="sxs-lookup"><span data-stu-id="71b01-142">onmouseup</span></span>](onmouseup.md)                      | <span data-ttu-id="71b01-143">Behandelt ein Ereignis, das auftritt, wenn der Benutzer eine Maustaste loslässt, während sich der Mauszeiger über dem Element befindet.</span><span class="sxs-lookup"><span data-stu-id="71b01-143">Handles an event that occurs when the user releases a mouse button while the pointer is over the element.</span></span>                                                                                                                     |
| [<span data-ttu-id="71b01-144">OnResize</span><span class="sxs-lookup"><span data-stu-id="71b01-144">onresize</span></span>](onresize.md)                        | <span data-ttu-id="71b01-145">Behandelt ein Ereignis, das auftritt, wenn die Größe eines Steuer Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="71b01-145">Handles an event that occurs when a control resizes.</span></span>                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="71b01-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71b01-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71b01-147">**Ambient-Ereignis Attribute**</span><span class="sxs-lookup"><span data-stu-id="71b01-147">**Ambient Event Attributes**</span></span>](ambient-event-attributes.md)
</dt> <dt>

[<span data-ttu-id="71b01-148">**Referenz zur Skin-Programmierung**</span><span class="sxs-lookup"><span data-stu-id="71b01-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 





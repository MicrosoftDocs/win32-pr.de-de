---
title: Eigenschaften, Methoden und Ereignisse
description: Eigenschaften, Methoden und Ereignisse
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Windows Media Player, Eigenschaften für das Objektmodell
- Windows Media Player, Methoden für das Objektmodell
- Windows Media Player, Ereignisse für das Objektmodell
- Windows Media Player-Objektmodell, Eigenschaften
- Windows Media Player-Objektmodell, Methoden
- Windows Media Player-Objektmodell, Ereignisse
- Objektmodell, Eigenschaften
- Objektmodell, Methoden
- Objektmodell, Ereignisse
- Windows Media Player ActiveX-Steuerelement, Eigenschaften für das Objektmodell
- ActiveX-Steuerelement, Eigenschaften für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Eigenschaften für das Objektmodell
- Windows Media Player Mobile, Eigenschaften für das Objektmodell
- Windows Media Player ActiveX-Steuerelement, Methoden für das Objektmodell
- ActiveX-Steuerelement, Methoden für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Methoden für das Objektmodell
- Windows Media Player Mobile, Methoden für das Objektmodell
- Windows Media Player ActiveX-Steuerelement, Ereignisse für das Objektmodell
- ActiveX-Steuerelement, Ereignisse für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Ereignisse für das Objektmodell
- Windows Media Player Mobile, Ereignisse für das Objektmodell
- Eigenschaften, Windows Media Player-Objektmodell
- Methoden, Windows Media Player-Objektmodell
- Ereignisse, Windows Media Player-Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100730"
---
# <a name="properties-methods-and-events"></a><span data-ttu-id="6eca3-127">Eigenschaften, Methoden und Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6eca3-127">Properties, Methods and Events</span></span>

<span data-ttu-id="6eca3-128">Jedes-Objekt verfügt über Methoden und Eigenschaften, über die Sie das Windows Media Player-Steuerelement programmieren können.</span><span class="sxs-lookup"><span data-stu-id="6eca3-128">Each object has methods and properties through which you can program the Windows Media Player control.</span></span> <span data-ttu-id="6eca3-129">Eine Methode ist eine Aktion, die das Objekt ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="6eca3-129">A method is an action that the object can take.</span></span> <span data-ttu-id="6eca3-130">Eine Eigenschaft ist ein Datenwert, den Sie lesen oder ändern können.</span><span class="sxs-lookup"><span data-stu-id="6eca3-130">A property is a data value that you can read or change.</span></span> <span data-ttu-id="6eca3-131">Die **Play** -Methode startet z. b. die Wiedergabe des Inhalts, und die Framerate-Eigenschaft gibt die aktuelle **Framerate** der wiedergegebenen Inhalte an.</span><span class="sxs-lookup"><span data-stu-id="6eca3-131">For example, the **Play** method starts the content playing, and the **frameRate** property indicates the current frame rate of the content that is playing.</span></span>

<span data-ttu-id="6eca3-132">Außerdem löst das **Player** -Objekt Ereignisse aus, die Ihnen die Möglichkeit bieten, Aktionen zu bestimmten Zeiten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6eca3-132">In addition, the **Player** object raises events that give you the opportunity to carry out actions at specific times.</span></span> <span data-ttu-id="6eca3-133">Sie schreiben Code in einem Ereignishandler, der ausgeführt wird, wenn Windows Media Player das entsprechende Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="6eca3-133">You write code in an event handler that will execute when Windows Media Player raises the corresponding event.</span></span> <span data-ttu-id="6eca3-134">Sie können z. b. Code in einem **PlayStateChange** -Ereignishandler schreiben, der bestimmt, ob die Änderung des Zustands lautet, dass das Medium beendet wurde. wenn dies der Fall ist, wird ein Dialogfeld mit der Frage angezeigt, ob die Medien wiedergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6eca3-134">For example, you can write code in a **PlayStateChange** event handler that determines whether the change in state is that the media ended and if so display a dialog box asking users if they want to play the media again.</span></span>

> [!Note]  
> <span data-ttu-id="6eca3-135">Alle Methoden im Windows Media Player-Objektmodell sind asynchron.</span><span class="sxs-lookup"><span data-stu-id="6eca3-135">All of the methods in the Windows Media Player object model are asynchronous.</span></span> <span data-ttu-id="6eca3-136">Wenn Sie zwei Methoden in derselben Prozedur aufrufen, kann die zweite Methode nicht darauf basieren, dass die erste Methode ihre Aktion abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="6eca3-136">If you call two methods in the same procedure, the second method cannot rely on the first method having completed its action.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6eca3-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6eca3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eca3-138">**Informationen zum Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="6eca3-138">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 





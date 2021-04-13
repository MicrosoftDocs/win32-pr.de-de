---
title: Ausblenden des Windows Media Player-Steuer Elements
description: Ausblenden des Windows Media Player-Steuer Elements
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement, Webseiten
- ActiveX-Steuerelement, Webseiten
- Einbettungen, Webseiten
- Windows Media Player, Ausblenden des ActiveX-Steuer Elements
- Windows Media Player-Objektmodell, Ausblenden des ActiveX-Steuer Elements
- Objektmodell, Ausblenden des ActiveX-Steuer Elements
- Windows Media Player Mobile, hidingactivex-Steuerelement
- Windows Media Player ActiveX-Steuerelement, ausblenden
- Windows Media Player Mobile ActiveX-Steuerelement, ausblenden
- ActiveX-Steuerelement, ausblenden
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement, Webseiten
- ActiveX-Steuerelement, Webseiten
- Seiten Einbettung, Ausblenden des ActiveX-Steuer Elements
- Ausblenden von Windows Media Player ActiveX-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310768"
---
# <a name="hiding-the-windows-media-player-control"></a><span data-ttu-id="00227-126">Ausblenden des Windows Media Player-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="00227-126">Hiding the Windows Media Player Control</span></span>

<span data-ttu-id="00227-127">Das Windows-Media Player ActiveX-Objekt wird mit dem Object-Element in eine Webseite eingebettet.</span><span class="sxs-lookup"><span data-stu-id="00227-127">The Windows Media Player ActiveX object is embedded in a webpage using the OBJECT element.</span></span> <span data-ttu-id="00227-128">Im Gegensatz zu früheren Versionen muss das Object-Element, das Windows-Media Player definiert, im body-Abschnitt einer Webseite zwischen den Tags <BODY> und </BODY> abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="00227-128">Unlike earlier versions, the OBJECT element that defines Windows Media Player must be placed in the BODY section of a webpage, between the <BODY> and </BODY> tags.</span></span> <span data-ttu-id="00227-129">Das Platzieren des Windows-Media Player ActiveX-Objekts im Head-Abschnitt einer Webseite, um die Benutzeroberfläche auszublenden, kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="00227-129">Placing the Windows Media Player ActiveX object in the HEAD section of a webpage to hide the user interface can produce unexpected results.</span></span>

<span data-ttu-id="00227-130">Wenn Sie das Windows Media Player ActiveX-Steuerelement im body-Abschnitt einer Webseite ablegen, wird die Benutzeroberfläche des Steuer Elements angezeigt.</span><span class="sxs-lookup"><span data-stu-id="00227-130">If you put the Windows Media Player ActiveX control in the BODY section of a webpage, the control user interface will be displayed.</span></span> <span data-ttu-id="00227-131">Wenn Sie nicht möchten, dass Sie angezeigt wird, und Sie eine eigene Benutzeroberfläche erstellen möchten, legen Sie die Attribute height und Width des Object-Elements auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="00227-131">If you do not want it to be displayed, and wish to create your own user interface, set the height and width attributes of the OBJECT element to zero.</span></span>

<span data-ttu-id="00227-132">Das Steuerelement kann auch durch Festlegen des *Players* unsichtbar gemacht werden. **uiMode** -Eigenschaft auf "unsichtbar".</span><span class="sxs-lookup"><span data-stu-id="00227-132">The control can also be made invisible by setting the *Player*.**uiMode** property to "invisible".</span></span> <span data-ttu-id="00227-133">Dies kann mithilfe eines param-Tags erfolgen, wie im nächsten Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="00227-133">This can be done using a PARAM tag as discussed in the next section.</span></span> <span data-ttu-id="00227-134">In diesem Fall ist der Speicherplatz für das Steuerelement mit Höhe und Breite reserviert, aber im reservierten Bereich wird nichts angezeigt, bis **uiMode** in etwas anderes als "unsichtbar" geändert wird.</span><span class="sxs-lookup"><span data-stu-id="00227-134">In this case, space is reserved for the control using height and width, but nothing is displayed in the reserved space until **uiMode** is changed to something other than "invisible".</span></span>

## <a name="related-topics"></a><span data-ttu-id="00227-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00227-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00227-136">**Verwenden des Windows Media Player-Steuer Elements in einer Webseite**</span><span class="sxs-lookup"><span data-stu-id="00227-136">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 





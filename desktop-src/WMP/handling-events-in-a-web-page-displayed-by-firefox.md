---
title: Behandeln von Ereignissen in einer Webseite, die von Firefox angezeigt wird
description: Behandeln von Ereignissen in einer Webseite, die von Firefox angezeigt wird
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
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
- Windows Media Player ActiveX-Steuerelement, Ereignis Behandlung
- Windows Media Player Mobile ActiveX-Steuerelement, Ereignis Behandlung
- ActiveX-Steuerelement, Ereignis Behandlung
- Einbettungen, Webseiten
- Einbettung von Webseiten, Ereignis Behandlung
- Windows Media Player, Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX-Steuerelement, Firefox
- Windows Media Player Mobile ActiveX-Steuerelement, Firefox
- ActiveX-Steuerelement, Firefox
- Firefox, Ereignis Behandlung
- Einbettung von Webseiten, Firefox
- Ereignisse, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9659d1920ffc4d5e39f4cd44e15e24b08f6ddc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311687"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="badae-128">Behandeln von Ereignissen in einer Webseite, die von Firefox angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="badae-128">Handling Events in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="badae-129">Wenn Sie das Windows Media Player-Steuerelement in eine Webseite einbetten, können Sie Skripts schreiben, mit denen Ereignisse behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="badae-129">When you embed the Windows Media Player control in a webpage, you can write script that handles events.</span></span> <span data-ttu-id="badae-130">Eine Liste der Ereignisse, die vom Player-Steuerelement ausgelöst werden, finden Sie unter [Player-Objekt](player-object.md).</span><span class="sxs-lookup"><span data-stu-id="badae-130">For a list of events raised by the Player control, see [Player Object](player-object.md).</span></span>

<span data-ttu-id="badae-131">Wenn der MIME-Typ, der einem eingebetteten Player-Steuerelement zugeordnet ist, application/x-MS-WMP ist, können Sie Ereignishandler schreiben, die das folgende Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="badae-131">If the mime type associated with an embedded Player control is application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



<span data-ttu-id="badae-132">Dabei ist *EventName* der Name eines Windows Media Player-Ereignisses, und *para* Meters ist eine Liste der Parameter des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="badae-132">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="badae-133">Der folgende Code enthält z. b. einen Handler für das [PlayStateChange](player-player-playstatechange.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="badae-133">For example, the following code has a handler for the [PlayStateChange](player-player-playstatechange.md) event.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



<span data-ttu-id="badae-134">Wenn Sie über mehrere Instanzen des Player-Steuer Elements auf einer Webseite verfügen und das im vorangehenden Beispiel gezeigte Format verwenden, ist jeder Ereignishandler an eine bestimmte Instanz des Player-Steuer Elements gebunden.</span><span class="sxs-lookup"><span data-stu-id="badae-134">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to a specific instance of the Player control.</span></span> <span data-ttu-id="badae-135">Im vorangehenden Beispiel wird der Ereignishandler nur aufgerufen, wenn sich der Wiedergabe Zustand für das Steuerelement mit ID = "Player" ändert.</span><span class="sxs-lookup"><span data-stu-id="badae-135">In the preceeding example, the event handler is called only when the play state changes for the control that has id="Player".</span></span>

<span data-ttu-id="badae-136">Wenn der MIME-Typ, der einem eingebetteten Player-Steuerelement zugeordnet ist, nicht application/x-MS-WMP ist, können Sie Ereignishandler schreiben, die das folgende Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="badae-136">If the mime type associated with an embedded Player control is not application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



<span data-ttu-id="badae-137">Dabei ist *EventName* der Name eines Windows Media Player-Ereignisses, und *para* Meters ist eine Liste der Parameter des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="badae-137">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="badae-138">Der folgende Code enthält z. b. einen Handler für das **PlayStateChange** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="badae-138">For example, the following code has a handler for the **PlayStateChange** event.</span></span>


```HTML
<OBJECT id="Player" type="application/asx" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Test.asx"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT>
  function OnDSPlayStateChangeEvt(NewState)
  {
    p1.innerHTML = "Play state: " + NewState;
  }
</SCRIPT>

```



<span data-ttu-id="badae-139">Wenn Sie über mehrere Instanzen des Player-Steuer Elements auf einer Webseite verfügen und das im vorangehenden Beispiel gezeigte Format verwenden, ist jeder Ereignishandler an alle Instanzen des Player-Steuer Elements gebunden, und der Ereignishandler wird aufgerufen, wenn sich der Wiedergabe Zustand für ein Player-Steuerelement auf der Seite ändert.</span><span class="sxs-lookup"><span data-stu-id="badae-139">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to all instances of the Player control and the event handler is called when the play state changes for any Player control on the page.</span></span>

> [!Note]  
> <span data-ttu-id="badae-140">Wenn der MIME-Typ nicht application/x-MS-WMP ist, wird das **Double Click** -Ereignis als ondsdblclickevt (nicht ondsdoubleclickevt) gesendet, um die Kompatibilität mit Version 6,4 des Player-Steuer Elements zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="badae-140">If the mime type is not application/x-ms-wmp, the **DoubleClick** event is sent as OnDSDblClickEvt (not OnDSDoubleClickEvt) for compatibility with version 6.4 of the Player control.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="badae-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="badae-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="badae-142">**Verwenden des Windows Media Player-Steuer Elements mit Firefox**</span><span class="sxs-lookup"><span data-stu-id="badae-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 





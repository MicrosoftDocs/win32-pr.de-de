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
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Behandeln von Ereignissen in einer Webseite, die von Firefox angezeigt wird

Wenn Sie das Windows Media Player-Steuerelement in eine Webseite einbetten, können Sie Skripts schreiben, mit denen Ereignisse behandelt werden. Eine Liste der Ereignisse, die vom Player-Steuerelement ausgelöst werden, finden Sie unter [Player-Objekt](player-object.md).

Wenn der MIME-Typ, der einem eingebetteten Player-Steuerelement zugeordnet ist, application/x-MS-WMP ist, können Sie Ereignishandler schreiben, die das folgende Format aufweisen:


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



Dabei ist *EventName* der Name eines Windows Media Player-Ereignisses, und *para* Meters ist eine Liste der Parameter des Ereignisses. Der folgende Code enthält z. b. einen Handler für das [PlayStateChange](player-player-playstatechange.md) -Ereignis.


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



Wenn Sie über mehrere Instanzen des Player-Steuer Elements auf einer Webseite verfügen und das im vorangehenden Beispiel gezeigte Format verwenden, ist jeder Ereignishandler an eine bestimmte Instanz des Player-Steuer Elements gebunden. Im vorangehenden Beispiel wird der Ereignishandler nur aufgerufen, wenn sich der Wiedergabe Zustand für das Steuerelement mit ID = "Player" ändert.

Wenn der MIME-Typ, der einem eingebetteten Player-Steuerelement zugeordnet ist, nicht application/x-MS-WMP ist, können Sie Ereignishandler schreiben, die das folgende Format aufweisen:


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



Dabei ist *EventName* der Name eines Windows Media Player-Ereignisses, und *para* Meters ist eine Liste der Parameter des Ereignisses. Der folgende Code enthält z. b. einen Handler für das **PlayStateChange** -Ereignis.


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



Wenn Sie über mehrere Instanzen des Player-Steuer Elements auf einer Webseite verfügen und das im vorangehenden Beispiel gezeigte Format verwenden, ist jeder Ereignishandler an alle Instanzen des Player-Steuer Elements gebunden, und der Ereignishandler wird aufgerufen, wenn sich der Wiedergabe Zustand für ein Player-Steuerelement auf der Seite ändert.

> [!Note]  
> Wenn der MIME-Typ nicht application/x-MS-WMP ist, wird das **Double Click** -Ereignis als ondsdblclickevt (nicht ondsdoubleclickevt) gesendet, um die Kompatibilität mit Version 6,4 des Player-Steuer Elements zu gewährleisten.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuer Elements mit Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 





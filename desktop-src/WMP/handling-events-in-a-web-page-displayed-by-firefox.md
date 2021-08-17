---
title: Behandeln von Ereignissen auf einer von Firefox angezeigten Webseite
description: Behandeln von Ereignissen auf einer von Firefox angezeigten Webseite
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
keywords:
- Windows Media Player,einbetten ActiveX Steuerelements
- Windows Media Player-Objektmodell, Einbetten ActiveX Steuerelement
- Objektmodell,Einbetten ActiveX Steuerelement
- Windows Media Player Mobil,einbetten ActiveX Steuerelement
- Windows Media Player ActiveX,Einbetten
- Windows Media Player Mobile ActiveX-Steuerelement,Einbetten
- ActiveX,Einbetten
- Windows Media Player ActiveX,Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement, Webseiten
- ActiveX,Webseiten
- Windows Media Player ActiveX,Ereignisbehandlung
- Windows Media Player Mobile ActiveX-Steuerelement, Ereignisbehandlung
- ActiveX,Ereignisbehandlung
- Einbetten, Webseiten
- Einbetten von Webseiten, Ereignisbehandlung
- Windows Media Player,Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player Mobil, Firefox
- Windows Media Player ActiveX,Firefox
- Windows Media Player Mobile ActiveX-Steuerelement,Firefox
- ActiveX,Firefox
- Firefox, Ereignisbehandlung
- Einbetten von Webseiten, Firefox
- events,Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e971caef18114b670678fc76d0515858bee77a94a5e3f8b5c24ca5322177b8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748415"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Behandeln von Ereignissen auf einer von Firefox angezeigten Webseite

Wenn Sie das Windows Media Player-Steuerelement in eine Webseite einbetten, können Sie ein Skript schreiben, das Ereignisse behandelt. Eine Liste der Ereignisse, die vom Player-Steuerelement ausgelöst werden, finden Sie unter [Player-Objekt](player-object.md).

Wenn der mime-Typ, der einem eingebetteten Player-Steuerelement zugeordnet ist, application/x-ms-wmp ist, können Sie Ereignishandler im folgenden Format schreiben:


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



Dabei *ist EventName* der Name eines Windows Media Player und *Params* eine Liste der Ereignisparameter. Der folgende Code enthält beispielsweise einen Handler für das [PlayStateChange-Ereignis.](player-player-playstatechange.md)


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



Wenn sie über mehrere Instanzen des Player-Steuerelements auf einer Webseite verfügen und das im voran sehenden Beispiel gezeigte Format verwenden, ist jeder Ereignishandler an eine bestimmte Instanz des Player-Steuerelements gebunden. Im voran folgenden Beispiel wird der Ereignishandler nur aufgerufen, wenn sich der Wiedergabezustand für das Steuerelement ändert, das id="Player" hat.

Wenn der mime-Typ, der einem eingebetteten Player-Steuerelement zugeordnet ist, nicht application/x-ms-wmp ist, können Sie Ereignishandler im folgenden Format schreiben:


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



Dabei *ist EventName* der Name eines Windows Media Player und *Params* eine Liste der Ereignisparameter. Der folgende Code enthält beispielsweise einen Handler für das **PlayStateChange-Ereignis.**


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



Wenn Sie über mehrere Instanzen des Player-Steuerelements auf einer Webseite verfügen und das im voranseitigen Beispiel gezeigte Format verwenden, ist jeder Ereignishandler an alle Instanzen des Player-Steuerelements gebunden, und der Ereignishandler wird aufgerufen, wenn sich der Wiedergabezustand für ein Player-Steuerelement auf der Seite ändert.

> [!Note]  
> Wenn der MIME-Typ nicht application/x-ms-wmp ist, wird das **DoubleClick-Ereignis** aus Kompatibilitätsproblemen mit Version 6.4 des Player-Steuerelements als OnDSDblClickEvt (nicht OnDSDoubleClickEvt) gesendet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuerelements mit Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 





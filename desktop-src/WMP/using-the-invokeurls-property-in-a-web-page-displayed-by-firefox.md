---
title: Verwenden der invokeurls-Eigenschaft in einer Webseite, die von Firefox angezeigt wird
description: Verwenden der invokeurls-Eigenschaft in einer Webseite, die von Firefox angezeigt wird
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement, Webseiten
- Windows Media Player ActiveX-Steuerelement, invokeurls-Eigenschaft
- Windows Media Player Mobile ActiveX-Steuerelement, invokeurls (Eigenschaft)
- Einbettungen, Webseiten
- Aufbetten von Webseiten, invokeurls (Eigenschaft)
- Windows Media Player, Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player ActiveX-Steuerelement, Firefox
- ActiveX-Steuerelement, Firefox
- Firefox, invokeurls (Eigenschaft)
- Einbettung von Webseiten, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0a2eb96e65d8fa6d2758669e3c844b2d13c0bc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "106337622"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a>Verwenden der invokeurls-Eigenschaft in einer Webseite, die von Firefox angezeigt wird

Einige Mediendateien enthalten eingebettete URLs, für die Windows Media Player Webseiten in einem Webbrowser Fenster oder-Frame anzeigt, wenn die Mediendatei abgespielt wird. In Windows Internet Explorer können Sie mit der Eigenschaft [Settings. invokeurls](settings-invokeurls.md) angeben, ob Seiten für eingebettete URLs angezeigt werden, und Sie können mit der Eigenschaft [Settings. defaultframe](settings-defaultframe.md) einen Frame zum Anzeigen solcher Seiten angeben.

In Firefox sind einige Problem Umgehungen erforderlich, um die **invokeurls** -Eigenschaft festzulegen und einen Frame zum Anzeigen von Seiten für eingebettete URLs anzugeben.

## <a name="setting-the-invokeurls-property"></a>Festlegen der invokeurls-Eigenschaft

Der Standardwert der **Settings. invokeurls** -Eigenschaft ist true. Wenn Sie also den Wert false festlegen möchten, müssen Sie ihn explizit festlegen. In Internet Explorer können Sie **invokeurls** in einem param-Element innerhalb des Objekt Elements des Player-Steuer Elements auf false festlegen.

Das Plug-in für Firefox unterstützt das Festlegen der **invokeurls** -Eigenschaft in einem param-Element nicht.

Sie können diese Einschränkung umgehen, indem Sie die **invokeurls** -Eigenschaft im Skript festlegen. Der folgende Code zeigt, wie die **invokeurls** -Eigenschaft auf einer Webseite, die sowohl von Internet Explorer als auch von Firefox angezeigt werden kann, auf false festgelegt wird.


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

  </BODY>
</HTML>

```



## <a name="displaying-webpages-in-a-frame"></a>Anzeigen von Webseiten in einem Frame

Eine Mediendatei kann URLs enthalten, in denen Webseiten in einem Browserfenster oder-Frame angezeigt werden, während die Mediendatei wiedergegeben wird. In Internet Explorer können Sie die Eigenschaft [Settings. defaultframe](settings-defaultframe.md) verwenden, um den Frame anzugeben, in dem diese Seiten angezeigt werden. Wenn Sie die **defaultframe** -Eigenschaft nicht festlegen, werden URLs in einem separaten Fenster des Standard Browsers angezeigt. Das Firefox-Plug-in unterstützt jedoch nicht die **Settings. defaultframe** -Eigenschaft. Um diese Einschränkung zu umgehen, legen Sie die Eigenschaft **Settings. invokeurls** auf false fest, und schreiben Sie einen [ScriptCommand](player-player-scriptcommand.md) -Ereignishandler, der den Speicherort des Zielframes festlegt. Das folgende Beispiel, das in Internet Explorer und Firefox funktioniert, veranschaulicht diese Vorgehensweise. Angenommen, die im Beispiel gezeigte Webseite wird in Frames 0 angezeigt, \[ \] und Sie möchten, dass die Seite der URL in Frames \[ 1 angezeigt wird \] .


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

    <SCRIPT for="Player" event="ScriptCommand(scType, scParam)">
      if( scType == "URL" )
      {
        parent.frames[1].location = scParam;
      }
    </script>

  </BODY>
</HTML>

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuer Elements mit Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 





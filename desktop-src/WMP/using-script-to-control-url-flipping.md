---
title: Verwenden des Skripts zum Steuern des URL-Flippings
description: Verwenden des Skripts zum Steuern des URL-Flippings
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player,Webbasierte Präsentationen
- Windows Media Player Objektmodell, webbasierte Präsentationen
- Objektmodell, webbasierte Präsentationen
- Windows Media Player Mobile, webbasierte Präsentationen
- Windows Media Player ActiveX-Steuerelement, webbasierte Präsentationen
- Windows Media Player Mobile ActiveX-Steuerelement, webbasierte Präsentationen
- ActiveX,Webbasierte Präsentationen
- Windows Media Player,URL-Flipping
- Windows Media Player-Objektmodell, URL-Flipping
- Objektmodell, URL-Flipping
- Windows Media Player Mobil, URL-Flipping
- Windows Media Player ActiveX,URL-Flipping
- Windows Media Player Mobiles ActiveX-Steuerelement, URL-Flipping
- ActiveX,URL-Flipping
- Webbasierte Präsentationen, URL-Flipping
- Erstellen webbasierter Präsentationen, URL-Flipping
- URL-Flipping
- Windows Media Player,Rich Media Streaming
- Windows Media Player-Objektmodell, Rich Media-Streaming
- Objektmodell, Rich Media Streaming
- Windows Media Player Mobil,Rich Media-Streaming
- Windows Media Player ActiveX,Rich Media Streaming
- Windows Media Player Mobile ActiveX-Steuerelement,Rich Media-Streaming
- ActiveX,Rich Media Streaming
- Webbasierte Präsentationen, Rich Media Streaming
- Erstellen webbasierter Präsentationen, Rich Media Streaming
- Rich Media Streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9470bf2b812d36bceb6159ab089e3b08c49bc84515320872b125ed6519568141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507130"
---
# <a name="using-script-to-control-url-flipping"></a>Verwenden des Skripts zum Steuern des URL-Flippings

Wenn ein Benutzer eine Verbindung mit einem Rich Media-Stream herstellt, während der Stream bereits ausgeführt wird, kann die gestreamte Webseite angezeigt werden, bevor alle Elemente eintreffen und zwischengespeichert wurden, wenn Windows Media Player die URL automatisch aufruft. In diesem Fall wird dem Benutzer eine leere oder unvollständige Webseite angezeigt, bis der nächste Satz von Daten im Cache eintrifft.

Sie können die Anzeige einer leeren oder unvollständigen Webseite vermeiden, indem Sie die URL mithilfe eines Skripts aufrufen, anstatt Windows Media Player automatisch ausführen zu lassen. Auf diese Weise können Sie den ersten URL-Flip ignorieren und dann nachfolgende URLs mithilfe von Skriptcode aufrufen.

> [!Note]  
> In diesem Abschnitt wird davon ausgegangen, dass Sie HTML mit dem Windows Media Encoder 9 Series SDK streamen und dass Sie den HTML-Stream so festgelegt haben, dass er wiederholt wird.

 

Zunächst müssen Sie eine Framesetwebseite erstellen, die den Frame mit dem eingebetteten Player und den Frame enthält, der den Streaming-HTML-Code anzeigt. Jeder dieser beiden Frames zeigt zunächst eine separate Webseite an, sodass Sie insgesamt drei Webseiten erstellen. Der folgende Beispielcode veranschaulicht die Framesetwebseite:


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



Das vorherige Webseitenbeispiel enthält zwei Frames. Der erste Frame wird in der linken Hälfte des Browserfensters angezeigt, und die Webseite mit dem Namen embed \_player.htm. Mit dem folgenden Beispielcode wird diese Webseite erstellt:


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



Der zweite Frame im Frameset wird in der rechten Hälfte des Browserfensters angezeigt und zeigt eine Webseite mit dem Namen "blank.htm" an. Mit dem folgenden Beispielcode wird diese Webseite erstellt:


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



Wenn die Framesetseite im Browser geladen wird, zeigt der linke Frame den eingebetteten Player und der rechte Frame den Text "Loading..." (Laden...) an. , um den Benutzer darüber zu informieren, dass weitere Daten in Kürze geplant sind. Wenn der erste URL-Skriptbefehl aus dem HTML-Stream eintrifft, ändert der Ereignishandler einfach den Wert des **booleschen Flags.** Wenn jeder nachfolgende URL-Skriptbefehl aus dem HTML-Stream eintrifft, lädt das Skript im Ereignishandler die neue URL in den Frame mit dem Namen "content", und die vollständige Webseite wird im Frame in der rechten Hälfte des Browserfensters angezeigt.

Weitere Informationen zum Streamen von HTML mit Windows Media finden Sie im Windows Media Encoder SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Rich Media Streaming**](rich-media-streaming.md)
</dt> <dt>

[**URL-Flipping**](url-flipping.md)
</dt> </dl>

 

 





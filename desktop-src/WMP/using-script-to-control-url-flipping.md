---
title: Verwenden von Skripts zum Steuern von URL-Flipping
description: Verwenden von Skripts zum Steuern von URL-Flipping
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player, webbasierte Präsentationen
- Windows Media Player-Objektmodell, webbasierte Präsentationen
- Objektmodell, webbasierte Präsentationen
- Windows Media Player Mobile, webbasierte Präsentationen
- Windows Media Player ActiveX-Steuerelement, webbasierte Präsentationen
- Windows Media Player Mobile ActiveX-Steuerelement, webbasierte Präsentationen
- ActiveX-Steuerelement, webbasierte Präsentationen
- Windows Media Player, URL-kippen
- Windows Media Player-Objektmodell, URL-kippen
- Objektmodell, URL-kippen
- Windows Media Player Mobile, URL-kippen
- Windows Media Player ActiveX-Steuerelement, URL-kippen
- Windows Media Player Mobile ActiveX-Steuerelement, URL-kippen
- ActiveX-Steuerelement, URL-kippen
- Webbasierte Präsentationen, URL-kippen
- Erstellen von webbasierten Präsentationen, URL-kippen
- URL-kippen
- Windows Media Player, Rich-Media-Streaming
- Windows Media Player-Objektmodell, Rich-Media-Streaming
- Objektmodell, Rich-Media-Streaming
- Windows Media Player Mobile, Rich-Media-Streaming
- Windows Media Player ActiveX-Steuerelement, Rich-Media-Streaming
- Windows Media Player Mobile ActiveX-Steuerelement, Rich-Media-Streaming
- ActiveX-Steuerelement, Rich-Media-Streaming
- Webbasierte Präsentationen, Rich-Media-Streaming
- Erstellen von webbasierten Präsentationen, Rich-Media-Streaming
- Rich-Media-Streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4815562bba92d67bb4b02ea0317d6c29accd9262
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "104388840"
---
# <a name="using-script-to-control-url-flipping"></a>Verwenden von Skripts zum Steuern von URL-Flipping

Wenn ein Benutzer eine Verbindung mit einem Rich-Media-Stream herstellt, während der Stream bereits ausgeführt wird, ist es möglich, dass die streamingwebseite angezeigt wird, bevor alle Elemente eingetroffen sind und zwischengespeichert wurden, wenn Windows Media Player die URL automatisch aufruft. Wenn dies der Fall ist, wird dem Benutzer eine leere oder unvollständige Webseite angezeigt, bis der nächste Satz von Daten im Cache ankommt.

Sie können vermeiden, dass eine leere oder unvollständige Webseite angezeigt wird, indem Sie die URL mithilfe eines Skripts aufrufen, anstatt Windows Media Player die automatische durchführen zu lassen. Auf diese Weise können Sie den ersten URL-Flip ignorieren und dann nachfolgende URLs mithilfe von Skriptcode aufrufen.

> [!Note]  
> In diesem Abschnitt wird davon ausgegangen, dass Sie HTML mit dem Windows Media Encoder 9-Reihe-SDK streamen und den HTML-Stream wiederholen.

 

Zunächst müssen Sie eine Frameset-Webseite erstellen, die den Frame mit dem eingebetteten Player und dem Frame enthält, in dem der Streaming-HTML-Code angezeigt wird. Bei jedem dieser beiden Frames wird anfänglich eine separate Webseite angezeigt, sodass Sie insgesamt drei Webseiten erstellen. Der folgende Beispielcode veranschaulicht die Frameset-Webseite:


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



Im vorherigen Beispiel für eine Webseite werden zwei Frames integriert. Der erste Frame wird in der linken Hälfte des Browserfensters angezeigt und zeigt die Webseite mit dem Namen Einbettungs \_player.htm an. Der folgende Beispielcode erstellt diese Webseite:


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



Der zweite Frame im Frameset wird in der rechten Hälfte des Browserfensters angezeigt und zeigt eine Webseite mit dem Namen "blank.htm" an. Der folgende Beispielcode erstellt diese Webseite:


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



Wenn die Frameset-Seite im Browser geladen wird, zeigt der linke Rahmen den eingebetteten Player an, und der Rechte Rahmen zeigt den Text "wird geladen..." , um den Benutzer darüber zu informieren, dass weitere Daten vorhanden sind. Wenn der erste URL-Skript Befehl aus dem HTML-Stream eintrifft, ändert der Ereignishandler einfach den Wert des **booleschen** Flags. Wenn jeder nachfolgende URL-Skript Befehl aus dem HTML-Stream eintrifft, lädt das Skript im Ereignishandler die neue URL in den Frame mit dem Namen "Content", und die gesamte Webseite wird in dem Frame angezeigt, der sich in der rechten Hälfte des Browserfensters befindet.

Weitere Informationen zum Streaming von HTML mithilfe von Windows-Medien finden Sie im Windows Media Encoder SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Rich-Media-Streaming**](rich-media-streaming.md)
</dt> <dt>

[**URL-Flipping**](url-flipping.md)
</dt> </dl>

 

 





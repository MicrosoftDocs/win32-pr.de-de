---
title: URL-Flipping
description: URL-Flipping
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "103714723"
---
# <a name="url-flipping"></a>URL-Flipping

Die Verwendung von Webseiten für Folien anzeigen wird als URL-Flipping bezeichnet und automatisch von Windows Media Player behandelt, wenn URL-Skript Befehle gefunden werden, die in den digitalen Mediendaten Strom eingebettet sind, der wiedergegeben wird. Sie können einen Zielframe für Ihre Seiten in jedem Skript Befehl angeben. Sie können ihn auch angeben, indem Sie die Eigenschaft **Settings. defaultframe** festlegen. Sie können diese Eigenschaft im Skriptcode oder mit einem param-Element innerhalb des Object-Elements festlegen, das das Windows Media Player-Steuerelement einbettet.

Sie können die URL-Skript Befehle in Ihrem JScript-Code genauso wie benutzerdefinierte Skript Befehle verarbeiten. Wenn Sie möchten, dass das Windows Media Player-Steuerelement URL-Skript Befehle ignoriert, damit Sie sie vollständig selbst verarbeiten können, legen Sie die *Einstellungen* fest. die **invokeurls** -Eigenschaft ist entweder im Skriptcode oder bei Verwendung eines Param-Elements wie zuvor beschrieben zu false.

Das folgende Beispiel veranschaulicht ein typisches Frameset für das URL-Flipping. Erstellen Sie zunächst eine Seite, die das Frameset beschreibt:


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



Erstellen Sie als nächstes die player.html-Datei, auf die im Frameset verwiesen wird, indem Sie den folgenden Code verwenden (es wird angenommen, dass die Datei "Video. wmv" im gleichen Verzeichnis wie die HTML-Dateien vorhanden ist):


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



Wenn Ihre Webseiten so klein sind, dass Sie schnell geladen werden können, genügt diese Einrichtung ggf. für Ihre Anforderungen. Wenn andererseits ihre Webseiten komplex sind, kann das umfangreiche Medien Streaming abhängig von der Verbindungsgeschwindigkeit Ihrer Zielgruppe effektiver sein.

> [!Note]  
> Das URL-kippen funktioniert nicht ordnungsgemäß mit Seiten, die im Netscape Navigator angezeigt werden. Anstatt in dem von **defaultframe** angegebenen Frame angezeigt zu werden, zeigt jeder im Navigator empfangene URL-Skript Befehl die URL in einem neuen Browserfenster an.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Web-Based Präsentationen**](creating-web-based-presentations.md)
</dt> <dt>

[**Verwenden von Skripts zum Steuern von URL-Flipping**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 





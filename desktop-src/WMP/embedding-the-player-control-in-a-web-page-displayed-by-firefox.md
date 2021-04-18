---
title: Einbetten des Player-Steuer Elements in eine von Firefox angezeigte Webseite
description: Einbetten des Player-Steuer Elements in eine von Firefox angezeigte Webseite
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
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
- Windows Media Player, Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX-Steuerelement, Firefox
- Windows Media Player Mobile ActiveX-Steuerelement, Firefox
- ActiveX-Steuerelement, Firefox
- Firefox, Informationen zum Einbetten von Webseiten
- Einbettungen, Webseiten
- Einbettung von Webseiten, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16063ea07a0262ab798e58ed02e4d5a5b6b5d65
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "106338023"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Einbetten des Player-Steuer Elements in eine von Firefox angezeigte Webseite

Wenn Sie das Windows Media Player-Steuerelement in eine Webseite einbetten möchten, die von einem Firefox-Browser angezeigt werden kann, erstellen Sie ein Objekt Element oder ein Einbettungs Element, das einen der folgenden MIME-Typen als **Type** -Attribut aufweist:

-   Anwendung/x-MS-WMP
-   Anwendung/ASX
-   Video/x-ms-ASF-Plugin
-   Application/x-Mplayer2
-   Video/x-ms-ASF
-   Video/x-ms-WM
-   Audiodatei/x-ms-WMA
-   Audiodatei/x-ms-Wax
-   Video/x-ms-WMV
-   Video/x-ms-wvx

Der bevorzugte MIME-Typ ist "application/x-MS-WMP".

In den folgenden Beispielen wird veranschaulicht, wie das Player-Steuerelement mit einem Object-Element oder einem Einbettungs Element eingebettet wird.


```HTML
<OBJECT id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320">
  <PARAM name="autostart" value="false"/>
</OBJECT>

<EMBED id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320"
  autostart="false"/>

```



Die vorangehenden Beispiele funktionieren in Firefox, aber nicht in Internet Explorer. Wenn Sie das Player-Steuerelement in eine Webseite einbetten möchten, die von Internet Explorer angezeigt werden kann, müssen Sie ein Object-Element erstellen, dessen **ClassID-** Attribut auf die Klassen-ID des Windows Media Player-Steuer Elements festgelegt ist.

Im folgenden Beispiel wird gezeigt, wie Sie das Windows Media Player-Steuerelement in eine Webseite einbetten, die sowohl von Internet Explorer als auch von Firefox richtig angezeigt werden kann. Skript auf der Seite erkennt den Browsertyp und generiert das entsprechende Objekttag.


```HTML
<HTML>
  <BODY>
    <SCRIPT type="text/javascript">
      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {
        document.write('<OBJECT id="Player"');
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');
        document.write(' width=300 height=200></OBJECT>');
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {
        document.write('<OBJECT id="Player"'); 
        document.write(' type="application/x-ms-wmp"'); 
        document.write(' width=300 height=200></OBJECT>');
      }         
    </SCRIPT>
  </BODY>
</HTML>

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuer Elements mit Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 





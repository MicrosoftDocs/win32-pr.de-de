---
title: Einbetten des Player-Steuerelements in eine webseite, die von Firefox angezeigt wird
description: Einbetten des Player-Steuerelements in eine webseite, die von Firefox angezeigt wird
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Windows Media Player,Einbetten ActiveX Steuerelements
- Windows Media Player-Objektmodell, Einbetten ActiveX Steuerelement
- Objektmodell,Einbetten ActiveX Steuerelement
- Windows Media Player Mobil,einbetten ActiveX Steuerelement
- Windows Media Player ActiveX,Einbetten
- Windows Media Player Mobile ActiveX-Steuerelement,Einbetten
- ActiveX,Einbetten
- Windows Media Player ActiveX,Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement,Webseiten
- ActiveX,Webseiten
- Windows Media Player,Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player Mobil, Firefox
- Windows Media Player ActiveX,Firefox
- Windows Media Player Mobile ActiveX-Steuerelement,Firefox
- ActiveX,Firefox
- Firefox,Informationen zum Einbetten von Webseiten
- Einbetten, Webseiten
- Einbetten von Webseiten, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c1db799df78cb6c62516798f4bbd196c093f02225386f0c1009bfa11d9a668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578587"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Einbetten des Player-Steuerelements in eine webseite, die von Firefox angezeigt wird

Um das Windows Media Player-Steuerelement in eine Webseite einbetten zu können, die von einem Firefox-Browser angezeigt werden kann, erstellen  Sie ein OBJECT-Element oder ein EMBED-Element, das einen der folgenden MIME-Typen als Typattribut hat:

-   application/x-ms-wmp
-   application/asx
-   video/x-ms-asf-plugin
-   application/x-mplayer2
-   video/x-ms-asf
-   video/x-ms-wm
-   audio/x-ms-wma
-   audio/x-ms-audio
-   video/x-ms-wmv
-   video/x-ms-wvx

Der bevorzugte MIME-Typ ist application/x-ms-wmp.

In den folgenden Beispielen wird gezeigt, wie Sie das Player-Steuerelement mithilfe eines OBJECT-Elements oder eines EMBED-Elements einbetten.


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



Die folgenden Beispiele funktionieren in Firefox, aber nicht in Internet Explorer. Um das Player-Steuerelement in eine Webseite einbetten zu können, die von Internet Explorer angezeigt werden kann, müssen Sie ein OBJECT-Element erstellen, für das ein **classid-Attribut** auf die Klassen-ID des Windows Media Player festgelegt ist.

Das folgende Beispiel zeigt, wie Sie das Windows Media Player-Steuerelement in eine Webseite einbetten, die sowohl von Internet Explorer firefox korrekt angezeigt werden kann. Das Skript auf der Seite erkennt den Browsertyp und generiert das entsprechende OBJECT-Tag.


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

[**Verwenden des Windows Media Player-Steuerelements mit Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 





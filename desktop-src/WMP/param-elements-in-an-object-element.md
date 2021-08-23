---
title: PARAM-Elemente in einem OBJECT-Element
description: PARAM-Elemente in einem OBJECT-Element
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- Windows Media Player,PARAM-Elemente im OBJECT-Element
- Windows Media Player Objektmodell, PARAM-Elemente im OBJECT-Element
- Objektmodell,PARAM-Elemente im OBJECT-Element
- Windows Media Player Mobile,PARAM-Elemente im OBJECT-Element
- Windows Media Player ActiveX-Steuerelement, PARAM-Elemente im OBJECT-Element
- Windows Media Player Mobiles ActiveX-Steuerelement, PARAM-Elemente im OBJECT-Element
- ActiveX-Steuerelement, PARAM-Elemente im OBJECT-Element
- Einbetten,Webseiten
- Webseiteneinbettung,PARAM-Elemente im OBJECT-Element
- PARAM-Elemente im OBJECT-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da684a39739703038793abb2f4fdd32b924f35cdffc0c0f9d796fb7dbb5532b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054428"
---
# <a name="param-elements-in-an-object-element"></a>PARAM-Elemente in einem OBJECT-Element

Windows Media Player verwendet das PARAM-Element, um bestimmte Startbedingungen für das Steuerelement zu definieren. Das PARAM-Element ist in das OBJECT-Element eingebettet.

Wenn Sie beispielsweise definieren möchten, ob die **autoStart-Eigenschaft** True ist, würden Sie das PARAM-Element in das OBJECT-Element einbetten.


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



In einem OBJECT-Element können beliebig viele PARAM-Elemente enthalten sein. PARAM verfügt über zwei Attribute: Name und Wert. Beide Attribute müssen festgelegt werden.

Die unterstützten PARAM-Attribute variieren geringfügig zwischen Browsern und MIME-Typen. Die folgende Tabelle zeigt die Attribute, die von den Browsern Internet Explorer und Firefox unterstützt werden. Der bevorzugte MIME-Typ für den Firefox-Browser ist application/x-ms-wmp. Es gibt jedoch mehrere andere MIME-Typen, mit denen Sie das Player-Steuerelement in eine Webseite einbetten können, die vom Firefox-Browser gehostet wird. Die vierte Spalte der Tabelle zeigt die Attribute, die unterstützt werden, wenn Sie einen anderen MIME-Typ als application/x-ms-wmp verwenden.



| PARAM-Name                                            | Internet Explorer | Firefox mit MIME-Typ application/x-ms-wmp | Firefox mit einem beliebigen anderen MIME-Typ |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [autoStart](settings-autostart.md)                   | Ja               | Ja                                         | Ja                              |
| [Gleichgewicht](settings-balance.md)                       | Ja               | Ja                                         | Ja                              |
| [baseURL](settings-baseurl.md)                       | Ja               | Ja                                         | Ja                              |
| [captioningID](closedcaption-captioningid.md)        | Ja               | Ja                                         | Ja                              |
| [currentMarker](controls-currentmarker.md)           | Ja               | Ja                                         | Ja                              |
| [currentPosition](controls-currentposition.md)       | Ja               | Ja                                         | Ja                              |
| [defaultFrame](settings-defaultframe.md)             | Ja               | Nein                                          | Nein                               |
| [enableContextMenu](player-enablecontextmenu.md)     | Ja               | Ja                                         | Ja                              |
| [enabled](player-enabled.md)                         | Ja               | Ja                                         | Ja                              |
| [enableErrorDialogs](settings-enableerrordialogs.md) | Ja               | Ja                                         | Nein                               |
| **fileName**                                          | Nein                | Ja                                         | Ja                              |
| [Fullscreen](player-fullscreen.md)                   | Ja               | Nein                                          | Nein                               |
| [invokeURLs](settings-invokeurls.md)                 | Ja               | Nein                                          | Nein                               |
| [Stumm](settings-mute.md)                             | Ja               | Ja                                         | Ja                              |
| [playCount](settings-playcount.md)                   | Ja               | Ja                                         | Nein                               |
| [Rate](settings-rate.md)                             | Ja               | Ja                                         | Ja                              |
| [SAMIFileName](closedcaption-samifilename.md)        | Ja               | Ja                                         | Ja                              |
| [SAMILang](closedcaption-samilang.md)                | Ja               | Ja                                         | Ja                              |
| [SAMIStyle](closedcaption-samistyle.md)              | Ja               | Ja                                         | Ja                              |
| **Src**                                               | Nein                | Ja                                         | Ja                              |
| [stretchToFit](player-stretchtofit.md)               | Ja               | Ja                                         | Nein                               |
| [URL](player-url.md)                                 | Ja               | Ja                                         | Ja                              |
| [volume](settings-volume.md)                         | Ja               | Ja                                         | Ja                              |
| [windowlessVideo](player-windowlessvideo.md)         | Ja               | Ja                                         | Ja                              |



 

> [!Note]  
> Die **Elemente fileName** und **SRC** PARAM werden vom Firefox-Plug-In unterstützt, jedoch nicht von Internet Explorer. Beide führen die gleiche  Funktion wie das URL-PARAM-Element aus.

 

Weitere Informationen [zu den Werten für die einzelnen](object-model-reference-for-scripting.md) Namensattribute finden Sie in der Objektmodellreferenz für die Skripterstellung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuerelements auf einer Webseite**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 





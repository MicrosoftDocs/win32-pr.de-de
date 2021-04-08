---
title: Param-Elemente in einem Object-Element
description: Param-Elemente in einem Object-Element
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- Windows-Media Player, param-Elemente im Object-Element
- Windows Media Player-Objektmodell, param-Elemente im Object-Element
- Objektmodell, param-Elemente im Object-Element
- Windows Media Player Mobile, param-Elemente im Object-Element
- Windows Media Player ActiveX-Steuerelement, param-Elemente im Object-Element
- Windows Media Player Mobile ActiveX-Steuerelement, param-Elemente im Object-Element
- ActiveX-Steuerelement, param-Elemente im Object-Element
- Einbettungen, Webseiten
- Seiten Einbettung, param-Elemente im Object-Element
- Param-Elemente im Object-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0fc5b9f64fa462386ec037eba34ed4e0659bb1
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "103857047"
---
# <a name="param-elements-in-an-object-element"></a>Param-Elemente in einem Object-Element

Windows Media Player verwendet das param-Element, um bestimmte Startbedingungen für das Steuerelement zu definieren. Das param-Element ist in das Object-Element eingebettet.

Wenn Sie z. b. definieren möchten, ob die **Autostart** -Eigenschaft auf true festgelegt ist, würden Sie das param-Element in das Object-Element einbetten.


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



Sie können beliebig viele param-Elemente in einem Objekt Element enthalten. Param verfügt über zwei Attribute: Name und Wert. Beide Attribute müssen festgelegt werden.

Die unterstützten param-Attribute unterscheiden sich geringfügig bei Browsern und MIME-Typen. In der folgenden Tabelle sind die Attribute aufgeführt, die von den Browsern Internet Explorer und Firefox unterstützt werden. Der bevorzugte MIME-Typ für den Firefox-Browser ist application/x-MS-WMP. es gibt jedoch mehrere andere MIME-Typen, mit denen Sie das Player-Steuerelement in eine Webseite einbetten können, die vom Firefox-Browser gehostet wird. Die vierte Spalte der Tabelle zeigt die Attribute, die unterstützt werden, wenn Sie einen anderen MIME-Typ als "application/x-MS-WMP" verwenden.



| Param-Name                                            | Internet Explorer | Firefox mit MIME-Typ "application/x-MS-WMP" | Firefox mit einem beliebigen anderen MIME-Typ |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [Autostart](settings-autostart.md)                   | ja               | ja                                         | ja                              |
| [Schwebe](settings-balance.md)                       | ja               | ja                                         | ja                              |
| [Basis](settings-baseurl.md)                       | ja               | ja                                         | ja                              |
| [captioningid](closedcaption-captioningid.md)        | ja               | ja                                         | ja                              |
| [currentmarker](controls-currentmarker.md)           | ja               | ja                                         | ja                              |
| [CurrentPosition](controls-currentposition.md)       | ja               | ja                                         | ja                              |
| [defaultframe](settings-defaultframe.md)             | ja               | nein                                          | nein                               |
| [enablecontextmenu](player-enablecontextmenu.md)     | ja               | ja                                         | ja                              |
| [enabled](player-enabled.md)                         | ja               | ja                                         | ja                              |
| [enableerrordialogfelder](settings-enableerrordialogs.md) | ja               | ja                                         | nein                               |
| **fileName**                                          | nein                | ja                                         | ja                              |
| [Vollbild](player-fullscreen.md)                   | ja               | nein                                          | nein                               |
| [invokeurls](settings-invokeurls.md)                 | ja               | nein                                          | nein                               |
| [verstum](settings-mute.md)                             | ja               | ja                                         | ja                              |
| [playcount](settings-playcount.md)                   | ja               | ja                                         | nein                               |
| [zinss](settings-rate.md)                             | ja               | ja                                         | ja                              |
| [Samifilename](closedcaption-samifilename.md)        | ja               | ja                                         | ja                              |
| [Samilang](closedcaption-samilang.md)                | ja               | ja                                         | ja                              |
| [Samistyle](closedcaption-samistyle.md)              | ja               | ja                                         | ja                              |
| **SRC**                                               | nein                | ja                                         | ja                              |
| [stretchdefit](player-stretchtofit.md)               | ja               | ja                                         | nein                               |
| [URL](player-url.md)                                 | ja               | ja                                         | ja                              |
| [volume](settings-volume.md)                         | ja               | ja                                         | ja                              |
| [windowlessvideo](player-windowlessvideo.md)         | ja               | ja                                         | ja                              |



 

> [!Note]  
> Die Parameter **filename** und **src** param werden vom Firefox-Plug-in, jedoch nicht von Internet Explorer unterstützt. Beide führen dieselbe Funktion aus wie das **URL** -param-Element.

 

Weitere Informationen zu den Werten für die einzelnen namens Attribute finden Sie in der [Objektmodell Referenz für die Skript](object-model-reference-for-scripting.md) Erstellung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einer Webseite**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 





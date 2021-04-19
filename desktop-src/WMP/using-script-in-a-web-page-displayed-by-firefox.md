---
title: Verwenden von Skripts in einer Webseite, die von Firefox angezeigt wird
description: Verwenden von Skripts in einer Webseite, die von Firefox angezeigt wird
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
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
- Windows Media Player ActiveX-Steuerelement, Skript Beispiel
- Windows Media Player Mobile ActiveX-Steuerelement, Skript Beispiel
- ActiveX-Steuerelement, Skript Beispiel
- Einbettungen, Webseiten
- Einbetten von Webseiten, Skript Beispiel
- Windows Media Player, Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX-Steuerelement, Firefox
- Windows Media Player Mobile ActiveX-Steuerelement, Firefox
- ActiveX-Steuerelement, Firefox
- Firefox, Skript Beispiel
- Einbettung von Webseiten, Firefox
- Skript Beispiel für die Einbettung von Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "106339848"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a>Verwenden von Skripts in einer Webseite, die von Firefox angezeigt wird

Skripts auf einer Webseite können das Player-Objektmodell verwenden, um den Player zu steuern, während der Benutzer mit der Seite interagiert. Das folgende Eingabe Element verfügt beispielsweise über ein Skript, mit dem das Player Volume festgelegt wird.


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



Viele der Objekte im Windows Media Player-Objektmodell werden von Internet Explorer und dem Firefox-Plug-in unterstützt. Es gibt jedoch einige Objekte, die vom Firefox-Plug-in nicht unterstützt werden. In der folgenden Tabelle werden alle Objekte im Player-Objektmodell aufgelistet, und es wird gezeigt, welche Objekte vom Firefox-Plug-in unterstützt werden.



| Object                                              | Firefox-Unterstützung |
|-----------------------------------------------------|-----------------|
| [Rom](cdrom-object.md)                           | nein              |
| [Cdromcollection](cdromcollection-object.md)       | nein              |
| [Closedcaption](closedcaption-object.md)           | ja             |
| [Steuerelemente](controls-object.md)                     | nein              |
| [DVD](dvd-object.md)                               | nein              |
| [Fehler](error-object.md)                           | ja             |
| [ErrorItem](erroritem-object.md)                   | ja             |
| [Medien](media-object.md)                           | ja             |
| [Mediacollection](mediacollection-object.md)       | nein              |
| [MetadataPicture](metadatapicture-object.md)       | nein              |
| [MetadataText](metadatatext-object.md)             | nein              |
| [Network](network-object.md)                       | ja             |
| [Player](player-object.md)                         | ja             |
| [PlayerApplication](playerapplication-object.md)   | nein              |
| [Abspielen](playlist-object.md)                     | ja             |
| [Playlistarray](playlistarray-object.md)           | nein              |
| [Playlistcollection](playlistcollection-object.md) | nein              |
| [Abfrage](query-object.md)                           | nein              |
| [Einstellungen](settings-object.md)                     | ja             |
| [StringCollection](stringcollection-object.md)     | nein              |



 

Das Firefox-Plug-in unterstützt das **Player** -Objekt, aber bestimmte Eigenschaften des **Player** -Objekts geben **null** in einem Firefox-Browser zurück. Beispielsweise gibt die [cdromcollection](player-cdromcollection.md) -Eigenschaft des **Player** -Objekts den Wert **null** zurück, da das Firefox-Plug-in das **CDROM** -Objekt nicht unterstützt. Ebenso geben die Eigenschaften " [DVD](player-dvd.md)", " [mediacollection](player-mediacollection.md)", " [playerapplication](player-playerapplication.md)" und " [playlistcollection](player-playlistcollection.md) " des **Player** -Objekts in einem Firefox-Browser den Wert **null** zurück.

Die **Player. pluginversioninfo** -Eigenschaft wird vom Firefox-Plug-in, aber nicht von Internet Explorer unterstützt. Diese Eigenschaft gibt die Version des Firefox-Plug-ins zurück.

Das Firefox-Plug-in unterstützt das **Medien** Objekt, einschließlich der [getItemInfoByType](media-getiteminfobytype.md) -Eigenschaft. In einem Firefox-Browser unterstützt die **getItemInfoByType** -Eigenschaft jedoch nicht die Rückgabe Typen **MetadataText** und **MetadataPicture** .

Das Firefox-Plug-in unterstützt das [Einstellungs](settings-object.md) Objekt außer der [setmode](settings-setmode.md) -Methode und der [requestmediaaccessrights](settings-requestmediaaccessrights.md) -Eigenschaft. In einem Firefox-Browser gibt die **requestmediaaccessright** -Eigenschaft immer false zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuer Elements mit Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 





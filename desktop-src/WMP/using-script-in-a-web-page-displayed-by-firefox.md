---
title: Verwenden eines Skripts auf einer Webseite, die von Firefox angezeigt wird
description: Verwenden eines Skripts auf einer Webseite, die von Firefox angezeigt wird
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Windows Media Player,Einbetten ActiveX Steuerelements
- Windows Media Player Objektmodell, Einbetten ActiveX Steuerelements
- Objektmodell, Einbetten ActiveX Steuerelements
- Windows Media Player Mobil, Einbetten ActiveX Steuerelements
- Windows Media Player ActiveX-Steuerelement, Einbetten
- Windows Media Player Mobiles ActiveX-Steuerelement, Einbetten
- ActiveX-Steuerelement, Einbetten
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobiles ActiveX-Steuerelement, Webseiten
- ActiveX-Steuerelement, Webseiten
- Windows Media Player ActiveX-Steuerelement, Skriptbeispiel
- Windows Media Player Mobile ActiveX-Steuerelement, Skriptbeispiel
- ActiveX-Steuerelement, Skriptbeispiel
- Einbetten,Webseiten
- Einbetten von Webseiten, Skriptbeispiel
- Windows Media Player, Firefox
- Windows Media Player Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player Mobil, Firefox
- Windows Media Player ActiveX-Steuerelement, Firefox
- Windows Media Player Mobile ActiveX-Steuerelement, Firefox
- ActiveX-Steuerelement, Firefox
- Firefox, Skriptbeispiel
- Einbetten von Webseiten, Firefox
- Skriptbeispiel für das Einbetten von Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450b03f7adefca1a887fb31207f0a3280e1925c9d3e1f1066df370d87f0a7779
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762060"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a>Verwenden eines Skripts auf einer Webseite, die von Firefox angezeigt wird

Skripts auf einer Webseite können das Player-Objektmodell verwenden, um den Player zu steuern, während der Benutzer mit der Seite interagiert. Das folgende INPUT-Element verfügt beispielsweise über ein Skript, das das Player-Volume festlegt.


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



Viele der Objekte im Windows Media Player-Objektmodell werden von Internet Explorer und vom Firefox-Plug-In unterstützt. Es gibt jedoch einige Objekte, die vom Firefox-Plug-In nicht unterstützt werden. Die folgende Tabelle enthält alle Objekte im Player-Objektmodell und zeigt, welche Objekte vom Firefox-Plug-In unterstützt werden.



| Object                                              | Firefox-Unterstützung |
|-----------------------------------------------------|-----------------|
| [Cdrom](cdrom-object.md)                           | Nein              |
| [Ccollection](cdromcollection-object.md)       | Nein              |
| [ClosedCaption](closedcaption-object.md)           | Ja             |
| [Steuerelemente](controls-object.md)                     | Nein              |
| [Dvd](dvd-object.md)                               | Nein              |
| [Fehler](error-object.md)                           | Ja             |
| [ErrorItem](erroritem-object.md)                   | Ja             |
| [Medien](media-object.md)                           | Ja             |
| [MediaCollection](mediacollection-object.md)       | Nein              |
| [MetadataPicture](metadatapicture-object.md)       | Nein              |
| [MetadataText](metadatatext-object.md)             | Nein              |
| [Netzwerk](network-object.md)                       | Ja             |
| [Player](player-object.md)                         | Ja             |
| [PlayerApplication](playerapplication-object.md)   | Nein              |
| [Wiedergabeliste](playlist-object.md)                     | Ja             |
| [PlaylistArray](playlistarray-object.md)           | Nein              |
| [PlaylistCollection](playlistcollection-object.md) | Nein              |
| [Abfrage](query-object.md)                           | Nein              |
| [Einstellungen](settings-object.md)                     | Ja             |
| [StringCollection](stringcollection-object.md)     | Nein              |



 

Das Firefox-Plug-In unterstützt das **Player-Objekt,** aber bestimmte Eigenschaften des **Player-Objekts** geben **null** in einem Firefox-Browser zurück. Die [ccollectionCollection-Eigenschaft](player-cdromcollection.md) des **Player-Objekts** gibt z. **B. NULL** zurück, da das Firefox-Plug-In das **C csv-Objekt** nicht unterstützt. Auf ähnliche Weise **geben** die Eigenschaften [dvd,](player-dvd.md) [mediaCollection,](player-mediacollection.md) [playerApplication](player-playerapplication.md)und [playlistCollection](player-playlistcollection.md) des **Player-Objekts** null in einem Firefox-Browser zurück.

Die **Player.pluginVersionInfo-Eigenschaft** wird vom Firefox-Plug-In unterstützt, jedoch nicht von Internet Explorer. Diese Eigenschaft gibt die Version des Firefox-Plug-Ins zurück.

Das Firefox-Plug-In  unterstützt das Media-Objekt, einschließlich der [getItemInfoByType-Eigenschaft.](media-getiteminfobytype.md) In einem Firefox-Browser unterstützt die **getItemInfoByType-Eigenschaft** jedoch nicht die Rückgabetypen **MetadataText** und **MetadataPicture.**

Das Firefox-Plug-In unterstützt das [Einstellungen-Objekt](settings-object.md) mit Ausnahme der [setMode-Methode](settings-setmode.md) und der [requestMediaAccessRights-Eigenschaft.](settings-requestmediaaccessrights.md) In einem Firefox-Browser gibt die **requestMediaAccessRight-Eigenschaft** immer FALSE zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Windows Media Player-Steuerelements mit Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 





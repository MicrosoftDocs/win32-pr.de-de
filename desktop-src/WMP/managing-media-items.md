---
title: Verwalten von Medienelementen
description: Verwalten von Medienelementen
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player,Library
- Windows Media Player-Objektmodell,Bibliothek
- Objektmodell,Bibliothek
- Windows Media Player Mobil, Bibliothek für Objektmodell
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobiles ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player bibliothek,Verwalten von Medienelementen
- Bibliothek,Verwalten von Medienelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac689bd6951f09b39db20975d52f6a8ccfc08668d3266d5964c2b7eac28cfd38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054628"
---
# <a name="managing-media-items"></a>Verwalten von Medienelementen

Ein **Medienobjekt** stellt ein Medienelement dar. Sie verfügt über Eigenschaften und Methoden, mit deren Hilfe Sie Informationen abrufen und dem Benutzer anzeigen können, oder um basierend auf dem abgerufenen Wert unterschiedliche Aktionen durchzuführen.

Ein Großteil Ihrer Arbeit mit **Medienobjekten** umfasst Metadaten zum Inhalt des Medienelements, die als Attribute bezeichnet werden. Im Thema [Medienelementattribute](media-item-attributes.md) wird beschrieben, wie Attributwerte gelesen und geändert werden. Weitere Informationen zu den Attributen und deren Verwendung finden Sie zusätzlich zu diesem Thema in den Richtlinien zur Verwendung von [Windows Medienmetadaten](/previous-versions/ms867702(v=msdn.10)) auf der Microsoft-Website.

Das **Media-Objekt** verfügt über Eigenschaften und Methoden, die einige Attribute direkt abrufen, z. B. den Namen oder die Dauer des Elements. Für Videoelemente können Sie die Höhe und Breite des Bilds und Markerinformationen basierend auf dem Namen oder Index eines Markers abrufen. Sie können auch bestimmen, ob ein bestimmtes Medienelement in einer bestimmten Wiedergabeliste enthalten ist.

## <a name="retrieving-a-media-object"></a>Abrufen eines Medienobjekts

Mit dem *Player* können Sie schnell auf das aktuelle Medienelement zugreifen. **currentMedia-Eigenschaft.**

In diesem Thema wurde das **Player-Objekt** wie folgt definiert:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Im folgenden C#-Beispiel wird ein **Media-Objekt** abgerufen, das das aktuelle Element darstellt.


```C++
IWMPMedia media;
media = Player.currentMedia;

```



Sie können ein neues Medienelement aus einer digitalen Mediendatei erstellen, indem Sie *player* verwenden. **newMedia-Methode.** Sie übergeben die -Methode den URL-Pfad an eine digitale Mediendatei und geben einen Verweis auf das neue **Medienobjekt** zurück. Die -Methode fügt das neue -Objekt der Bibliothek nicht direkt hinzu. Sie können das Objekt jedoch an die *Wiedergabeliste* übergeben. **appendItem-Methode** oder *wiedergabeliste*. **insertItem-Methode.**

Im folgenden C#-Beispiel wird ein **Medienobjekt** basierend auf einem der digitalen Medienbeispiele erstellt, die mit dem Windows Media Player SDK installiert wurden.


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> Sie müssen zwei umgekehrte Schrägstriche () in eine Zeichenfolge einschließen \\ (oder das @-Zeichen in C#) verwenden, um einen tatsächlichen umgekehrten Schrägstrich darzustellen. Dies liegt daran, dass C# einen einzelnen umgekehrten Schrägstrich verwendet, um eine Escapesequenz zu definieren.

 

Sie können ein neues Medienelement aus einer digitalen Mediendatei erstellen und der Bibliothek in einem Schritt mithilfe der *MediaCollection* hinzufügen. **add-Methode.** Wie der *Player*. **newMedia-Methode:** Die **add-Methode** nimmt einen Pfad zu einer digitalen Mediendatei an.

Im folgenden C#-Beispiel wird ein **Medienobjekt** basierend auf einer der SDK-Beispieldateien erstellt und der Bibliothek hinzugefügt.


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



Sie können ein **Medienobjekt** abrufen, das ein Medienelement in einer Wiedergabeliste darstellt, indem Sie die *Wiedergabeliste* verwenden. **item-Methode.** Im folgenden C#-Beispiel wird das sechste Medienelement aus der aktuellen Wiedergabeliste abgerufen.


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Controls.currentItem**](controls-currentitem.md)
</dt> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player.newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Arbeiten mit der Bibliothek**](working-with-the-library.md)
</dt> </dl>

 

 





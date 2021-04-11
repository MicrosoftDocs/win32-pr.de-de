---
title: Verwalten von Medien Elementen
description: Verwalten von Medien Elementen
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell, Bibliothek
- Windows Media Player Mobile, Bibliothek für Objektmodell
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player-Bibliothek, Verwalten von Medien Elementen
- Bibliothek, Verwalten von Medien Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100810"
---
# <a name="managing-media-items"></a>Verwalten von Medien Elementen

Ein **Medien** Objekt stellt ein Medien Element dar. Es verfügt über Eigenschaften und Methoden, die Sie verwenden können, um Informationen abzurufen und für den Benutzer anzuzeigen, oder um verschiedene Aktionen basierend auf dem von Ihnen abzurufenden Wert auszuführen.

Ein Großteil der Arbeit mit **Medien** Objekten umfasst Metadaten zum Inhalt des Medien Elements, die als Attribute bezeichnet werden. Das Thema [Medien Element Attribute](media-item-attributes.md) beschreibt das Lesen und Ändern von Attributwerten. Weitere Informationen zu den Attributen und deren Verwendung finden Sie in den [Richtlinien zur Verwendung von Windows Media-Metadaten](/previous-versions/ms867702(v=msdn.10)) auf der Microsoft-Website.

Das **Medien** Objekt verfügt über Eigenschaften und Methoden, die einige Attribute direkt abrufen, z. b. den Namen oder die Dauer des Elements. Bei Videoelementen können Sie die Höhe und Breite des Bilds abrufen und Markerinformationen auf Grundlage des Namens oder Indexes eines Markers abrufen. Sie können auch bestimmen, ob ein bestimmtes Medien Element in einer bestimmten Wiedergabeliste enthalten ist.

## <a name="retrieving-a-media-object"></a>Abrufen eines Medien Objekts

Sie können schnell auf das aktuelle Medien Element zugreifen, indem Sie den *Player* verwenden. **currentMedia** -Eigenschaft.

In diesem Thema wurde das **Player** -Objekt wie folgt definiert:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Im folgenden c#-Beispiel wird ein **Medien** Objekt abgerufen, das das aktuelle Element darstellt.


```C++
IWMPMedia media;
media = Player.currentMedia;

```



Mithilfe des *Players* können Sie ein neues Medien Element aus einer digitalen Mediendatei erstellen. **newmedia** -Methode. Sie übergeben die-Methode den URL-Pfad an eine digitale Mediendatei und geben einen Verweis auf das neue **Medien** Objekt zurück. Die-Methode fügt das neue-Objekt nicht direkt der Bibliothek hinzu. Sie können das Objekt jedoch an die *Wiedergabeliste* übergeben. **appendItem** -Methode oder die *Wiedergabeliste*. **InsertItem** -Methode.

Im folgenden c#-Beispiel wird ein **Medien** Objekt erstellt, das auf einem der Digital Media-Beispiele basiert, das mit dem Windows Media Player SDK installiert wurde.


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> Sie müssen zwei umgekehrte Schrägstriche ( \) oder das @-Zeichen in c#) in einer Zeichenfolge einschließen, um einen tatsächlichen umgekehrten Schrägstrich darzustellen. Dies liegt daran, dass c# einen einzelnen umgekehrten Schrägstrich zum Definieren einer Escapesequenz verwendet.

 

Sie können ein neues Medien Element aus einer digitalen Mediendatei erstellen und es der Bibliothek in einem Schritt mithilfe von *mediacollection* hinzufügen. Methode **Hinzufügen** . Wie der *Player*. **newmedia** -Methode, die **Add** -Methode nimmt einen Pfad zu einer digitalen Mediendatei an.

Im folgenden c#-Beispiel wird ein **Medien** Objekt erstellt, das auf einer der SDK-Beispieldateien basiert, und dieses Objekt wird der Bibliothek hinzugefügt.


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



Mithilfe der *Wiedergabeliste* können Sie ein **Medien** Objekt abrufen, das ein Medien Element in einer Wiedergabeliste darstellt. **Item** -Methode. Im folgenden c#-Beispiel wird das sechste Medien Element aus der aktuellen Wiedergabeliste abgerufen.


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Controls. happtitem**](controls-currentitem.md)
</dt> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Mediacollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. newmedia**](player-newmedia.md)
</dt> <dt>

[**Wiedergabeliste. Element**](playlist-item.md)
</dt> <dt>

[**Arbeiten mit der Bibliothek**](working-with-the-library.md)
</dt> </dl>

 

 





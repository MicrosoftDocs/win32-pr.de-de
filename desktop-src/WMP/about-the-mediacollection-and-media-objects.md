---
title: Informationen zu MediaCollection und Medienobjekten
description: Informationen zu MediaCollection und Medienobjekten
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Windows Media Player,MediaCollection-Objekt
- Windows Media Player-Objektmodell, MediaCollection-Objekt
- Objektmodell,MediaCollection-Objekt
- Windows Media Player ActiveX,MediaCollection-Objekt
- ActiveX,MediaCollection-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, MediaCollection-Objekt
- Windows Media Player Mobile,MediaCollection-Objekt
- MediaCollection-Objekt
- Windows Media Player,Media-Objekt
- Windows Media Player Objektmodell, Medienobjekt
- Objektmodell, Medienobjekt
- Windows Media Player ActiveX,Medienobjekt
- ActiveX,Medienobjekt
- Windows Media Player Mobiles ActiveX-Steuerelement, Medienobjekt
- Windows Media Player Mobil,Medienobjekt
- Medienobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082bea6eb3707915422a0bfa5cba63a2a999ac8df27ffa13876e74ffcfc6a882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583682"
---
# <a name="about-the-mediacollection-and-media-objects"></a>Informationen zu MediaCollection und Medienobjekten

Die **MediaCollection-** und **Media-Objekte** steuern die Mediensammlung, die die Speicherorte von digitalen Mediendateien definiert, auf die Windows Media Player können. Sie erhalten das **MediaCollection-Objekt** aus der **mediaCollection-Eigenschaft** des **Player-Objekts.** Die **mediaCollection-Eigenschaft** gibt das **MediaCollection-Objekt** zurück. Sie können erst auf die Eigenschaften des **MediaCollection-Objekts zugreifen,** nachdem Sie es erstellt haben. Verwenden Sie beispielsweise den folgenden Code, um ein **Media-Objekt** (einen Titel) hinzuzufügen:


```C++
player.mediacollection.add('laure.wma');

```



Sie haben der Mediensammlung die Datei laure.wma hinzugefügt.

Sie können das aktuelle **Media-Objekt** mithilfe der **currentMedia-Eigenschaft** des **Players erhalten.** Dieser Code ruft beispielsweise die **duration-Eigenschaft** des aktuellen **Media-Objekts** ab:


```C++
myduration = player.currentmedia.duration;

```



Es gibt viele Möglichkeiten, ein **Medienobjekt zu** erhalten, damit Sie auf seine Eigenschaften zugreifen können. Wenn Sie beispielsweise auf die **duration-Eigenschaft** des aktuellen Mediums zugreifen möchten, kann jede der folgenden Codezeilen verwendet werden.

So erhalten Sie die Dauer der aktuell abspielten Medien:


```C++
player.currentMedia.duration;

```



So erhalten Sie die Dauer der aktuellen Medien in einer Wiedergabeliste:


```C++
player.controls.currentItem.duration;

```



So erhalten Sie die Dauer des dritten Medienelements in einer Wiedergabeliste:


```C++
player.currentPlaylist.item(2).duration;

```



So erhalten Sie die Dauer des dritten Medienelements in einem "Jazz"-Genre:


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



So erhalten Sie die Dauer des dritten Medienelements in der zweiten Wiedergabeliste:


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 





---
title: Informationen zu mediacollection und Media Objects
description: Informationen zu mediacollection und Media Objects
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Windows Media Player, mediacollection-Objekt
- Windows Media Player-Objektmodell, mediacollection-Objekt
- Objektmodell, mediacollection-Objekt
- Windows Media Player ActiveX-Steuerelement, mediacollection-Objekt
- ActiveX-Steuerelement, mediacollection-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, mediacollection-Objekt
- Windows Media Player Mobile, mediacollection-Objekt
- Mediacollection-Objekt
- Windows Media Player, Medienobjekt
- Windows Media Player-Objektmodell, Medienobjekt
- Objektmodell, Medienobjekt
- Windows Media Player ActiveX-Steuerelement, Medienobjekt
- ActiveX-Steuerelement, Medienobjekt
- Windows Media Player Mobile ActiveX-Steuerelement, Medienobjekt
- Windows Media Player Mobile, Medienobjekt
- Medienobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340438"
---
# <a name="about-the-mediacollection-and-media-objects"></a>Informationen zu mediacollection und Media Objects

**Mediacollection** und **Media** Objects steuern die Mediensammlung, in der die Speicherorte digitaler Mediendateien definiert sind, auf die Windows Media Player zugreifen kann. Sie erhalten das **mediacollection** -Objekt aus der **mediacollection** -Eigenschaft des **Player** -Objekts. Die **mediacollection** -Eigenschaft gibt das **mediacollection** -Objekt zurück. Sie können nur auf die Eigenschaften des **mediacollection** -Objekts zugreifen, nachdem Sie es erstellt haben. Wenn Sie z. b. ein **Medien** Objekt (einen Song) hinzufügen möchten, verwenden Sie den folgenden Code:


```C++
player.mediacollection.add('laure.wma');

```



Sie haben der Mediensammlung die Datei "Laure. wma" hinzugefügt.

Sie können das aktuelle **Medien** Objekt mit der **currentMedia** -Eigenschaft des **Players** erhalten. Mit diesem Code wird beispielsweise die **Duration** -Eigenschaft des aktuellen **Medien** Objekts abgerufen:


```C++
myduration = player.currentmedia.duration;

```



Es gibt viele Möglichkeiten, ein **Medien** Objekt zu erhalten, sodass Sie auf seine Eigenschaften zugreifen können. Wenn Sie z. b. auf die **Duration** -Eigenschaft des aktuellen Mediums zugreifen möchten, können Sie jede der folgenden Codezeilen verwenden.

So erhalten Sie die Dauer der derzeit Wiedergabe Medien:


```C++
player.currentMedia.duration;

```



So erhalten Sie die Dauer des aktuellen Mediums in einer Wiedergabeliste:


```C++
player.controls.currentItem.duration;

```



So erhalten Sie die Dauer des dritten Medien Elements in einer Wiedergabeliste:


```C++
player.currentPlaylist.item(2).duration;

```



So erhalten Sie die Dauer des dritten Medien Elements in einem "Jazz"-Genre:


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



So erhalten Sie die Dauer des dritten Medien Elements in der zweiten Wiedergabeliste:


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 





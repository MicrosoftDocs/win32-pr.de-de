---
title: Wiedergabelisten und Medienelemente
description: Wiedergabelisten und Medienelemente
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Windows Media Player, Wiedergabelisten
- Windows Media Player-Objektmodell, Wiedergabelisten
- Objektmodell, Wiedergabelisten
- Windows Media Player Mobile, Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten
- ActiveX-Steuerelement, Wiedergabelisten
- Wiedergabelisten, Medienelemente
- Metadatei-Wiedergabelisten, Medienelemente
- Windows Media Metadatei-Wiedergabelisten, Medienelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4716a8ce07e7b0ec8348ce1a6981e23291335e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947571"
---
# <a name="playlists-and-media-items"></a>Wiedergabelisten und Medienelemente

Eine Wiedergabeliste ist ein Satz von Medien Elementen. Ein **Wiedergabe** Listen Objekt kann die **Medien** Objekte, die diese Elemente darstellen, bearbeiten.

## <a name="retrieving-media-items"></a>Abrufen von Medien Elementen

Eine vorhandene Wiedergabeliste finden Sie in der *Wiedergabeliste*. **count** -Eigenschaft, um zu bestimmen, wie viele Medienelemente in der Wiedergabeliste angezeigt werden, und Sie können einen Verweis auf das **Medien** Objekt, das einem bestimmten Element entspricht, mithilfe der *Wiedergabeliste* erhalten. **Item** -Eigenschaft.

Im folgenden c#-Beispiel wird ein Objekt Verweis auf ein bestimmtes Medien Element abgerufen. (In diesem Thema ist die Variable *plist* ein Verweis auf ein **Wiedergabe** Listen Objekt.)


```C++
currMedia = pList.Item(0);

```



Im folgenden c#-Beispiel werden die Namen aller Medienelemente in einer Wiedergabeliste abgerufen und in ein ListBox-Element mit dem Namen "lstoutput" eingefügt.


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a>Hinzufügen von Elementen zu einer Wiedergabeliste

Sie können ein Medien Element am Ende einer Wiedergabeliste oder an einer bestimmten Position in einer Wiedergabeliste mit der *Wiedergabeliste* hinzufügen. **appendItem** und *Wiedergabeliste*. **InsertItem** -Methoden.

In diesem Thema wurde das **Player** -Objekt wie folgt definiert:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Im folgenden c#-Beispiel werden beide Verfahren veranschaulicht, indem das aktuelle Medien Element einer Wiedergabeliste mit dem Namen "bluestest" hinzugefügt wird, zuerst am Ende und dann am Anfang der Wiedergabeliste.


```C++
IWMPPlaylistCollection pListColl;
IWMPPlaylistArray pListArray;
IWMPPlaylist pList;

// Initialize the Media object
IWMPMedia currMedia = Player.currentMedia;

if(currMedia != null)
{
    // Retrieve the playlist collection
    pListColl = Player.playlistCollection;

    // Retrieve a playlist array containing
    // playlists named BluesTest
    pListArray = pListColl.getByName("BluesTest");

    // Retrieve the first element with this name from the
    // array.
    pList = pListArray.Item(0);

    // Add the current item to the end, and then, the beginning
    // of the specified playlist.
    pList.appendItem(currMedia);
    pList.insertItem(0, currMedia);
}

```



Beim Erstellen einer neuen, leeren Wiedergabeliste mit *playlistcollection*. **newwiedergabe** -Methode: Sie können Medienelemente hinzufügen, indem Sie die *Wiedergabeliste* wiederholt aufrufen. **appendItem** -Methode.

## <a name="manipulating-media-items-in-a-playlist"></a>Bearbeiten von Medien Elementen in einer Wiedergabeliste

Mithilfe der *Wiedergabeliste* können Sie die Position eines Medien Elements in der Wiedergabeliste ändern. " **muveitem** "-Methode. Geben Sie das Element anhand seines aktuellen Indexes an, und geben Sie dann den neuen Index an. Im folgenden c#-Beispiel wird ein Element in einer Wiedergabeliste von Index 5 in Index 0 verschoben.


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



Sie können ein Medien Element mithilfe der **Wiedergabeliste** aus der Wiedergabeliste entfernen. **RemoveItem** -Methode. Beachten Sie, dass die Indexwerte der nachfolgenden Elemente geändert werden, wenn es sich bei dem entfernten Element nicht um das letzte Element in der Wiedergabeliste handelt. Im folgenden c#-Beispiel wird das angegebene Element entfernt.


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> Benutzer können den Inhalt einer Wiedergabeliste außerhalb Ihrer Anwendung ändern. Wenn Sie die Elemente in einer Wiedergabeliste bearbeiten, sollten Sie die Wiedergabelisten bezogenen Ereignisse des Windows Media Player-Steuer Elements überwachen und behandeln, um sicherzustellen, dass der Code ordnungsgemäß funktioniert. Diese Ereignisse sind *Player*. **Currentplaylistchange** und *Player*. **Playlistchange**.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> </dl>

 

 





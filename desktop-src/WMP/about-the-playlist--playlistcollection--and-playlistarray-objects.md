---
title: Informationen zu den Wiedergabelisten-, playlistcollection-und playlistarray-Objekten
description: Informationen zu den Wiedergabelisten-, playlistcollection-und playlistarray-Objekten
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Windows Media Player, Wiedergabelisten Objekt
- Windows Media Player-Objektmodell, Wiedergabelisten Objekt
- Objektmodell, Wiedergabelisten Objekt
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten Objekt
- ActiveX-Steuerelement, Wiedergabelisten Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten Objekt
- Windows Media Player Mobile, Wiedergabelisten Objekt
- Wiedergabelisten Objekt
- Windows Media Player, playlistcollection-Objekt
- Windows Media Player-Objektmodell, playlistcollection-Objekt
- Objektmodell, playlistcollection-Objekt
- Windows Media Player ActiveX-Steuerelement, playlistcollection-Objekt
- ActiveX-Steuerelement, playlistcollection-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, playlistcollection-Objekt
- Windows Media Player Mobile, playlistcollection-Objekt
- Playlistcollection-Objekt
- Windows Media Player, playlistarray-Objekt
- Windows Media Player-Objektmodell, playlistarray-Objekt
- Object Model, playlistarray-Objekt
- Windows Media Player ActiveX-Steuerelement, playlistarray-Objekt
- ActiveX-Steuerelement, playlistarray-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, playlistarray-Objekt
- Windows Media Player Mobile, playlistarray-Objekt
- Playlistarray-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337572"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a>Informationen zu den Wiedergabelisten-, playlistcollection-und playlistarray-Objekten

Die **Wiedergabe** Listen, **playlistcollection** und **playlistarray** -Objekte steuern die Wiedergabelisten, die von Windows Media Player verwendet werden können, um die Reihenfolge anzugeben, in der der Inhalt wiedergegeben wird. Sie erhalten das **playlistcollection** -Objekt aus der **playlistcollection** -Eigenschaft des **Player** -Objekts. Die **playlistcollection** -Eigenschaft gibt das **playlistcollection** -Objekt zurück. Sie können nur auf die Eigenschaften des **playlistcollection** -Objekts zugreifen, nachdem Sie es erstellt haben. Wenn Sie z. b. eine neue Wiedergabeliste erstellen möchten, müssen Sie zuerst das **playlistcollection** -Objekt und dann eine-Methode für dieses Objekt verwenden.


```C++
player.playlistcollection.newplaylist('myplaylist');
```



Sie können die aktuelle Wiedergabeliste mit der **currentwiedergabe** -Eigenschaft erhalten. Um z. b. den Namen der aktuellen Wiedergabeliste zu erhalten, verwenden Sie den folgenden Code:


```C++
myname = player.currentplaylist.name;
```



Das **playlistarray** -Objekt wird von den Methoden **GetAll** und **getByName** des **playlistcollection** -Objekts zurückgegeben. Um beispielsweise die Anzahl der Wiedergabelisten zu erhalten, verwenden Sie den folgenden Code:


```C++
howmany = player.playlistcollection.getAll().count;
```



Verwenden Sie den folgenden Code, um eine bekannte Wiedergabeliste nach Namen abzurufen:


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Playlistarray-Objekt**](playlistarray-object.md)
</dt> <dt>

[**Playlistcollection-Objekt**](playlistcollection-object.md)
</dt> </dl>

 

 





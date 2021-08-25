---
title: Corpora.playlist
description: Die Wiedergabelisteneigenschaft ruft ein Wiedergabelistenobjekt ab, das die Titel auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk befinden, oder die Titeleinträge auf Stammebene für die DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- C csv.playlist Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29419b68c50718165e49c0fbe9e75487e9154c19243453981ab352f03e8209a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864180"
---
# <a name="cdromplaylist"></a>Corpora.playlist

Die **Wiedergabelisteneigenschaft** ruft ein **Wiedergabelistenobjekt** ab, das die Titel auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk befinden, oder die Titeleinträge auf Stammebene für die DVD.

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein schreibgeschütztes **Wiedergabelistenobjekt.**

## <a name="remarks"></a>Hinweise

In der Regel sind DVDs in Titel organisiert. Jeder Titel enthält mindestens ein Kapitel. Jede DVD wird anders erstellt, sodass die Verwendung von Titeln und Kapiteln dem Inhaltsautor obliegt.

Bei DVD ruft diese Methode eine Wiedergabeliste ab, die als erstes Element ein **Medienobjekt** enthält, das die DVD-Medien darstellt. Die Wiedergabe des Elements führt dazu, dass die DVD von Anfang an wiedergegeben wird, wenn es sich um die erste Wiedergabe nach dem Einfügen einer neuen DVD handelt, oder die Wiedergabe wird wieder aufgenommen, wenn die DVD mit der letzten angezeigten DVD identisch ist. Wenn dieses Element während der Wiedergabe als aktuelles Element festgelegt wird, wird die DVD von Anfang an wiedergegeben.

Zusätzliche Elemente **(Medienobjekte)** in der Wiedergabeliste sind DVD-Titel, die durch geschachtelte Wiedergabelisten dargestellt werden. Wenn Sie *Controls* angeben. **currentItem** entspricht einem dieser geschachtelten Wiedergabelistenelemente, Windows Media Player legt die geschachtelte Wiedergabeliste automatisch auf *Player* fest. **currentPlaylist** nach Beginn der Kapitelwiedergabe. Sie können dann die **currentPlaylist-Objekteigenschaften,** -Methoden und -Ereignisse verwenden, um mit DVD-Kapiteln zu arbeiten, bei denen es sich ebenfalls um Wiedergabelistenelemente handelt.

Um den Wert dieser Eigenschaft abzurufen, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird *C csv* verwendet. **Wiedergabeliste** zum Ausfüllen eines HTML-Textelements namens myText mit den Titeln der Audio-CD, die sich derzeit auf dem ersten CD-Laufwerk befindet. Verwenden Sie *C csvCollection*. **count,** um die Anzahl der verfügbaren CD-Laufwerke zu bestimmen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Chole-Objekt**](cdrom-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






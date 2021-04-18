---
title: Cdrom. Wiedergabeliste
description: Die Wiedergabelisten Eigenschaft ruft ein Wiedergabelisten Objekt ab, das die Spuren auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk oder die Titel Einträge auf der Stamm Ebene für DVD darstellt.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Cdrom. Wiedergabelisten-Fenster Media Player
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
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345291"
---
# <a name="cdromplaylist"></a>Cdrom. Wiedergabeliste

Die **Wiedergabe** Listen Eigenschaft ruft ein **Wiedergabe** Listen Objekt ab, das die Spuren auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk oder die Titel Einträge auf der Stamm Ebene für DVD darstellt.

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein Schreib geschütztes **Wiedergabe** Listen Objekt.

## <a name="remarks"></a>Bemerkungen

In der Regel sind DVDs in Titeln organisiert. Jeder Titel enthält ein oder mehrere Kapitel. Jede DVD wird unterschiedlich erstellt, sodass Titel und Kapitel für den Inhalts Autor verwendet werden.

Bei der DVD ruft diese Methode eine Wiedergabeliste ab, die als erstes Element ein **Medien** Objekt enthält, das das DVD-Medium darstellt. Die Wiedergabe des Elements führt dazu, dass die DVD von Anfang an wiedergegeben wird, wenn es sich um das erste Mal nach dem Einfügen einer neuen DVD handelt, oder die Wiedergabe wieder aufzunehmen, wenn die DVD mit der letzten angezeigten DVD identisch ist. Wenn Sie dieses Element während der Wiedergabe als das aktuelle Element festlegen, wird die DVD von Anfang an wiedergegeben.

Zusätzliche Elemente (**Medien** Objekte) in der Wiedergabeliste sind DVD-Titel, die durch in der Liste dargestellte Wiedergabelisten dargestellt werden. Wenn Sie Steuer *Elemente* angeben. das Element, das einem dieser in der Liste eingefügten Wiedergabelisten Elemente entspricht, **wird von Windows** Media Player automatisch die geklickte Wiedergabeliste als *Player* festgelegt. **currentwiedergabe** nach Beginn der Wiedergabe des Kapitels. Sie können dann die Eigenschaften, Methoden und Ereignisse des **currentwiedergabe** -Objekts verwenden, um mit DVD-Kapiteln zu arbeiten, die auch Wiedergabelisten Elemente sind.

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird *CDROM* verwendet. **Wiedergabeliste** zum Ausfüllen eines HTML-Text Elements mit dem Namen "MyText" mit den Titeln der AudioCD, die sich zurzeit auf dem ersten CD-Laufwerk befinden. Verwenden Sie *cdromcollection*. **Anzahl, um** die Anzahl der verfügbaren CD-Laufwerke zu bestimmen. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrom-Objekt**](cdrom-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






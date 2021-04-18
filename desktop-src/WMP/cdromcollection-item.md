---
title: Cdromcollection. Item-Methode
description: Die Item-Methode ruft das CDROM-Objekt am angegebenen Index ab.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, cdromcollection-Klasse
- Cdromcollection-Klasse, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365812"
---
# <a name="cdromcollectionitem-method"></a>Cdromcollection. Item-Methode

Die **Item** -Methode ruft das **CDROM** -Objekt am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Die **Zahl** (**Long**), die den Index enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **CDROM** -Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *cdromcollection* verwendet. **Element** , mit dem der Wiedergabelisten Name der einzelnen auf dem Computer verfügbaren CD gedruckt werden soll. Wenn das Laufwerk tatsächlich DVD-Inhalte enthält, ist Windows XP oder höher erforderlich. Ein HTML-TEXTAREA-Element wurde mit ID = "Playlists" erstellt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrom. drivespecifier**](cdrom-drivespecifier.md)
</dt> <dt>

[**Cdromcollection-Objekt**](cdromcollection-object.md)
</dt> <dt>

[**Cdromcollection. Count**](cdromcollection-count.md)
</dt> <dt>

[**Playlist.name**](playlist-name.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






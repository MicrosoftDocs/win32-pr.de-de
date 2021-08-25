---
title: CcollectionCollection.item-Methode
description: Die item-Methode ruft das Cobjekt am angegebenen Index ab.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- item-Methode Windows Media Player
- item-Methode Windows Media Player , Ccollection-Klasse
- CcollectionCollection-Klasse Windows Media Player , Item-Methode
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
ms.openlocfilehash: a5f700a17c29c382e96a5601bd9bbfabf3c4ede1b253d9f271b1d37ab1106ee2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864080"
---
# <a name="cdromcollectionitem-method"></a>CcollectionCollection.item-Methode

Die **item-Methode** ruft das **Cobjekt** am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Zahl** (**long**), die den Index enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Cakus-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *Ccollection* verwendet. **Element** zum Drucken des Wiedergabelistennamens von jeder cd, die auf dem Computer verfügbar ist. Wenn das Laufwerk tatsächlich DVD-Inhalt enthält, ist Windows XP oder höher erforderlich. Ein HTML-TextArea-Element wurde mit id = "playlists" erstellt. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**C csv.driveSpecifier**](cdrom-drivespecifier.md)
</dt> <dt>

[**CcollectionCollection-Objekt**](cdromcollection-object.md)
</dt> <dt>

[**CcollectionCollection.count**](cdromcollection-count.md)
</dt> <dt>

[**Playlist.name**](playlist-name.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






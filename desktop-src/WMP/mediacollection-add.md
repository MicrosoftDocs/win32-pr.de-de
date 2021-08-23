---
title: MediaCollection.add-Methode
description: Die add-Methode fügt der Bibliothek ein neues Medienelement oder eine Wiedergabeliste hinzu. | MediaCollection.add-Methode
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Hinzufügen einer Windows Media Player
- Add-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , Add-Methode
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b26d21f67496f345324efdca93dbf85e59947f1616e0c5620faead2807a6ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647910"
---
# <a name="mediacollectionadd-method"></a>MediaCollection.add-Methode

Die **add-Methode** fügt der Bibliothek ein neues Medienelement oder eine Wiedergabeliste hinzu.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfad* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Pfad enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Media-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Diese Methode lädt ein vorhandenes Medienelement oder eine Wiedergabeliste unter Berücksichtigung eines Pfads zu einer Datei in die Bibliothek. Diese Methode ändert die Datei nicht. Diese Methode schlägt fehl, wenn ein ungültiger lokaler Pfad angegeben wird, digitale Mediendateien jedoch nicht auf Gültigkeit überprüft werden, bevor sie der Bibliothek hinzugefügt werden.

Diese Methode akzeptiert sowohl statische als auch automatische Wiedergabelistendateien. Die *PlaylistCollection.* **Die importPlaylist-Methode** kann auch verwendet werden, um der Bibliothek eine statische Wiedergabeliste hinzuzufügen.

Um diese Methode verwenden zu können, ist Vollzugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Microsoft JScript Beispiel werden der Mediensammlung drei Medienobjekte Windows Media Player medien. Das **Player-Objekt** wurde mit ID="Player" erstellt.


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.remove**](mediacollection-remove.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






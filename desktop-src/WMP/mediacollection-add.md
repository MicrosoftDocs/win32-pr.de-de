---
title: Mediacollection. Add-Methode
description: Die Add-Methode fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu. | Mediacollection. Add-Methode
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Hinzufügen von Methoden Fenster Media Player
- Add-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, Methode hinzufügen
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
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361364"
---
# <a name="mediacollectionadd-method"></a>Mediacollection. Add-Methode

Die **Add** -Methode fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Pfad enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Medien** Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode lädt ein vorhandenes Medien Element oder eine vorhandene Wiedergabeliste in die Bibliothek, wenn ein Pfad zu einer Datei vorhanden ist. Diese Methode verschiebt oder ändert die Datei nicht. Bei dieser Methode tritt ein Fehler auf, wenn ein ungültiger lokaler Pfad vorliegt, aber digitale Mediendateien nicht auf Gültigkeit überprüft werden, bevor Sie der Bibliothek hinzugefügt werden.

Diese Methode akzeptiert sowohl statische als auch automatische Wiedergabelisten Dateien. Die *playlistcollection*. die **importwiedergabe** -Methode kann auch verwendet werden, um der Bibliothek eine statische Wiedergabeliste hinzuzufügen.

Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden Microsoft JScript-Beispiel werden der Windows Media Player-Mediensammlung drei Medienobjekte hinzugefügt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. Remove**](mediacollection-remove.md)
</dt> <dt>

[**Playlistcollection. importwiedergabe**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






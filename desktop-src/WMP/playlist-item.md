---
title: Wiedergabe. Item-Methode
description: Die Item-Methode ruft das Medien Element am angegebenen Index ab.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367797"
---
# <a name="playlistitem-method"></a>Wiedergabe. Item-Methode

Die **Item** -Methode ruft das Medien Element am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die den Index des abzurufenden Elements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Medien** Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird die *Wiedergabeliste* verwendet. **Element** zum Abrufen eines Medien Elements aus der aktuellen Wiedergabeliste basierend auf einer Benutzer Auswahl. Es wurde ein HTML-SELECT-Element mit dem Namen "weblist" erstellt und mit den Titeln aus der aktuellen Wiedergabeliste gefüllt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Wiedergabeliste. InsertItem**](playlist-insertitem.md)
</dt> <dt>

[**Wiedergabeliste. RemoveItem**](playlist-removeitem.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






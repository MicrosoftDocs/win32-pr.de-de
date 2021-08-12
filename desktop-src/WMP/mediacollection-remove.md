---
title: MediaCollection.remove-Methode
description: Die remove-Methode entfernt ein Element aus der Medienauflistung.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- remove-Methode Windows Media Player
- remove-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , remove-Methode
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dd0643741a15bf114acfef63459e67c332b06b33e6284b032979d4ad15c1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574607"
---
# <a name="mediacollectionremove-method"></a>MediaCollection.remove-Methode

Die **remove-Methode** entfernt ein Element aus der Medienauflistung.

## <a name="syntax"></a>Syntax


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Element* \[ In\]
</dt> <dd>

**Medienobjekt,** das entfernt werden soll.

</dd> <dt>

*löschen* \[ In\]
</dt> <dd>

**Boolescher Wert,** der angibt, ob das Element entfernt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode löscht ein Element aus der Bibliothek. Diese Methode löscht keine Dateien vom Computer des Benutzers.

Um diese Methode verwenden zu können, ist vollzugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird nach aufforderung des Benutzers das erste Medienelement in der Mediensammlung mithilfe von *MediaCollection* endgültig gelöscht. **entfernen Sie**. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






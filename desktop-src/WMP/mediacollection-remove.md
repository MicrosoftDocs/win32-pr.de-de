---
title: Mediacollection. Remove-Methode
description: Die Remove-Methode entfernt ein Element aus der Medien Auflistung.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- Methode "Windows Media Player entfernen"
- Remove-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, Methode entfernen
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
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360397"
---
# <a name="mediacollectionremove-method"></a>Mediacollection. Remove-Methode

Die **Remove** -Methode entfernt ein Element aus der Medien Auflistung.

## <a name="syntax"></a>Syntax


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Element* \[ in\]
</dt> <dd>

Das zu entfernende **Medien** Objekt.

</dd> <dt>

*Löschen* \[ in\]
</dt> <dd>

**Boolescher** Wert, der angibt, ob das Element entfernt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode löscht ein Element aus der Bibliothek. Mit dieser Methode werden keine Dateien auf dem Computer des Benutzers gelöscht.

Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird nach dem auffordern des Benutzers das erste Medien Element dauerhaft in der Mediensammlung mithilfe von *mediacollection* gelöscht. **Entfernen** Sie. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






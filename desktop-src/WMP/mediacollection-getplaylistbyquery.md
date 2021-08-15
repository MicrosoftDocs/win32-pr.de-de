---
title: MediaCollection.getPlaylistByQuery-Methode
description: Die getPlaylistByQuery-Methode ruft ein Playlist-Objekt ab, das Media-Objekte enthält, die den Abfragebedingungen entsprechen.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- getPlaylistByQuery-Windows Media Player
- getPlaylistByQuery-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , getPlaylistByQuery-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f64f054fe59865fb8d213d343696c86d83a5f8698d498c854660f76dc9085f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837143"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a>MediaCollection.getPlaylistByQuery-Methode

Die **getPlaylistByQuery-Methode** ruft ein **Playlist-Objekt** ab, das **Media-Objekte** enthält, die den Abfragebedingungen entsprechen.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Abfrage* \[ In\]
</dt> <dd>

**Abfrageobjekt,** das die Bedingungen definiert, die zum Erstellen der Wiedergabeliste verwendet werden.

</dd> <dt>

*mediaType* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Medientyp enthält. Muss einen der folgenden Werte enthalten: "audio", "video", "photo", "playlist" oder "other".

</dd> <dt>

*sortAttribute* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den für die Sortierung verwendeten Attributnamen enthält. Eine leere Zeichenfolge ("") bedeutet, dass keine Sortierung angewendet wird.

</dd> <dt>

*sortAscending* \[ In\]
</dt> <dd>

**Boolescher Wert**, true, der angibt, dass die Wiedergabeliste in aufsteigender Reihenfolge sortiert werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Playlist-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Bei zusammengesetzten Abfragen, die **Die Abfrage verwenden,** wird die Zwischenschreibung nicht beachtet.

Wenn die durch den  Abfrageparameter angegebene Verbundabfrage eine Bedingung enthält, die auf dem **MediaType-Attribut** basiert, wird diese Bedingung ignoriert. Der Wert für den *mediaType-Parameter* wird immer verwendet. Wenn die Verbundabfrage beispielsweise die Bedingung "MediaType Gleich Audio" enthält und der Wert für den *mediaType-Parameter* "video" ist, enthält die resultierende Wiedergabeliste nur Videoelemente.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**MediaType-Attribut**](mediatype-attribute.md)
</dt> <dt>

[**Abfrageobjekt**](query-object.md)
</dt> </dl>

 

 






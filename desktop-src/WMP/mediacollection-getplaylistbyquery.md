---
title: Mediacollection. getplaylistbyquery-Methode
description: Die getplaylistbyquery-Methode ruft ein Wiedergabelisten Objekt ab, das Media-Objekte enthält, die den Abfragebedingungen entsprechen.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- getplaylistbyquery-Methode, Windows-Media Player
- getplaylistbyquery-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getplaylistbyquery-Methode
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
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371077"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a>Mediacollection. getplaylistbyquery-Methode

Die **getplaylistbyquery** -Methode ruft ein **Wiedergabe** Listen Objekt ab, das **Media** -Objekte enthält, die den Abfragebedingungen entsprechen.

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

*Abfrage* \[ in\]
</dt> <dd>

**Query** -Objekt, das die Bedingungen definiert, die zum Erstellen der Wiedergabeliste verwendet werden.

</dd> <dt>

*mediaType* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Medientyp enthält. Muss einen der folgenden Werte enthalten: "Audiodatei", "Video", "Photo", "Wiedergabeliste" oder "Other".

</dd> <dt>

*SortAttribute* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den für die Sortierung verwendeten Attributnamen enthält. Eine leere Zeichenfolge ("") bedeutet, dass keine Sortierung angewendet wird.

</dd> <dt>

*SortAscending* \[ in\]
</dt> <dd>

**Boolescher** Wert, der angibt, dass die Wiedergabeliste in aufsteigender Reihenfolge sortiert werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Bei Verbund Abfragen mit **Abfrage** wird die Groß-/Kleinschreibung nicht beachtet

Wenn die durch den *Abfrage* Parameter angegebene Verbund Abfrage eine Bedingung enthält, die auf dem **mediaType** -Attribut basiert, wird diese Bedingung ignoriert. Der Wert für den *mediaType* -Parameter wird immer verwendet. Wenn die Verbund Abfrage z. b. die Bedingung "MediaType ist mit Audiodaten" enthält und der Wert für den *mediaType* -Parameter "Video" ist, enthält die resultierende Wiedergabeliste nur Video Elemente.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**MediaType-Attribut**](mediatype-attribute.md)
</dt> <dt>

[**Query-Objekt**](query-object.md)
</dt> </dl>

 

 






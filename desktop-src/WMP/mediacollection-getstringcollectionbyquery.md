---
title: MediaCollection.getStringCollectionByQuery-Methode
description: Die getStringCollectionByQuery-Methode ruft ein StringCollection-Objekt ab, das alle Zeichenfolgen enthält, die den Abfragebedingungen entsprechen.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- getStringCollectionByQuery-Windows Media Player
- getStringCollectionByQuery-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , getStringCollectionByQuery-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d9e8f2eae2ce52a566d4db6b8298187df1d4d444432e99dda22d3cacc0ed3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390110"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a>MediaCollection.getStringCollectionByQuery-Methode

Die **getStringCollectionByQuery-Methode** ruft ein **StringCollection-Objekt** ab, das alle Zeichenfolgen enthält, die den Abfragebedingungen entsprechen.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Attributnamen enthält.

</dd> <dt>

*Abfrage* \[ In\]
</dt> <dd>

**Abfrageobjekt.**

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

**Boolescher Wert**, true, der angibt, dass **die StringCollection** in aufsteigender Reihenfolge sortiert werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **StringCollection-Objekt** zurück.

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

 

 






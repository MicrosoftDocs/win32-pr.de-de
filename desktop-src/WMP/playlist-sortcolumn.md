---
title: PLAYLIST.sortColumn
description: Die sortColumn-Methode sortiert die Daten in der angegebenen Spalte.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- PLAYLIST.sortColumn Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34dfce7306ceb39d64665538a21dbaef965ea799141a2756c2fea5bbe23ea9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335657"
---
# <a name="playlistsortcolumn"></a>PLAYLIST.sortColumn

Die **sortColumn-Methode** sortiert die Daten in der angegebenen Spalte.

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*Spalte*
</dt> <dd>

**Number** (**long**) gibt den Index der zu sortierende Spalte an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode sortiert die angegebene Spalte auf die gleiche Weise wie die Spaltenheaderschaltflächen im **PLAYLIST-Element.** Wenn die Spalte noch nicht sortiert wurde, wird sie in alphanumerischer Reihenfolge sortiert. Wenn sie sortiert wurde, wird ihre Reihenfolge umgekehrt.

Damit diese Methode funktioniert, muss das **allowColumnSorting-Attribut** auf TRUE festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.allowColumnSorting**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 






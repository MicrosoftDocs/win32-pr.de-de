---
title: Playlist. SortColumn
description: Die SortColumn-Methode sortiert die Daten in der angegebenen Spalte.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- Wiedergabeliste. SortColumn-Fenster Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364561"
---
# <a name="playlistsortcolumn"></a>Playlist. SortColumn

Die **SortColumn** -Methode sortiert die Daten in der angegebenen Spalte.

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*Kolumne*
</dt> <dd>

**Zahl** (**Long**), die den Index der zu sortierenden Spalte angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode sortiert die angegebene Spalte auf die gleiche Weise wie die Spaltenheader Schaltflächen im **Wiedergabe** Listenelement. Wenn die Spalte noch nicht sortiert wurde, wird Sie in alphanumerischer Reihenfolge sortiert. Wenn Sie sortiert wurde, wird die Reihenfolge umgekehrt.

Damit diese Methode funktioniert, muss das **allowcolumnsortierung** -Attribut auf "true" festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabeliste. allowcolumnsortierung**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 






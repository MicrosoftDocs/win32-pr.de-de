---
title: LISTBOX.findItem
description: Die findItem-Methode sucht nach einer bestimmten Zeichenfolge, beginnend mit dem Element, das dem angegebenen Elementindex folgt.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- LISTBOX.findItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3625c8d8e9993d09e7b5b41911ead8df857c257a7a2354d71c8d81c1fecc645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135323"
---
# <a name="listboxfinditem"></a>LISTBOX.findItem

Die **findItem-Methode** sucht nach einer bestimmten Zeichenfolge, beginnend mit dem Element, das dem angegebenen Elementindex folgt.

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Startindex*
</dt> <dd>

**Zahl** (**long**), die den Index des Elements enthält, an dem die Suche gestartet werden soll.

</dd> <dt>

<span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*Searchstring*
</dt> <dd>

**Zeichenfolge,** die den zu suchden Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**long**) zurück, die den Index des Elements enthält, das die Zeichenfolge enthält.

## <a name="remarks"></a>Hinweise

Um die Suche in der ersten Zeile des Listenfeldsteuerelements zu starten, verwenden Sie 1 als *startIndex*. Um nach dem Auffinden der ersten Zeile weiterhin nach Text zu suchen, verwenden Sie den zurückgegebenen Zeilenindex als *startIndex,* und die Suche beginnt in der nächsten Zeile. Diese Methode sucht nach Teilzeichenfolgen und berücksichtigt nicht die Groß-/Kleinschreibung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LISTBOX-Element**](listbox-element.md)
</dt> </dl>

 

 






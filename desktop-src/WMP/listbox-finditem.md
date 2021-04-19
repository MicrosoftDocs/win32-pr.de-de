---
title: ListBox. FindItem
description: Die FindItem-Methode sucht nach einer angegebenen Zeichenfolge, beginnend mit dem Element, das dem angegebenen Element Index folgt.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- ListBox. FindItem-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356467"
---
# <a name="listboxfinditem"></a>ListBox. FindItem

Die **FindItem** -Methode sucht nach einer angegebenen Zeichenfolge, beginnend mit dem Element, das dem angegebenen Element Index folgt.

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Start Index*
</dt> <dd>

**Zahl** (**Long**), die den Index des Elements enthält, an dem die Suche beginnen soll.

</dd> <dt>

<span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*
</dt> <dd>

**Zeichenfolge** , die den zu suchenden Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück, die den Index des Elements enthält, das die Zeichenfolge enthält.

## <a name="remarks"></a>Bemerkungen

Um die Suche in der ersten Zeile des Listenfeld-Steuer Elements zu starten, verwenden Sie 1 als *startIndex*. Wenn Sie nach dem Suchen der ersten Zeile nach Text suchen möchten, verwenden Sie den zurückgegebenen Zeilen Index als *startIndex*, und die Suche wird in der nächsten Zeile gestartet. Diese Methode sucht nach Teil Zeichenfolgen und wird nicht zwischen Groß-und Kleinschreibung unterschieden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ListBox-Element**](listbox-element.md)
</dt> </dl>

 

 






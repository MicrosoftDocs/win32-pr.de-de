---
title: ListBox. getnextselecteditem
description: Die getnextselecteditem-Methode ruft das nächste ausgewählte Element im Listenfeld-Steuerelement ab, beginnend mit dem Element, das mit dem angegebenen Index beginnt.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- ListBox. getnextselecteditem-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354154"
---
# <a name="listboxgetnextselecteditem"></a>ListBox. getnextselecteditem

Die **getnextselecteditem** -Methode ruft das nächste ausgewählte Element im Listenfeld-Steuerelement ab, beginnend mit dem Element, das mit dem angegebenen Index beginnt.

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Start Index*
</dt> <dd>

**Number** (**Long**) mit dem Index des Elements, das dem abgerufenen Element vorangestellt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück, die den Index des nächsten ausgewählten Elements enthält.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie zum Starten der Suche von Anfang an den Wert 1 für den Start Index.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ListBox-Element**](listbox-element.md)
</dt> </dl>

 

 






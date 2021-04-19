---
title: ListBox. InsertItem
description: Die InsertItem-Methode fügt den angegebenen Text am angegebenen Index im Listenfeld-Steuerelement ein.
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- ListBox. InsertItem-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3600b40ca164c71bd62c0a9a368516d6ad0e1edd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366065"
---
# <a name="listboxinsertitem"></a>ListBox. InsertItem

Die **InsertItem** -Methode fügt den angegebenen Text am angegebenen Index im Listenfeld-Steuerelement ein.

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Sin*
</dt> <dd>

**Zahl** (**Long**), die den Index der abzurufenden Zeile enthält.

</dd> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

**Zeichenfolge** , die den einzufügenden Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn eine Zeile eingefügt wird, werden die Zeilen Indizes für die Zeilen unterhalb der eingefügten Zeile um 1 erhöht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ListBox-Element**](listbox-element.md)
</dt> </dl>

 

 






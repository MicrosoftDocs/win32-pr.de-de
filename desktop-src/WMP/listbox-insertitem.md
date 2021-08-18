---
title: LISTBOX.insertItem
description: Die insertItem-Methode fügt den angegebenen Text am angegebenen Index in das Listenfeld-Steuerelement ein.
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- LISTBOX.insertItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0344bbc9fbe4f8f2b680866f70c0fe16398ad08cbf4a916c454223fdff04614e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135303"
---
# <a name="listboxinsertitem"></a>LISTBOX.insertItem

Die **insertItem-Methode** fügt den angegebenen Text am angegebenen Index in das Listenfeld-Steuerelement ein.

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Index*
</dt> <dd>

**Number** (**long**), die den Index der abzurufenden Zeile enthält.

</dd> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

**Eine Zeichenfolge,** die den zu einfügenden Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn eine Zeile eingefügt wird, werden die Zeilenindizes für die Zeilen unterhalb der eingefügten Zeile um eins erhöht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LISTBOX-Element**](listbox-element.md)
</dt> </dl>

 

 






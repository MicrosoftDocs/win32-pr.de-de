---
title: EDITBOX.getLine
description: Die getLine-Methode ruft den Text für die Zeile mit dem angegebenen Index ab.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- EDITBOX.getLine-Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28d555cb684fa849b5fc7cdb42ebaf0ab4fb278b4ef126845add2f12ddf59948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578836"
---
# <a name="editboxgetline"></a>EDITBOX.getLine

Die **getLine-Methode** ruft den Text für die Zeile mit dem angegebenen Index ab.

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Index*
</dt> <dd>

**Number** (**long**), die den Index der abzurufenden Zeile enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge zurück.**

## <a name="remarks"></a>Hinweise

Wenn der Index ungültig ist, wird eine leere Zeichenfolge zurückgegeben. Diese Methode kann erst aufgerufen werden, nachdem das Steuerelement sichtbar wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EDITBOX-Element**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getLineFromChar**](editbox-getlinefromchar.md)
</dt> <dt>

[**EDITBOX.getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 






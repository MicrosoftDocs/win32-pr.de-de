---
title: EditBox. getline
description: Die getline-Methode ruft den Text für die Zeile mit dem angegebenen Index ab.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- EditBox. getline-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0b9a15f9eff8c2612e7a242a205c1d9411a60c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357952"
---
# <a name="editboxgetline"></a>EditBox. getline

Die **getline** -Methode ruft den Text für die Zeile mit dem angegebenen Index ab.

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Sin*
</dt> <dd>

**Zahl** (**Long**), die den Index der abzurufenden Zeile enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Index ungültig ist, wird eine leere Zeichenfolge zurückgegeben. Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EditBox-Element**](editbox-element.md)
</dt> <dt>

[**EditBox. getlinefromchar**](editbox-getlinefromchar.md)
</dt> <dt>

[**EditBox. getlineingedex**](editbox-getlineindex.md)
</dt> </dl>

 

 






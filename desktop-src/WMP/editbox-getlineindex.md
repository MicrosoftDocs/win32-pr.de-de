---
title: EditBox. getlineingedex
description: Die getlineindex-Methode ruft den Zeichen Index des ersten Zeichens in der Zeile mit dem angegebenen Zeilen Index ab.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- EditBox. getlineingedex-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352176"
---
# <a name="editboxgetlineindex"></a>EditBox. getlineingedex

Die **getlineindex** -Methode ruft den Zeichen Index des ersten Zeichens in der Zeile mit dem angegebenen Zeilen Index ab.

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Sin*
</dt> <dd>

**Number** (**Long**) mit dem Index der Zeile, deren Zeichen Index abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der angegebene Zeilen Index 1 ist, wird die Zeile verwendet, die die Einfügemarke enthält.

Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EditBox-Element**](editbox-element.md)
</dt> <dt>

[**EditBox. getline**](editbox-getline.md)
</dt> <dt>

[**EditBox. getlinefromchar**](editbox-getlinefromchar.md)
</dt> </dl>

 

 






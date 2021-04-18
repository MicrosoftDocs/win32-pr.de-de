---
title: EditBox. getlinefromchar
description: Die getlinefromchar-Methode ruft den Zeilen Index für den angegebenen Zeichen Index ab.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- EditBox. getlinefromchar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365852"
---
# <a name="editboxgetlinefromchar"></a>EditBox. getlinefromchar

Die **getlinefromchar** -Methode ruft den Zeilen Index für den angegebenen Zeichen Index ab.

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Sin*
</dt> <dd>

**Zahl** (**Long**), die den Index des Zeichens enthält, dessen Zeilen Index abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die angegebene Zeichenposition 1 ist, ruft diese Methode den Zeilen Index der aktuellen Zeile ab.

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

[**EditBox. getlineingedex**](editbox-getlineindex.md)
</dt> </dl>

 

 






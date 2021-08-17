---
title: EDITBOX.getLineFromChar
description: Die getLineFromChar-Methode ruft den Zeilenindex für den angegebenen Zeichenindex ab.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- EDITBOX.getLineFromChar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 110030c3c756a91c993857cef125c51669f71eb9a358eb7261205fde0b0ad4a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749306"
---
# <a name="editboxgetlinefromchar"></a>EDITBOX.getLineFromChar

Die **getLineFromChar-Methode** ruft den Zeilenindex für den angegebenen Zeichenindex ab.

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Index*
</dt> <dd>

**Number** (**long**), die den Index des Zeichens enthält, dessen Zeilenindex abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**long**) zurück.

## <a name="remarks"></a>Hinweise

Wenn die angegebene Zeichenposition 1 ist, ruft diese Methode den Zeilenindex der aktuellen Zeile ab.

Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EDITBOX-Element**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getLine**](editbox-getline.md)
</dt> <dt>

[**EDITBOX.getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 






---
title: EditBox. getSelectionEnd
description: Die getSelectionEnd-Methode ruft die Endposition des ausgewählten Texts im EditBox-Steuerelement ab.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- EditBox. getSelectionEnd-Windows-Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372772"
---
# <a name="editboxgetselectionend"></a>EditBox. getSelectionEnd

Die **getSelectionEnd** -Methode ruft die Endposition des ausgewählten Texts im EditBox-Steuerelement ab.

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**Long**) zurück.

## <a name="remarks"></a>Bemerkungen

Wenn kein Text ausgewählt ist, gibt diese Methode die Position der Einfügemarke zurück.

Wenn das Steuerelement mehrzeilige Elemente ist, gibt diese Methode den Zeichen Index im-Steuerelement zurück, nicht den Zeilen Index.

Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EditBox-Element**](editbox-element.md)
</dt> <dt>

[**EditBox. getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**EditBox. ReplaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**EditBox. setSelection**](editbox-setselection.md)
</dt> </dl>

 

 






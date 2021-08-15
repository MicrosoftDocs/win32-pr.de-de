---
title: EDITBOX.getSelectionEnd
description: Die getSelectionEnd-Methode ruft die Endposition des ausgewählten Texts im Editbox-Steuerelement ab.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- EDITBOX.getSelectionEnd Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8dff56bda802286ed76ba3b448478dfa57d005c13baf229612e190bbf163b25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838844"
---
# <a name="editboxgetselectionend"></a>EDITBOX.getSelectionEnd

Die **getSelectionEnd-Methode** ruft die Endposition des ausgewählten Texts im Editbox-Steuerelement ab.

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** **(long) zurück.**

## <a name="remarks"></a>Hinweise

Wenn kein Text ausgewählt ist, gibt diese Methode die Position der Einfügemarke zurück.

Wenn das Steuerelement mehrzeilenweise ist, gibt diese Methode den Zeichenindex im -Steuerelement zurück, nicht den Zeilenindex.

Diese Methode kann erst aufgerufen werden, nachdem das Steuerelement sichtbar wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EDITBOX-Element**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**EDITBOX.replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**EDITBOX.setSelection**](editbox-setselection.md)
</dt> </dl>

 

 






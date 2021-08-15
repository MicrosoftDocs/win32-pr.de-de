---
title: EDITBOX.getSelectionStart
description: Die getSelectionStart-Methode ruft die Anfangsposition des ausgewählten Texts im Bearbeitungsfeld-Steuerelement ab.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- EDITBOX.getSelectionStart Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c555cc7231440e15275dcd44a2508f1d8cc5ba53a8137db861cc71b61528ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340031"
---
# <a name="editboxgetselectionstart"></a>EDITBOX.getSelectionStart

Die **getSelectionStart-Methode** ruft die Anfangsposition des ausgewählten Texts im Bearbeitungsfeld-Steuerelement ab.

``` syntax
        elementID.getSelectionStart()
```

## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**long**) zurück.

## <a name="remarks"></a>Hinweise

Wenn kein Text ausgewählt ist, gibt diese Methode die Position der Einfügemarke zurück.

Wenn das Steuerelement mehrzeiligen Ist, gibt diese Methode den Zeichenindex im Steuerelement zurück, nicht den Zeilenindex.

Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EDITBOX-Element**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getSelectionEnd**](editbox-getselectionend.md)
</dt> <dt>

[**EDITBOX.replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**EDITBOX.setSelection**](editbox-setselection.md)
</dt> </dl>

 

 






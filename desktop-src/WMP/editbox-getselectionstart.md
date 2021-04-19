---
title: EditBox. getSelectionStart
description: Die getSelectionStart-Methode ruft die Anfangsposition des ausgewählten Texts im EditBox-Steuerelement ab.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- EditBox. getSelectionStart Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2508119e5b1d46d09b3531582e86caad7e7facbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362178"
---
# <a name="editboxgetselectionstart"></a>EditBox. getSelectionStart

Die **getSelectionStart** -Methode ruft die Anfangsposition des ausgewählten Texts im EditBox-Steuerelement ab.

``` syntax
        elementID.getSelectionStart()
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

[**EditBox. getSelectionEnd**](editbox-getselectionend.md)
</dt> <dt>

[**EditBox. ReplaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**EditBox. setSelection**](editbox-setselection.md)
</dt> </dl>

 

 






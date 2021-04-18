---
title: EditBox. ReplaceSelection
description: Die ReplaceSelection-Methode ersetzt die aktuelle Auswahl durch den angegebenen Text.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- EditBox. ReplaceSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368328"
---
# <a name="editboxreplaceselection"></a>EditBox. ReplaceSelection

Die **ReplaceSelection** -Methode ersetzt die aktuelle Auswahl durch den angegebenen Text.

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*NewValue*
</dt> <dd>

**Zeichenfolge** , die den Text enthält, um den markierten Text zu ersetzen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn kein Text ausgewählt ist, wird der Ersetzungstext an der aktuellen Position der Einfügemarke eingefügt.

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

[**EditBox. getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**EditBox. setSelection**](editbox-setselection.md)
</dt> </dl>

 

 






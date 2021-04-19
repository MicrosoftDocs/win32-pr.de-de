---
title: EditBox. editstyle
description: Das editstyle-Attribut gibt den Stil des Steuer Elements "Bearbeitungsfeld" an oder ruft ihn ab.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- EditBox. editstyle-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366771"
---
# <a name="editboxeditstyle"></a>EditBox. editstyle

Das **editstyle** -Attribut gibt den Stil des Steuer Elements "Bearbeitungsfeld" an oder ruft ihn ab.

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen der folgenden Werte enthält.



| Wert     | BESCHREIBUNG                                                                     |
|-----------|---------------------------------------------------------------------------------|
| normal    | Standard. Zeigt den normalen Text in einer einzelnen Zeile an.                                 |
| password  | Zeigt Sternchen ( \* ) anstelle von Text an. Kann nur zur Entwurfszeit angegeben werden. |
| Großbuchstaben | Zeigt Text als Großbuchstaben an.                                                 |
| Kleinbuchstaben | Zeigt Text in Kleinbuchstaben an.                                                 |
| number    | Zeigt nur Zahlen an.                                                          |
| mehrzeiligen | Zeigt mehrere Textzeilen an. Kann nur zur Entwurfszeit angegeben werden.          |



 

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann zur Entwurfszeit nur auf "Password" oder "Multiline" festgelegt werden. Wenn Sie auf "Multiline" festgelegt ist, kann der Wert zur Laufzeit nicht geändert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EditBox-Element**](editbox-element.md)
</dt> </dl>

 

 






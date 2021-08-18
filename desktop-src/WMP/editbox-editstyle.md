---
title: EDITBOX.editStyle
description: Das editStyle-Attribut gibt das Format des Bearbeitungsfeld-Steuerelements an oder ruft es ab.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- EDITBOX.editStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4d40d1933c68c4e34707f01a4d425045c773297e8567ba8ea13a88c6fbc57c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749461"
---
# <a name="editboxeditstyle"></a>EDITBOX.editStyle

Das **editStyle-Attribut** gibt das Format des Bearbeitungsfeld-Steuerelements an oder ruft es ab.

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff, die einen der folgenden Werte enthält.



| Wert     | Beschreibung                                                                     |
|-----------|---------------------------------------------------------------------------------|
| normal    | Standard. Zeigt normalen Text in einer einzelnen Zeile an.                                 |
| password  | Zeigt Sternchen ( \* ) statt Text an. Kann nur zur Entwurfszeit angegeben werden. |
| Großbuchstaben | Zeigt Text in Großbuchstaben an.                                                 |
| Kleinbuchstaben | Zeigt Text in Kleinbuchstaben an.                                                 |
| number    | Zeigt nur Zahlen an.                                                          |
| Mehrzeiligen | Zeigt mehrere Textzeilen an. Kann nur zur Entwurfszeit angegeben werden.          |



 

## <a name="remarks"></a>Hinweise

Dieses Attribut kann zur Entwurfszeit nur auf "password" oder "multiline" festgelegt werden. Wenn er auf "multiline" festgelegt ist, kann der Wert zur Laufzeit nicht geändert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EDITBOX-Element**](editbox-element.md)
</dt> </dl>

 

 






---
title: Controls. CurrentPosition
description: Die CurrentPosition-Eigenschaft gibt die aktuelle Position im Medien Element in Sekunden vom Anfang an oder ruft Sie ab.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Controls. CurrentPosition-Fenster Media Player
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371712"
---
# <a name="controlscurrentposition"></a>Controls. CurrentPosition

Die **CurrentPosition** -Eigenschaft gibt die aktuelle Position im Medien Element in Sekunden vom Anfang an oder ruft Sie ab.

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/schreibnummer (**Double**). 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **CurrentPosition** verwendet, um eine vom Benutzer bereitgestellte Position zu suchen. Ein HTML-Schaltflächen Element wird erstellt, um den JScript-Code auszuführen. Ein HTML-Text Eingabe Element namens SetPosition wurde erstellt, um dem Benutzer einen Wert in Sekunden zu akzeptieren. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> </dl>

 

 






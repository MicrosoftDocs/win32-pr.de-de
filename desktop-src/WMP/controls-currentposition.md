---
title: Controls.currentPosition
description: Die currentPosition-Eigenschaft gibt die aktuelle Position im Medienelement in Sekunden ab dem Anfang an oder ruft sie ab.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Controls.currentPosition Windows Media Player
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
ms.openlocfilehash: be64d23b65a396cfb15e9f7b19b4571bdb26cbb7f308241e9a381375b9d26a40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341877"
---
# <a name="controlscurrentposition"></a>Controls.currentPosition

Die **currentPosition-Eigenschaft** gibt die aktuelle Position im Medienelement in Sekunden ab dem Anfang an oder ruft sie ab.

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/Schreibnummer (**double**). 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **currentPosition verwendet,** um eine vom Benutzer bereitgestellte Position zu suchen. Es wird ein HTML BUTTON-Element erstellt, um den JScript auszuführen. Ein HTML TEXT-Eingabeelement namens setPosition wurde erstellt, um einen Wert in Sekunden vom Benutzer zu akzeptieren. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> </dl>

 

 






---
title: Controls. Previous-Methode
description: Die vorherige Methode legt das aktuelle Element auf das vorherige Element in der Wiedergabeliste fest.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- vorherige Methode, Windows Media Player
- vorherige Methode, Windows Media Player, Steuerelement Klasse
- Steuerelement-Klasse, Windows Media Player, vorherige Methode
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372147"
---
# <a name="controlsprevious-method"></a>Controls. Previous-Methode

Die **vorherige** Methode legt das aktuelle Element auf das vorherige Element in der Wiedergabeliste fest.

## <a name="syntax"></a>Syntax


```JScript
Controls.previous()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn sich die Wiedergabeliste auf dem ersten Eintrag befindet, wenn **Previous** aufgerufen wird, wird der letzte Eintrag in der Wiedergabeliste zum aktuellen Eintrag.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **zurück verwendet, um zum** vorherigen Element in der aktuellen Wiedergabeliste zu wechseln. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
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
</dt> <dt>

[**Steuerelemente. Next**](controls-next.md)
</dt> <dt>

[**Controls. Pause**](controls-stop.md)
</dt> </dl>

 

 






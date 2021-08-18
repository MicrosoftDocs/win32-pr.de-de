---
title: Controls.previous-Methode
description: Die vorherige Methode legt das aktuelle Element auf das vorherige Element in der Wiedergabeliste fest.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- vorherige Methode Windows Media Player
- previous-Methode Windows Media Player , Controls-Klasse
- Controls-Klasse Windows Media Player , vorherige Methode
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
ms.openlocfilehash: f67dbc80fb731f32eefb36f2a0f66c852da3da69dbc6b7ae56c03ebafb06e07e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119329"
---
# <a name="controlsprevious-method"></a>Controls.previous-Methode

Die **vorherige** Methode legt das aktuelle Element auf das vorherige Element in der Wiedergabeliste fest.

## <a name="syntax"></a>Syntax


```JScript
Controls.previous()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn sich die Wiedergabeliste beim Aufrufen des **vorherigen** Eintrags im ersten Eintrag befindet, wird der letzte Eintrag in der Wiedergabeliste zum aktuellen Eintrag.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML BUTTON-Element erstellt, das **mithilfe** von previous zum vorherigen Element in der aktuellen Wiedergabeliste wechselt. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Controls.next**](controls-next.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> </dl>

 

 






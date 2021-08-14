---
title: Controls.stop-Methode
description: Die Stop-Methode beendet die Wiedergabe des Medienelements. | Controls.stop-Methode
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- Stop-Windows Media Player
- Stop-Methode Windows Media Player , Controls-Klasse
- Steuert die klasse Windows Media Player , stop-Methode
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b882f462903c2c5f75a3655cd26b927e7439043828dad41fcce7d0e64e4ce812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580159"
---
# <a name="controlsstop-method"></a>Controls.stop-Methode

Die **Stop-Methode** beendet die Wiedergabe des Medienelements.

## <a name="syntax"></a>Syntax


```JScript
Controls.stop()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode bewirkt Windows Media Player, dass alle systemressourcen, die sie verwendet, wie z. B. das Audiogerät, frei geben. Das aktuelle Medienelement wird jedoch nicht freigegeben.

Wenn der Player beendet wird, wird die Spur an den Anfang zurücklädt. Der **Aufruf** von play beginnt dann von Anfang an mit der Wiedergabe des Clips. Um einen Wiedergabevorgang anzuhalten, ohne die aktuelle Position zu ändern, verwenden Sie die **pause-Methode.**

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML BUTTON-Element erstellt, das **stop verwendet,** um die Wiedergabe zu beenden. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Controls.next**](controls-next.md)
</dt> <dt>

[**Controls.pause**](controls-pause.md)
</dt> <dt>

[**Controls.previous**](controls-previous.md)
</dt> </dl>

 

 






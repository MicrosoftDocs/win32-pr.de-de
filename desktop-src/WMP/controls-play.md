---
title: Controls.play-Methode
description: Die Wiedergabemethode bewirkt, dass das aktuelle Medienelement mit der Wiedergabe beginnt, oder setzt die Wiedergabe eines angehaltenen Elements fort.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- play-Methode Windows Media Player
- Play-Methode Windows Media Player , Controls-Klasse
- Steuert die Klasse Windows Media Player , play-Methode
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ce3c1572515b320a62b1b3c76aac72e44101e21f3b0f89d7c3356046ea95f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997450"
---
# <a name="controlsplay-method"></a>Controls.play-Methode

Die **Wiedergabemethode** bewirkt, dass das aktuelle Medienelement mit der Wiedergabe beginnt, oder setzt die Wiedergabe eines angehaltenen Elements fort.

## <a name="syntax"></a>Syntax


```JScript
Controls.play()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn diese Methode beim schnellen Weiterleiten oder Zurückspulen aufgerufen wird, *Einstellungen* der Wert von . **rate** ist auf 1,0 festgelegt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML BUTTON-Element erstellt, das **play** verwendet, um das aktuelle Medienelement wiederzuspielen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
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
</dt> </dl>

 

 






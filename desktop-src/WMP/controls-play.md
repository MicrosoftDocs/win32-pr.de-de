---
title: Controls. Play-Methode
description: Die Play-Methode bewirkt, dass das aktuelle Medien Element wiedergegeben wird, oder die Wiedergabe eines angehaltenen Elements wird wieder aufgenommen.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- Wiedergabemethode Windows Media Player
- Play-Methode, Windows Media Player, Controls-Klasse
- Steuerelement-Klasse, Windows Media Player, Wiedergabemethode
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
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358696"
---
# <a name="controlsplay-method"></a>Controls. Play-Methode

Die **Play** -Methode bewirkt, dass das aktuelle Medien Element wiedergegeben wird, oder die Wiedergabe eines angehaltenen Elements wird wieder aufgenommen.

## <a name="syntax"></a>Syntax


```JScript
Controls.play()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode während der schnellen Weiterleitung oder rebuggen aufgerufen wird, der Wert von *Settings*. die **Rate** ist auf 1,0 festgelegt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **Play** zum Wiedergeben des aktuellen Medien Elements verwendet. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> </dl>

 

 






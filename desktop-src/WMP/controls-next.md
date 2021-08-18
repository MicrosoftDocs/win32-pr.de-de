---
title: Controls.next-Methode
description: Die nächste Methode legt das aktuelle Element auf das nächste Element in der Wiedergabeliste fest.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- next-Methode Windows Media Player
- next-Methode Windows Media Player , Controls-Klasse
- Steuert die Klasse Windows Media Player , next-Methode
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a40c063163b0dadaa3db2d0d6281ace64312f68ee999763e6b27d4bd98f84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997470"
---
# <a name="controlsnext-method"></a>Controls.next-Methode

Die **nächste** Methode legt das aktuelle Element auf das nächste Element in der Wiedergabeliste fest.

## <a name="syntax"></a>Syntax


```JScript
Controls.next()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn sich die Wiedergabeliste beim **nächsten** Aufruf auf dem letzten Eintrag befindet, wird der erste Eintrag in der Wiedergabeliste zum aktuellen Eintrag.

Bei serverseitigen Wiedergabelisten überspringt diese Methode das nächste Element in der serverseitigen Wiedergabeliste, nicht die Clientwiedergabeliste.

Beim Wiedergeben einer DVD überspringt diese Methode das nächste logische Kapitel in der Wiedergabesequenz, das möglicherweise nicht das nächste Kapitel in der Wiedergabeliste ist. Bei der Wiedergabe von DVD-Dateien wird diese Methode weiterhin mit der nächsten Methode übersprungen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML BUTTON-Element erstellt, das **neben** verwendet, um zum nächsten Element in der aktuellen Wiedergabeliste zu wechseln. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
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

[**Controls.previous**](controls-previous.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> </dl>

 

 






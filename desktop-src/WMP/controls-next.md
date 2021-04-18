---
title: Controls. Next-Methode
description: Die Next-Methode legt das aktuelle Element auf das nächste Element in der Wiedergabeliste fest.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- nächste Methode, Windows Media Player
- Next Method Windows Media Player, Controls-Klasse
- Steuerelemente-Klasse, Windows Media Player, nächste Methode
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
ms.openlocfilehash: 8f58e6d11eafe38b4ab26e0275bd5c986cd4e4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371790"
---
# <a name="controlsnext-method"></a>Controls. Next-Methode

Die **Next** -Methode legt das aktuelle Element auf das nächste Element in der Wiedergabeliste fest.

## <a name="syntax"></a>Syntax


```JScript
Controls.next()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn sich die Wiedergabeliste auf dem letzten Eintrag befindet, wenn **Next** aufgerufen wird, wird der erste Eintrag in der Wiedergabeliste zum aktuellen Eintrag.

Bei serverseitigen Wiedergabelisten springt diese Methode zum nächsten Element in der serverseitigen Wiedergabeliste, nicht zur Client Wiedergabeliste.

Beim Abspielen einer DVD überspringt diese Methode das nächste logische Kapitel in der Wiedergabe Sequenz, das möglicherweise nicht das nächste Kapitel in der Wiedergabeliste ist. Bei der Wiedergabe von DVD-Stills springt diese Methode zum nächsten weiter.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das **Next** verwendet, um zum nächsten Element in der aktuellen Wiedergabeliste zu wechseln. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Controls-Objekt**](controls-object.md)
</dt> <dt>

[**Controls. Previous**](controls-previous.md)
</dt> <dt>

[**Controls. Pause**](controls-stop.md)
</dt> </dl>

 

 






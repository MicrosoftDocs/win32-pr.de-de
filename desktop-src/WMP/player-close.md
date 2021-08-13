---
title: Player.close-Methode
description: Die close-Methode gibt Windows Media Player Ressourcen frei.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- close-Methode Windows Media Player
- close-Methode Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , close-Methode
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29e68aed11b095dff80c8c91c88410f98b9a236bbcadcbff75da0fc0de392fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467880"
---
# <a name="playerclose-method"></a>Player.close-Methode

Die **close-Methode** gibt Windows Media Player Ressourcen frei.

## <a name="syntax"></a>Syntax


```JScript
Player.close()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode schließt die aktuelle digitale Mediendatei, nicht Windows Media Player sich selbst.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML BUTTON-Element erstellt, das beim Klicken die Wiedergabe in Windows Media Player beendet und die verwendeten Ressourcen freigibt. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






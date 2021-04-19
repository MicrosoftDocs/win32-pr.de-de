---
title: Player. Close-Methode
description: Die Close-Methode gibt Windows Media Player-Ressourcen frei.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- Schließen von Methoden Fenstern Media Player
- Close-Methode, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, Close-Methode
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
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358620"
---
# <a name="playerclose-method"></a>Player. Close-Methode

Die **Close** -Methode gibt Windows Media Player-Ressourcen frei.

## <a name="syntax"></a>Syntax


```JScript
Player.close()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode schließt die aktuelle digitale Mediendatei, nicht Windows Media Player selbst.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das beim Klicken auf die Wiedergabe in Windows-Media Player beendet und die verwendeten Ressourcen freigibt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






---
title: Player.newMedia-Methode
description: Die newMedia-Methode erstellt ein neues Media-Objekt.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- newMedia-Windows Media Player
- newMedia-Methode Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , newMedia-Methode
topic_type:
- apiref
api_name:
- Player.newMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e3ad30db7ec43bcc0ee6c1470dc608ccf1625390486d9fcd0fd4bf018affdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338105"
---
# <a name="playernewmedia-method"></a>Player.newMedia-Methode

Die **newMedia-Methode** erstellt ein neues **Media-Objekt.**

## <a name="syntax"></a>Syntax


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URL* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die die URL der digitalen Mediendatei enthält, mit der das **Medienobjekt erstellt** werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Media-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Der *URL-Parameter* darf keine leere Zeichenfolge oder NULL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






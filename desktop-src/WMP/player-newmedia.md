---
title: Player. newmedia-Methode
description: Die newmedia-Methode erstellt ein neues Medienobjekt.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- newmedia-Methode, Windows-Media Player
- newmedia-Methode, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, newmedia-Methode
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
ms.openlocfilehash: aaafb97f836135aa9dd112372b1931c8561cb40b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354765"
---
# <a name="playernewmedia-method"></a>Player. newmedia-Methode

Die **newmedia** -Methode erstellt ein neues **Medien** Objekt.

## <a name="syntax"></a>Syntax


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URL* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die URL der digitalen Mediendatei enthält, mit der das **Medien** Objekt erstellt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Medien** Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Der *URL* -Parameter darf keine leere Zeichenfolge oder NULL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






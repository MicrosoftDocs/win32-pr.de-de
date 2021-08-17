---
title: Player.openPlayer-Methode
description: Die openPlayer-Methode wird Windows Media Player der angegebenen URL geöffnet. | Player.openPlayer-Methode
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- openPlayer-Windows Media Player
- openPlayer-Methode Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , openPlayer-Methode
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42245ec29f7d7caeac17f116d1f592f74f10ba95716d5d16734ecd21bbcbb60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747568"
---
# <a name="playeropenplayer-method"></a>Player.openPlayer-Methode

Die **openPlayer-Methode** wird Windows Media Player der angegebenen URL geöffnet.

## <a name="syntax"></a>Syntax


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URL* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die die URL des medienelements darstellt, das wiedergibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode startet Windows Media Player, bei der die angegebene URL als aktuelles Medienelement festgelegt ist. Wenn der Player zuvor im Skinmodus geschlossen wurde, wird er mit der zuletzt vom Benutzer ausgewählten Skin geöffnet. Andernfalls wird der Player im Vollmodus geöffnet.

Wenn diese Methode von einem Windows Media PlayerActiveX-Steuerelement aufgerufen wird, das in den Remotemodus eingebettet ist, ist das Verhalten mit *dem PlayerApplication identisch.* **switchToPlayerApplication-Methode.**

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**PlayerApplication.switchToPlayerApplication**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 






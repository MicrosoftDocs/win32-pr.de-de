---
title: Player. openplayer-Methode
description: Die openplayer-Methode öffnet Windows Media Player unter Verwendung der angegebenen URL. | Player. openplayer-Methode
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- openplayer-Methode, Windows-Media Player
- openplayer-Methode, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, openplayer-Methode
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
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356427"
---
# <a name="playeropenplayer-method"></a>Player. openplayer-Methode

Die **openplayer** -Methode öffnet Windows Media Player unter Verwendung der angegebenen URL.

## <a name="syntax"></a>Syntax


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*URL* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die URL des wieder zugebende Medien Elements darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird Windows Media Player gestartet, wobei der angegebene URL als Aktuelles Medien Element festgelegt ist. Wenn der Spieler zuvor im Skin-Modus geschlossen wurde, wird er mithilfe der Skin geöffnet, die zuletzt vom Benutzer ausgewählt wurde. Andernfalls wird der Spieler im vollständigen Modus geöffnet.

Wenn diese Methode von einem Windows Media-playeractivex-Steuerelement aufgerufen wird, das im Remote Modus eingebettet ist, ist das Verhalten mit der *playerapplication* identisch. **switchtoplayerapplication** -Methode.

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Playerapplication. switchtoplayerapplication**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 






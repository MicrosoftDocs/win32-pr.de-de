---
title: Player. KeyUp-Ereignis
description: Das KeyUp-Ereignis tritt auf, wenn eine Taste losgelassen wird. | Player. KeyUp-Ereignis
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- KeyUp-Ereignisfenster Media Player
- KeyUp-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, KeyUp-Ereignis
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373679"
---
# <a name="playerkeyup-event"></a>Player. KeyUp-Ereignis

Das **KeyUp** -Ereignis tritt auf, wenn eine Taste losgelassen wird.

## <a name="syntax"></a>Syntax


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nKeyCode* 
</dt> <dd>

**Number** (**int**), der angibt, welcher physische Schlüssel gedrückt wird. Mögliche Werte finden Sie unter " [Player. KeyDown](player-player-keydown.md)"-Ereignis.

</dd> <dt>

*nshiftstate* 
</dt> <dd>

**Number** (**int**): gibt ein Bitfeld mit den geringsten signifikanten Bits an, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






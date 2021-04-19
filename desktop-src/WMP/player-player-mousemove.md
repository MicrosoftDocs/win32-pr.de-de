---
title: Player. mousermove-Ereignis
description: Das MouseMove-Ereignis tritt auf, wenn der Mauszeiger verschoben wird. | Player. mousermove-Ereignis
ms.assetid: 026928a3-25a6-4e67-837a-df71c05e49ee
keywords:
- Media Player "mousmove-Ereignisfenster"
- Mousmove-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, mousmove-Ereignis
topic_type:
- apiref
api_name:
- Player.MouseMove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a536609ba5e3095fed9826b071084491a81b385f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358010"
---
# <a name="playermousemove-event"></a>Player. mousermove-Ereignis

Das **MouseMove** -Ereignis tritt auf, wenn der Mauszeiger verschoben wird.

## <a name="syntax"></a>Syntax


```JScript
Player.MouseMove(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nschaltfläche* 
</dt> <dd>

**Number** (**int**): gibt ein Bitfeld mit Bits an, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schaltflächen gedrückt werden.

</dd> <dt>

*nshiftstate* 
</dt> <dd>

**Number** (**int**): gibt ein Bitfeld mit den geringsten signifikanten Bits an, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.

</dd> <dt>

*Designer* 
</dt> <dd>

**Number** (**Long**) gibt die x-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements an.

</dd> <dt>

*herrlichen* 
</dt> <dd>

**Number** (**Long**) gibt die y-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements an.

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

 

 






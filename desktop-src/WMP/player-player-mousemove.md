---
title: Player.MouseMove-Ereignis
description: Das MouseMove-Ereignis tritt auf, wenn der Mauszeiger bewegt wird. | Player.MouseMove-Ereignis
ms.assetid: 026928a3-25a6-4e67-837a-df71c05e49ee
keywords:
- Windows Media Player des MouseMove-Ereignisses
- MouseMove-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , MouseMove-Ereignis
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
ms.openlocfilehash: fb864e2a8bf686bd39f2d44ba8f5558516d72034f606579a79c76a5d86ab3990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338097"
---
# <a name="playermousemove-event"></a>Player.MouseMove-Ereignis

Das **MouseMove-Ereignis** tritt auf, wenn der Mauszeiger bewegt wird.

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

*nButton* 
</dt> <dd>

**Number** (**int**), die ein Bitfeld mit Bits angibt, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Einige, alle oder keine der Bits können festgelegt werden, was darauf hinweist, dass einige, alle oder keine der Schaltflächen gedrückt werden.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**), die ein Bitfeld mit den am wenigsten signifikanten Bits angibt, die der UMSCHALTTASTE (Bit 0), der STRG-Taste (Bit 1) und der ALT-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden, was darauf hinweist, dass einige, alle oder keine der Tasten gedrückt werden.

</dd> <dt>

*Fx* 
</dt> <dd>

**Number** (**long**), die die x-Koordinate des Mauszeigers relativ zur oberen linken Ecke des Steuerelements angibt.

</dd> <dt>

*Fy* 
</dt> <dd>

**Number** (**long**), die die y-Koordinate des Mauszeigers relativ zur oberen linken Ecke des Steuerelements angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten JScript-Datei auf eine Methode zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






---
title: Player.DoubleClick-Ereignis
description: Das DoubleClick-Ereignis tritt auf, wenn der Benutzer auf eine Maustaste doppelklickt.
ms.assetid: e2055cff-e4b0-49e3-a93a-7084789b6842
keywords:
- DoubleClick-Ereignis Windows Media Player
- DoubleClick-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , DoubleClick-Ereignis
topic_type:
- apiref
api_name:
- Player.DoubleClick
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8e6a21c46a8b1c5d7960d70233e38333f9ff2052826bb68d573d4b2f0cd15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995920"
---
# <a name="playerdoubleclick-event"></a>Player.DoubleClick-Ereignis

Das **DoubleClick-Ereignis** tritt auf, wenn der Benutzer auf eine Maustaste doppelklickt.

## <a name="syntax"></a>Syntax


```JScript
Player.DoubleClick(
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

**Number** (**int**), die ein Bitfeld mit Bits angibt, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Es wird nur eines der Bits festgelegt, das die Schaltfläche angibt, die das Ereignis verursacht hat.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






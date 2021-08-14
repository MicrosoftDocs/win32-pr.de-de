---
title: Player.MouseUp-Ereignis
description: Das MouseUp-Ereignis tritt auf, wenn der Benutzer eine Maustaste freigibt. | Player.MouseUp-Ereignis
ms.assetid: 0f209fc4-2aad-46b1-84ba-2bfbecbe2930
keywords:
- Windows Media Player des MouseUp-Ereignisses
- MouseUp-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , MouseUp-Ereignis
topic_type:
- apiref
api_name:
- Player.MouseUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 728259d1a64367101da3645e15c0274ef01fc9115ec6fb98c29c5c2a7baf2970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835209"
---
# <a name="playermouseup-event"></a>Player.MouseUp-Ereignis

Das **MouseUp-Ereignis** tritt auf, wenn der Benutzer eine Maustaste freigibt.

## <a name="syntax"></a>Syntax


```JScript
Player.MouseUp(
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

 

 






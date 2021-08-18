---
title: Player.Click-Ereignis
description: Das Click-Ereignis tritt auf, wenn der Benutzer auf eine Maustaste klickt.
ms.assetid: c2d5fab9-9b53-4d0c-a001-8cbf4430e713
keywords:
- Klicken Sie auf Windows Media Player
- Click event Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , Click-Ereignis
topic_type:
- apiref
api_name:
- Player.Click
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60e6368c6ccb70d0bc87c9fc2d1d99770b4fa36dfe957365d48a2e26c00a163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995930"
---
# <a name="playerclick-event"></a>Player.Click-Ereignis

Das **Click-Ereignis** tritt auf, wenn der Benutzer auf eine Maustaste klickt.

## <a name="syntax"></a>Syntax


```JScript
Player.Click(
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

**Number** (**int**) gibt ein Bitfeld mit Bits an, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entspricht. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Es wird nur eines der Bits festgelegt, was die Schaltfläche angibt, die das Ereignis verursacht hat.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**) gibt ein Bitfeld mit den am wenigsten signifikanten Bits an, die der UMSCHALTTASTE (Bit 0), der STRG-Taste (Bit 1) und der ALT-Taste (Bit 2) entspricht. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden, was darauf hinweist, dass einige, alle oder keine der Tasten gedrückt werden.

</dd> <dt>

*Fx* 
</dt> <dd>

**Number** **(long)** gibt die x-Koordinate des Mauszeigers relativ zur oberen linken Ecke des Steuerelements an.

</dd> <dt>

*Fy* 
</dt> <dd>

**Number** (**long)** gibt die y-Koordinate des Mauszeigers relativ zur oberen linken Ecke des Steuerelements an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens auf eine Methode in einer importierten JScript-Datei zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt typisieren, einschließlich Groß- und Groß-/Schreibanforderungen.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 






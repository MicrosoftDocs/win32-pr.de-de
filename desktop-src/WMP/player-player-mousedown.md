---
title: Player.MouseDown-Ereignis
description: Das MouseDown-Ereignis tritt auf, wenn der Benutzer eine Maustaste drückt. | Player.MouseDown-Ereignis
ms.assetid: cc2fd2ca-c974-4683-98ca-2202c4d5b240
keywords:
- MouseDown-Ereignis Windows Media Player
- MouseDown-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , MouseDown-Ereignis
topic_type:
- apiref
api_name:
- Player.MouseDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d267516e02d2e2866df7dbf213228dc3b8854ab3a9488e57e70d743c9b224638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835487"
---
# <a name="playermousedown-event"></a>Player.MouseDown-Ereignis

Das **MouseDown-Ereignis** tritt auf, wenn der Benutzer eine Maustaste drückt.

## <a name="syntax"></a>Syntax


```JScript
Player.MouseDown(
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

 

 






---
description: Legt einen Ereignisschlüssel fest, der die Wiedergaberate einer Animationsspur ändert.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: ID3DXAnimationController::KeyTrackSpeed-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 21ad7b0b1423a25ede319a623cad0a8b453af481d4aac5fae4e5bcce252dd31e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791190"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a>ID3DXAnimationController::KeyTrackSpeed-Methode

Legt einen Ereignisschlüssel fest, der die Wiedergaberate einer Animationsspur ändert.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nachverfolgen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Bezeichner der zu ändernden Spur.

</dd> <dt>

*NewSpeed* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Neue Geschwindigkeit der Animationsspur.

</dd> <dt>

*StartTime* \[ In\]
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Globaler Zeitschlüssel. Gibt die globale Zeit an, zu der die Änderung stattfindet.

</dd> <dt>

*Dauer* \[ In\]
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Übergangszeit, die angibt, wie lange der reibungslose Übergang dauern wird.

</dd> <dt>

*Übergang* \[ In\]
</dt> <dd>

Typ: **[ **D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md)**

Gibt den Übergangstyp an, der für den Übergang zwischen Geschwindigkeiten verwendet wird. Siehe [**D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignishand handle für das Prioritätsmischungsereignis. **NULL** wird zurückgegeben, wenn mindestens einer der Eingabeparameter ungültig ist oder kein kostenloses Ereignis verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 

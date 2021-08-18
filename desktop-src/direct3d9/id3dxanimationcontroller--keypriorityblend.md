---
description: Legt Blendingereignisschlüssel für die angegebene Animationsspur fest.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: ID3DXAnimationController::KeyPriorityBlend-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33d2b4e18fc93dff3054a98442c86a4c05467898afe09fc3bc82ccbd2f0ba456
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279040"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a>ID3DXAnimationController::KeyPriorityBlend-Methode

Legt Blendingereignisschlüssel für die angegebene Animationsspur fest.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewBlendWeight* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die Zahl zwischen 0 und 1, die zum Mischen von Spuren verwendet wird.

</dd> <dt>

*StartTime* \[ In\]
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Globale Zeit zum Starten der Mischung.

</dd> <dt>

*Dauer* \[ In\]
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Globale Zeitdauer der Mischung.

</dd> <dt>

*Übergang* \[ In\]
</dt> <dd>

Typ: **[ **D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md)**

Gibt den Übergangstyp an, der für die Dauer der Mischung verwendet wird. Siehe [**D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignishandle für das Prioritätsmischungsereignis. **NULL** wird zurückgegeben, wenn mindestens einer der Eingabeparameter ungültig ist oder kein kostenloses Ereignis verfügbar ist.

## <a name="remarks"></a>Hinweise

Der Animationscontroller kombiniert sich in drei Phasen: Spuren mit niedriger Priorität werden zuerst kombiniert, Spuren mit hoher Priorität werden in zweiter Linie kombiniert, und dann werden die Ergebnisse beider kombiniert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 

---
description: Legt einen Ereignisschlüssel fest, der die Gewichtung einer Animationsspur ändert. Die Gewichtung wird als Multiplikator verwendet, wenn mehrere Spuren kombiniert werden.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: ID3DXAnimationController::KeyTrackWeight-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16bd95c675486b17f3071a279a01916e3db557c598830282f4d5b288dbc1f0fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026630"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a>ID3DXAnimationController::KeyTrackWeight-Methode

Legt einen Ereignisschlüssel fest, der die Gewichtung einer Animationsspur ändert. Die Gewichtung wird als Multiplikator verwendet, wenn mehrere Spuren kombiniert werden.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
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

*NewWeight* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Neue Gewichtung der Spur.

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

Gibt den Übergangstyp an, der für den Übergang zwischen Gewichtungen verwendet wird. Siehe [**D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignishand handle für das Prioritätsmischungsereignis. **NULL** wird zurückgegeben, wenn mindestens einer der Eingabeparameter ungültig ist oder kein kostenloses Ereignis verfügbar ist.

## <a name="remarks"></a>Hinweise

Die Gewichtung wird wie ein Multiplikator verwendet, um zu bestimmen, wie viel dieser Spur mit anderen Spuren kombiniert werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 

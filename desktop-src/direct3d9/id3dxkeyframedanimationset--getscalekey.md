---
description: Abrufen von Skalierungsinformationen für einen bestimmten Keyframe in der Animationsmenge.
ms.assetid: 7f4a0bf3-2922-4fd7-bb85-b387d3e983a7
title: ID3DXKeyframedAnimationSet::GetScaleKey-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 199b5596e05bd013f3384c2a182bbe8e905cb609ae869c194d811fb97d3d254b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121157"
---
# <a name="id3dxkeyframedanimationsetgetscalekey-method"></a>ID3DXKeyframedAnimationSet::GetScaleKey-Methode

Abrufen von Skalierungsinformationen für einen bestimmten Keyframe in der Animationsmenge.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Animation* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Animationsindex.

</dd> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Keyframe.

</dd> <dt>

*pScaleKeys* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Zeiger auf die Skalierungsdaten. Siehe [**D3DXKEY \_ VECTOR3.**](d3dxkey-vector3.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 

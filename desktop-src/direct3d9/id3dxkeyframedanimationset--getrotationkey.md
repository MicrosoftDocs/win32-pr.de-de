---
description: Abrufen von Drehungsinformationen für einen bestimmten Keyframe im Animationssatz.
ms.assetid: d62b8d5e-328e-4227-b2e8-cb6e5ccc4b3f
title: ID3DXKeyframedAnimationSet::GetRotationKey-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5abb39061b1782b7794ec475a6217677c8723625e2752237c122a694435f2862
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951470"
---
# <a name="id3dxkeyframedanimationsetgetrotationkey-method"></a>ID3DXKeyframedAnimationSet::GetRotationKey-Methode

Abrufen von Drehungsinformationen für einen bestimmten Keyframe im Animationssatz.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
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

*pRotationKeys* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md)**

Zeiger auf die Drehungsdaten. Siehe [**D3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 

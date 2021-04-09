---
description: Legen Sie die Rotations Informationen für einen bestimmten Keyframe im Animations Satz fest.
ms.assetid: b31edc88-0d77-49f3-b4c4-39cd866e1379
title: 'ID3DXKeyframedAnimationSet:: abskey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b03a6818a6a59904c3db5b4819775d9e58d4f8ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050924"
---
# <a name="id3dxkeyframedanimationsetsetrotationkey-method"></a>ID3DXKeyframedAnimationSet:: abskey-Methode

Legen Sie die Rotations Informationen für einen bestimmten Keyframe im Animations Satz fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Animation* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Animations Index.

</dd> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Keyframe.

</dd> <dt>

" *protationkeys* \[ " in\]
</dt> <dd>

Typ: **[ **LPD3DXKEY \_ Quaternion**](d3dxkey-quaternion.md)**

Zeiger auf die Rotationsdaten. Siehe [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 

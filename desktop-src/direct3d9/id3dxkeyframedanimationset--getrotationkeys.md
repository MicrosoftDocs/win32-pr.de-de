---
description: Füllt ein Array mit rotierenden Schlüsseldaten, die für die Keyframe-Animation verwendet werden.
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'ID3DXKeyframedAnimationSet:: getrotationkeys-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af9242ccf75bc1e5443f040399ffbd8a939ed92e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762309"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a>ID3DXKeyframedAnimationSet:: getrotationkeys-Methode

Füllt ein Array mit rotierenden Schlüsseldaten, die für die Keyframe-Animation verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
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

" *protationkeys* \[ " in\]
</dt> <dd>

Typ: **[ **LPD3DXKEY \_ Quaternion**](d3dxkey-quaternion.md)**

Zeiger auf ein vom Benutzer zugewiesenes Array von [**D3DXKEY \_ Quaternion**](d3dxkey-quaternion.md) Quaternionen, das die Methode mit Animations Rotationsdaten ausfüllen soll.

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet:: getnumrotationkeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 

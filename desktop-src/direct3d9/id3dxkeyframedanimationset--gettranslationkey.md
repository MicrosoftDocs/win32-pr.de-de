---
description: Sie erhalten Übersetzungs Informationen für einen bestimmten Keyframe im Animations Satz.
ms.assetid: 757af408-8a9c-4294-9343-91f52d4cc1ab
title: 'ID3DXKeyframedAnimationSet:: gettranslationkey-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f61d1caecb46477d16be4367588ab5609bfd6224
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367486"
---
# <a name="id3dxkeyframedanimationsetgettranslationkey-method"></a>ID3DXKeyframedAnimationSet:: gettranslationkey-Methode

Sie erhalten Übersetzungs Informationen für einen bestimmten Keyframe im Animations Satz.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTranslationKey(
  [in]  UINT              Animation,
  [in]  UINT              Key,
  [out] LPD3DXKEY_VECTOR3 pTranslationKey
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

*ptranslationkey* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Zeiger auf die Rotations Informationen. Siehe [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).

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

 

 

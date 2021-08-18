---
description: Legen Sie Übersetzungsinformationen für einen bestimmten Keyframe im Animationssatz fest.
ms.assetid: 4a926c0f-6d57-48d4-bb3b-60766fc78e40
title: ID3DXKeyframedAnimationSet::SetTranslationKey-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f699a1988c53fc52b4ce413e4c0a655b7d943ddabc0c8e5fcb25ad627e32667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987340"
---
# <a name="id3dxkeyframedanimationsetsettranslationkey-method"></a>ID3DXKeyframedAnimationSet::SetTranslationKey-Methode

Legen Sie Übersetzungsinformationen für einen bestimmten Keyframe im Animationssatz fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTranslationKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pTranslationKey
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

KeyFrame.

</dd> <dt>

*pTranslationKey* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Zeiger auf die Übersetzungsdaten. Siehe [**D3DXKEY \_ VECTOR3.**](d3dxkey-vector3.md)

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

 

 

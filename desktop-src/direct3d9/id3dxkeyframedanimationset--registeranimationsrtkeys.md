---
description: Registrieren sie die SRT-Keyframedaten (Scale, Rotate, Translate) für eine Animation.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 07ec4db0bb02eb0a177375fc37af67264f1368b2ab952c0b170580112e4dbf40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987370"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a>ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys-Methode

Registrieren sie die SRT-Keyframedaten (Scale, Rotate, Translate) für eine Animation.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf den Animationsnamen.

</dd> <dt>

*NumScaleKeys* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Skalierungsschlüssel.

</dd> <dt>

*NumRotationKeys* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Rotationsschlüssel.

</dd> <dt>

*NumTranslationKeys* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Übersetzungsschlüssel.

</dd> <dt>

*pScaleKeys* \[ In\]
</dt> <dd>

Typ: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Adresse eines Zeigers auf ein vom Benutzer zugeordnetes Array von [**D3DXKEY \_ VECTOR3-Vektoren,**](d3dxkey-vector3.md) die die Methode mit Skalierungsdaten auffüllt.

</dd> <dt>

*pRotationKeys* \[ In\]
</dt> <dd>

Typ: **const [**LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md) \***

Adresse eines Zeigers auf ein vom Benutzer zugeordnetes Array von [**D3DXKEY \_ QUATERNION-Quaternionen,**](d3dxkey-quaternion.md) die die Methode mit Drehungsdaten auffüllt.

</dd> <dt>

*pTranslationKeys* \[ In\]
</dt> <dd>

Typ: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Adresse eines Zeigers auf ein vom Benutzer zugeordnetes Array von [**D3DXKEY \_ VECTOR3-Vektoren,**](d3dxkey-vector3.md) die die Methode mit Übersetzungsdaten auffüllt.

</dd> <dt>

*pAnimationIndex* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Gibt den Animationsindex zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 

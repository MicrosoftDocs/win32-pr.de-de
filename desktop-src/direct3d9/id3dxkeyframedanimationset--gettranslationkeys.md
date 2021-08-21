---
description: Füllt ein Array mit Übersetzungsschlüsseldaten aus, die für die Keyframe-Animation verwendet werden.
ms.assetid: ecb791ad-e586-4057-9239-facd37a47637
title: ID3DXKeyframedAnimationSet::GetTranslationKeys-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39b2c086442b6a235730f9ec228b377f0a8b8f39a83d7c5043cfbca56dae2345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987360"
---
# <a name="id3dxkeyframedanimationsetgettranslationkeys-method"></a>ID3DXKeyframedAnimationSet::GetTranslationKeys-Methode

Füllt ein Array mit Übersetzungsschlüsseldaten aus, die für die Keyframe-Animation verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTranslationKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pTranslationKeys
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Animation* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Animationsindex.

</dd> <dt>

*pTranslationKeys* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Zeiger auf ein vom Benutzer zugeordnetes Array von [**D3DXKEY \_ VECTOR3-Vektoren,**](d3dxkey-vector3.md) das von der -Methode mit Animationsübersetzungsdaten gefüllt werden soll.

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 

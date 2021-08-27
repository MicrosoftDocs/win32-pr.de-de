---
description: Abrufen des Einflusses, den ein bestimmter Wermut auf einen bestimmten Scheitelpunkt hat.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: ID3DX10SkinInfo::GetBoneInfluence-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9b53f642b6e62bb37c6979602b1ae66e09ffc2eb42a6d47c70c6b895a01ba273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096550"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a>ID3DX10SkinInfo::GetBoneInfluence-Methode

Abrufen des Einflusses, den ein bestimmter Wermut auf einen bestimmten Scheitelpunkt hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Unterindex* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein Index, der einen vorhandenen Auswerter angibt. Muss zwischen 0 und dem von [**ID3DX10SkinInfo::GetNumBones zurückgegebenen**](id3dx10skininfo-getnumbones.md)Wert sein.

</dd> <dt>

*InfluenceIndex* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein Index in der Liste der Scheitelpunkte, die es beeinflusst.

</dd> <dt>

*pWeight* \[ In\]
</dt> <dd>

Typ: **\* float**

Die Menge der Einflussmöglichkeiten zwischen 0 und 1, die der Würfe über den Scheitelpunkt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert E \_ INVALIDARG sein.

## <a name="remarks"></a>Hinweise

Verwenden Sie ID3DX10SkinInfo::GetBoneInfluenceCount, um herauszufinden, wie viele Scheitelpunkte die Folie beeinflusst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

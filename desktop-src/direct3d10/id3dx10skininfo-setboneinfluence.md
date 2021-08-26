---
description: Legen Sie den Einfluss eines bestimmten 1000-000-00-00-Scheitelpunkts auf einen bestimmten Scheitelpunkt fest.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: ID3DX10SkinInfo::SetBoneInfluence-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1bf2f2a6ec92a1e4551bdc22d43bd143c9da5c8114c44619c073a838de52c606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069960"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a>ID3DX10SkinInfo::SetBoneInfluence-Methode

Legen Sie den Einfluss eines bestimmten 1000-000-00-00-Scheitelpunkts auf einen bestimmten Scheitelpunkt fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein Index, der einen vorhandenen Zeichner angibt. Muss zwischen 0 und dem von [**ID3DX10SkinInfo::GetNumBones zurückgegebenen Wert liegen.**](id3dx10skininfo-getnumbones.md)

</dd> <dt>

*InfluenceIndex* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein Index in der Liste der Scheitelpunkt, die er beeinflusst.

</dd> <dt>

*Gewichtung* \[ In\]
</dt> <dd>

Typ: **float**

Die Menge des Einflusses zwischen 0 und 1, die der Schwenk über den Scheitelpunkt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert E \_ INVALIDARG sein.

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

 

 

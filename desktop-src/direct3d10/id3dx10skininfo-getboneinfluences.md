---
description: Abrufen einer Liste von Scheitelpunkten, die von einem bestimmten Fluss beeinflusst werden, sowie eine Liste der Einflussfaktoren, die Dies auf jeden Scheitelpunkt hat.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: ID3DX10SkinInfo::GetBoneInfluences-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 38d6901abd871a2b65f4d6816ad4d4b7a0d2effb5ccbd3f4ccee20bc0b8d5ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752910"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a>ID3DX10SkinInfo::GetBoneInfluences-Methode

Abrufen einer Liste von Scheitelpunkten, die von einem bestimmten Fluss beeinflusst werden, sowie eine Liste der Einflussfaktoren, die Dies auf jeden Scheitelpunkt hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Unterindex* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein Index, der einen vorhandenen Auswerter angibt. Muss zwischen 0 und dem von [**ID3DX10SkinInfo::GetNumBones zurückgegebenen**](id3dx10skininfo-getnumbones.md)Wert sein.

</dd> <dt>

*Offset* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein Offset vom Anfang der Liste der beeinflussten Scheitelpunkte des Gerüsts. Dies muss zwischen 0 und dem wert sein, der von [**ID3DX10SkinInfo::GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md)zurückgegeben wird.

</dd> <dt>

*Anzahl* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der abzurufenden Indizes und Gewichtungen. Muss zwischen 0 und dem wert sein, der von ID3DX10SkinInfo::GetBoneInfluenceCount zurückgegeben wird.

</dd> <dt>

*pDestIndices* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Eine Liste der Indizes im Scheitelpunktpuffer, die jeweils einen von der Ziege beeinflussten Scheitelpunkt darstellen. Diese Werte entsprechen den Werten in pDestWeights, sodass pDestIndices \[ i \] pDestWeights \[ i entspricht. \]

</dd> <dt>

*pDestWeights* \[ in, out\]
</dt> <dd>

Typ: **\* float**

Eine Liste der Einflussmöglichkeiten, die die Zählung auf die einzelnen Scheitelpunkte hat. Diese Werte entsprechen den Werten in pDestIndices, sodass pDestWeights \[ i \] pDestIndices \[ i \] entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert E \_ INVALIDARG oder E \_ OUTOFMEMORY sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

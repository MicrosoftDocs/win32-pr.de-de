---
description: Suchen Sie den Index, der angibt, wo sich ein angegebener Scheitelpunkt in der Liste der beeinflussten Scheitelpunkte eines bestimmten Gitters befindet.
ms.assetid: vs|directx_sdk|~\id3dx10skininfo_findboneinfluenceindex.htm
title: ID3DX10SkinInfo::FindBoneInfluenceIndex-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.FindBoneInfluenceIndex
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 85b68240a52ddf442d834a9acec919ea9c607f2dcbc43d2046a3d070aa9ddf84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634500"
---
# <a name="id3dx10skininfofindboneinfluenceindex-method"></a>ID3DX10SkinInfo::FindBoneInfluenceIndex-Methode

Suchen Sie den Index, der angibt, wo sich ein angegebener Scheitelpunkt in der Liste der beeinflussten Scheitelpunkte eines bestimmten Gitters befindet.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindBoneInfluenceIndex(
  [in] UINT BoneIndex,
  [in] UINT VertexIndex,
  [in] UINT *pInfluenceIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein Index, der einen vorhandenen Zeichner angibt. Muss zwischen 0 und dem von [**ID3DX10SkinInfo::GetNumBones zurückgegebenen Wert liegen.**](id3dx10skininfo-getnumbones.md)

</dd> <dt>

*VertexIndex* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Der Index des Scheitelpunkts im Scheitelpunktpuffer.

</dd> <dt>

*pInfluenceIndex* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Der Index des Scheitelpunkts in der Liste der beeinflussten Scheitelpunkte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert sein: E \_ INVALIDARG.

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

 

 

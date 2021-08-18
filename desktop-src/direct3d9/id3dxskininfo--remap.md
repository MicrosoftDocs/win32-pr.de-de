---
description: Updates beeinflussen Informationen, um Scheitelpunkte abzugleichen, nachdem sie neu angeordnet wurden. Diese Methode sollte aufgerufen werden, wenn der Zielvertexpuffer extern neu angeordnet wurde.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: ID3DXSkinInfo::Remap-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941a71539184b7d49e35627c932da77b4494486c35506b1b4e5f69ad52c40829
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727780"
---
# <a name="id3dxskininforemap-method"></a>ID3DXSkinInfo::Remap-Methode

Updates beeinflussen Informationen, um Scheitelpunkte abzugleichen, nachdem sie neu angeordnet wurden. Diese Methode sollte aufgerufen werden, wenn der Zielvertexpuffer extern neu angeordnet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NumVertices* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der zuzuordnenden Scheitelpunkte.

</dd> <dt>

*pVertexRemap* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Array von DWORDS, dessen Länge von NumVertices angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Jedes Element in pVertexRemap gibt den vorherigen Scheitelpunktindex für diese Position an. Wenn sich beispielsweise ein Scheitelpunkt an Position 3 befand, aber an Position 5 neu zugeordnet wurde, sollte das fünfte Element von pVertexRemap 3 enthalten. Das von [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) zurückgegebene Vertex-Neuzuordnungsarray kann verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 

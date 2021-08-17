---
description: Führt ein einheitliches Mosaik basierend auf der Mosaikebene aus.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: ID3DXPatchMesh::Tessellate-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1bd1bb3f242078603f84a0ff12c05c0e824a55e759f147c8aa230490ab36af39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802010"
---
# <a name="id3dxpatchmeshtessellate-method"></a>ID3DXPatchMesh::Tessellate-Methode

Führt ein einheitliches Mosaik basierend auf der Mosaikebene aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fTessLevel* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Mosaikebene. Dies ist die Anzahl von Scheitelpunkten, die zwischen vorhandenen Scheitelpunkten eingeführt werden. Der Bereich dieses float-Parameters ist 0 < fTessLevel <= 32.

</dd> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Resultierendes Mosaikgitternetz. Siehe [**ID3DXMesh.**](id3dxmesh.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion wird effizienter ausgeführt, wenn das Patchmesh mit [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md)optimiert wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 

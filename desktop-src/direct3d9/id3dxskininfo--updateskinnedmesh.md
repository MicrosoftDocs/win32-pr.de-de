---
description: Wendet software skinning auf die Zielvertices basierend auf den aktuellen Matrizen an.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: ID3DXSkinInfo::UpdateSkinnedMesh-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22b36e1836570a10647f5b737a68afa1e65a4dce80fe9d49061a3eee8a799651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729452"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a>ID3DXSkinInfo::UpdateSkinnedMesh-Methode

Wendet software skinning auf die Zielvertices basierend auf den aktuellen Matrizen an.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBoneTransforms* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matrix für die Transformation von Kasten.

</dd> <dt>

*pBoneInvTransposeTransforms* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Umgekehrtes Transponieren der Transformationsmatrix der Transformation.

</dd> <dt>

*pVerticesSrc* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf den Puffer, der die Quellvertices enthält.

</dd> <dt>

*pVerticesDst* \[ In\]
</dt> <dd>

Typ: **[ **PVOID**](../winprog/windows-data-types.md)**

Zeiger auf den Puffer, der die Zielvertices enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Wenn diese Methode verwendet wird, um Scheitelpunkte mit zwei Positionselementen zu skinnen, wird das zweite Positionselement mit der Umkehrung des Kastens anstelle des Kastens selbst skint.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 

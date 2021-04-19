---
description: Wendet das softwareskinning auf die Ziel Vertices basierend auf den aktuellen Matrizen an.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'ID3DXSkinInfo:: updateskinnedmesh-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 645e6ae1e1cb84991b352c250b137cd3ae2491f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367340"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a>ID3DXSkinInfo:: updateskinnedmesh-Methode

Wendet das softwareskinning auf die Ziel Vertices basierend auf den aktuellen Matrizen an.

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

*pbonetransformationen* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Matrix Transformationsmatrix.

</dd> <dt>

*pboneinvtranspo/Transformationen* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Umgekehrte Umwandlung der "Bone Transform"-Matrix.

</dd> <dt>

*pverticessrc* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Zeiger auf den Puffer, der die Quell Vertices enthält.

</dd> <dt>

*pverticesdst* \[ in\]
</dt> <dd>

Typ: **[ **pVoid**](../winprog/windows-data-types.md)**

Zeiger auf den Puffer, der die Ziel Vertices enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode verwendet wird, um Vertices mit zwei Positions Elementen zu verwenden, wird das zweite Positions Element mit der Umkehrung des knotes und nicht mit dem Knochen selbst gespaut.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 

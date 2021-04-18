---
description: Erstellt ein Skin-Mesh aus einem anderen Mesh.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: D3DXCreateSkinInfoFromBlendedMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530926"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a>D3DXCreateSkinInfoFromBlendedMesh-Funktion

Erstellt ein Skin-Mesh aus einem anderen Mesh.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Zeiger auf ein [**ID3DXBaseMesh**](id3dxbasemesh.md) -Objekt, das Mesh, aus dem das Skin Mesh erstellt werden soll.

</dd> <dt>

*Numbones* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die Länge des Arrays, das an die boneid angehängt ist. Siehe [**D3DXBONECOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*pbonecombinationtable* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***

Zeiger auf ein Array von Bone-Kombinationen. Siehe [**D3DXBONECOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*ppskininfo* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Adresse eines Zeigers auf eine [**ID3DXSkinInfo**](id3dxskininfo.md) -Schnittstelle, die das erstellte Skin-Mesh-Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: E \_ outo-Memory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

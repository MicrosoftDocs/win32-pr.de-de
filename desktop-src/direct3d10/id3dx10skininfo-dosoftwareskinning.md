---
description: Führt die Software in einem Array von Vertices aus.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: ID3DX10SkinInfo::D osoftwareskinning-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54dfe909e36be0273e0679a824ff0674b0e3b38c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363142"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a>ID3DX10SkinInfo::D osoftwareskinning-Methode

Führt die Software in einem Array von Vertices aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartVertex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein 0-basierter Index in psrcvertices.

</dd> <dt>

*VertexCount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der zu transformierenden Scheitel Punkte.

</dd> <dt>

*psrcvertices* \[ in\]
</dt> <dd>

Typ: **void \***

Zeiger auf ein Array von Vertices, die transformiert werden sollen.

</dd> <dt>

*Srcstride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Größe eines Scheitel Punkts in psrcvertices (in Byte).

</dd> <dt>

*pdestvertices* \[ in, out\]
</dt> <dd>

Typ: **void \***

Zeiger auf ein Array von Vertices, das mit den transformierten Scheitel Punkten gefüllt wird.

</dd> <dt>

*Deststride* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Größe eines Scheitel Punkts in pdestvertices (in Byte).

</dd> <dt>

*pbonematrices* \[ in\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ein Array von Matrizen, das verwendet wird, um die jedem Knochen zugeordneten Punkte zu transformieren, sodass die dem "Bone i" zugeordneten Scheitel Punkte \[ \] von pbonematrices i transformiert werden \[ \] . Dieses Array wird nur verwendet, um die Matrizen zu transformieren, wenn der isnormal-Wert in pchanneldescs auf **false** festgelegt ist, andernfalls wird pinversetransposebonematrices verwendet.

</dd> <dt>

*pinverabversieinbonematrices* \[ in\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Wenn dieser Wert **null** ist, wird er auf pbonematrices festgelegt. Dieses Array von Matrizen wird nur verwendet, um die Scheitel Punkte zu transformieren, wenn der isnormal-Wert in pchanneldescs auf **true** festgelegt ist, andernfalls wird pbonematrices verwendet.

</dd> <dt>

*pchanneldescs* \[ in\]
</dt> <dd>

Type: **[ **d3dx10 \_ Skinning \_ Channel**](d3dx10-skinning-channel.md)\***

Zeiger auf eine d3dx10 \_ SKINNING \_ Channel-Struktur, die den Member der Vertex-decl bestimmt, auf der das softwareskinning ausgeführt wird.

</dd> <dt>

*Numchannels* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der d3dx10 \_ Skinning \_ Channel-Strukturen in pchanneldescs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg.

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie ein Beispiel für die Verwendung der softwareskinning:


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

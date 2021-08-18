---
description: Führen Sie software skinning auf einem Array von Scheitelungen aus.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: ID3DX10SkinInfo::D oSoftwareSkinning-Methode (D3DX10.h)
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
ms.openlocfilehash: 20f68f51d6886d53d74cd31691e52c362c60d2bf9be2beb0656564cb20fcb80a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729810"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a>ID3DX10SkinInfo::D oSoftwareSkinning-Methode

Führen Sie software skinning auf einem Array von Scheitelungen aus.

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

*StartVertex* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein 0-basierter Index in pSrcVertices.

</dd> <dt>

*VertexCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der zu transformierenden Scheitelzeichen.

</dd> <dt>

*pSrcVertices* \[ In\]
</dt> <dd>

Typ: **\* void**

Zeiger auf ein Array von scheitelpunkts, die transformiert werden soll.

</dd> <dt>

*SrcStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Größe eines Scheitelpunkts in pSrcVertices in Bytes.

</dd> <dt>

*pDestVertices* \[ in, out\]
</dt> <dd>

Typ: **\* void**

Zeiger auf ein Array von Scheitelpunkt, das mit den transformierten Scheitelpunkt gefüllt wird.

</dd> <dt>

*DestStride* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Größe eines Scheitelpunkts in pDestVertices in Bytes.

</dd> <dt>

*pBoneMatrices* \[ In\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ein Array von Matrizen, die verwendet werden, um die punkte zu transformieren, die den einzelnen Gittern zugeordnet sind, damit die Scheitelpunkte, die dem I-Scheitelpunkt zugeordnet sind, von \[ \] pBoneMatrices \[ i transformiert \] werden. Dieses Array wird nur verwendet, um die Matrizen zu transformieren, wenn der IsNormal-Wert in pChannelDescs auf **FALSE** festgelegt ist. Andernfalls wird pInverseTransposeBoneMatrices verwendet.

</dd> <dt>

*pInverseTransposeBoneMatrices* \[ In\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Wenn dieser Wert **NULL ist,** wird er auf pBoneMatrices festgelegt. Dieses Array von Matrizen wird nur verwendet, um die Scheitelungen zu transformieren, wenn der IsNormal-Wert in pChannelDescs auf **TRUE** festgelegt ist. Andernfalls wird pBoneMatrices verwendet.

</dd> <dt>

*pChannelDescs* \[ In\]
</dt> <dd>

Typ: **[ **D3DX10 \_ SKINNING \_ CHANNEL**](d3dx10-skinning-channel.md)\***

Zeiger auf eine D3DX10 SKINNING CHANNEL-Struktur, die den Member der Scheitelpunkt-Decl bestimmt, auf der die Softwares \_ \_ skinning erfolgt.

</dd> <dt>

*NumChannels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der D3DX10 \_ SKINNING \_ CHANNEL-Strukturen in pChannelDescs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert sein: E \_ INVALIDARG.

## <a name="remarks"></a>Hinweise

Hier ist ein Beispiel für die Verwendung von Software-Skinning:


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
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

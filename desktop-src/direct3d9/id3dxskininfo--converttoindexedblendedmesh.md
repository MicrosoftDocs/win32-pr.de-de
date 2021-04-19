---
description: Nimmt ein Mesh an und gibt ein neues Mesh mit pro-Vertex-Blend-Gewichtungen,-Indizes und einer Bone-Kombinations Tabelle zurück. In der Tabelle wird beschrieben, welche Knochen Paletten welche Teilmengen des Netzes beeinflussen.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'ID3DXSkinInfo:: convertdeindexedblendedmesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373541"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a>ID3DXSkinInfo:: convertdeindexedblendedmesh-Methode

Nimmt ein Mesh an und gibt ein neues Mesh mit pro-Vertex-Blend-Gewichtungen,-Indizes und einer Bone-Kombinations Tabelle zurück. In der Tabelle wird beschrieben, welche Knochen Paletten welche Teilmengen des Netzes beeinflussen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Das eingabemesh. Siehe [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*Optionen* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Derzeit nicht verwendet.

</dd> <dt>

*palettesize* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der für die Matrix Palette verfügbaren Knochen Matrizen.

</dd> <dt>

*padjackocyin* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Informationen zur Eingabe Gitter Informationen.

</dd> <dt>

*padjacumcyout* \[ in\]
</dt> <dd>

Typ: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Informationen zur Ausgabe Gitter Informationen.

</dd> <dt>

*pfakeremap* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Array von DWords, eines pro Gesicht, das die ursprüngliche Gitterfläche angibt, die den einzelnen Flächen im gemischten Mesh entspricht. Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Gesichts Umwandlungs Daten zurückgegeben.

</dd> <dt>

*ppvertexremap* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitel Punkten den alten Scheitel Punkten zugeordnet werden. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunkt Zuordnung ändern müssen. Dieser Parameter ist optional. **Null** kann verwendet werden.

</dd> <dt>

*pmaxvertexinfl* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein DWORD-Wert, der die maximale Anzahl der für den Scheitelpunkt für diese Skinning-Methode erforderlichen Knochen Einflüsse enthält.

</dd> <dt>

*pnumbonekombinationen* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Anzahl der Knochen in der Tabelle mit der Knochen Kombination.

</dd> <dt>

*ppbonecombinationtable* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Zeiger auf die Tabelle mit der Knochen Kombination. Die Daten werden in einer [**D3DXBONECOMBINATION**](d3dxbonecombination.md) -Struktur organisiert.

</dd> <dt>

*ppmesh* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Zeiger auf das neue Mesh.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Jedes Element in den Umwandlungs-Arrays gibt den vorherigen Index für diese Position an. Wenn sich z. b. ein Scheitelpunkt an Position 3, aber an Position 5 neu zugeordnet wurde, enthält das fünfte Element von pvertexremap 3.

Diese Methode kann nicht auf Hardware ausgeführt werden, die eine Scheitelpunkt Mischung mit fester Funktion nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 

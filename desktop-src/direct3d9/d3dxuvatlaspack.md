---
description: Packen Sie Gitternetzpartitionierungsdaten in einen Atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: D3DXUVAtlasPack-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6990d6fbc114c874b31d0035a2415d48161d3065718efce3783a041a2097e96f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749660"
---
# <a name="d3dxuvatlaspack-function"></a>D3DXUVAtlasPack-Funktion

Packen Sie Gitternetzpartitionierungsdaten in einen Atlas.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein Eingabegittermodell (siehe [**ID3DXMesh),**](id3dxmesh.md)das die Objektgeometrie zum Berechnen des Atlas enthält. Das Gitternetz muss mindestens Positionsdaten und 2D-Texturkoordinaten enthalten.

</dd> <dt>

*dwWidth* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Texturbreite.

</dd> <dt>

*dwHeight* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Texturhöhe.

</dd> <dt>

*fGutter* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der minimale Abstand zwischen zwei Diagrammen im Atlas in Texeln. Der Bundt wird immer um die Breite skaliert. Wenn also ein Bundel von 2,5 für eine Textur mit einer Länge von 512 x 512 verwendet wird, beträgt der Mindestabstand zwischen zwei Diagrammen 2,5/512,0 Texel.

</dd> <dt>

*dwTextureIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nullbasierter Texturkoordinatenindex, der an identifiziert, welche Texturkoordinaten verwendet werden.

</dd> <dt>

*pdwPartitionResultAdjacency* 
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Gitternetz angeben. Sie sollte von der ppPartitionResultAdjacency abgeleitet werden, die von [**D3DXUVAtlasPartition zurückgegeben wird.**](d3dxuvatlaspartition.md) Dieser Wert darf nicht **NULL sein,** da Pack wissen muss, wo Diagramme im Partitionsschritt abgeschnitten wurden, um die Kanten der einzelnen Diagramme zu finden.

</dd> <dt>

*pCallback* \[ In\]
</dt> <dd>

Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Ein Zeiger auf eine Rückruffunktion (siehe [LPD3DXUVATLASCB),](lpd3dxuvatlascb.md)die für die Überwachung des Fortschritts nützlich ist.

</dd> <dt>

*fCallbackFrequency* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Geben Sie an, wie oft D3DX den Rückruf aufruft. Ein angemessener Standardwert ist 0,0001f.

</dd> <dt>

*pUserContent* \[ In\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ein void-Zeiger, der an die Rückruffunktion zurück übergeben werden soll.

</dd> <dt>

*dwOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Dieser Optionsparameter ist derzeit reserviert.

</dd> <dt>

*pFacePartitioning* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Ein Zeiger auf einen [**ID3DXBuffer,**](id3dxbuffer.md) der das Array der endgültigen Gesichtspartitionierung enthält. Jedes Element enthält ein DWORD pro Gesicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D OK, andernfalls ist der Wert \_ D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[UVAtlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 

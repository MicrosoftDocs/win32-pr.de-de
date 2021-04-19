---
description: Packen Sie Mesh-Partitionierungs Daten in einen Atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: D3DXUVAtlasPack-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 31de326160120fe14a71841cb5f2d18e1c8d4e57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357234"
---
# <a name="d3dxuvatlaspack-function"></a>D3DXUVAtlasPack-Funktion

Packen Sie Mesh-Partitionierungs Daten in einen Atlas.

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

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein Eingabe Mesh (siehe [**ID3DXMesh**](id3dxmesh.md)), das die Objekt Geometrie zum Berechnen des Atlas enthält. Das Mesh muss mindestens Positionsdaten und 2D-Texturkoordinaten enthalten.

</dd> <dt>

*dwwidth* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Textur Breite.

</dd> <dt>

*dwheight* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Textur Höhe.

</dd> <dt>

nicht mehr  \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Mindestabstand in texeln zwischen zwei Diagrammen im Atlas. Der bundbundwert wird immer durch die Breite skaliert. Wenn also ein bundbundwert von 2,5 für eine 512 x 512-Textur verwendet wird, ist der minimale Abstand zwischen zwei Diagrammen 2,5/512,0 Texels.

</dd> <dt>

*dwtextureindex* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

NULL basierter Texturkoordinaten Index, der angibt, welcher Satz von Texturkoordinaten verwendet werden soll.

</dd> <dt>

*pdwpartitionresultadjacency* 
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt. Sie sollte von der pppartitionresultadjacency abgeleitet werden, die von [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md)zurückgegeben wird. Dieser Wert darf nicht **null** sein, da Pack wissen muss, wo Diagramme im Partitions Schritt abgeschnitten wurden, um die Kanten der einzelnen Diagramme zu ermitteln.

</dd> <dt>

*pCallback* \[ in\]
</dt> <dd>

Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Ein Zeiger auf eine Rückruffunktion (siehe [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)), die zum Überwachen des Fortschritts nützlich ist.

</dd> <dt>

" *schcallbackfrequency* \[ " in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Geben Sie an, wie oft D3DX den Rückruf aufruft. ein angemessener Standardwert ist 0,0001 f.

</dd> <dt>

*pusercontent* \[ in\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ein void-Zeiger, der an die Rückruffunktion zurückgegeben werden soll.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Dieser Optionsparameter ist derzeit reserviert.

</dd> <dt>

*pfacepartitionierung* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Ein Zeiger auf ein [**ID3DXBuffer**](id3dxbuffer.md) -Wert, der das Array der abschließenden Gesichts Partitionierung enthält. Jedes Element enthält ein DWORD pro Gesicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK; andernfalls ist der Wert D3DERR \_ invalidcall.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uvatlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 

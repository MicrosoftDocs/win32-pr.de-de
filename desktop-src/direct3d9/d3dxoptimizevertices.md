---
description: Generiert eine optimierte Vertex-Neuzuordnung für eine Dreiecksliste. Diese Funktion wird häufig verwendet, nachdem die von D3DXOptimizeFaces generierte Neuzuordnung des Gesichts angewendet wurde.
ms.assetid: a3b9cb68-204e-4e8f-a985-738d1cea1e29
title: D3DXOptimizeVertices-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a60d7d47e78cd197a7bfcf6285509c9187e32e074347f63f8e76ef9ef866adfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044798"
---
# <a name="d3dxoptimizevertices-function"></a>D3DXOptimizeVertices-Funktion

Generiert eine optimierte Vertex-Neuzuordnung für eine Dreiecksliste. Diese Funktion wird häufig verwendet, nachdem die von [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)generierte Neuzuordnung des Gesichts angewendet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXOptimizeVertices(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pVertexRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pIndices* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf Indizes der Dreiecksliste, die zum Sortieren von Scheitelpunkten verwendet werden sollen.

</dd> <dt>

*NumFaces* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Gesichter in der Dreiecksliste.

</dd> <dt>

*NumVertices* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Scheitelpunkte, auf die von der Dreiecksliste verwiesen wird.

</dd> <dt>

*Indizes32Bit* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Flag, das den Indextyp angibt: **TRUE,** wenn Indizes 32 Bit sind (mehr als 65535 Scheitelpunkte), **FALSE,** wenn Indizes 16 Bit (65535 oder weniger Scheitelpunkte) sind.

</dd> <dt>

*pVertexRemap* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf einen Zielpuffer, der den neuen Index für jeden Scheitelpunkt enthält. Der in *pVertexRemap* gespeicherte Wert für ein bestimmtes Element ist die Quellvertexposition in der neuen Scheitelpunktreihenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Standardmäßig verwendet ein Gitternetz 16-Bit-Indizes, wenn es erstellt wird, sofern die Anwendung nichts anderes angibt. Um zu überprüfen, ob ein vorhandenes Gitternetz 16-Bit- oder 32-Bit-Indizes verwendet, rufen Sie [**ID3DXBaseMesh::GetOptions**](id3dxbasemesh--getoptions.md) auf, und suchen Sie nach dem \_ 32-BIT-Flag D3DXMESH.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

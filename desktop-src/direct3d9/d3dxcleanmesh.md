---
description: Bereinigt ein Mesh und bereitet es auf Vereinfachung vor.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: D3DXCleanMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5565978dc1ad0e80c33718275ea65080930ce7cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365109"
---
# <a name="d3dxcleanmesh-function"></a>D3DXCleanMesh-Funktion

Bereinigt ein Mesh und bereitet es auf Vereinfachung vor.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cleantype* \[ in\]
</dt> <dd>

Typ: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**

Vertex-Vorgänge, die zur Vorbereitung der Bereinigung durchgeführt werden sollen. Siehe [**D3DXCLEANTYPE**](./d3dxcleantype.md).

</dd> <dt>

*pmeshat* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das zu bereinigende Mesh darstellt.

</dd> <dt>

*padjackocyin* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt, die bereinigt werden sollen.

</dd> <dt>

*ppmeshout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das zurückgegebene bereinigte Mesh darstellt. Das gleiche Mesh wird zurückgegeben, das übergangen wurde, wenn keine Bereinigung notwendig war.

</dd> <dt>

*padjacumcyout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Ausgabe Mesh angibt.

</dd> <dt>

*pperrorsandwarning* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der eine Zeichenfolge mit Fehlern und Warnungen enthält, die die im Mesh gefundenen Probleme erläutern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Diese Funktion bereinigt ein Mesh mithilfe der Reinigungsmethode und der Optionen, die im cleantype-Parameter angegeben sind. Eine Beschreibung der verfügbaren Optionen finden Sie in der [**D3DXCLEANTYPE**](./d3dxcleantype.md) -Enumeration.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

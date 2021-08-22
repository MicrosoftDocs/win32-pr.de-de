---
description: Bereinigt ein Gitternetz und bereitet es auf eine Vereinfachung vor.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: D3DXCleanMesh-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: adc5d60b66dc9eaa06314e18ead26412b8572e9dbc649070c37891a62fb9ecbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495910"
---
# <a name="d3dxcleanmesh-function"></a>D3DXCleanMesh-Funktion

Bereinigt ein Gitternetz und bereitet es auf eine Vereinfachung vor.

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

*CleanType* \[ In\]
</dt> <dd>

Typ: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**

Vertexvorgänge, die als Vorbereitung für die Gitternetzbereinigung ausgeführt werden sollen. Siehe [**D3DXCLEANTYPE.**](./d3dxcleantype.md)

</dd> <dt>

*pMeshIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das zu bereinigende Gitternetz darstellt.

</dd> <dt>

*pAdencyencyIn* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes zu bereinigende Gesicht im Gitternetz angibt.

</dd> <dt>

*ppMeshOut* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das zurückgegebene bereinigte Gitternetz darstellt. Dasselbe Gitternetz wird zurückgegeben, das übergeben wurde, wenn keine Bereinigung erforderlich war.

</dd> <dt>

*pAdjaencyOut* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Ausgabegitternetz angibt.

</dd> <dt>

*ppErrorsAndWarnings* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Puffer zurück, der eine Zeichenfolge mit Fehlern und Warnungen enthält, die die im Netz gefundenen Probleme erklären.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion bereinigt ein Gitternetz mithilfe der Bereinigungsmethode und der optionen, die im CleanType-Parameter angegeben sind. Eine Beschreibung der verfügbaren Optionen finden Sie in der [**D3DXCLEANTYPE-Enumeration.**](./d3dxcleantype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

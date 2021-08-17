---
description: Mosaik des angegebenen Gittermodells mithilfe des N-Patch-Mosaikschemas.
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: D3DXTessellateNPatches-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1df63068f3eef608f797f8048231e744412c32f9e01a31a089c50f8a46465a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122722"
---
# <a name="d3dxtessellatenpatches-function"></a>D3DXTessellateNPatches-Funktion

Mosaik des angegebenen Gittermodells mithilfe des N-Patch-Mosaikschemas.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMeshIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das Gitternetz zum Mosaik darstellt.

</dd> <dt>

*pAdencyencyIn* \[ In\]
</dt> <dd>

Typ: **const CONST \* DWORD**

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Quellgitternetz angibt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*NumSegs* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Anzahl der Segmente pro Edge, für die ein Mosaik zu erstellen ist.

</dd> <dt>

*QuadraticInterpNormals* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Legen Sie diese Einstellung auf **TRUE** fest, um die quadratische Interpolation für Normalitäten zu verwenden. für lineare Interpolation auf **FALSE** festgelegt.

</dd> <dt>

*ppMeshOut* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das zurückgegebene Mosaikgitter darstellt.

</dd> <dt>

*ppAdencyencyOut* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle.**](id3dxbuffer.md) Wenn der Wert dieses Parameters nicht auf **NULL** festgelegt ist, enthält dieser Puffer ein Array von drei DWORDs pro Gesicht, die die drei Nachbarn für jedes Gesicht im Ausgabegitternetz angeben. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion setzt den N-Patch-Algorithmus ins Mosaik.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

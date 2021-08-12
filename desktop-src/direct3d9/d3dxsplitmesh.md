---
description: Teilt ein Gitternetz in Gitternetze auf, die kleiner als die angegebene Größe sind.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: D3DXSplitMesh-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aee07e79286867ce11ce394e852fdfc01c6a1e41dc75b8c979838844b4f09d2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298252"
---
# <a name="d3dxsplitmesh-function"></a>D3DXSplitMesh-Funktion

Teilt ein Gitternetz in Gitternetze auf, die kleiner als die angegebene Größe sind.

## <a name="syntax"></a>Syntax


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMeshIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das Quellgitternetz darstellt.

</dd> <dt>

*pAdencyencyIn* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes zu vereinfachende Gesicht im Gitternetz angibt.

</dd> <dt>

*MaxSize* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md)**

Maximale Anzahl von Scheitelpunkten im resultierenden Gitternetz.

</dd> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md)**

Optionsflags für die neuen Gitternetze.

</dd> <dt>

*pMeshesOut* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Anzahl der zurückgegebenen Gitternetze.

</dd> <dt>

*ppMeshArrayOut* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puffer mit einem Array von [**ID3DXMesh-Schnittstellen**](id3dxmesh.md) für die neuen Gitternetze. Für ein Quellgitternetz, das in n Gitternetze aufgeteilt ist, ist *ppMeshArrayOut* ein Array von n **ID3DXMesh-Zeigern.**

</dd> <dt>

*ppAdencyencyArrayOut* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puffer, der ein Array von Adjazenzarrays (DWORDs) für die neuen Gitternetze enthält. Siehe [**ID3DXBuffer**](id3dxbuffer.md). Dieser Parameter ist optional.

</dd> <dt>

*ppFaceRemapArrayOut* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puffer, der ein Array von Gesichtsneuzuordnungsarrays (DWORDs) für die neuen Gitternetze enthält. Siehe [**ID3DXBuffer**](id3dxbuffer.md). Dieser Parameter ist optional.

</dd> <dt>

*ppVertRemapArrayOut* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puffer, der ein Array von Vertexarrays für die neuen Gitternetze enthält. Siehe [**ID3DXBuffer**](id3dxbuffer.md). Dieser Parameter ist optional.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion wird häufig verwendet, um ein Gitternetz mit 32-Bit-Indizes (mehr als 65535 Scheitelpunkte) in mehrere Gitternetze aufzuteilen, von denen jedes über 16-Bit-Indizes verfügt.

Die Arrays adency, vertex remap und face remap sind Arrays, bei denen jedes Array n DWORD-Zeiger enthält, gefolgt von den DWORD-Daten, auf die die Zeiger verweisen. Um beispielsweise die Gesichtszuordnungsinformationen für Gesicht 3 in Gitternetz 2 abzurufen, könnte der folgende Code verwendet werden, vorausgesetzt, die Gesichtszuordnungsdaten wurden in einer Variablen namens *ppFaceRemapArrayOut* zurückgegeben.


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

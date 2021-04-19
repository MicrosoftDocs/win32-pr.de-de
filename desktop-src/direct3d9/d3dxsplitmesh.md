---
description: Teilt ein Mesh in die Netze, die kleiner als die angegebene Größe sind.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: D3DXSplitMesh-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364362"
---
# <a name="d3dxsplitmesh-function"></a>D3DXSplitMesh-Funktion

Teilt ein Mesh in die Netze, die kleiner als die angegebene Größe sind.

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

*pmeshat* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das quellmesh darstellt.

</dd> <dt>

*padjackocyin* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Mesh angibt, das vereinfacht werden soll.

</dd> <dt>

*MaxSize* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md)**

Maximale Anzahl der Scheitel Punkte im resultierenden Mesh.

</dd> <dt>

*Optionen* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md)**

Optionsflags für die neuen Netze.

</dd> <dt>

*pmeshesout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Anzahl der zurückgegebenen Netzen.

</dd> <dt>

*ppmesharrayout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puffer, der ein Array von [**ID3DXMesh**](id3dxmesh.md) -Schnittstellen für die neuen Meshes enthält. Bei einem quellmesh, das in n Meshes aufgeteilt ist, ist *ppmesharrayout* ein Array von n **ID3DXMesh** -Zeigern.

</dd> <dt>

*ppyouts-cyarrayout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Puffer, der ein Array von annähernden Arrays (DWords) für die neuen Meshes enthält. Siehe [**ID3DXBuffer**](id3dxbuffer.md). Dieser Parameter ist optional.

</dd> <dt>

*ppfakeremaparamerayout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puffer, der ein Array von Flächen Umwandlungs Arrays (DWords) für die neuen Meshes enthält. Siehe [**ID3DXBuffer**](id3dxbuffer.md). Dieser Parameter ist optional.

</dd> <dt>

*ppvertremaparamerayout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Puffer, der ein Array von Vertex-neuumwandlungs Arrays für die neuen Meshes enthält. Siehe [**ID3DXBuffer**](id3dxbuffer.md). Dieser Parameter ist optional.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird häufig verwendet, um ein Mesh mit 32-Bit-Indizes (mehr als 65535 Scheitel Punkten) in mehr als ein Mesh aufzuteilen, die jeweils über 16-Bit-Indizes verfügen.

Die Arrays "ency", "Vertex Umwandlungs" und "Face Umwandlungs" sind Arrays sind "DWords", wobei jedes Array n DWORD-Zeiger enthält, gefolgt von den DWORD-Daten, auf die die Zeiger verweisen. Um z. b. die Gesichts Umwandlungs Informationen für Gesicht 3 in Mesh 2 abzurufen, könnte der folgende Code verwendet werden, vorausgesetzt, die Daten zur gleich Umgestaltung wurden in einer Variablen mit dem Namen *ppfakeremaparamerayout* zurückgegeben.


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

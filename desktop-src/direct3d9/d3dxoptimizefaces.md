---
description: Generiert eine optimierte Gesichtsumwandung für eine Dreiecksliste.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: D3DXOptimizeFaces-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 165f81d9b829ce7a7b22ced6fb37851f926ed861f11b79feca3a63c763dabbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525229"
---
# <a name="d3dxoptimizefaces-function"></a>D3DXOptimizeFaces-Funktion

Generiert eine optimierte Gesichtsumwandung für eine Dreiecksliste.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pIndices* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf Dreieckslistenindizes, die zum Ordnen von Scheitelpunkten verwendet werden.

</dd> <dt>

*NumFaces* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Gesichter in der Dreiecksliste. Bei 16-Bit-Gittern ist dies auf 2^16 bis 1 (65535) oder weniger Gesichter beschränkt.

</dd> <dt>

*NumVertices* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Scheitelzeichen, auf die von der Dreiecksliste verwiesen wird.

</dd> <dt>

*Indices32Bit* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Flag, das den Indextyp angibt: **TRUE,** wenn Indizes 32-Bit sind (mehr als 65535 Indizes), **FALSE,** wenn Indizes 16-Bit sind (65535 oder weniger Indizes).

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf das ursprüngliche Gitternetz, das geteilt wurde, um das aktuelle Gesicht zu generieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Optimierungsprozedur dieser Funktion entspricht funktional dem Aufruf von [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) mit dem D3DXMESHOPT DEVICEINDEPENDENT-Flag, aber diese Funktion nutzt \_ Vertexcaches effizienter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

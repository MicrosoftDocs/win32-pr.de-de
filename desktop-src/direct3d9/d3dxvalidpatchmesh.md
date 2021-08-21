---
description: Überprüft ein Patchnetz und gibt die Anzahl degenerierter Scheitelpunkte und Patches zurück.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: D3DXValidPatchMesh-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c3b7b28c763691af83dbb1ed0fe406fa6d370c82f9d8ffa702afa69566f2597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523811"
---
# <a name="d3dxvalidpatchmesh-function"></a>D3DXValidPatchMesh-Funktion

Überprüft ein Patchnetz und gibt die Anzahl degenerierter Scheitelpunkte und Patches zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMeshIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**

Zeiger auf eine [**ID3DXPatchMesh-Schnittstelle,**](id3dxpatchmesh.md) die das zu testende Patchmesh darstellt.

</dd> <dt>

*pNumDegenerateVertices* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Gibt die Anzahl degenerierter Scheitelpunkte im Patchgitternetz zurück.

</dd> <dt>

*pNumDegeneratePatches* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Gibt die Anzahl degenerierter Patches im Patchnetz zurück.

</dd> <dt>

*ppErrorsAndWarnings* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Zeiger auf einen Puffer zurück, der eine Zeichenfolge mit Fehlern und Warnungen enthält, die die im Patchnetz gefundenen Probleme erklären.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Methode überprüft das Gitternetz, indem auf ungültige Indizes überprüft wird. Fehlerinformationen sind in der Debuggerausgabe verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

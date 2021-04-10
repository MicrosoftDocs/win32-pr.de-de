---
description: Überprüft ein patchmesh und gibt die Anzahl der degenerierten Vertices und Patches zurück.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: D3DXValidPatchMesh-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961583"
---
# <a name="d3dxvalidpatchmesh-function"></a>D3DXValidPatchMesh-Funktion

Überprüft ein patchmesh und gibt die Anzahl der degenerierten Vertices und Patches zurück.

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

*pmeshat* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**

Zeiger auf eine [**ID3DXPatchMesh**](id3dxpatchmesh.md) -Schnittstelle, die das zu testende patchmesh darstellt.

</dd> <dt>

*pnumdägeneratevertices* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Gibt die Anzahl der degenerierten Scheitel Punkte im patchmesh zurück.

</dd> <dt>

*pnumdägeneratepatches* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Gibt die Anzahl der degenerierten Patches im patchmesh zurück.

</dd> <dt>

*pperrorsandwarning* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Gibt einen Zeiger auf einen Puffer zurück, der eine Zeichenfolge mit Fehlern und Warnungen enthält, in denen die im patchmesh gefundenen Probleme erläutert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Diese Methode überprüft das Mesh, indem auf ungültige Indizes überprüft wird. Fehlerinformationen sind in der Debugger-Ausgabe verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

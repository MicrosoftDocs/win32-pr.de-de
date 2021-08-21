---
description: Erstellt ein Gittermodellobjekt mithilfe eines FVF-Codes (Flexible Vertex Format).
ms.assetid: 4681f181-8a16-42d4-bbfa-bdee5ed69fd3
title: D3DXCreateMeshFVF-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMeshFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db168b710d0454c30ccd3dc19252b455ae22178cb70bba84972b8f904a411109
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857110"
---
# <a name="d3dxcreatemeshfvf-function"></a>D3DXCreateMeshFVF-Funktion

Erstellt ein Gittermodellobjekt mithilfe eines FVF-Codes (Flexible Vertex Format).

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateMeshFVF(
  _In_  DWORD             NumFaces,
  _In_  DWORD             NumVertices,
  _In_  DWORD             Options,
  _In_  DWORD             FVF,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NumFaces* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Gesichter für das Gitternetz. Der gültige Bereich für diese Zahl ist größer als 0 und ein Wert kleiner als der maximale DWORD-Wert(in der Regel 2werte – 1), da der letzte Index reserviert ist.

</dd> <dt>

*NumVertices* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Scheitelpunkte für das Gitternetz. Dieser Parameter muss größer als 0 sein.

</dd> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren Flags aus der [**D3DXMESH-Enumeration,**](./d3dxmesh.md) die Erstellungsoptionen für das Gitternetz angeben.

</dd> <dt>

*FVF* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus [D3DFVF,](d3dfvf.md) die das Scheitelpunktformat für das zurückgegebene Gitternetz beschreibt. Diese Funktion unterstützt D3DFVF \_ XYZRHW nicht.

</dd> <dt>

*pD3DDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das Geräteobjekt, das dem Gittermodell zugeordnet werden soll.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das erstellte Gittermodellobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 

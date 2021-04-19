---
description: Erstellt ein Mesh-Objekt mit einem Deklarator.
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: D3DXCreateMesh-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cfb56fe5c52d2726dff0877522b6f72f70437552
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355824"
---
# <a name="d3dxcreatemesh-function"></a>D3DXCreateMesh-Funktion

Erstellt ein Mesh-Objekt mit einem Deklarator.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateMesh(
  _In_        DWORD               NumFaces,
  _In_        DWORD               NumVertices,
  _In_        DWORD               Options,
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _In_        LPDIRECT3DDEVICE9   pD3DDevice,
  _Out_       LPD3DXMESH          *ppMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Numerische Werte* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Flächen für das Mesh. Der gültige Bereich für diese Zahl ist größer als 0 und ein kleiner als der maximale DWORD-Wert (in der Regel 65534), da der letzte Index reserviert ist.

</dd> <dt>

*Numvertices* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Scheitel Punkte für das Mesh. Dieser Parameter muss größer als 0 (null) sein.

</dd> <dt>

*Optionen* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Optionen für das Mesh angibt.

</dd> <dt>

*pdeclaration* \[ in\]
</dt> <dd>

Typ: **Konstanten [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, das das Scheitelpunkt Format für das zurückgegebene Mesh beschreibt. Dieser Parameter muss einem flexiblen Scheitelpunkt Format (FVF) direkt zugeordnet werden.

</dd> <dt>

*pD3DDevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das Geräte Objekt, das dem Mesh zugeordnet werden soll.

</dd> <dt>

*ppmesh* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das erstellte Mesh-Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 

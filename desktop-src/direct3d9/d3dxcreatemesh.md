---
description: 'D3DXCreateMesh-Funktion: Erstellt ein Gittermodellobjekt mithilfe eines Deklarators.'
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: D3DXCreateMesh-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: 8a1e9ed35325390f3315cd269d89284fd3426a9f1cbad4c1c025be06dd33204f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676260"
---
# <a name="d3dxcreatemesh-function"></a>D3DXCreateMesh-Funktion

Erstellt ein Gittermodellobjekt mithilfe eines Deklarators.

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

*NumFaces* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Gesichter für das Gitter. Der gültige Bereich für diese Zahl ist größer als 0 und eins kleiner als das maximale DWORD (in der Regel 65534), da der letzte Index reserviert ist.

</dd> <dt>

*NumVertices* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Scheitelzeichen für das Gitternetz. Dieser Parameter muss größer als 0 sein.

</dd> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination eines oder mehrerer Flags aus der [**D3DXMESH-Enumeration,**](./d3dxmesh.md) die Optionen für das Gitternetz angeben.

</dd> <dt>

*pDeclaration* \[ In\]
</dt> <dd>

Typ: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) das das Scheitelpunktformat für das zurückgegebene Netz beschreibt. Dieser Parameter muss direkt einem flexiblen Scheitelpunktformat (FVF) zuordnen.

</dd> <dt>

*pD3DDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das Geräteobjekt, das dem Netz zugeordnet werden soll.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das erstellte Gittermodellobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 

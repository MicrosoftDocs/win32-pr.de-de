---
description: Klont ein Gitternetz mithilfe eines FVF-Codes (Flexible Vertex Format).
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: ID3DXBaseMesh::CloneMeshFVF-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc0e389678240396d22e616a39ed0050b1f73b0b974dbe2800fcda2c6d4076a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121812"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a>ID3DXBaseMesh::CloneMeshFVF-Methode

Klont ein Gitternetz mithilfe eines FVF-Codes (Flexible Vertex Format).

## <a name="syntax"></a>Syntax


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren [**D3DXMESH-Flags,**](./d3dxmesh.md) die Erstellungsoptionen für das Gitternetz angeben.

</dd> <dt>

*FVF* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination von FVF-Codes, die das Scheitelpunktformat für die Scheitelpunkte im Ausgabegitternetz angibt. Die Werte der Codes finden Sie unter [D3DFVF](d3dfvf.md).

</dd> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das dem Gittermodell zugeordnete Geräteobjekt darstellt.

</dd> <dt>

*ppCloneMesh* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das geklonte Gitternetz darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

**ID3DXBaseMesh::CloneMeshFVF** wird verwendet, um das Vertexdatenlayout neu zu formatiert und zu ändern. Dies erfolgt durch Erstellen eines neuen Gittermodellobjekts. Verwenden Sie es beispielsweise, um Platz für Normalitäten, Texturkoordinaten, Farben, Gewichtungen usw. hinzuzufügen, die zuvor nicht vorhanden waren.

[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) aktualisiert die Scheitelpunktdeklaration mit unterschiedlichen semantischen Informationen, ohne das Layout des Scheitelpunktpuffers zu ändern. Diese Methode ändert den Inhalt des Scheitelpunktpuffers nicht. Verwenden Sie sie beispielsweise, um eine 3D-Texturkoordinate als binormal oder Tangens neu zu bezeichnen oder umgekehrt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 

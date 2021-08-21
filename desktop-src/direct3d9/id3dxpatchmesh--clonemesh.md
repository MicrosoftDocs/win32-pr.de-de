---
description: Erstellt ein neues Patchgitter mit der angegebenen Scheitelpunktdeklaration.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: ID3DXPatchMesh::CloneMesh-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1418bf890ae0ba10adec9e0c7de74eb5f118f91566554eb325cc2badaedfc613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294381"
---
# <a name="id3dxpatchmeshclonemesh-method"></a>ID3DXPatchMesh::CloneMesh-Methode

Erstellt ein neues Patchgitter mit der angegebenen Scheitelpunktdeklaration.

## <a name="syntax"></a>Syntax


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination eines oder mehrerer [**D3DXMESH-Flags,**](./d3dxmesh.md) die Erstellungsoptionen für das Gitternetz angeben.

</dd> <dt>

*pDecl* \[ In\]
</dt> <dd>

Typ: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) die das Scheitelpunktformat für die Scheitelpunkte im Ausgabegitternetz angeben.

</dd> <dt>

*pMesh* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXPatchMesh-Schnittstelle,**](id3dxpatchmesh.md) die das geklonte Netz darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

**CloneMesh konvertiert** den Scheitelpunktpuffer in die neue Scheitelpunktdeklaration. Einträge in der Scheitelpunktdeklaration, die für das ursprüngliche Gitternetz neu sind, werden auf 0 festgelegt. Wenn das aktuelle Gitternetz über Adjacency verfügt, verfügt das neue Gitternetz auch über Adjacency.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 

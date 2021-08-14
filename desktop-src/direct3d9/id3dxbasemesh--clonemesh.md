---
description: Klont ein Gitternetz mithilfe eines Deklarators.
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: ID3DXBaseMesh::CloneMesh-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97fec8b0881cdef43051afcb06d63ec20284cb116299912ce0acf7ac4c54a0f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521863"
---
# <a name="id3dxbasemeshclonemesh-method"></a>ID3DXBaseMesh::CloneMesh-Methode

Klont ein Gitternetz mithilfe eines Deklarators.

## <a name="syntax"></a>Syntax


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Optionen* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehr [**D3DXMESH-Flags,**](./d3dxmesh.md) die Erstellungsoptionen für das Gitternetz angeben.

</dd> <dt>

*pDeclaration* \[ In\]
</dt> <dd>

Typ: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Ein Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) die das Scheitelpunktformat für die Scheitelpunkte im Ausgabegitternetz angeben.

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

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

**ID3DXBaseMesh::CloneMesh** wird verwendet, um das Vertexdatenlayout neu zu erstellen und zu ändern. Dies erfolgt durch Erstellen eines neuen Gittermodellobjekts. Verwenden Sie es beispielsweise, um Platz für Normal- und Texturkoordinaten, Farben, Gewichtungen usw. hinzuzufügen, die zuvor nicht vorhanden waren.

[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) aktualisiert die Scheitelpunktdeklaration mit anderen semantischen Informationen, ohne das Layout des Scheitelpunktpuffers zu ändern. Diese Methode ändert nicht den Inhalt des Scheitelpunktpuffers. Verwenden Sie ihn beispielsweise, um eine 3D-Texturkoordinate als binormaler Oder Tangens oder umgekehrt neu zu beschriften.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh::CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 

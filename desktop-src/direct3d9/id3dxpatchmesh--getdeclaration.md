---
description: 'ID3DXPatchMesh::GetDeclaration-Methode: Ruft die Scheitelpunktdeklaration ab.'
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: ID3DXPatchMesh::GetDeclaration-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0fde070b1b013e651c84ffea7098eb8225aed8f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093298"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a>ID3DXPatchMesh::GetDeclaration-Methode

Ruft die Scheitelpunktdeklaration ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDeclaration* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) die das Scheitelpunktformat der Gitternetzvertices beschreiben. Die Dimension dieses Deklaratorarrays ist [**MAX \_ FVF \_ DECL \_ SIZE.**](./max-fvf-decl-size.md) Das Vertexelementarray endet mit dem [**D3DDECL-END-Makro. \_**](d3ddecl-end.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Bemerkungen

Das Array von Elementen enthält das [**D3DDECL-END-Makro, \_**](d3ddecl-end.md) das die Deklaration beendet.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 

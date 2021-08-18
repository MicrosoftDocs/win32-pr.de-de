---
description: Optimiert das Patchgitter für effizientes Mosaik.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: ID3DXPatchMesh::Optimize-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 245f3ddb2c85f5de6ae2acc040f929387d522c12d65eeb4d4307f162b8532af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120724"
---
# <a name="id3dxpatchmeshoptimize-method"></a>ID3DXPatchMesh::Optimize-Methode

Optimiert das Patchgitter für effizientes Mosaik.

## <a name="syntax"></a>Syntax


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Derzeit nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT.

## <a name="remarks"></a>Hinweise

Nachdem eine Anwendung Adjazienzinformationen für ein Gitternetz generiert hat, können die Gitternetzdaten optimiert (neu angeordnet) werden, um eine bessere Zeichnungsleistung zu erzielen. Diese Methode bestimmt, welche Patches nebeneinander liegen (innerhalb der angegebenen Toleranz).

Außerdem werden Adjazieninformationen verwendet, um das Mosaik zu optimieren. Generieren Sie einmal Adjacency-Informationen, und erstellen Sie wiederholt mosaiken, indem Sie [**ID3DXPatchMesh::Tessellate aufrufen.**](id3dxpatchmesh--tessellate.md) Die durchgeführte Optimierung ist unabhängig von der tatsächlich verwendeten Mosaikebene. Wenn jedoch die Gitternetzvertices geändert werden, müssen Sie die Adjacency-Informationen erneut generieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh::GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 

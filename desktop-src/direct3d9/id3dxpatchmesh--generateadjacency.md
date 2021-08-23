---
description: Generieren Sie eine Liste der Gitternetzränder und der Patches, die sich die einzelnen Ränder teilen.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: ID3DXPatchMesh::GenerateAdjacency-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 41e821d853a8a8f981f1174d654f17475c0363cdcc97bb537e308ccd72e38190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987200"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a>ID3DXPatchMesh::GenerateAdjacency-Methode

Generieren Sie eine Liste der Gitternetzränder und der Patches, die sich die einzelnen Ränder teilen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fTolerance* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gibt an, dass Scheiteltices, die sich an der Position um weniger als die Toleranz unterscheiden, als zufällig behandelt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Nachdem eine Anwendung Adjazienzinformationen für ein Gitternetz generiert hat, können die Gitternetzdaten für eine bessere Zeichnungsleistung optimiert werden. Diese Methode bestimmt, welche Patches nebeneinander liegen (innerhalb der angegebenen Toleranz). Diese Informationen werden intern verwendet, um das Mosaik zu optimieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 

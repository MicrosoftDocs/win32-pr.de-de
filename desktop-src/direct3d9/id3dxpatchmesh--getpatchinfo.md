---
description: Ruft die Attribute des Patches ab.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: ID3DXPatchMesh::GetPatchInfo-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10b6d327b665b30418478d06d21433614587824eeb481202a9bef202b8727001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847440"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a>ID3DXPatchMesh::GetPatchInfo-Methode

Ruft die Attribute des Patches ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PatchInfo* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**

Zeiger auf die Strukturen, die die Patchattribute enthalten. Weitere Informationen zu Patchattributen finden Sie unter [**D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 





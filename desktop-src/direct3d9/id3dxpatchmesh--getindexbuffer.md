---
description: Ruft den Meshindexpuffer ab.
ms.assetid: d9152f3b-c8e6-4def-8cf1-a517ca4d34e7
title: ID3DXPatchMesh::GetIndexBuffer-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c7b32c5414f72b1dd16a6c309294056e81468f8e039e73d1d43c05d5ac3dd0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294353"
---
# <a name="id3dxpatchmeshgetindexbuffer-method"></a>ID3DXPatchMesh::GetIndexBuffer-Methode

Ruft den Meshindexpuffer ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppIB* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Zeiger auf den Indexpuffer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Der Indexpuffer enthält die Scheitelpunktreihenfolge im Scheitelpunktpuffer. Der Indexpuffer wird verwendet, um auf den Scheitelpunktpuffer zuzugreifen, wenn das Gitternetz gerendert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 

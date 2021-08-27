---
description: Ruft den Vertexpuffer des Gitters ab.
ms.assetid: 4ea4e99b-5c2c-467b-8b5d-8174c446680a
title: ID3DXPatchMesh::GetVertexBuffer-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f6b6a630a24ba5d0427862f7b0799d9b4c4b14661d2adf33b0e56ccae78dfa10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802038"
---
# <a name="id3dxpatchmeshgetvertexbuffer-method"></a>ID3DXPatchMesh::GetVertexBuffer-Methode

Ruft den Vertexpuffer des Gitters ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVertexBuffer(
  [out] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppVB* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***

Zeiger auf den Scheitelpunktpuffer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Methode geht von einem einheitlichen Mosaik aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 

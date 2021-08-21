---
description: Entsperren Sie den Scheitelpunktpuffer.
ms.assetid: 98b82fd1-56e8-45f3-bf26-a1e3b54c2979
title: ID3DXPatchMesh::UnlockVertexBuffer-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e9f710455ae08f3548b9a778716b1d8deebad15fcf53e8c9e4ede551b3a821d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294193"
---
# <a name="id3dxpatchmeshunlockvertexbuffer-method"></a>ID3DXPatchMesh::UnlockVertexBuffer-Methode

Entsperren Sie den Scheitelpunktpuffer.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnlockVertexBuffer();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Der Scheitelpunktpuffer wird normalerweise gesperrt, in geschrieben und dann zum Lesen entsperrt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 





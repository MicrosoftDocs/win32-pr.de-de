---
description: 'ID3DXBaseMesh::GetVertexBuffer-Methode: Ruft den Vertexpuffer ab, der dem Gitternetz zugeordnet ist.'
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: ID3DXBaseMesh::GetVertexBuffer-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc0fc1f47ba3ed27af8f06d1a1f5ea83b884cdbe645d8597cd9513e7ad5c0387
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118850"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a>ID3DXBaseMesh::GetVertexBuffer-Methode

Ruft den Vertexpuffer ab, der dem Gitternetz zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppVB* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***

Die Adresse eines Zeigers auf eine [**IDirect3DVertexBuffer9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) die das dem Gittermodell zugeordnete Vertexpufferobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 

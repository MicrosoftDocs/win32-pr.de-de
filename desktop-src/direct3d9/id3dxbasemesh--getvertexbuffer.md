---
description: 'ID3DXBaseMesh::GetVertexBuffer-Methode: Ruft den Scheitelpunktpuffer ab, der dem Gitternetz zugeordnet ist.'
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
ms.openlocfilehash: 9533188e3e2effe1759b58f70c9f033cc491844c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115368"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a>ID3DXBaseMesh::GetVertexBuffer-Methode

Ruft den Scheitelpunktpuffer ab, der dem Gitternetz zugeordnet ist.

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

Adresse eines Zeigers auf eine [**IDirect3DVertexBuffer9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) die das dem Gittermodell zugeordnete Scheitelpunktpufferobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 

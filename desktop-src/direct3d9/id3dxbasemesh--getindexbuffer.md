---
description: 'ID3DXBaseMesh::GetIndexBuffer-Methode: Ruft die Daten in einem Indexpuffer ab.'
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: ID3DXBaseMesh::GetIndexBuffer-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d47f13a60a681df83df788d91a69c9981746e18df4c65062a9191d2e18de2006
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848490"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a>ID3DXBaseMesh::GetIndexBuffer-Methode

Ruft die Daten in einem Indexpuffer ab.

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

Adresse eines Zeigers auf eine [**IDirect3DIndexBuffer9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) die das Indexpufferobjekt darstellt, das dem Gittermodell zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 

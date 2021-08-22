---
description: 'ID3DXMesh::SetAttributeTable-Methode: Legt die Attributtabelle für ein Gitternetz und die Anzahl der in der Tabelle gespeicherten Einträge fest.'
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: ID3DXMesh::SetAttributeTable-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e93bc3f077d239fb93ac23898635dfc2fe5157ed5d78c32719fca6980606658c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606940"
---
# <a name="id3dxmeshsetattributetable-method"></a>ID3DXMesh::SetAttributeTable-Methode

Legt die Attributtabelle für ein Gitternetz und die Anzahl der in der Tabelle gespeicherten Einträge fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAttribTable* \[ In\]
</dt> <dd>

Typ: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***

Zeiger auf ein Array von [**D3DXATTRIBUTERANGE-Strukturen,**](d3dxattributerange.md) das die Einträge in der Meshattributtabelle darstellt.

</dd> <dt>

*cAttribTableSize* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Attribute in der Meshattributtabelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Wenn eine Anwendung die Informationen in einer Attributtabelle nachverfolgt und die Tabelle aufgrund von Änderungen an Attributen oder Gesichtern neu anordnt, ermöglicht diese Methode der Anwendung, die Attributtabellen zu aktualisieren, anstatt [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) erneut aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

**ID3DXMesh::LockAttributeBuffer**
</dt> </dl>

 

 

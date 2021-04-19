---
description: Legt die Attribut Tabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: ID3DXMesh::-Methode (D3DX9Mesh. h)
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
ms.openlocfilehash: 17ae3458bffd05114415a92538a8ce8ef2cc847e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353345"
---
# <a name="id3dxmeshsetattributetable-method"></a>ID3DXMesh::-Methode

Legt die Attribut Tabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pattribtable* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***

Ein Zeiger auf ein Array von [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) -Strukturen, die die Einträge in der Tabelle des Mesh-Attributs darstellen.

</dd> <dt>

"" "" "".  \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl von Attributen in der Tabelle "Mesh-Attribut".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung die Informationen in einer Attribut Tabelle nachverfolgt und die Tabelle als Ergebnis von Änderungen an Attributen oder Gesichtern neu anordnet, ermöglicht diese Methode der Anwendung, die Attribut Tabellen zu aktualisieren, anstatt [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md) erneut aufzurufende.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

**ID3DXMesh:: LockAttributeBuffer**
</dt> </dl>

 

 

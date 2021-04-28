---
description: 'ID3DXBaseMesh::GetAttributeTable-Methode: Ruft entweder eine Attributtabelle für ein Gitternetz oder die Anzahl von Einträgen ab, die in einer Attributtabelle für ein Gitternetz gespeichert sind.'
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: ID3DXBaseMesh::GetAttributeTable-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f5d27de884f72b46db900487e26f1099bf30949
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115448"
---
# <a name="id3dxbasemeshgetattributetable-method"></a>ID3DXBaseMesh::GetAttributeTable-Methode

Ruft entweder eine Attributtabelle für ein Gitternetz oder die Anzahl der Einträge ab, die in einer Attributtabelle für ein Gitternetz gespeichert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAttribTable* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***

Zeiger auf ein Array von [**D3DXATTRIBUTERANGE-Strukturen,**](d3dxattributerange.md) das die Einträge in der Attributtabelle des Gitters darstellt. Geben Sie **NULL** an, um den Wert für pAttribTableSize abzurufen.

</dd> <dt>

*pAttribTableSize* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf die Anzahl der in pAttribTable gespeicherten Einträge oder auf einen Wert, der mit der Anzahl von Einträgen gefüllt werden soll, die in der Attributtabelle für das Gitternetz gespeichert sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Eine Attributtabelle wird von [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) erstellt und D3DXMESHOPT \_ ATTRSORT für den Flags-Parameter übergeben.

Eine Attributtabelle wird verwendet, um Bereiche des Gitternetzes zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien usw. gezeichnet werden müssen. Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitternetzes auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner gezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 

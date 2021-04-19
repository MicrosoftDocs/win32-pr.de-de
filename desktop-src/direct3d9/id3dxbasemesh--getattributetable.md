---
description: Ruft entweder eine Attribut Tabelle für ein Mesh oder die Anzahl der in einer Attribut Tabelle gespeicherten Einträge für ein Mesh ab.
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: 'ID3DXBaseMesh:: GetAttributeTable-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 70c93c8f477655200418793f53706731b42a47ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370442"
---
# <a name="id3dxbasemeshgetattributetable-method"></a>ID3DXBaseMesh:: GetAttributeTable-Methode

Ruft entweder eine Attribut Tabelle für ein Mesh oder die Anzahl der in einer Attribut Tabelle gespeicherten Einträge für ein Mesh ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pattribtable* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***

Zeiger auf ein Array von [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) -Strukturen, das die Einträge in der Attribut Tabelle des Mesh darstellt. Geben Sie **null** an, um den Wert für pattribtablesize abzurufen.

</dd> <dt>

*pattribtablesize* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Anzahl der in pattribtable gespeicherten Einträge oder ein Wert, der mit der Anzahl der in der Attribut Tabelle für das Mesh gespeicherten Einträge aufgefüllt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Eine Attribut Tabelle wird von [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md) erstellt und D3DXMESHOPT \_ attrsort für den flags-Parameter übergeben.

Eine Attribut Tabelle wird verwendet, um Bereiche des Netzes zu identifizieren, die mit unterschiedlichen Texturen, renderzuständen, Materialien usw. gezeichnet werden müssen. Außerdem kann die Anwendung die Attribut Tabelle verwenden, um Teile eines Netzes auszublenden, indem beim Zeichnen des Frames kein angegebener Attribut Bezeichner gezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 

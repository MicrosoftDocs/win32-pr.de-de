---
description: 'ID3DX10Mesh::SetAttributeTable-Methode: Legt die Attributtabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.'
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: ID3DX10Mesh::SetAttributeTable-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6cdaedef52693810519ebb92e6f523afbfe078df68a2a13b7fae7ce0fad98fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634540"
---
# <a name="id3dx10meshsetattributetable-method"></a>ID3DX10Mesh::SetAttributeTable-Methode

Legt die Attributtabelle für ein Gitternetz und die Anzahl der in der Tabelle gespeicherten Einträge fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAttribTable* \[ In\]
</dt> <dd>

Typ: **const [**D3DX10 \_ ATTRIBUTE \_ RANGE**](d3dx10-attribute-range.md) \***

Zeiger auf ein Array von D3DX10 \_ ATTRIBUTE \_ RANGE-Strukturen, die die Einträge in der Gitternetzattributtabelle darstellen.

</dd> <dt>

*cAttribTableSize* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Attribute in der Gitternetzattributtabelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Wenn eine Anwendung die Informationen in einer Attributtabelle nachverfolgt und die Tabelle infolge von Änderungen an Attributen oder Gesichtern neu ansortiert, ermöglicht diese Methode der Anwendung, die Attributtabellen zu aktualisieren, anstatt ID3DX10Mesh::Optimize erneut auf aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

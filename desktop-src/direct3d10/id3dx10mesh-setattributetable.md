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
ms.openlocfilehash: 4e06b181bb512e16e9caaa0d233ebbd3472bfcf8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084008"
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

## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung die Informationen in einer Attributtabelle nachverfolgt und die Tabelle infolge von Änderungen an Attributen oder Gesichtern neu ansortiert, ermöglicht diese Methode der Anwendung, die Attributtabellen zu aktualisieren, anstatt ID3DX10Mesh::Optimize erneut auf aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

---
description: Ruft eine Konstante von einem Array von Konstanten ab. Ein Array besteht aus Elementen.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'ID3DXConstantTable:: getconstantelements-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5396c70c1c4286223d9f45fb8ab9b73a019becb1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363144"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a>ID3DXConstantTable:: getconstantelements-Methode

Ruft eine Konstante von einem Array von Konstanten ab. Ein Array besteht aus Elementen.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hconstant* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für das Array von Konstanten. Dieser Wert darf nicht **null** sein.

</dd> <dt>

*Index* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

NULL basierter Index des Elements im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt einen eindeutigen Bezeichner für die Element Konstante zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**ID3DXConstantTable:: getconstant**](id3dxconstanttable--getconstant.md) oder [**ID3DXConstantTable:: getconstantbyname**](id3dxconstanttable--getconstantbyname.md), um eine Konstante zu erhalten, die nicht Teil eines Arrays ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 

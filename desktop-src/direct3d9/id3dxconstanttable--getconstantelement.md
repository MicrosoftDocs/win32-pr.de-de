---
description: Ruft eine Konstante aus einem Array von Konstanten ab. Ein Array besteht aus Elementen.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: ID3DXConstantTable::GetConstantElement-Methode (D3DX9Shader.h)
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
ms.openlocfilehash: 9cb1adacadb92cf3a2f9a3e041e4a94a840994db3244233509350448008bd675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748780"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a>ID3DXConstantTable::GetConstantElement-Methode

Ruft eine Konstante aus einem Array von Konstanten ab. Ein Array besteht aus Elementen.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hConstant* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für das Array von Konstanten. Dieser Wert darf nicht **NULL** sein.

</dd> <dt>

*Index* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Nullbasierter Index des Elements im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt einen eindeutigen Bezeichner für die Elementkonstante zurück.

## <a name="remarks"></a>Hinweise

Um eine Konstante abzurufen, die nicht Teil eines Arrays ist, verwenden Sie [**ID3DXConstantTable::GetConstant**](id3dxconstanttable--getconstant.md) oder [**ID3DXConstantTable::GetConstantByName**](id3dxconstanttable--getconstantbyname.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 

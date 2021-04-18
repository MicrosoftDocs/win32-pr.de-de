---
description: Ruft eine Konstante ab, indem ihr Index gesucht wird.
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: 'ID3DXConstantTable:: getconstant-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4ab7318dc4a05f586db77817653e7df59ef6083
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361210"
---
# <a name="id3dxconstanttablegetconstant-method"></a>ID3DXConstantTable:: getconstant-Methode

Ruft eine Konstante ab, indem ihr Index gesucht wird.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hconstant* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für die übergeordnete Datenstruktur. Wenn die Konstante ein Parameter der obersten Ebene ist (es gibt keine übergeordnete Datenstruktur), verwenden Sie **null**.

</dd> <dt>

*Index* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

NULL basierter Index der Konstanten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt einen eindeutigen Bezeichner für die Konstante zurück.

## <a name="remarks"></a>Bemerkungen

Um eine Konstante von einem Array von Konstanten zu erhalten, verwenden Sie [**ID3DXConstantTable:: getconstantelements**](id3dxconstanttable--getconstantelement.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 

---
description: Eine Konstante aus der Konstanten Tabelle erhalten.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'ID3DXTextureShader:: getconstantelements-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b5089b6e539a8104586e27b58388a324462b37
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219541"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a>ID3DXTextureShader:: getconstantelements-Methode

Eine Konstante aus der Konstanten Tabelle erhalten.

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

Ein [handle](handles.md) für das Array von Konstanten. Dieser Wert darf nicht **null** sein.

</dd> <dt>

*Index* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

NULL basierter Index des Elements in der Konstanten Tabelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt einen eindeutigen Bezeichner für die Konstante zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**ID3DXTextureShader:: getconstant**](id3dxtextureshader--getconstant.md) oder [**ID3DXTextureShader:: getconstantbyname**](id3dxtextureshader--getconstantbyname.md), um eine Konstante zu erhalten, die nicht Teil eines Arrays ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

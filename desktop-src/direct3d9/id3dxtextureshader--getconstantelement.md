---
description: Sie erhalten eine Konstante aus der Konstantentabelle.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: ID3DXTextureShader::GetConstantElement-Methode (D3DX9Shader.h)
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
ms.openlocfilehash: 02d21efb3ef0ed5d4602833571b2b1a32e73df73b76f82a357cda574e93e84ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747389"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a>ID3DXTextureShader::GetConstantElement-Methode

Sie erhalten eine Konstante aus der Konstantentabelle.

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

Ein [Handle](handles.md) für das Array von Konstanten. Dieser Wert darf nicht **NULL sein.**

</dd> <dt>

*Index* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Nullbasierter Index des Elements in der Konstantentabelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt einen eindeutigen Bezeichner an die Konstante zurück.

## <a name="remarks"></a>Hinweise

Um eine Konstante zu erhalten, die nicht Teil eines Arrays ist, verwenden Sie [**ID3DXTextureShader::GetConstant**](id3dxtextureshader--getconstant.md) oder [**ID3DXTextureShader::GetConstantByName**](id3dxtextureshader--getconstantbyname.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

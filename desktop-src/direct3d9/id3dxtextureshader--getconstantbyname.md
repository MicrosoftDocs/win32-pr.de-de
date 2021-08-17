---
description: 'ID3DXTextureShader::GetConstantByName-Methode: Ruft eine Konstante ab, indem deren Name gesucht wird.'
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: ID3DXTextureShader::GetConstantByName-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55b3de81179c01171d7ee5ff7b845295709dfb8ead1a9bc1a7cdf615bc37c44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729101"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a>ID3DXTextureShader::GetConstantByName-Methode

Ruft eine Konstante ab, indem deren Name nach gesucht wird.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hConstant* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Ein [Handle](handles.md) für die übergeordnete Datenstruktur. Wenn die Konstante ein Parameter der obersten Ebene ist (es gibt keine übergeordnete Datenstruktur), verwenden Sie **NULL**.

</dd> <dt>

*pName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die den Namen der Konstante enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt einen eindeutigen Bezeichner für die Konstante zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

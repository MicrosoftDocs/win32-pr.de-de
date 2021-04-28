---
description: 'ID3DXTextureShader::GetConstantByName-Methode: Ruft eine Konstante ab, indem ihr Name gesucht wird.'
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
ms.openlocfilehash: 825aca3f3227a340952092985f4730018fe316e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117658"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a>ID3DXTextureShader::GetConstantByName-Methode

Ruft eine Konstante ab, indem ihr Name gesucht wird.

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

Ein [Handle](handles.md) für die übergeordnete Datenstruktur. Wenn die Konstante ein Parameter der obersten Ebene ist (es gibt keine übergeordnete Datenstruktur), verwenden Sie **NULL.**

</dd> <dt>

*pName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die den Namen der Konstante enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt einen eindeutigen Bezeichner an die Konstante zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

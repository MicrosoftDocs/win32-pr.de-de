---
description: 'ID3DXTextureShader::SetFloat-Methode: Legt eine Gleitkommazahl fest.'
ms.assetid: 69bb9b15-5d66-4b1a-9559-29bcb38a965f
title: ID3DXTextureShader::SetFloat-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cc6461fa72607579a0dceca324172cefa8174ef3613b31bd2379dbdab9f518f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118093674"
---
# <a name="id3dxtextureshadersetfloat-method"></a>ID3DXTextureShader::SetFloat-Methode

Legt eine Gleitkommazahl fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hConstant,
  [in] FLOAT      f
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hConstant* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für die Konstante. Siehe [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*f* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gleitkommazahl.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

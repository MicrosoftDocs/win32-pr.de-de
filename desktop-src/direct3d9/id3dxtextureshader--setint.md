---
description: 'ID3DXTextureShader::SetInt-Methode: Legt einen ganzzahligen Wert fest.'
ms.assetid: e7dcf3f4-1d0c-432a-85fc-0473c49956ff
title: ID3DXTextureShader::SetInt-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetInt
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 984115e6e28c6d2c9cfe574a6097c94d6eca96e6f649f10bd7411f40abd13667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747340"
---
# <a name="id3dxtextureshadersetint-method"></a>ID3DXTextureShader::SetInt-Methode

Legt einen ganzzahligen Wert fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hConstant,
  [in] INT        n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hConstant* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für die Konstante. Siehe [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **INT**](../winprog/windows-data-types.md)**

Wert für ganze Zahl.

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

 

 

---
description: Legt einen 4D-Vektor fest.
ms.assetid: befed2a8-7695-4f06-a6ee-aff466d1940a
title: 'ID3DXTextureShader:: setvector-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b7bc7e3b7f4920c21c52111410c626090e452fa7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364360"
---
# <a name="id3dxtextureshadersetvector-method"></a>ID3DXTextureShader:: setvector-Methode

Legt einen 4D-Vektor fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hconstant* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für die Vektor Konstante. Siehe [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pvector* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf einen 4D-Vektor. Siehe [**D3DXVECTOR4**](d3dxvector4.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 





---
description: Ruft einen Pixel-Shader ab.
ms.assetid: 173a20a5-dda0-493f-a161-2dc2881e71f2
title: ID3DXBaseEffect::GetPixelShader-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bb948510e2b54582169db5cfdfe4e4f43bf2d931de895cbb06f7f3f3cd1cafce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094114"
---
# <a name="id3dxbaseeffectgetpixelshader-method"></a>ID3DXBaseEffect::GetPixelShader-Methode

Ruft einen Pixel-Shader ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPixelShader(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DPIXELSHADER9 *ppPShader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*ppPShader* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***

Gibt ein Pixel-Shaderobjekt zurück. Siehe [**IDirect3DPixelShader9-Objekt.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 

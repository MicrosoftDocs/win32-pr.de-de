---
description: 'D3DXGetPixelShaderProfile-Funktion: Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.'
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: D3DXGetPixelShaderProfile-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc609e742a4f780f3cb8c34e4dbc4cc40842ee51
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473656"
---
# <a name="d3dxgetpixelshaderprofile-function"></a>D3DXGetPixelShaderProfile-Funktion

Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das Gerät. Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der HLSL-Profilname.

Wenn das Gerät keine Pixelshader unterstützt, gibt die Funktion **NULL** zurück.

## <a name="remarks"></a>Hinweise

Ein Shaderprofil gibt die zu verwendende Assembly-Shaderversion und die Funktionen an, die dem HLSL-Compiler beim Kompilieren eines Shaders zur Verfügung stehen. In der folgenden Tabelle sind die unterstützten Pixel-Shaderprofile aufgeführt.




| Shaderprofil | BESCHREIBUNG | 
|----------------|-------------|
| ps_1_1 | Kompilieren Sie in ps_1_1 Version. | 
| ps_1_2 | Kompilieren Sie in ps_1_2 Version. | 
| ps_1_3 | Kompilieren Sie in ps_1_3 Version. | 
| ps_1_4 | Kompilieren Sie in ps_1_4 Version. | 
| ps_2_0 | Kompilieren Sie in ps_2_0 Version. | 
| ps_2_a | Identisch mit dem ps_2_0-Profil, mit den folgenden zusätzlichen Funktionen, die der Compiler als Ziel hat:<ul><li>Die Anzahl temporärer Register (r#) ist größer oder gleich 22.</li><li>Beliebige Quelle swizzle.</li><li>Farbverlaufsanweisungen: dsx, dsy.</li><li>Prädikation.</li><li>Kein Leselimit für abhängige Textur.</li><li>Keine Beschränkung für die Anzahl der Texturanweisungen.</li></ul> | 
| ps_2_b | Identisch mit dem ps_2_0-Profil, mit den folgenden zusätzlichen Funktionen, die der Compiler als Ziel hat:<ul><li>Die Anzahl temporärer Register (r#) ist größer oder gleich 32.</li><li>Keine Beschränkung für die Anzahl der Texturanweisungen.</li></ul> | 
| ps_3_0 | Kompilieren Sie in ps_3_0 Version. | 




 

Weitere Informationen zu den Unterschieden zwischen Shaderversionen finden Sie unter [Pixelshader-Unterschiede.](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 

---
description: 'D3DXGetVertexShaderProfile-Funktion: Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.'
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: D3DXGetVertexShaderProfile-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5c646fb9779ca923480487cb96f184c76eff9ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473626"
---
# <a name="d3dxgetvertexshaderprofile-function"></a>D3DXGetVertexShaderProfile-Funktion

Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
LPCSTR D3DXGetVertexShaderProfile(
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

Wenn das Gerät keine Vertex-Shader unterstützt, gibt die Funktion **NULL** zurück.

## <a name="remarks"></a>Hinweise

Ein Shaderprofil gibt die zu verwendende Assembly-Shaderversion und die Funktionen an, die dem HLSL-Compiler beim Kompilieren eines Shaders zur Verfügung stehen. In der folgenden Tabelle sind die unterstützten Vertex-Shaderprofile aufgeführt.




| Shaderprofil | BESCHREIBUNG | 
|----------------|-------------|
| vs_1_1 | Kompilieren Sie in vs_1_1 Version. | 
| vs_2_0 | Kompilieren Sie in vs_2_0 Version. | 
| vs_2_a | Identisch mit dem vs_2_0-Profil, mit den folgenden zusätzlichen Funktionen, die der Compiler als Ziel hat:<ul><li>Die Anzahl temporärer Register (r#) ist größer oder gleich 13.</li><li>Dynamische Flusssteuerungsanweisung.</li><li>Prädikation.</li></ul> | 
| vs_3_0 | Kompilieren Sie in vs_3_0 Version. | 




 

Weitere Informationen zu den Unterschieden zwischen Shaderversionen finden Sie unter [Vertex-Shaderunterschiede.](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 

---
description: Diese Funktion, die ein Shader-Reflektionsobjekt zum Abrufen von Informationen über einen kompilierten Shader erstellt, ist nicht mehr vorhanden. Verwenden Sie stattdessen D3DReflect oder D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: D3DX10ReflectShader-Funktion (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 7694aa0dcfcc256358993f29c9ed448c1648b35768e5844a959726a6737c2371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753080"
---
# <a name="d3dx10reflectshader-function"></a>D3DX10ReflectShader-Funktion

Diese Funktion, die ein Shader-Reflektionsobjekt zum Abrufen von Informationen über einen kompilierten Shader erstellt, ist nicht mehr vorhanden. Verwenden Sie stattdessen [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) oder [**D3D11Reflect.**](../direct3dhlsl/d3d11reflect.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pShaderBytecode* \[ In\]
</dt> <dd>

Typ: **const \* void**

Ein Zeiger auf den kompilierten Shader. Informationen zum Abrufen dieses Zeigers finden Sie [unter Abrufen eines Zeigers auf einen kompilierten Shader.](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)

</dd> <dt>

*BytecodeLength* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Länge von pShaderBytecode.

</dd> <dt>

*ppReflector* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***

Adresse einer Shaderreflektionsschnittstelle (siehe [**ID3D10ShaderReflection1-Schnittstelle**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 10-Rückgabecodes zurück.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Hier ist ein Beispiel für die Erstellung eines Shader-Reflektionsobjekts. In diesem Beispiel wird davon ausgegangen, dass Sie mit einem kompilierten Shader beginnen (dargestellt als ).


```
pVSBuf
```



, die Sie im [HLSLWithoutFX10-Beispiel sehen können.](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

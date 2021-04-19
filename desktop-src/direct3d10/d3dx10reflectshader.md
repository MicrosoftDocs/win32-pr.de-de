---
description: Diese Funktion, die ein Shader-Reflektionsobjekt zum Abrufen von Informationen über einen kompilierten Shader erstellt, ist nicht mehr vorhanden. Verwenden Sie stattdessen D3DReflect oder D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: D3DX10ReflectShader-Funktion (D3DX10Core. h)
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
ms.openlocfilehash: 15201bcbde2792bbd31cbf4dad7b87d7ddac5053
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355194"
---
# <a name="d3dx10reflectshader-function"></a>D3DX10ReflectShader-Funktion

Diese Funktion, die ein Shader-Reflektionsobjekt zum Abrufen von Informationen über einen kompilierten Shader erstellt, ist nicht mehr vorhanden. Verwenden Sie stattdessen [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) oder [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).

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

*pshaderbytecode* \[ in\]
</dt> <dd>

Typ: Konstante **void \***

Ein Zeiger auf den kompilierten Shader. Informationen zum Aufrufen dieses Zeigers finden Sie unter [Getting a Pointer to a-kompilierter Shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

</dd> <dt>

*Bytecodelta ength* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**

Länge von pshaderbytecode.

</dd> <dt>

*ppreflector* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***

Adresse einer Shader Reflection-Schnittstelle (siehe [**ID3D10ShaderReflection1 Interface**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie ein Beispiel für das Erstellen eines shaderreflektionsobjekt. Im Beispiel wird davon ausgegangen, dass Sie mit einem kompilierten Shader beginnen (angezeigt als


```
pVSBuf
```



die Sie in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)sehen können).


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
| Header<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

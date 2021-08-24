---
title: Shadertyp
description: Die Syntax zum Deklarieren einer Shadervariablen in einem Effekt wurde von Direct3D 9 in Direct3D 10 geändert.
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- Shadertyp HLSL
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c08c0d68a57180c8d2cf0b566caaaa383f34fc0b9f096e34484811a73a20d0fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854700"
---
# <a name="shader-type"></a>Shadertyp

Die Syntax zum Deklarieren einer Shadervariablen in einem Effekt wurde von Direct3D 9 in Direct3D 10 geändert.

## <a name="shader-type-for-direct3d-10"></a>Shadertyp für Direct3D 10

Deklarieren Sie eine Shadervariable innerhalb eines Effektpasses (in Direct3D 10) mithilfe der Shadertypsyntax:



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SetPixelShader** Compile( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile( **ShaderTarget, ShaderFunction** ); |



 

### <a name="parameters"></a>Parameter



| Element                                                                                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**<br/>         | Der Direct3D-API-Aufruf, der das Shaderobjekt erstellt. Kann entweder **SetPixelShader oder** **SetGeometryShader** oder **SetVertexShader sein.**<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>         | Das Shadermodell, mit dem kompiliert werden soll. Dies gilt für alle Ziele, einschließlich aller Direct3D 9-Ziele sowie der Ziele des [Shadermodells 4:](dx-graphics-hlsl-sm4.md) vs \_ 4 \_ 0, gs \_ 4 \_ 0 und ps \_ 4 \_ 0.<br/>                                                                                                                                                                                                                                          |
| <span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**<br/> | Eine ASCII-Zeichenfolge, die den Namen der Shadereinstiegspunktfunktion enthält. Dies ist die Funktion, die mit der Ausführung beginnt, wenn der Shader aufgerufen wird. (...) stellt die Shaderargumente dar. Dies sind die gleichen Argumente, die an die Shadererstellungs-API übergeben werden: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) oder [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) oder [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).<br/> |



 

### <a name="example"></a>Beispiel

Hier ist ein Beispiel, das einen Vertex-Shader und ein Pixel-Shaderobjekt erstellt, die für ein bestimmtes Shadermodell kompiliert wurden. Im Direct3D 10-Beispiel gibt es keinen Geometrie-Shader, sodass der Zeiger auf **NULL festgelegt ist.**


```
// Direct3D 10
technique10 Render
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, VS() ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PS() ) );
    }
}
```



## <a name="shader-type-for-direct3d-9"></a>Shadertyp für Direct3D 9

Deklarieren Sie eine Shadervariable innerhalb eines Effektpasses (für Direct3D 9) mithilfe der Shadertypsyntax:



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| **PixelShader** = **ShaderTarget ShaderFunction(...); kompilieren VertexShader** = **ShaderTarget ShaderFunction(...); kompilieren** |



 

### <a name="parameters"></a>Parameter



| Element                                                                                                                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**<br/>                                         | Eine Shadervariable, die den kompilierten Shader darstellt. Kann entweder **PixelShader oder** **VertexShader sein.**<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>                             | Das [Shadermodell, mit](dx-graphics-hlsl-models.md) dem kompiliert werden soll. hängt vom Typ der Shadervariablen ab.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**<br/> | Eine ASCII-Zeichenfolge, die den Namen der Shadereinstiegspunktfunktion enthält. Dies ist die Funktion, die mit der Ausführung beginnt, wenn der Shader aufgerufen wird. (...) stellt die Shaderargumente dar. Dies sind die gleichen Argumente, die an die Shadererstellungs-API übergeben werden: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) oder [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).<br/> |



 

### <a name="example"></a>Beispiel

Hier ist ein Beispiel für einen Vertex-Shader und ein Pixel-Shaderobjekt, die für ein bestimmtes Shadermodell kompiliert wurden.


```
// Direct3D 9
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_2_0 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_2_0 RenderScenePS( true );
    }
}
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 


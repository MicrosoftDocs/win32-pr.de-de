---
title: Shadertyp
description: Die Syntax zum Deklarieren einer shadervariablen in einem Effekt hat sich von Direct3D 9 auf Direct3D 10 geändert.
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
ms.openlocfilehash: 0ca3332c441279d7f9221efe8cfa7638908ddc44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976792"
---
# <a name="shader-type"></a>Shadertyp

Die Syntax zum Deklarieren einer shadervariablen in einem Effekt hat sich von Direct3D 9 auf Direct3D 10 geändert.

## <a name="shader-type-for-direct3d-10"></a>Shadertyp für Direct3D 10

Deklarieren Sie eine shadervariable innerhalb eines Effekts (in Direct3D 10) mithilfe der shadertypsyntax:



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Setpixelshader** Compile ( **shadertarget, shaderfunction** ); **Setgeometryshader** Compile ( **shadertarget, shaderfunction** ); **Setvertexshader** Compile ( **shadertarget, shaderfunction** ); |



 

### <a name="parameters"></a>Parameter



| Element                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**Setxxxshader**<br/>         | Der Direct3D-API-Befehl, der das Shader-Objekt erstellt. Kann wie folgt lauten: **setpixelshader** oder **setgeometryshader** oder **setvertexshader**.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**Shadertarget**<br/>         | Das Shader-Modell, mit dem kompiliert werden soll. Dies gilt für alle Ziele, einschließlich aller Direct3D 9-Ziele plus der [Shader Model 4](dx-graphics-hlsl-sm4.md) -Ziele: vs \_ 4 \_ 0, GS \_ 4 \_ 0 und PS \_ 4 \_ 0.<br/>                                                                                                                                                                                                                                          |
| <span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**Shaderfunction**<br/> | Eine ASCII-Zeichenfolge, die den Namen der Shader-Einstiegspunkt Funktion enthält. Dies ist die Funktion, die mit der Ausführung beginnt, wenn der Shader aufgerufen wird. Der (...) stellt die Shader-Argumente dar. Dabei handelt es sich um dieselben Argumente, die an die Shader-Erstellungs-API übergeben werden: [**vssetshader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) oder [**gssetshader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) oder [**pssetshader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).<br/> |



 

### <a name="example"></a>Beispiel

Es folgt ein Beispiel, das ein Vertex-Shader-und Pixel-Shader-Objekt erstellt, das für ein bestimmtes Shader-Modell kompiliert wird. Im Beispiel Direct3D 10 gibt es keinen Geometry-Shader, sodass der Zeiger auf **null** festgelegt ist.


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

Deklarieren Sie eine shadervariable innerhalb eines Effekts (für Direct3D 9) mithilfe der shadertypsyntax:



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| **Pixelshader** = **shaderziel-shaderfunktion kompilieren (...); Vertexshader** = **shaderziel-shaderfunktion kompilieren (...);** |



 

### <a name="parameters"></a>Parameter



| Element                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**Xxxshader**<br/>                                         | Eine Shader-Variable, die den kompilierten Shader darstellt. Kann entweder " **Pixelshader** " oder " **Vertexshader**" lauten.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**Shadertarget**<br/>                             | Das [Shader-Modell](dx-graphics-hlsl-models.md) , mit dem kompiliert werden soll. hängt vom Typ der shadervariablen ab.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**Shaderfunction (...)**<br/> | Eine ASCII-Zeichenfolge, die den Namen der Shader-Einstiegspunkt Funktion enthält. Dies ist die Funktion, die mit der Ausführung beginnt, wenn der Shader aufgerufen wird. Der (...) stellt die Shader-Argumente dar. Dabei handelt es sich um dieselben Argumente, die an die Shader-Erstellungs-API ( [**setvertexshader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) oder [**setpixelshader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) übermittelt werden.<br/> |



 

### <a name="example"></a>Beispiel

Im folgenden finden Sie ein Beispiel für ein Vertex-Shader-und Pixel-Shader-Objekt, das für ein bestimmtes Shader-Modell kompiliert wurde.


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

 


---
description: Eine Effekt Funktion wird in HLSL geschrieben und mit der folgenden Syntax deklariert.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Effekt Funktions Syntax (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483198"
---
# <a name="effect-function-syntax-direct3d-10"></a>Effekt Funktions Syntax (Direct3D 10)

Eine Effekt Funktion wird in HLSL geschrieben und mit der folgenden Syntax deklariert.

## <a name="syntax"></a>Syntax

*ReturnType* *FunctionName* (Argument \[ *List* \] )

{

<dl> \[ *Anweisungen* \]
</dl>

};



| Name         | BESCHREIBUNG                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Beliebiger [HLSL-Typ](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)                                                                                                                                                                                                       |
| FunctionName | Eine ASCII-Zeichenfolge, die den Namen der Shader-Funktion eindeutig identifiziert.                                                                                                                                                                                            |
| Argument List | Mindestens ein durch Kommas getrenntes Argument (siehe [Funktionsargumente (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).                                                                                                                             |
| Anweisungen   | Mindestens eine-Anweisung (siehe [Anweisungen (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)), die den Hauptteil der Funktion bilden. Wenn eine Funktion ohne Text definiert ist, wird Sie als Prototyp betrachtet. und müssen vor der Verwendung mit einem Text neu definiert werden. |



 

Eine Effekt Funktion kann ein Shader sein, oder es kann sich einfach um eine Funktion handeln, die von einem Shader aufgerufen wird. Eine Funktion wird durch ihren Namen, die Typen ihrer Parameter und die Zielplattform eindeutig identifiziert. Daher können Funktionen überladen werden. Jede gültige HLSL-Funktion sollte diesem Format entsprechen. eine ausführlichere Liste der Syntax für HLSL-Funktionen finden Sie unter [Functions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).

## <a name="example"></a>Beispiel

Das [BasicHLSL10-Beispiel](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) verwendet einen Pixel-Shader und einen Vertex-Shader. Die Pixel-Shader-Funktion heißt rendersceneps und ist unten dargestellt.


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](d3d10-effect-format.md)
</dt> </dl>

 

 

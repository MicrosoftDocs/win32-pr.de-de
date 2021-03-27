---
title: Effekt Funktions Syntax (Direct3D 11)
description: Eine Effekt Funktion ist in HLSL geschrieben und wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f569211d5f178b96cf7415478010285e7a836b58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727377"
---
# <a name="effect-function-syntax-direct3d-11"></a>Effekt Funktions Syntax (Direct3D 11)

Eine Effekt Funktion ist in HLSL geschrieben und wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.

## <a name="syntax"></a>Syntax

*ReturnType* *FunctionName* (Argument \[ *List* \] )

{

<dl> \[ *Anweisungen* \]
</dl>

};



| Name         | BESCHREIBUNG                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Beliebiger [HLSL-Typ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)                                                                                                                                                                                                       |
| FunctionName | Eine ASCII-Zeichenfolge, die den Namen der Shader-Funktion eindeutig identifiziert.                                                                                                                                                                                            |
| Argument List | Mindestens ein durch Kommas getrenntes Argument (siehe [Funktionsargumente (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).                                                                                                                             |
| Anweisungen   | Mindestens eine-Anweisung (siehe [Anweisungen (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)), die den Hauptteil der Funktion bilden. Wenn eine Funktion ohne Text definiert ist, wird Sie als Prototyp betrachtet. und müssen vor der Verwendung mit einem Text neu definiert werden. |



 

Eine Effekt Funktion kann ein Shader sein, oder es kann sich einfach um eine Funktion handeln, die von einem Shader aufgerufen wird. Eine Funktion wird durch ihren Namen, die Typen ihrer Parameter und die Zielplattform eindeutig identifiziert. Daher können Funktionen überladen werden. Jede gültige HLSL-Funktion sollte diesem Format entsprechen. eine ausführlichere Liste der Syntax für HLSL-Funktionen finden Sie unter [Functions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).

## <a name="example"></a>Beispiel

Im folgenden finden Sie ein Beispiel für eine Pixel-Shader-Funktion.


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

[Effekt Format](d3d11-effect-format.md)
</dt> </dl>

 

 
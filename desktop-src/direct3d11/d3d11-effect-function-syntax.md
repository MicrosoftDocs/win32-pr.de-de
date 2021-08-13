---
title: Effect-Funktionssyntax (Direct3D 11)
description: Eine Effect-Funktion wird in HLSL geschrieben und mit der in diesem Abschnitt beschriebenen Syntax deklariert.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 945f7104d44947f37af71ce664dd99ff64362062b1d42af62af2054538bacb52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046618"
---
# <a name="effect-function-syntax-direct3d-11"></a>Effect-Funktionssyntax (Direct3D 11)

Eine Effect-Funktion wird in HLSL geschrieben und mit der in diesem Abschnitt beschriebenen Syntax deklariert.

## <a name="syntax"></a>Syntax

*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )

{

<dl> \[ *Anweisungen* \]
</dl>

};



| Name         | BESCHREIBUNG                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Beliebiger [HLSL-Typ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)                                                                                                                                                                                                       |
| FunctionName | Eine ASCII-Zeichenfolge, die den Namen der Shaderfunktion eindeutig identifiziert.                                                                                                                                                                                            |
| Argumentlist | Ein oder mehrere Argumente, getrennt durch Kommas (siehe [Funktionsargumente (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).                                                                                                                             |
| Anweisungen   | Eine oder mehrere Anweisungen (siehe [Anweisungen (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)), die den Text der Funktion bilden. Wenn eine Funktion ohne Text definiert wird, wird sie als Prototyp betrachtet. und müssen vor der Verwendung mit einem Text neu definiert werden. |



 

Eine Effektfunktion kann ein Shader oder einfach eine Funktion sein, die von einem Shader aufgerufen wird. Eine Funktion wird durch ihren Namen, die Typen ihrer Parameter und die Zielplattform eindeutig identifiziert. Daher können Funktionen überladen werden. Jede gültige HLSL-Funktion sollte in dieses Format passen. Eine ausführlichere Liste der Syntax für HLSL-Funktionen finden Sie unter [Functions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).

## <a name="example"></a>Beispiel

Im Folgenden wird ein Beispiel für eine Pixelshaderfunktion dargestellt.


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

[Effektformat](d3d11-effect-format.md)
</dt> </dl>

 

 
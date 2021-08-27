---
title: Stream Out-Syntax
description: Ein Geometrie-Shader mit Stream out wird mit einer bestimmten Syntax deklariert.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43980d79d9c338a965d7ab2f2ceb008411d9713dec935d953dd5a1854c40465b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096390"
---
# <a name="stream-out-syntax"></a>Stream Out-Syntax

Ein Geometrie-Shader mit Stream out wird mit einer bestimmten Syntax deklariert. In diesem Thema wird die Syntax beschrieben. In der Effect Runtime wird diese Syntax in einen Aufruf von [**ID3D11Device::CreateGeometryShaderWithStreamOutput konvertiert.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)

## <a name="construct-syntax"></a>Konstruktsyntax


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| Name                   | BESCHREIBUNG                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | Optional. Eine ASCI-Zeichenfolge, die den Namen einer Geometrie-Shadervariablen mit stream out eindeutig identifiziert. Dies ist optional, da ConstructGSWithSO direkt in einem SetGeometryShader- oder BindInterfaces-Aufruf platziert werden kann. |
| **ShaderVar**          | Eine Geometrie-Shader- oder Vertex-Shadervariable.                                                                                                                                                                               |
| **OutputDecl0**        | Eine Zeichenfolge, die definiert, welche Shader-Ausgaben in Stream 0 gestreamt werden. Syntax finden Sie weiter unten.                                                                                                                                 |



 

Dies ist die Syntax, die in fx \_ 4 \_ 0-Dateien definiert wurde. Beachten Sie, dass es in gs \_ 4 \_ 0- und \_ vs x-Shadern nur einen Datenstrom gibt. Der resultierende Shader gibt einen Stream sowohl an die Streamausgabeeinheit als auch an die Rasterizereinheit aus.


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| Name                   | BESCHREIBUNG                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | Optional. Eine ASCI-Zeichenfolge, die den Namen einer Geometrie-Shadervariablen mit stream out eindeutig identifiziert. Dies ist optional, da ConstructGSWithSO direkt in einem SetGeometryShader- oder BindInterfaces-Aufruf platziert werden kann. |
| **ShaderVar**          | Eine Geometrie-Shader- oder Vertex-Shadervariable.                                                                                                                                                                               |
| **OutputDecl0**        | Eine Zeichenfolge, die definiert, welche Shader-Ausgaben in Stream 0 gestreamt werden. Syntax finden Sie weiter unten.                                                                                                                                 |
| **OutputDecl1**        | Eine Zeichenfolge, die definiert, welche Shader-Ausgaben in Stream 1 gestreamt werden. Syntax finden Sie weiter unten.                                                                                                                                 |
| **OutputDecl2**        | Eine Zeichenfolge, die definiert, welche Shader-Ausgaben in Stream 2 ausgegeben werden. Syntax finden Sie weiter unten.                                                                                                                                 |
| **OutputDecl3**        | Eine Zeichenfolge, die definiert, welche Shader-Ausgaben in Stream 3 ausgegeben werden. Syntax finden Sie weiter unten.                                                                                                                                 |
| **RasterizedStream**   | Eine ganze Zahl, die angibt, welcher Stream an den Rasterizer gesendet wird.                                                                                                                                                         |



 

Beachten Sie, dass gs \_ 5 \_ 0-Shader bis zu vier Datenströme definieren können. Der resultierende Shader gibt einen Stream für jede Ausgabedeklaration ohne **NULL** und einen Stream für die Rasterizereinheit an die Streamausgabeeinheit aus.

## <a name="stream-out-declaration-syntax"></a>Stream Out-Deklarationssyntax


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| Name              | BESCHREIBUNG                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| **Buffer**        | Optional. Eine ganze Zahl, 0 <= Puffer < 4, die angibt, an welchen Stream-Outpuffer der Wert gehen soll. |
| **Semantische**      | Eine Zeichenfolge zusammen mit SemanticIndex, die angibt, welcher Wert ausgegeben werden soll.                                 |
| **SemanticIndex** | Optional. Der Index, der der Semantik zugeordnet ist.                                                         |
| **Mask**          | Optional. Eine Komponentenmaske, die angibt, welche Komponenten des Werts ausgegeben werden.                       |



 

Es gibt eine spezielle Semantik mit der Bezeichnung "$SKIP", die eine leere Semantik angibt, wodurch der entsprechende Arbeitsspeicher im Stream-Out-Puffer unverändert bleibt. Die $SKIP Semantik kann keinen SemanticIndex, aber eine Maske haben.

Die gesamte Stream-Out-Deklaration kann **NULL sein.**

## <a name="example"></a>Beispiel


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 





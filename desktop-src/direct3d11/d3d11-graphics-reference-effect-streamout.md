---
title: Stream out-Syntax
description: Ein Geometry-Shader mit Stream out wird mit einer bestimmten Syntax deklariert.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ea78d1b2109e343f01800b3a3d5e1bf6efaba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992791"
---
# <a name="stream-out-syntax"></a>Stream out-Syntax

Ein Geometry-Shader mit Stream out wird mit einer bestimmten Syntax deklariert. In diesem Thema wird die-Syntax beschrieben. In der Effect-Laufzeit wird diese Syntax in einen-Befehl von [**ID3D11Device::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)-Alias konvertiert.

## <a name="construct-syntax"></a>Syntax erstellen


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| Name                   | BESCHREIBUNG                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Streamingshadervar** | Optional. Eine ASCI-Zeichenfolge, die den Namen einer Geometry-shadervariablen mit Stream out eindeutig identifiziert. Dies ist optional, da constructgswithso direkt in einem setgeometryshader-oder bindinterfaces-aufrufen platziert werden kann. |
| **Shadervar**          | Eine Geometry-Shader-oder Vertex-Shader-Variable.                                                                                                                                                                               |
| **OutputDecl0**        | Eine Zeichenfolge, die definiert, welche shaderausgaben in Stream 0 gestreamt werden. Die Syntax finden Sie weiter unten.                                                                                                                                 |



 

Dies ist die Syntax, die in FX \_ 4 \_ 0-Dateien definiert wurde. Beachten Sie, dass in GS \_ 4 \_ 0 und vs \_ x-Shadern nur ein Datenstrom vorhanden ist. Der resultierende Shader gibt einen Datenstrom sowohl an die Stream-out-Einheit als auch an die Raster-Einheit aus.


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| Name                   | BESCHREIBUNG                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Streamingshadervar** | Optional. Eine ASCI-Zeichenfolge, die den Namen einer Geometry-shadervariablen mit Stream out eindeutig identifiziert. Dies ist optional, da constructgswithso direkt in einem setgeometryshader-oder bindinterfaces-aufrufen platziert werden kann. |
| **Shadervar**          | Eine Geometry-Shader-oder Vertex-Shader-Variable.                                                                                                                                                                               |
| **OutputDecl0**        | Eine Zeichenfolge, die definiert, welche shaderausgaben in Stream 0 gestreamt werden. Die Syntax finden Sie weiter unten.                                                                                                                                 |
| **OutputDecl1**        | Eine Zeichenfolge, die definiert, welche shaderausgaben in Stream 1 gestreamt werden. Die Syntax finden Sie weiter unten.                                                                                                                                 |
| **OutputDecl2**        | Eine Zeichenfolge, die definiert, welche shaderausgaben in Stream 2 gestreamt werden. Die Syntax finden Sie weiter unten.                                                                                                                                 |
| **OutputDecl3**        | Eine Zeichenfolge, die definiert, welche shaderausgaben in Stream 3 gestreamt werden. Die Syntax finden Sie weiter unten.                                                                                                                                 |
| **Rasterizedstream**   | Eine ganze Zahl, die angibt, welcher Stream an den Rasterizer gesendet wird.                                                                                                                                                         |



 

Beachten Sie, dass GS \_ 5 \_ 0-Shader bis zu vier Datenströme definieren können. Der resultierende Shader gibt einen Datenstrom für jede Ausgabe Deklaration ungleich **null** und einen Stream der Raster-Einheit an die Datenstrom Ausgabe aus.

## <a name="stream-out-declaration-syntax"></a>Syntax der Stream out-Deklaration


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| Name              | BESCHREIBUNG                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| **Buffer**        | Optional. Eine ganze Zahl, 0 <= Puffer < 4, die angibt, an welchen Stream-out-Puffer der Wert gesendet wird. |
| **Tischer**      | Eine Zeichenfolge zusammen mit semanticindex, die angibt, welcher Wert ausgegeben werden soll.                                 |
| **Semanticindex** | Optional. Der der Semantik zugeordnete Index.                                                         |
| **Mask**          | Optional. Eine Komponenten Maske, die angibt, welche Komponenten des Werts ausgegeben werden.                       |



 

Es gibt eine besondere Semantik mit der Bezeichnung "$Skip", die eine leere Semantik angibt, sodass der entsprechende Arbeitsspeicher im Stream-out-Puffer unverändert bleibt. Die $Skip Semantik darf keinen semanticindex aufweisen, kann jedoch eine Maske aufweisen.

Die gesamte Stream out-Deklaration kann **null** sein.

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

 

 





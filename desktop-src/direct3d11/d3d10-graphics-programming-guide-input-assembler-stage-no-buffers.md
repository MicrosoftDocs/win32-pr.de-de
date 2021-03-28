---
title: Verwenden der Input-Assembler-Phase ohne Puffer
description: Das Erstellen und Binden von Puffern ist nicht erforderlich, wenn die Shader keine Puffer erfordern. Dieser Abschnitt enthält ein Beispiel für einfache Vertex-und Pixel-Shader, die ein einzelnes Dreieck zeichnen.
ms.assetid: 84d24494-f2cb-4ca1-84fd-635e20f2c9ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3aa4c63176d184e1e67349149bd1f4044159e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104975953"
---
# <a name="using-the-input-assembler-stage-without-buffers"></a>Verwenden der Input-Assembler-Phase ohne Puffer

Das Erstellen und Binden von Puffern ist nicht erforderlich, wenn die Shader keine Puffer erfordern. Dieser Abschnitt enthält ein Beispiel für einfache Vertex-und Pixel-Shader, die ein einzelnes Dreieck zeichnen.

-   [Vertex-Shader](#vertex-shader)
-   [Pixelshader](#pixel-shader)
-   [Verfahren](#technique)
-   [Anwendungscode](#application-code)
-   [Zugehörige Themen](#related-topics)

## <a name="vertex-shader"></a>Vertexshader

Beispielsweise können Sie einen Vertexshader deklarieren, der seine eigenen Scheitel Punkte erstellt.


```
struct VSIn
{
    uint vertexId : SV_VertexID;
};

struct VSOut
{
    float4 pos : SV_Position;
    float4 color : color;
};

VSOut VSmain(VSIn input)
{
    VSOut output;
    
    if (input.vertexId == 0)
        output.pos = float4(0.0, 0.5, 0.5, 1.0);
    else if (input.vertexId == 2)
        output.pos = float4(0.5, -0.5, 0.5, 1.0);
    else if (input.vertexId == 1)
        output.pos = float4(-0.5, -0.5, 0.5, 1.0);
    
    output.color = clamp(output.pos, 0, 1);
    
    return output;
}
```



## <a name="pixel-shader"></a>Pixelshader


```
// NoBuffer.fx
// Copyright (c) 2004 Microsoft Corporation. All rights reserved.
//

struct PSIn
{
    float4 pos : SV_Position;
    linear float4 color : color;
};

struct PSOut
{
    float4 color : SV_Target;
};


PSOut PSmain(PSIn input)
{
    PSOut output;
    
    output.color = input.color;
    
    return output;
}
```



## <a name="technique"></a>Verfahren

Eine Technik ist eine Sammlung von Renderingdurchläufen (es muss mindestens ein Durchlauf vorhanden sein).


```
VertexShader vsCompiled = CompileShader( vs_4_0, VSmain() );

technique10 t0
{
    pass p0
    {
        SetVertexShader( vsCompiled );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PSmain() ));
    }  
}
```



## <a name="application-code"></a>Anwendungscode


```
m_pD3D11Device->IASetInputLayout( NULL );

m_pD3D11Device->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
    
ID3DX11EffectTechnique * pTech = NULL;
pTech = m_pEffect->GetTechniqueByIndex(0);
pTech->GetPassByIndex(iPass)->Apply(0);

m_pD3D11Device->Draw( 3, 0 );
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ersten Einstieg in die Input-Assembler Phase](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> </dl>

 

 





---
title: Anfügen (DirectX HLSL Stream-Output-Objekt)
description: Fügen Sie Geometry-Shader-Output-Daten an einen vorhandenen Datenstrom an.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 97ab88961b22529accb4402fc2bd095ede5275c1
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "104313889"
---
# <a name="append-directx-hlsl-stream-output-object"></a>Anfügen (DirectX HLSL Stream-Output-Objekt)

Fügen Sie Geometry-Shader-Output-Daten an einen vorhandenen Datenstrom an.



|                            |
|----------------------------|
| Append ( *streamdatatype*); |



 

## <a name="parameters"></a>Parameter



| Element                                                                                                                             | BESCHREIBUNG                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**Streamdatatype**<br/> | Eine Beschreibung der Dateneingabe. Diese Beschreibung muss mit dem Stream-Object-Vorlagen Parameter namens [DataType](dx-graphics-hlsl-so-type.md)identisch sein.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Keine

## <a name="example"></a>Beispiel

Dieser Code Ausschnitt (aus dem [cubemapgs-Beispiel](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) zeigt ein partielles Beispiel für das Anfügen von Dreiecks leisten primitiven an ein Stream-Output-Objekt.


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stream-Output-Objekt](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 






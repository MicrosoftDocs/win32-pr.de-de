---
title: Append (DirectX HLSL Stream-Output Object)
description: Fügen Sie geometry-shader-output-Daten an einen vorhandenen Stream an.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 956d4b2e37c4430e20fc4b75b2847c096c7832369d036f5224d8c36d86b7c66c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068170"
---
# <a name="append-directx-hlsl-stream-output-object"></a>Append (DirectX HLSL Stream-Output Object)

Fügen Sie geometry-shader-output-Daten an einen vorhandenen Stream an.

Append( *StreamDataType*);



 

## <a name="parameters"></a>Parameter



| Element                                                                                                                             | BESCHREIBUNG                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**<br/> | Eine Dateneingabebeschreibung. Diese Beschreibung muss mit dem Vorlagenparameter stream-object namens [DataType übereinstimmen.](dx-graphics-hlsl-so-type.md)<br/> |



 

## <a name="return-value"></a>Rückgabewert

Keine

## <a name="example"></a>Beispiel

Dieser Codeausschnitt (aus dem [CubeMapGS-Beispiel)](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)zeigt ein partielles Beispiel für das Anfügen von Dreiecksstreifenprimitiven an ein Streamausgabeobjekt.


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



## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stream-Output-Objekt](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 






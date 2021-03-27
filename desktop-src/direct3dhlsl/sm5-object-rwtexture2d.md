---
title: RWTexture2D
description: Eine Ressource mit Lese-/Schreibzugriff. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- RWTexture2D HLSL
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdeae4dd47d3ad4bf5d756c2ca362033eae6814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352969"
---
# <a name="rwtexture2d"></a>RWTexture2D

Eine Ressource mit Lese-/Schreibzugriff.



| Methode                                                        | BESCHREIBUNG                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2d-getdimensions.md) | Ruft die Ressourcen Dimensionen ab. |
| [**Laden**](rwtexture2d-load.md)                              | Liest Textur Daten.           |
| [**KOM\[\]**](sm5-object-rwtexture2d-operatorindex.md)  | Ruft eine Ressourcen Variable ab.     |



 

Sie können RWTexture2D-Objekten mit der Speicher Klasse **globallycoherent** als Präfix versehen. Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können. Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung nur eine unsorderte Zugriffs Ansicht (UAV) innerhalb der aktuellen Gruppe.

Ein RWTexture2D-Objekt erfordert einen Elementtyp in einer Deklarations Anweisung für das-Objekt. Beispielsweise ist die folgende Deklaration nicht korrekt:


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



Die folgende Deklaration ist korrekt:


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



Da ein RWTexture2D-Objekt ein Objekt vom Typ "UAV" ist, unterscheiden sich seine Eigenschaften von einem Objekt der Shader-Ressourcen Ansicht (SRV), z. b. einem [Texture2D](sm5-object-texture2d.md) -Objekt. Beispielsweise können Sie aus einem RWTexture2D-Objekt lesen und darin schreiben, aber Sie können nur aus einem Texture2D-Objekt lesen.

Ein RWTexture2D-Objekt kann keine Methoden aus einem [Texture2D](sm5-object-texture2d.md) -Objekt verwenden, z. b. [Sample](dx-graphics-hlsl-to-sample.md). Da Sie jedoch mehrere Ansichts Typen für dieselbe Ressource erstellen können, können Sie mehrere Textur Typen als einzelne Textur in mehreren Shadern deklarieren. Die folgenden Code Ausschnitte zeigen z. b., wie Sie ein RWTexture2D-Objekt als *tex* in einem Compute-Shader deklarieren und verwenden können, und dann ein Texture2D-Objekt als *tex* in einem Pixelshader deklarieren und verwenden.

> [!Note]  
> Die Runtime erzwingt bestimmte Verwendungs Muster, wenn Sie mehrere Ansichts Typen für dieselbe Ressource erstellen. Beispielsweise können Sie mit der Laufzeit nicht gleichzeitig eine UAV-Zuordnung für eine Ressource und eine SRV-Zuordnung für dieselbe Ressource aktivieren.

 

Der folgende Code ist für den Compute-Shader:


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



Der folgende Code ist für den Pixelshader:


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieses Objekt wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shader Model 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





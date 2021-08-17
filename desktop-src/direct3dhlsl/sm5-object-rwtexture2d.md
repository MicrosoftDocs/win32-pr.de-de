---
title: RWTexture2D
description: Eine Lese-/Schreibressource. | RWTexture2D
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
ms.openlocfilehash: c015aaa8606f5d04386b7839584203c5672e4ac1bf031b89eb4c41ca69f7dd14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985930"
---
# <a name="rwtexture2d"></a>RWTexture2D

Eine Lese-/Schreibressource.



| Methode                                                        | Beschreibung                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2d-getdimensions.md) | Ruft die Ressourcendimensionen ab. |
| [**Laden**](rwtexture2d-load.md)                              | Liest Texturdaten.           |
| [**Operator\[\]**](sm5-object-rwtexture2d-operatorindex.md)  | Ruft eine Ressourcenvariable ab.     |



 

Sie können RWTexture2D-Objekten global und global die **Speicherklasse vorangestellt werden.** Diese Speicherklasse bewirkt Speicherbarrieren und Synchronisierungen, um Daten über die gesamte GPU zu leeren, damit andere Gruppen Schreibvorgänge sehen können. Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung nur eine ungeordnete Zugriffsansicht (UAV) innerhalb der aktuellen Gruppe.

Ein RWTexture2D-Objekt erfordert einen Elementtyp in einer Deklarations-Anweisung für das -Objekt. Die folgende Deklaration ist beispielsweise nicht korrekt:


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



Die folgende Deklaration ist richtig:


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



Da ein RWTexture2D-Objekt ein UAV-Objekt ist, unterscheiden sich seine Eigenschaften von einem SRV-Objekt (Shader Resource View), z. B. [einem Texture2D-Objekt.](sm5-object-texture2d.md) Beispielsweise können Sie aus einem RWTexture2D-Objekt lesen und in dieses schreiben, aber nur aus einem Texture2D-Objekt.

Ein RWTexture2D-Objekt kann keine Methoden aus einem [Texture2D-Objekt](sm5-object-texture2d.md) wie [Sample verwenden.](dx-graphics-hlsl-to-sample.md) Da Sie jedoch mehrere Ansichtstypen für dieselbe Ressource erstellen können, können Sie mehrere Texturtypen als eine einzelne Textur in mehreren Shadern deklarieren. Die folgenden Codeausschnitte zeigen beispielsweise, wie Sie ein RWTexture2D-Objekt als *Tex* in einem Compute-Shader deklarieren und verwenden und dann ein Texture2D-Objekt *als* Tex in einem Pixel-Shader deklarieren und verwenden können.

> [!Note]  
> Die Runtime erzwingt bestimmte Verwendungsmuster, wenn Sie mehrere Ansichtstypen für dieselbe Ressource erstellen. Beispielsweise lässt die Laufzeit nicht zu, dass Sie sowohl eine UAV-Zuordnung für eine Ressource als auch eine SRV-Zuordnung für dieselbe Ressource gleichzeitig aktiv haben.

 

Der folgende Code gilt für den Compute-Shader:


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



Der folgende Code gilt für den Pixel-Shader:


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



## <a name="minimum-shader-model"></a>Minimales Shadermodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ShaderModell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





---
title: RWTexture1DArray
description: Eine Lese-/Schreibressource. | RWTexture1DArray
ms.assetid: 214c7e7d-4e74-4f4f-bf78-98e9df0b3a0e
keywords:
- RWTexture1DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c25bbc29e9835f79fa65510d97a3fd0241b06b5ad3415db1059c755a3ac5e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509272"
---
# <a name="rwtexture1darray"></a>RWTexture1DArray

Eine Lese-/Schreibressource.



| Methode                                                             | BESCHREIBUNG                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1darray-getdimensions.md) | Ruft die Ressourcendimensionen ab. |
| [**Laden**](rwtexture1darray-load.md)                              | Liest Texturdaten.           |
| [**Operator\[\]**](sm5-object-rwtexture1darray-operatorindex.md)  | Ruft eine Ressourcenvariable ab.     |



 

Sie können **RWTexture1DArray-Objekten** die Speicherklasse **globallycoherent voran stellen.** Diese Speicherklasse bewirkt Speicherbarrieren und Synchronisierungen, um Daten über die gesamte GPU zu leeren, damit andere Gruppen Schreibvorgänge sehen können. Ohne diesen Bezeichner leert eine Speicherbarriere oder Synchronisierung einen UAV nur innerhalb der aktuellen Gruppe.

Ein **RWTexture1DArray-Objekt** erfordert einen Elementtyp in einer Deklarations-Anweisung für das -Objekt. Die folgende Deklaration ist beispielsweise richtig:


```
RWTexture1DArray<float> tex;
```



Da ein **RWTexture1DArray-Objekt** ein UAV-Objekt ist, unterscheiden sich seine Eigenschaften von einem SRV-Objekt (Shader Resource View), z. B. [**einem Texture1DArray-Objekt.**](sm5-object-texture1darray.md) Sie können beispielsweise aus einem **RWTexture1DArray-Objekt** lesen und in dieses schreiben, aber nur aus einem **Texture1DArray-Objekt.**

Ein **RWTexture1DArray-Objekt** kann keine Methoden aus einem [**Texture1DArray-Objekt**](sm5-object-texture1darray.md) wie [Sample verwenden.](dx-graphics-hlsl-to-sample.md) Da Sie jedoch mehrere Ansichtstypen für dieselbe Ressource erstellen können, können Sie mehrere Texturtypen als eine einzelne Textur in mehreren Shadern deklarieren. Beispielsweise können Sie ein **RWTexture1DArray-Objekt** als *Tex* in einem Compute-Shader deklarieren und verwenden und dann ein **Texture1DArray-Objekt** als *Tex* in einem Pixel-Shader deklarieren und verwenden.

> [!Note]  
> Die Runtime erzwingt bestimmte Verwendungsmuster, wenn Sie mehrere Ansichtstypen für dieselbe Ressource erstellen. Beispielsweise lässt die Laufzeit nicht zu, dass Sie sowohl eine UAV-Zuordnung für eine Ressource als auch eine SRV-Zuordnung für dieselbe Ressource gleichzeitig aktiv haben.

 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ShaderModell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





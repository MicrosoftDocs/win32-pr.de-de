---
title: RWTexture1DArray
description: Eine Ressource mit Lese-/Schreibzugriff. | RWTexture1DArray
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
ms.openlocfilehash: 2e7f6841cb1f15b12c9755da2a9fae50e42ed333
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961419"
---
# <a name="rwtexture1darray"></a>RWTexture1DArray

Eine Ressource mit Lese-/Schreibzugriff.



| Methode                                                             | BESCHREIBUNG                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1darray-getdimensions.md) | Ruft die Ressourcen Dimensionen ab. |
| [**Laden**](rwtexture1darray-load.md)                              | Liest Textur Daten.           |
| [**KOM\[\]**](sm5-object-rwtexture1darray-operatorindex.md)  | Ruft eine Ressourcen Variable ab.     |



 

Sie können **RWTexture1DArray** -Objekten mit der Speicher Klasse **globallycoherent** als Präfix versehen. Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können. Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung eine UAV nur innerhalb der aktuellen Gruppe.

Ein **RWTexture1DArray** -Objekt erfordert einen Elementtyp in einer Deklarations Anweisung für das-Objekt. Beispielsweise ist die folgende Deklaration richtig:


```
RWTexture1DArray<float> tex;
```



Da ein **RWTexture1DArray** -Objekt ein Objekt vom Typ "UAV" ist, unterscheiden sich seine Eigenschaften von einem Objekt der Shader-Ressourcen Ansicht (SRV), z. b. einem [**Texture1DArray**](sm5-object-texture1darray.md) -Objekt. Beispielsweise können Sie aus einem **RWTexture1DArray** -Objekt lesen und darin schreiben, aber Sie können nur aus einem **Texture1DArray** -Objekt lesen.

Ein **RWTexture1DArray** -Objekt kann keine Methoden aus einem [**Texture1DArray**](sm5-object-texture1darray.md) -Objekt verwenden, z. b. [Sample](dx-graphics-hlsl-to-sample.md). Da Sie jedoch mehrere Ansichts Typen für dieselbe Ressource erstellen können, können Sie mehrere Textur Typen als einzelne Textur in mehreren Shadern deklarieren. Beispielsweise können Sie ein **RWTexture1DArray** -Objekt als *tex* in einem Compute-Shader deklarieren und verwenden und dann ein **Texture1DArray** -Objekt als *tex* in einem Pixelshader deklarieren und verwenden.

> [!Note]  
> Die Runtime erzwingt bestimmte Verwendungs Muster, wenn Sie mehrere Ansichts Typen für dieselbe Ressource erstellen. Beispielsweise können Sie mit der Laufzeit nicht gleichzeitig eine UAV-Zuordnung für eine Ressource und eine SRV-Zuordnung für dieselbe Ressource aktivieren.

 

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

 

 





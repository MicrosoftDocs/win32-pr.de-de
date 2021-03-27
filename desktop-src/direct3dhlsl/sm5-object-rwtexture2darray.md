---
title: RWTexture2DArray
description: Eine Ressource mit Lese-/Schreibzugriff. | RWTexture2DArray
ms.assetid: 6a6f3655-f1c0-4d5b-91a2-d79da65858b8
keywords:
- RWTexture2DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ada0fcaba729eff37f41f1ae7666841175689ff
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981521"
---
# <a name="rwtexture2darray"></a>RWTexture2DArray

Eine Ressource mit Lese-/Schreibzugriff.



| Methode                                                             | BESCHREIBUNG                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2darray-getdimensions.md) | Ruft die Ressourcen Dimensionen ab. |
| [**Laden**](rwtexture2darray-load.md)                              | Liest Textur Daten.           |
| [**KOM\[\]**](sm5-object-rwtexture2darray-operatorindex.md)  | Ruft eine Ressourcen Variable ab.     |



 

Sie können **RWTexture2DArray** -Objekten mit der Speicher Klasse **globallycoherent** als Präfix versehen. Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können. Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung eine UAV nur innerhalb der aktuellen Gruppe.

Ein **RWTexture2DArray** -Objekt erfordert einen Elementtyp in einer Deklarations Anweisung für das-Objekt. Beispielsweise ist die folgende Deklaration richtig:


```
RWTexture2DArray<float> tex;
```



Da ein **RWTexture2DArray** -Objekt ein Objekt vom Typ "UAV" ist, unterscheiden sich seine Eigenschaften von einem Objekt der Shader-Ressourcen Ansicht (SRV), z. b. einem [**Texture2DArray**](sm5-object-texture2darray.md) -Objekt. Beispielsweise können Sie aus einem **RWTexture2DArray** -Objekt lesen und darin schreiben, aber Sie können nur aus einem **Texture2DArray** -Objekt lesen.

Ein **RWTexture2DArray** -Objekt kann keine Methoden aus einem [**Texture2DArray**](sm5-object-texture2darray.md) -Objekt verwenden, z. b. [Sample](dx-graphics-hlsl-to-sample.md). Da Sie jedoch mehrere Ansichts Typen für dieselbe Ressource erstellen können, können Sie mehrere Textur Typen als einzelne Textur in mehreren Shadern deklarieren. Beispielsweise können Sie ein **RWTexture2DArray** -Objekt als *tex* in einem Compute-Shader deklarieren und verwenden und dann ein **Texture2DArray** -Objekt als *tex* in einem Pixelshader deklarieren und verwenden.

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

 

 





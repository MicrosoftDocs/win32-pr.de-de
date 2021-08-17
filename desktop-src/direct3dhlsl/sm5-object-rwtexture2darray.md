---
title: RWTexture2DArray
description: Eine Lese-/Schreibressource. | RWTexture2DArray
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
ms.openlocfilehash: e9ae4d4c7c47012b71a70916f5861975176b86e6612cb2a4fec3ea6c9c6e17cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095130"
---
# <a name="rwtexture2darray"></a>RWTexture2DArray

Eine Lese-/Schreibressource.



| Methode                                                             | BESCHREIBUNG                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2darray-getdimensions.md) | Ruft die Ressourcendimensionen ab. |
| [**Laden**](rwtexture2darray-load.md)                              | Liest Texturdaten.           |
| [**Operator\[\]**](sm5-object-rwtexture2darray-operatorindex.md)  | Ruft eine Ressourcenvariable ab.     |



 

Sie können **RWTexture2DArray-Objekten** die **speicherklasse globallycoherent** voran stellen. Diese Speicherklasse bewirkt Speicherbarrieren und Synchronisierungen, um Daten über die gesamte GPU zu leeren, sodass andere Gruppen Schreibvorgänge sehen können. Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung eine UAV nur innerhalb der aktuellen Gruppe.

Ein **RWTexture2DArray-Objekt** erfordert einen Elementtyp in einer Deklarations-Anweisung für das Objekt. Die folgende Deklaration ist beispielsweise richtig:


```
RWTexture2DArray<float> tex;
```



Da ein **RWTexture2DArray-Objekt** ein Objekt vom Typ UAV ist, unterscheiden sich seine Eigenschaften von einem Objekt vom Typ shader resource view (SRV), z.B. einem [**Texture2DArray-Objekt.**](sm5-object-texture2darray.md) Beispielsweise können Sie aus einem **RWTexture2DArray-Objekt** lesen und in dieses schreiben, aber sie können nur aus einem **Texture2DArray-Objekt** lesen.

Ein **RWTexture2DArray-Objekt** kann keine Methoden aus einem [**Texture2DArray-Objekt**](sm5-object-texture2darray.md) wie [Sample](dx-graphics-hlsl-to-sample.md)verwenden. Da Sie jedoch mehrere Ansichtstypen für dieselbe Ressource erstellen können, können Sie mehrere Texturtypen als einzelne Textur in mehreren Shadern deklarieren. Beispielsweise können Sie ein **RWTexture2DArray-Objekt** als *Tex* in einem Compute-Shader deklarieren und verwenden und dann ein **Texture2DArray-Objekt** als *Tex* in einem Pixel-Shader deklarieren und verwenden.

> [!Note]  
> Die Runtime erzwingt bestimmte Verwendungsmuster, wenn Sie mehrere Ansichtstypen für dieselbe Ressource erstellen. Beispielsweise lässt die Runtime nicht zu, dass sowohl eine UAV-Zuordnung für eine Ressource als auch eine SRV-Zuordnung für dieselbe Ressource gleichzeitig aktiv ist.

 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shadermodell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





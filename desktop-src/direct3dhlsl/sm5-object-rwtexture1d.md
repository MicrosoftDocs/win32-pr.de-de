---
title: RWTexture1D
description: Eine Lese-/Schreibressource. | RWTexture1D
ms.assetid: 47866e5a-b26b-4264-9291-c8940882d662
keywords:
- RWTexture1D HLSL
topic_type:
- apiref
api_name:
- RWTexture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67fb82897e6b07dad486d134c7d36004ed5bfb1e050ed80446c50df5842eac32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671380"
---
# <a name="rwtexture1d"></a>RWTexture1D

Eine Lese-/Schreibressource.



| Methode                                                        | Beschreibung                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1d-getdimensions.md) | Ruft die Ressourcendimensionen ab. |
| [**Laden**](rwtexture1d-load.md)                              | Liest Texturdaten.           |
| [**Operator\[\]**](sm5-object-rwtexture1d-operatorindex.md)  | Ruft eine Ressourcenvariable ab.     |



 

Sie können **RWTexture1D-Objekten** global die **Speicherklasse** voran stellen. Diese Speicherklasse bewirkt Speicherbarrieren und Synchronisierungen, um Daten über die gesamte GPU zu leeren, sodass andere Gruppen Schreibvorgänge sehen können. Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung eine UAV nur innerhalb der aktuellen Gruppe.

Ein **RWTexture1D-Objekt** erfordert einen Elementtyp in einer Deklarations-Anweisung für das Objekt. Die folgende Deklaration ist beispielsweise richtig:


```
RWTexture1D<float> tex;
```



Da es sich bei einem **RWTexture1D-Objekt** um ein Objekt vom Typ UAV handelt, unterscheiden sich seine Eigenschaften von einem Objekt vom Typ shader resource view (SRV), z.B. einem [**Texture1D-Objekt.**](sm5-object-texture1d.md) Beispielsweise können Sie aus einem **RWTexture1D-Objekt** lesen und in dieses schreiben, aber sie können nur aus einem **Texture1D-Objekt** lesen.

Ein **RWTexture1D-Objekt** kann keine Methoden aus einem [**Texture1D-Objekt**](sm5-object-texture1d.md) verwenden, z. [B. Sample](dx-graphics-hlsl-to-sample.md). Da Sie jedoch mehrere Ansichtstypen für dieselbe Ressource erstellen können, können Sie mehrere Texturtypen als einzelne Textur in mehreren Shadern deklarieren. Beispielsweise können Sie ein **RWTexture1D-Objekt** als *Tex* in einem Compute-Shader deklarieren und verwenden und dann ein **Texture1D-Objekt** als *Tex* in einem Pixel-Shader deklarieren und verwenden.

> [!Note]  
> Die Runtime erzwingt bestimmte Verwendungsmuster, wenn Sie mehrere Ansichtstypen für dieselbe Ressource erstellen. Beispielsweise lässt die Runtime nicht zu, dass sowohl eine UAV-Zuordnung für eine Ressource als auch eine SRV-Zuordnung für dieselbe Ressource gleichzeitig aktiv ist.

 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shadermodell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





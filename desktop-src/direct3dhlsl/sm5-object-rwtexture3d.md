---
title: RWTexture3D
description: Eine Lese-/Schreibressource. | RWTexture3D
ms.assetid: 4d02810e-4f3c-4b20-b057-0ff27d6732b5
keywords:
- RWTexture3D HLSL
topic_type:
- apiref
api_name:
- RWTexture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bc2630d339bfb465b570ba62b346cd931301425f4feeb4367407ffd52336e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789863"
---
# <a name="rwtexture3d"></a>RWTexture3D

Eine Lese-/Schreibressource.



| Methode                                                        | BESCHREIBUNG                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture3d-getdimensions.md) | Ruft die Ressourcendimensionen ab. |
| [**Laden**](rwtexture3d-load.md)                              | Liest Texturdaten.           |
| [**Operator\[\]**](sm5-object-rwtexture3d-operatorindex.md)  | Ruft eine Ressourcenvariable ab.     |



 

Sie können **RWTexture3D-Objekten** die Speicherklasse **globalcoherent voran stellen.** Diese Speicherklasse bewirkt Speicherbarrieren und Synchronisierungen, um Daten über die gesamte GPU zu leeren, damit andere Gruppen Schreibvorgänge sehen können. Ohne diesen Bezeichner leert eine Speicherbarriere oder Synchronisierung einen UAV nur innerhalb der aktuellen Gruppe.

Ein **RWTexture3D-Objekt** erfordert einen Elementtyp in einer Deklarations-Anweisung für das -Objekt. Die folgende Deklaration ist beispielsweise richtig:


```
RWTexture3D<float> tex;
```



Da ein **RWTexture3D-Objekt** ein UAV-Objekt ist, unterscheiden sich seine Eigenschaften von einem SRV-Objekt (Shader Resource View), z. B. [**einem Texture3D-Objekt.**](sm5-object-texture3d.md) Beispielsweise können Sie aus einem **RWTexture3D-Objekt** lesen und in dieses schreiben, aber nur aus einem **Texture3D-Objekt.**

Ein **RWTexture3D-Objekt** kann keine Methoden aus einem [**Texture3D-Objekt**](sm5-object-texture3d.md) wie [Sample verwenden.](dx-graphics-hlsl-to-sample.md) Da Sie jedoch mehrere Ansichtstypen für dieselbe Ressource erstellen können, können Sie mehrere Texturtypen als eine einzelne Textur in mehreren Shadern deklarieren. Beispielsweise können Sie ein **RWTexture3D-Objekt** als *Tex* in einem Compute-Shader deklarieren und verwenden und dann ein **Texture3D-Objekt** als *Tex* in einem Pixel-Shader deklarieren und verwenden.

> [!Note]  
> Die Runtime erzwingt bestimmte Verwendungsmuster, wenn Sie mehrere Ansichtstypen für dieselbe Ressource erstellen. Beispielsweise lässt die Laufzeit nicht zu, dass Sie sowohl eine UAV-Zuordnung für eine Ressource als auch eine SRV-Zuordnung für dieselbe Ressource gleichzeitig aktiv haben.

 

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

 

 





---
title: RWTexture3D
description: Eine Ressource mit Lese-/Schreibzugriff. | RWTexture3D
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
ms.openlocfilehash: 9b89ed7ff724eabef9fc2b2757c6ac0e5272c69e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352669"
---
# <a name="rwtexture3d"></a>RWTexture3D

Eine Ressource mit Lese-/Schreibzugriff.



| Methode                                                        | BESCHREIBUNG                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture3d-getdimensions.md) | Ruft die Ressourcen Dimensionen ab. |
| [**Laden**](rwtexture3d-load.md)                              | Liest Textur Daten.           |
| [**KOM\[\]**](sm5-object-rwtexture3d-operatorindex.md)  | Ruft eine Ressourcen Variable ab.     |



 

Sie können **RWTexture3D** -Objekten mit der Speicher Klasse **globallycoherent** als Präfix versehen. Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können. Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung eine UAV nur innerhalb der aktuellen Gruppe.

Ein **RWTexture3D** -Objekt erfordert einen Elementtyp in einer Deklarations Anweisung für das-Objekt. Beispielsweise ist die folgende Deklaration richtig:


```
RWTexture3D<float> tex;
```



Da ein **RWTexture3D** -Objekt ein Objekt vom Typ "UAV" ist, unterscheiden sich seine Eigenschaften von einem Objekt der Shader-Ressourcen Ansicht (SRV), z. b. einem [**Texture3D**](sm5-object-texture3d.md) -Objekt. Beispielsweise können Sie aus einem **RWTexture3D** -Objekt lesen und darin schreiben, aber Sie können nur aus einem **Texture3D** -Objekt lesen.

Ein **RWTexture3D** -Objekt kann keine Methoden aus einem [**Texture3D**](sm5-object-texture3d.md) -Objekt verwenden, z. b. [Sample](dx-graphics-hlsl-to-sample.md). Da Sie jedoch mehrere Ansichts Typen für dieselbe Ressource erstellen können, können Sie mehrere Textur Typen als einzelne Textur in mehreren Shadern deklarieren. Beispielsweise können Sie ein **RWTexture3D** -Objekt als *tex* in einem Compute-Shader deklarieren und verwenden und dann ein **Texture3D** -Objekt als *tex* in einem Pixelshader deklarieren und verwenden.

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

 

 





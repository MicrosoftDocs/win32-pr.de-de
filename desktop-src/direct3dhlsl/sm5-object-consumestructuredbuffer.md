---
title: Consumestructuredbuffer
description: Ein Eingabepuffer, der als Stream angezeigt wird, aus dem der Shader Werte abrufen kann. Nur strukturierte Puffer können T-Typen annehmen, die Strukturen sind.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- Consumestructuredbuffer HLSL
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993598"
---
# <a name="consumestructuredbuffer"></a>Consumestructuredbuffer

Ein Eingabepuffer, der als Stream angezeigt wird, aus dem der Shader Werte abrufen kann. Nur strukturierte Puffer können T-Typen annehmen, die Strukturen sind.



| Methode                                                                    | BESCHREIBUNG                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [**Nutzen**](sm5-object-consumestructuredbuffer-consume.md)             | Entfernt einen Wert vom Ende des Puffers. |
| [**GetDimensions**](sm5-object-consumestructuredbuffer-getdimensions.md) | Ruft die Ressourcen Dimensionen ab.               |



 

Das an diese Ressource gebundene UAV-Format muss mit dem \_ unbekanntem DXGI-Format erstellt werden \_ .

Die an diese Ressource gebundene UAV muss mit dem D3D11- [**\_ Puffer- \_ UAV- \_ Flag " \_ Append**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)" erstellt werden.

Weitere Informationen über die Nutzung strukturierter Puffer finden Sie in beiden Abschnitten: [Anfügen und](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) Verwenden von Puffer und [strukturiertem Puffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

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

 

 
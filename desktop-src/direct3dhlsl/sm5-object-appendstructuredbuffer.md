---
title: Appendstructuredbuffer
description: Ausgabepuffer, der als Stream angezeigt wird, an den der Shader anfügen kann. Nur strukturierte Puffer können T-Typen annehmen, die Strukturen sind.
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- Appendstructuredbuffer HLSL
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c140052c861c8da3df6378fc3bc49816998c130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728185"
---
# <a name="appendstructuredbuffer"></a>Appendstructuredbuffer

Ausgabepuffer, der als Stream angezeigt wird, an den der Shader anfügen kann. Nur strukturierte Puffer können T-Typen annehmen, die Strukturen sind.



| Methode                                                                   | BESCHREIBUNG                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [**Anfügen**](sm5-object-appendstructuredbuffer-append.md)               | Fügt einen Wert an das Ende des Puffers an. |
| [**GetDimensions**](sm5-object-appendstructuredbuffer-getdimensions.md) | Ruft die Ressourcen Dimensionen ab.             |



 

Das an diese Ressource gebundene UAV-Format muss mit dem \_ unbekanntem DXGI-Format erstellt werden \_ .

Die an diese Ressource gebundene UAV muss mit dem D3D11- [**\_ Puffer- \_ UAV- \_ Flag " \_ Append**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)" erstellt werden.

Weitere Informationen zu einem strukturierteren Anfüge Puffer finden Sie in beiden Abschnitten: [Anfügen und](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) Verwenden von Puffer und [strukturiertem Puffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

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

 

 
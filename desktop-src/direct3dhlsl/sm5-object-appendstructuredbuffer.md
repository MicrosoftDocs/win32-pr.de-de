---
title: AppendStructuredBuffer
description: Ausgabepuffer, der als Stream angezeigt wird, an den der Shader angefügt werden kann. Nur strukturierte Puffer können T-Typen annehmen, die Strukturen sind.
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- AppendStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23efdb58b8effc0ccdaf32da31ad93dfaf8f6eae602c6769c947ffa0c0f505d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510109"
---
# <a name="appendstructuredbuffer"></a>AppendStructuredBuffer

Ausgabepuffer, der als Stream angezeigt wird, an den der Shader angefügt werden kann. Nur strukturierte Puffer können T-Typen annehmen, die Strukturen sind.



| Methode                                                                   | Beschreibung                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [**Anfügen**](sm5-object-appendstructuredbuffer-append.md)               | Fügt einen Wert an das Ende des Puffers an. |
| [**GetDimensions**](sm5-object-appendstructuredbuffer-getdimensions.md) | Ruft die Ressourcendimensionen ab.             |



 

Das an diese Ressource gebundene UAV-Format muss im FORMAT DXGI FORMAT UNKNOWN erstellt \_ \_ werden.

Die an diese Ressource gebundene UAV muss mit [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)erstellt worden sein.

Weitere Informationen zu einem strukturierten Puffer zum Anfügen finden Sie in beiden Abschnitten: [Anfügen und Nutzen](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) von Puffern und [strukturierten Puffern.](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)

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

 

 
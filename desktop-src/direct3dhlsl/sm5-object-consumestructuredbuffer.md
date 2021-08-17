---
title: ConsumeStructuredBuffer
description: Ein Eingabepuffer, der als Stream angezeigt wird, aus dem der Shader Werte pullen kann. Nur strukturierte Puffer können T-Typen verwenden, die Strukturen sind.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- ConsumeStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4e0530c98b78f9b18b0934874fb5a082779694ced2f171293d0a38dc458a08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986090"
---
# <a name="consumestructuredbuffer"></a>ConsumeStructuredBuffer

Ein Eingabepuffer, der als Stream angezeigt wird, aus dem der Shader Werte pullen kann. Nur strukturierte Puffer können T-Typen verwenden, die Strukturen sind.



| Methode                                                                    | Beschreibung                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [**Nutzen**](sm5-object-consumestructuredbuffer-consume.md)             | Entfernt einen Wert vom Ende des Puffers. |
| [**GetDimensions**](sm5-object-consumestructuredbuffer-getdimensions.md) | Ruft die Ressourcendimensionen ab.               |



 

Das an diese Ressource gebundene UAV-Format muss mit dem FORMAT DXGI \_ FORMAT \_ UNKNOWN erstellt werden.

Die an diese Ressource gebundene UAV muss mit [**D3D11 \_ BUFFER \_ UAV \_ FLAG APPEND erstellt \_ worden sein.**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)

Weitere Informationen zum Nutzen strukturierter Puffer finden [](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) Sie in beiden Abschnitten: Anfügen und Nutzen des Puffers und [des strukturierten Puffers.](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)

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

 

 
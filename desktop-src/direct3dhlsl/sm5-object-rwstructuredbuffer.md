---
title: Rwstructuredbuffer
description: Ein Lese-/Schreibpuffer, der einen T-Typ, der eine Struktur ist, annehmen kann.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- Rwstructuredbuffer HLSL
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390497"
---
# <a name="rwstructuredbuffer"></a>Rwstructuredbuffer

Ein Lese-/Schreibpuffer, der einen T-Typ, der eine Struktur ist, annehmen kann.



| Methode                                                                     | BESCHREIBUNG                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [**Dekrementcounter**](sm5-object-rwstructuredbuffer-decrementcounter.md) | Dekremente den ausgeblendeten Wert des Objekts. |
| [**GetDimensions**](sm5-object-rwstructuredbuffer-getdimensions.md)       | Ruft die Ressourcen Dimensionen ab.           |
| [**Incrementcounter**](sm5-object-rwstructuredbuffer-incrementcounter.md) | Erhöht den ausgeblendeten Wert des Objekts. |
| [**Laden**](rwstructuredbuffer-load.md)                                    | Liest Puffer Daten.                      |
| [**KOM\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)        | Gibt eine Ressourcen Variable zurück.            |



 

Eine Ressourcen Variable kann auch an einen ungeordneten oder Interlocked-Vorgang übermittelt werden.

Rwstructuredbuffer-Objekten kann die Speicher Klasse **globallycoherent** vorangestellt werden. Diese Speicher Klasse bewirkt, dass Speicherbarrieren und Synchronisierungen Daten über die gesamte GPU leeren, sodass andere Gruppen Schreibvorgänge sehen können. Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung nur eine UAV innerhalb der aktuellen Gruppe.

Das an diese Ressource gebundene UAV-Format muss mit dem \_ unbekanntem DXGI-Format erstellt werden \_ .

Weitere Informationen über [strukturierte Puffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)finden Sie im Übersichts Material.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieses Objekt wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Unterstützt |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Shader [Model 5](d3d11-graphics-reference-sm5.md) und höhere Shader-Modelle [Shader Model 4](dx-graphics-hlsl-sm4.md) (verfügbar über die Direct3D 11-API mithilfe der 10,0-oder 10,1-Featureebene ([**D3D \_ Feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) auf Geräten, die Compute-Shader unterstützen. Weitere Informationen zur Unterstützung von Compute-Shadern auf downlevelhardware finden Sie unter Compute-Shader [auf downlevelhardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)<br/> | ja       |



 

Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shader Model 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 


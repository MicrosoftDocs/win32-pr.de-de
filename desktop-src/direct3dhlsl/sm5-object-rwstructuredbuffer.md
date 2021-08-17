---
title: RWStructuredBuffer
description: Ein Lese-/Schreibpuffer, der einen T-Typ annehmen kann, der eine Struktur ist.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- RWStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58eacc277eac2d55aca0e6068698d11110768cfbe3ab6b564b97a0607715a7ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095150"
---
# <a name="rwstructuredbuffer"></a>RWStructuredBuffer

Ein Lese-/Schreibpuffer, der einen T-Typ annehmen kann, der eine Struktur ist.



| Methode                                                                     | BESCHREIBUNG                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [**DecrementCounter**](sm5-object-rwstructuredbuffer-decrementcounter.md) | Dekrement wird der ausgeblendete Zähler des Objekts. |
| [**GetDimensions**](sm5-object-rwstructuredbuffer-getdimensions.md)       | Ruft die Ressourcendimensionen ab.           |
| [**IncrementCounter**](sm5-object-rwstructuredbuffer-incrementcounter.md) | Erhöht den ausgeblendeten Zähler des Objekts. |
| [**Laden**](rwstructuredbuffer-load.md)                                    | Liest Pufferdaten.                      |
| [**Operator\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)        | Gibt eine Ressourcenvariable zurück.            |



 

Eine Ressourcenvariable kann auch an jeden ungeordneten oder interlocked-Vorgang übergeben werden.

RWStructuredBuffer-Objekten kann global die **Speicherklasse** vorangestellt werden. Diese Speicherklasse bewirkt Speicherbarrieren und Synchronisierungen, um Daten über die gesamte GPU zu leeren, sodass andere Gruppen Schreibvorgänge sehen können. Ohne diesen Spezifizierer leert eine Speicherbarriere oder Synchronisierung nur einen UAV innerhalb der aktuellen Gruppe.

Das an diese Ressource gebundene UAV-Format muss im FORMAT DXGI FORMAT UNKNOWN erstellt \_ \_ werden.

Weitere Informationen zu [strukturierten Puffern](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)finden Sie im Übersichtsmaterial.

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Unterstützt |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher [Shadermodelle ShaderModell 4](dx-graphics-hlsl-sm4.md) (verfügbar über die Direct3D 11-API mit 10.0- oder 10.1-Featureebene ([**D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) auf Geräten, die Compute-Shader unterstützen. Weitere Informationen zur Unterstützung von Compute-Shadern auf kompatibler Hardware finden Sie unter [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)<br/> | ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shadermodell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 


---
title: SV_DomainLocation
description: Definiert die Position auf der Hülle des aktuellen Domänenpunkts, der ausgewertet wird.
ms.assetid: 907f568c-7c45-41e5-96c4-6e6b816a4a53
keywords:
- SV_DomainLocation HLSL
topic_type:
- apiref
api_name:
- SV_DomainLocation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 481d4def3d13ee69138f31adaae3c7d90c2e27ab11702fe3191db94540d9835c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067530"
---
# <a name="sv_domainlocation"></a>SV \_ DomainLocation

Definiert die Position auf der Hülle des aktuellen Domänenpunkts, der ausgewertet wird.

## <a name="type"></a>Typ



| Typ       | Eingabetopologie               |
|--------|----------------|
| float2 | Quad Patch     |
| float3 | tri patch      |
| float2 | isoline        |



 

## <a name="remarks"></a>Hinweise

Dieser Systemwert ist erforderlich.

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      | x      |          |       |         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Semantik](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





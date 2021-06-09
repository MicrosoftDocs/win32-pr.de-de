---
title: SV_DomainLocation
description: Definiert den Speicherort auf der Hülle des aktuellen Domänenpunkts, der ausgewertet wird.
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
ms.openlocfilehash: fc39a71bcbfb6f3719ecfc7d0abe463a1fd127e4
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827049"
---
# <a name="sv_domainlocation"></a>SV \_ DomainLocation

Definiert den Speicherort auf der Hülle des aktuellen Domänenpunkts, der ausgewertet wird.

## <a name="type"></a>Typ



| Typ       | Eingabetopologie               |
|--------|----------------|
| float2 | Quad-Patch     |
| float3 | Tri Patch      |
| float2 | Isoline        |



 

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

 

 





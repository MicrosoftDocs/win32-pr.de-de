---
title: SV_InsideTessFactor
description: Definiert die Mosaikmenge innerhalb einer Patchoberfläche.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90d31aa6a11ce8e2bdd75ff1171705cc9b3de437
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826614"
---
# <a name="sv_insidetessfactor"></a>SV \_ InsideTessFactor

Definiert die Mosaikmenge innerhalb einer Patchoberfläche.

## <a name="type"></a>Typ



|  Typ          | Eingabetopologie               |
|------------|----------------|
| float \[ 2\] | Quad Patch     |
| float      | tri patch      |
| unused     | isoline        |



 

Mosaikfaktoren müssen als Array deklariert werden. sie können nicht in einen einzelnen Vektor gepackt werden.

## <a name="remarks"></a>Hinweise

Dieser Wert muss während der Patchkonst constant-Funktion des Hüllen-Shaders definiert werden.

Erforderlicher Ausgabewert für den Hüllen-Shader, wenn Quad- oder Tri-Patches verwendet werden. Dieser Wert ist eine erforderliche Eingabe für den Domänen-Shader, damit Die Hardware mit den Signaturen über den Mosaik-Shader übereinstimmen kann.

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Semantik](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





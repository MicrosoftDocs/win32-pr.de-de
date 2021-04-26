---
title: SV_InsideTessFactor
description: Definiert den Mosaikbetrag innerhalb einer Patchoberfläche.
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
ms.openlocfilehash: 4d047f7961868de020ac50ffce22b6ce02d078a5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996917"
---
# <a name="sv_insidetessfactor"></a>SV \_ InsideTessFactor

Definiert den Mosaikbetrag innerhalb einer Patchoberfläche.

## <a name="type"></a>Typ



|            |                |
|------------|----------------|
| Typ       | Eingabetopologie |
| float \[ 2\] | Quad-Patch     |
| float      | Tri Patch      |
| unused     | Isoline        |



 

Mosaikfaktoren müssen als Array deklariert werden. sie können nicht in einen einzelnen Vektor gepackt werden.

## <a name="remarks"></a>Hinweise

Dieser Wert muss während der Patchkonstantenfunktion des Hüllen-Shaders definiert werden.

Erforderlicher Ausgabewert für den Hüllen-Shader bei Verwendung von Quad- oder Tri-Patches. Dieser Wert ist eine erforderliche Eingabe für den Domänen-Shader, damit die Hardware mit den Signaturen über den Mosaikator übereinstimmt.

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Semantik](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





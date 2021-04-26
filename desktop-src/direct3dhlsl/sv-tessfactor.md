---
title: SV_TessFactor
description: Definiert den Mosaikbetrag an jedem Rand eines Patches.
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 808365fbcba4a1180c1838b94a6c098aa4c6f9ac
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999057"
---
# <a name="sv_tessfactor"></a>SV \_ TessFactor

Definiert den Mosaikbetrag an jedem Rand eines Patches.

## <a name="type"></a>Typ



|            |                |
|------------|----------------|
| Typ       | Eingabetopologie |
| float \[ 4\] | Quad-Patch     |
| float \[ 3\] | Tri Patch      |
| float \[ 2\] | Isoline        |



 

Mosaikfaktoren müssen als Array deklariert werden. sie können nicht in einen einzelnen Vektor gepackt werden.

## <a name="remarks"></a>Hinweise

Der Wert für den Mosaikfaktor muss während der Patchkonstantenfunktion des Hüllen-Shaders definiert werden.

Erforderlicher Ausgabewert für den Hüllen-Shader bei Verwendung von Quad- oder Tri-Patches. Dieser Wert ist auch ein erforderlicher Eingabewert für den Domänen-Shader, um die patchkonstanten Datensignaturen zwischen den Mosaikstufen abzugleichen.

Bei einer Isolinie ist der erste Wert in SV \_ TessFactor der Mosaikfaktor für die Liniendichte, der zweite Wert der Mosaikfaktor für Liniendetails.

### <a name="tri-patch-tessellation-factors"></a>Tri Patch Tessellation Factors

Die erste Komponente stellt den Mosaikfaktor für den u==0-Rand des Patches bereit. Die zweite Komponente stellt den Mosaikfaktor für den v==0-Rand des Patches bereit. Die dritte Komponente stellt den Mosaikfaktor für den w==0-Rand des Patches dar.

### <a name="quad-patch-tessellation-factors"></a>Quad Patch Tessellation Factors

Die erste Komponente stellt den Mosaikfaktor für den u==0-Rand des Patches dar. Die zweite Komponente stellt den Mosaikfaktor für den v==0-Rand des Patches dar. Die dritte Komponente stellt den Mosaikfaktor für den u==1-Rand des Patches dar. Die vierte Komponente stellt den Mosaikfaktor für den v==1-Rand des Patches dar. Die Reihenfolge der Ränder ist im Uhrzeigersinn, beginnend mit der Kante u==0, die die linke Seite des Patches ist, und von der v==0-Kante, die der obere Rand des Patches ist.

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

 

 





---
title: SV_TessFactor
description: Definiert die Mosaikmenge an jedem Rand eines Patches.
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
ms.openlocfilehash: 308034fe607283ef9f1213cca1cabb4a7229765e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118895"
---
# <a name="sv_tessfactor"></a>SV \_ TessFactor

Definiert die Mosaikmenge an jedem Rand eines Patches.

## <a name="type"></a>Typ



|  Typ          |  Eingabetopologie              |
|------------|----------------|
| float \[ 4\] | Quad Patch     |
| float \[ 3\] | tri patch      |
| float \[ 2\] | isoline        |



 

Mosaikfaktoren müssen als Array deklariert werden. sie können nicht in einen einzelnen Vektor gepackt werden.

## <a name="remarks"></a>Bemerkungen

Der Wert für den Mosaikfaktor muss während der Patchkonstationsfunktion des Hüllen-Shaders definiert werden.

Erforderlicher Ausgabewert für den Hüllen-Shader, wenn Quad- oder Tri-Patches verwendet werden. Dieser Wert ist auch ein erforderlicher Eingabewert für den Domänen-Shader, der mit den Patchkonstten-Datensignaturen zwischen den Mosaikstufen übereinstimmen soll.

Bei einer Isoline ist der erste Wert in SV TessFactor der Mosaikfaktor der Liniendichte, der zweite Wert ist der Mosaikfaktor für \_ Zeilendetails.

### <a name="tri-patch-tessellation-factors"></a>Tri Patch Tessellation Factors

Die erste Komponente stellt den Mosaikfaktor für den u==0-Rand des Patches dar. Die zweite Komponente stellt den Mosaikfaktor für den v==0-Rand des Patches dar. Die dritte Komponente stellt den Mosaikfaktor für den w==0-Rand des Patches dar.

### <a name="quad-patch-tessellation-factors"></a>Quad Patch Tessellation Factors

Die erste Komponente stellt den Mosaikfaktor für den u==0-Rand des Patches dar. Die zweite Komponente stellt den Mosaikfaktor für den v==0-Rand des Patches dar. Die dritte Komponente stellt den Mosaikfaktor für den u==1-Rand des Patches dar. Die vierte Komponente stellt den Mosaikfaktor für den v==1-Rand des Patches dar. Die Reihenfolge der Ränder ist im Uhrzeigersinn, beginnend mit der Kante u==0, die die linke Seite des Patches ist, und von der v==0-Kante, die der obere Rand des Patches ist.

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

 

 





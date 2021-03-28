---
title: SV_TessFactor
description: Definiert den Mosaik Betrag an jedem Rand eines Patches.
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
ms.openlocfilehash: 8fa49b19109985b590747098826199b33a32dd2d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976216"
---
# <a name="sv_tessfactor"></a>SV-Mosaik \_ Faktor

Definiert den Mosaik Betrag an jedem Rand eines Patches.

## <a name="type"></a>Typ



|            |                |
|------------|----------------|
| Typ       | Eingabe Topologie |
| float \[ 4\] | Quad-Patch     |
| float \[ 3\] | Tri-Patch      |
| float \[ 2\] | Isolation        |



 

Mosaik Faktoren müssen als Array deklariert werden. Sie können nicht in einen einzigen Vektor gepackt werden.

## <a name="remarks"></a>Bemerkungen

Der Wert für den Mosaik Faktor muss während der Patch-konstantenfunktion des Hull-Shaders definiert werden.

Erforderlicher Ausgabewert für den Hull-Shader bei Verwendung von Quad-oder Tri-Patches. Bei diesem Wert handelt es sich auch um einen erforderlichen Eingabe Wert für den Domänen-Shader, um die Daten Signaturen der patchkonstanten zwischen den Mosaik Stufen abzugleichen.

Bei einer Isolationsstufe ist der erste Wert in SV \_ Tess Factor der Mosaik Faktor für die Zeilen Dichte, der zweite Wert ist der Mosaik Faktor für die Zeilen Genauigkeit.

### <a name="tri-patch-tessellation-factors"></a>Drei Patch-Mosaik Faktoren

Die erste Komponente stellt den Tesselations Faktor für den u = = 0-Rand des Patches bereit. Die zweite Komponente stellt den Tesselations Faktor für den v = = 0-Rand des Patches bereit. Die dritte Komponente stellt den Tesselations Faktor für den w = = 0-Rand des Patches bereit.

### <a name="quad-patch-tessellation-factors"></a>Vier patchmosaik Faktoren

Die erste Komponente stellt den Tesselations Faktor für den u = = 0-Rand des Patches bereit. Die zweite Komponente stellt den Tesselations Faktor für den v = = 0-Rand des Patches bereit. Die dritte Komponente stellt den Tesselations Faktor für den u = = 1-Rand des Patches bereit. Die vierte Komponente stellt den Tesselations Faktor für den v = = 1-Rand des Patches bereit. Die Reihenfolge der Kanten ist im Uhrzeigersinn, beginnend ab dem "u = = 0"-Rand, der linken Seite des Patches und vom "v = = 0"-Rand, der am Anfang des Patches steht.

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Semantik](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





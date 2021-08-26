---
title: Register – gs_5_0
description: Die folgenden Eingabe- und Ausgaberegister werden in version 5 0 des Geometrie-Shaders \_ implementiert.
ms.assetid: 9E99F584-611F-4CFC-B69A-66F2B4545D36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e0bac8baf9be8428b53fa7949229361edf04132079a7a6ca6989dab92c44aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023500"
---
# <a name="registers---gs_5_0"></a>Register : gs \_ 5 \_ 0

Die folgenden Eingabe- und Ausgaberegister werden in version 5 0 des Geometrie-Shaders \_ implementiert.

## <a name="input-registers"></a>Eingaberegister



| Registertyp                                     | Anzahl              | R/W | Dimension         | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|---------------------------------------------------|--------------------|-----|-------------------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                 | 4096(r \# +x \# \[ n \] ) | R/W | 4                 | Nein               | Keine     | Ja          |
| 32-Bit Indexable Temp Array (x \# \[ n \] )            | 4096(r \# +x \# \[ n \] ) | R/W | 4                 | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe \[ (v-Scheitelpunktelement \] \[ \] )             | 32                 | R   | 4(comp) \* 32(vert) | Ja              | Keine     | Ja          |
| Primitive 32-Bit-Eingabe-ID (vPrim)                 | 1                  | R   | 1                 | Nein               | Keine     | Ja          |
| 32-Bit-Eingabeinstanz-ID (vInstanceID)            | 1                  | R   | 1                 | Nein               | Keine     | Ja          |
| Element in einer Eingaberessource (t \# )                | 128                | R   | 1                 | Nein               | Keine     | Ja          |
| Sampler (s \# )                                     | 16                 | R   | 1                 | Nein               | Keine     | Ja          |
| ConstantBuffer-Referenz (cb \# \[ index \] )          | 15                 | R   | 4                 | Ja (Inhalt)    | Keine     | Ja          |
| Direktverweis auf ConstantBuffer (icb \[ index \] ) | 1                  | R   | 4                 | Ja (Inhalt)    | Keine     | Ja          |



 

## <a name="output-registers"></a>Ausgaberegister



| Registertyp                                               | Anzahl | R/W | Dimension | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (Verwerfen des Ergebnisses, nützlich für Ops mit mehreren Ergebnissen) | Nicht zutreffend   | W   | Nicht zutreffend       | Nicht zutreffend              | –      | Nein           |
| 32-Bit-Ausgabe– Vertex Data-Element (o \# )                     | 32    | W   | Nicht zutreffend       | N/V              | 4        | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





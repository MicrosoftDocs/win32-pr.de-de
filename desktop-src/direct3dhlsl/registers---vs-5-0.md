---
title: Register – vs_5_0
description: Die folgenden Eingabe- und Ausgaberegister werden in Version 5 0 des Vertex-Shaders \_ implementiert.
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f9c80125a4640e558872e29e435d48e7420bbd6c504577a5e0c84781f8a47d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853900"
---
# <a name="registers---vs_5_0"></a>Registrierungen im Vergleich zu \_ 5 \_ 0

Die folgenden Eingabe- und Ausgaberegister werden in Version 5 0 des Vertex-Shaders \_ implementiert.

## <a name="input-registers"></a>Eingaberegister



| Registertyp                                      | Anzahl              | R/W | Dimension | Indizierbar von r\# | Standardeinstellungen | Erfordert DCL |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                  | 4096(r \# +x \# \[ n \] ) | R/W | 4         | Nein               | Keine     | Ja          |
| 32-Bit-indizierbares temporäres Array (x \# \[ n \] )             | 4096(r \# +x \# \[ n \] ) | R/W | 4         | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe (v \# )                                 | 32                 | R   | 4         | Ja              | Keine     | Ja          |
| Element in einer Eingaberessource (t \# )                 | 128                | R   | 1         | Nein               | Keine     | Ja          |
| Sampler (s \# )                                      | 16                 | R   | 1         | Nein               | Keine     | Ja          |
| ConstantBuffer-Referenz \# \[ (CB-Index \] )           | 15                 | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |
| iImmediate ConstantBuffer-Referenz (icb \[ index \] ) | 1                  | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |



 

## <a name="output-registers"></a>Ausgaberegister



| Registertyp                                                      | Anzahl | R/W | Dimension | Indizierbar von r\# | Standardeinstellungen | Erfordert DCL |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (Verwerfen des Ergebnisses, nützlich für Vorgänge mit mehreren Ergebnissen) | Nicht zutreffend   | W   | Nicht zutreffend       | Nicht zutreffend              | –      | Nein           |
| 32-Bit-Ausgabe Vertex-Datenelement (o \# )                            | 32    | W   | 4         | Nicht zutreffend              | –      | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





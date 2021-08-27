---
title: Register – ps_5_0
description: Die folgenden Eingabe- und Ausgaberegister werden in der Pixelshaderversion 5 \_ 0 implementiert.
ms.assetid: F16E5CB8-E1DB-48CD-8C20-DBF1DF971110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d432e53626d547bcaf421a4b4ffd9c2aa0f5d0a78ecc3aff9f0b87059c40c0ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095340"
---
# <a name="registers---ps_5_0"></a>Register – ps \_ 5 \_ 0

Die folgenden Eingabe- und Ausgaberegister werden in der Pixelshaderversion 5 \_ 0 implementiert.

## <a name="input-registers"></a>Eingaberegister



| Registertyp                                     | Anzahl              | R/W | Dimension | Indizierbar von r\# | Standardeinstellungen | Erfordert DCL |
|---------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                 | 4096(r \# +x \# \[ n \] ) | R/W | 4         | Nein               | Keine     | Ja          |
| 32-Bit-Indizierbares temporäres Array (x \# \[ n \] )            | 4096(r \# +x \# \[ n \] ) | R/W | 4         | Ja              | Keine     | Ja          |
| 32-Bit-Eingabeattribut (v \# )                      | 32                 | R   | 4         | Ja              | Keine     | Ja          |
| Element in einer Eingaberessource (t \# )                | 128                | R   | 1         | Nein               | Keine     | Ja          |
| Sampler (s \# )                                     | 16                 | R   | 1         | Nein               | Keine     | Ja          |
| ConstantBuffer-Referenz \# \[ (CB-Index \] )          | 15                 | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |
| Direkter ConstantBuffer-Verweis (icb \[ index \] ) | 1                  | R   | 4         | Ja (Inhalt)    | Keine     | Ja          |



 

## <a name="output-registers"></a>Ausgaberegister



| Registertyp                                                      | Anzahl                   | R/W | Dimension                                | Indizierbar von r\# | Standardeinstellungen | Erfordert DCL |
|--------------------------------------------------------------------|-------------------------|-----|------------------------------------------|------------------|----------|--------------|
| NULL (Verwerfen des Ergebnisses, nützlich für Vorgänge mit mehreren Ergebnissen) | Nicht zutreffend                     | W   | Nicht zutreffend                                      | Nicht zutreffend              | –      | Nein           |
| 32-Bit-Ausgabeelement (o \# )                                        | 8                       | W   | 4                                        | Nicht zutreffend              | –      | Nein           |
| Ungeordnete Zugriffsansicht (u \# )                                        | 8 \# – von Renderzielen | R/W | D3D11 \_ PS \_ CS \_ UAV \_ REGISTER \_ COMPONENTS | Nein               | Nein       | Ja          |
| 32-Bit \[ 0.0f.. 1,0f \] Float-Ausgabetiefe (oDepth)                  | 1                       | W   | 1                                        | Nicht zutreffend              | –      | Ja          |
| 32-Bit-UINT-Ausgabebeispielmaske (oMask)                             | 1                       | W   | 1                                        | Nicht zutreffend              | –      | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





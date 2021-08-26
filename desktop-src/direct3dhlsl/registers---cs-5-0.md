---
title: Register – cs_5_0
description: Die folgenden Eingabe- und Ausgaberegister werden in der Compute-Shaderversion 5 \_ 0 implementiert.
ms.assetid: A602BA9F-0934-472F-BB07-5E7A97763CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01d761fba2b126559e18caf7cf917482d83fec952798b80c3ffc756a5bf3418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023580"
---
# <a name="registers---cs_5_0"></a>Register : cs \_ 5 \_ 0

Die folgenden Eingabe- und Ausgaberegister werden in der Compute-Shaderversion 5 \_ 0 implementiert.

## <a name="input-registers"></a>Eingaberegister



| Registertyp                                        | Anzahl                                                  | R/W | Dimension                        | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|------------------------------------------------------|--------------------------------------------------------|-----|----------------------------------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                    | 4096(r \# +x \# \[ n \] )                                     | R/W | 4                                | Nein               | Keine     | Ja          |
| 32-Bit Indexable Temp Array (x \# \[ n \] )               | 4096(r \# +x \# \[ n \] )                                     | R/W | 4                                | Ja              | Keine     | Ja          |
| Gemeinsamer 32-Bit-Threadgruppenspeicher (g \# \[ n \] )         | 8192 (Summe aller shared memory decls für thread group) | R/W | 1 (kann auf verschiedene Weise deklariert werden) | Ja              | Keine     | Ja          |
| Element in einer Eingaberessource (t \# )                   | 128                                                    | R   | 1                                | Nein               | Keine     | Ja          |
| Sampler (s \# )                                        | 16                                                     | R   | 1                                | Nein               | Keine     | Ja          |
| ConstantBuffer-Referenz (cb \# \[ index \] )             | 15                                                     | R   | 4                                | Ja (Inhalt)   | Keine     | Ja          |
| Direktverweis auf ConstantBuffer (icb \[ index \] )    | 1                                                      | R   | 4                                | Ja (Inhalt)    | Keine     | Ja          |
| ThreadID (vThreadID.xyz)                             | 1                                                      | R   | 3                                | Nein               | –      | Ja          |
| ThreadGroupID (vThreadGroupID.xyz)                   | 1                                                      | R   | 3                                | Nein               | –      | Ja          |
| ThreadIDInGroup (vThreadIDInGroup.xyz)               | 1                                                      | R   | 3                                | Nein               | –      | Ja          |
| ThreadIDInGroupFlattened (vThreadIDInGroupFlattened) | 1                                                      | R   | 1                                | Nein               | –      | Ja          |



 

## <a name="output-registers"></a>Ausgaberegister



| Registertyp                                               | Anzahl | R/W | Dimension | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (Verwerfen des Ergebnisses, nützlich für Ops mit mehreren Ergebnissen) | Nicht zutreffend   | W   | Nicht zutreffend       | Nicht zutreffend              | –      | Nein           |
| Ungeordnete Zugriffsansicht (u \# )                                 | 8     | R/W | 1         | Nein               | Nein       | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





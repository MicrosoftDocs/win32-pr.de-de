---
title: Register-ds_5_0
description: Die folgenden Eingabe-und Ausgabe Register werden in der Domänen-Shader-Version 5 \_ 0 implementiert.
ms.assetid: 8AE00EC6-0BDC-4F63-B95C-FF434B98D7CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b787f4a1f7e647a49340d49796dc2986e442178f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311048"
---
# <a name="registers---ds_5_0"></a>Register-DS \_ 5 \_ 0

Die folgenden Eingabe-und Ausgabe Register werden in der Domänen-Shader-Version 5 \_ 0 implementiert.

## <a name="input-registers"></a>Eingabe Register



| Registriungstyp                                              | Anzahl                | R/W | Dimension                           | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|------------------------------------------------------------|----------------------|-----|-------------------------------------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                          | 4096 (r \# + x \# \[ n \] )   | R/W | 4                                   | Nein               | Keine     | Ja          |
| 32-Bit indizierbares temporäres Array (x \# \[ n \] )                     | 4096 (r \# + x \# \[ n \] )   | R/W | 4                                   | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe Steuerungs Punkte (VCP- \[ Vertex- \] \[ Element \] )     | 32 siehe Hinweis 1 unten. | R   | 4 (Komponente) \* 32 (Element) \* 32 (Vert) | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe Patch-Konstanten (VPC- \[ Scheitelpunkt \] )               | 32 siehe Hinweis 2 weiter unten. | R   | 4                                   | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe Speicherort in Domäne (vdomain. XY, vDomain.XYZ)) | 1                    | R   | 3                                   | Nein               | –      | Ja          |
| 32-Bit uint Eingabe primitiveid (vprim)                      | 1                    | R   | 1                                   | Nein               | –      | Ja          |
| -Element in einer Eingabe Ressource (t \# )                         | 128                  | R   | 128                                 | Ja              | Keine     | Ja          |
| Sampler (e \# )                                              | 16                   | R   | 1                                   | Ja              | Keine     | Ja          |
| iconstantbuffer-Referenz (CB- \# \[ Index \] )                  | 15                   | R   | 4                                   | Ja              | Keine     | Ja          |
| iimmediate constantbuffer-Referenz (ICB- \[ Index \] )         | 1                    | R   | 4                                   | Ja (Inhalt)    | Keine     | Ja          |



 

**Hinweis 1:** Der Domänen-Shader sieht die Hull-shaderausgaben in zwei separaten Register Sätzen. Die VCP-Register können alle Ausgabe Steuerungs Punkte des Hull-Shader anzeigen. Die VPC-Register können alle Ausgabedaten der patchkonstante des Hull-Shader anzeigen.

**Hinweis 2:** Da der Code für den Hull-Shader das Patchen konstanter Verzweigungen oder joinphasen mit Namen wie z. b. SV \_ Tess Factor ausgibt, muss der Domänen-Shader diese Deklarationen auf der entsprechenden VPC-Eingabe abgleichen, wenn diese Werte angezeigt werden sollen.

## <a name="output-registers"></a>Ausgabe Register



| Registriungstyp                           | Anzahl | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Ausgabe-Vertex-Daten Element (o \# ) | 32    | W   | 4         | Ja              | Keine     | Ja          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





---
title: Register – hs_5_0
description: 'Ein Hüllen-Shader besteht aus drei unterschiedlichen Phasen: Kontrollpunktphase, Forkphase und Joinphase. Jede Phase verfügt über eigene Sätze von Eingabe- und Ausgaberegistern.'
ms.assetid: 82F689EF-D3F4-40B5-9A2C-1F97F4CE6501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3891130b4a952cb991615dbcc386e245d5eb8abedc2d8cec0b441eb6b3c2fbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854030"
---
# <a name="registers---hs_5_0"></a>Register – hs \_ 5 \_ 0

Ein Hüllen-Shader besteht aus drei unterschiedlichen Phasen: Kontrollpunktphase, Forkphase und Joinphase. Jede Phase verfügt über eigene Sätze von Eingabe- und Ausgaberegistern.

## <a name="control-point-phase"></a>Kontrollpunktphase

Die \_ \_ hs-Steuerungspunktphase \_ ist ein Shaderprogramm mit dem folgenden Registermodell.

### <a name="input-registers"></a>Eingaberegister



| Registertyp                                     | Anzahl                 | R/W | Dimension | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|---------------------------------------------------|-----------------------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                 | 4096(r \# +x \# \[ n \] )    | R/W | 4         | Nein               | Keine     | Ja          |
| Indizierbares 32-Bit-Temp Array (x \# \[ n \] )            | 4096(r \# +x \# \[ n \] )    | R/W | 4         | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe \[ (v-Scheitelpunktelement \] \[ \] )             | 32(element) \* 32(vert) | R   | 4         | Ja              | Keine     | Ja          |
| 32-Bit-UINT-Eingabe vOutputControlPointID(23.7)     | 1                     | R   | 1         | Nein               | Keine     | Ja          |
| 32-Bit-UINT-EingabeprimitiveID (vPrim)             | 1                     | R   | 1         | Nein               | –      | Ja          |
| Element in einer Eingaberessource (t \# )                | 128                   | R   | 128       | Ja              | Keine     | Ja          |
| Sampler (s \# )                                     | 16                    | R   | 1         | Ja              | Keine     | Ja          |
| ConstantBuffer-Referenz (cb \# \[ index \] )          | 15                    | R   | 4         | Ja              | Keine     | Ja          |
| Direktverweis auf ConstantBuffer (icb \[ index \] ) | 1                     | R   | 4         | Ja (Inhalt)   | Keiner     | Ja          |



 

### <a name="output-registers"></a>Ausgaberegister



| Registertyp                           | Anzahl | R/W | Dimension | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Ausgabe– Vertex Data-Element (o \# ) | 32    | W   | 4         | Ja              | Keine     | Ja          |



 

Jedes Ausgaberegister für die Hüllen-Shader-Kontrollpunktphase ist bis zu einem 4-Vektor, von dem bis zu 32 Register deklariert werden können. Es werden auch 1 bis 32 Ausgabekontrollpunkte deklariert, wodurch die erforderliche Speichermenge skaliert wird. Betrachten wir die maximal zulässige Aggregatanzahl von Skalaren in der gesamten Ausgabe der Hüllen-Shader-Kontrollpunkt-Phase als \# maximale \_ \_ CP-Ausgabe.

\#cp \_ output max = \_ 3968 Skalar.

Dieser Grenzwert basiert hier auf einem Entwurfspunkt für bestimmte Hardware mit 4096 \* 32-Bit-Speicher. Die Ausgabemenge für den Kontrollpunkt beträgt 3968 =4096-128. Dies ist 32(Kontrollpunkte) \* 4(Komponenten) \* 32(Elemente) - 4(Komponenten) \* 32(Elemente). Die Subtraktion reserviert 128 Skalaren (einen Kontrollpunkt) Speicherplatz, der für phase 2 und 3 des Hüllen-Shaders reserviert ist. Die Wahl, 128 Skalar für Patchkonst constants zu reservieren , anstatt zu erlauben, dass die Menge einfach den 4096-Skalaren des Speichers beträgt, die von Ausgabekontrollpunkten nicht verwendet wird, ist die Grenze eines anderen bestimmten Hardwareentwurfs. Die Kontrollpunktphase kann 32 Ausgabekontrollpunkte deklarieren, aber sie können nicht vollständig 32 Elemente mit jeweils 4 Komponenten sein, da der Gesamtspeicher zu hoch wäre.

## <a name="fork-phase"></a>Forkphase

Die folgenden Register sind im hs \_ fork-Phasenmodell \_ sichtbar.

Die folgenden Eingaberessourcen (t), Sampler (s), konstanten Puffer (cb) und unmittelbar konstanter Puffer (icb) sind alle mit allen anderen \# Hüllen-Shaderphasen \# gemeinsam \# genutzt. Das heißt, dass der Hüllen-Shader aus API-/DDI-Sicht für alle Phasen über einen einzelnen Satz von Eingaberessourcenstatus verfügt. Dies geht mit der Tatsache ein, dass der Hüllen-Shader aus API-/DDI-Sicht ein einzelner atomarer Shader ist. Die Phasen in diesem Sind Implementierungsdetails.

### <a name="input-registers"></a>Eingaberegister



| Registertyp                                                                         | Anzahl              | R/W | Dimension                           | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|---------------------------------------------------------------------------------------|--------------------|-----|-------------------------------------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                                                     | 4096(r \# +x \# \[ n \] ) | R/W | 4                                   | Nein               | Keine     | Ja          |
| Indizierbares 32-Bit-Temp Array (x \# \[ n \] )                                                | 4096(r \# +x \# \[ n \] ) | R/W | 4                                   | Ja              | Keine     | Ja          |
| 32-Bit-Eingabekontrollpunkte (Scheitelpunktelement \[ \] \[ \] ) (Phase vor der Steuerung)     | 32 Siehe Hinweis unten  | R   | 4(Component) \* 32(element) \* 32(vert) | Ja              | Keine     | Ja          |
| 32-Bit-Ausgabekontrollpunkte (vocp \[ \] \[ vertex-Element \] \] ) (Phase nach der Steuerungspunkt) | 32 Siehe Hinweis unten  | R   | 4(Component) \* 32(element) \* 32(vert) | Ja              | Keine     | Ja          |
| 32-Bit-UINT-EingabeprimitiveID (vPrim)                                                 | 1                  | R   | 1                                   | Nein               | –      | Ja          |
| 32-Bit UINT Input ForkInstanceID(23.8) (vForkInstanceID)                              | 1                  | R   | 1                                   | Nein               | –      | Ja          |
| Element in einer Eingaberessource (t \# )                                                    | 128                | R   | 128                                 | Ja              | Keine     | Ja          |
| Sampler (s \# )                                                                         | 16                 | R   | 1                                   | Ja              | Keine     | Ja          |
| ConstantBuffer-Referenz (cb \# \[ index \] )                                              | 15                 | R   | 4                                   | Ja              | Keine     | Ja          |
| Direktverweis auf ConstantBuffer (icb \[ index \] )                                     | 1                  | R   | 4                                   | Ja (Inhalt)   | Keiner     | Ja          |



 

> [!Note]
> Die Deklarationen des Eingangskontrollpunktregisters (Control Point Register, Deklarationen) der Hüllen-Shader-Forkphase müssen eine beliebige Teilmenge der Eingangs- (Vorkontrollpunktphase) der Hüllen-Shader-Kontrollpunkt-Eingabe \[ \] sein. Ebenso müssen die Deklarationen für die Eingabe der Ausgabekontrollpunkte (vocp) eine beliebige Teilmenge der Ausgabekontrollpunkte des Hüllen-Shaders (Phase nach der Steuerungspunkt) entlang der Elementachse \[ \] sein.
> 
> Entlang der Scheitelpunktachse muss die Anzahl der Steuerpunkte, die für die einzelnen Bzw. vocp gelesen werden sollen, auf ähnliche Weise eine Teilmenge der Anzahl der Eingangskontrollpunkte des Hüllen-Shaders bzw. der Anzahl der Ausgabekontrollpunkte des Hüllen-Shaders \[ \] sein. Wenn beispielsweise die Scheitelpunktachse der vocp-Register mit n Scheitelpunkten deklariert wird, werden die Ausgabekontrollpunkte der Kontrollpunktphase 0..n-1 als schreibgeschützte Eingabe für die \[ \] Forkphase verfügbar.

### <a name="output-registers"></a>Ausgaberegister



| Registrieren                                        | Anzahl               | R/W | Dimension | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|-------------------------------------------------|---------------------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Ausgabeelement "Patch Constant Data" (o \# ) | 32 Siehe Hinweis 1 unten | W   | 4         | Ja              | Keine     | Ja          |



 

> [!Note]  
> Die Ausgaben für den Hüllen-Shader fork und die Joinphase sind ein gemeinsamer Satz von vier Registern mit vier Vektoren. Die Ausgaben der einzelnen Fork- oder Joinphasenprogramme dürfen sich nicht überlappen. Vom System interpretierte Werte wie TessFactors stammen aus diesem Bereich.

## <a name="join-phase"></a>Einbindungsphase

Die folgenden Register sind im \_ hs-Joinphasenmodell \_ sichtbar. Es gibt drei Sätze von Eingaberegistern: Kontrollpunkt-Phasen-Eingabesteuerungspunkte (Control Point Phase Control Points,Cp), VoCP-Steuerungspunkt-Phasen-Ausgabekontrollpunkte (vocp) und Patchkonst constants (vcp). vpc ist die aggregierte Ausgabe aller Hüllen-Shader-Forkphasenprogramme. Die Ausgabe der Hüllen-Shader-Joinphase o registers befindet sich im gleichen Registerbereich wie die Ausgaben der \# Hüllen-Shader-Forkphase.

Die folgenden Eingaberessourcen (t), Sampler (s), konstanten Puffer (cb) und unmittelbar konstanter Puffer (icb) sind alle mit allen anderen \# Hüllen-Shaderphasen \# gemeinsam \# genutzt. Das heißt, dass der Hüllen-Shader aus API-/DDI-Sicht für alle Phasen über einen einzelnen Satz von Eingaberessourcenstatus verfügt. Dies geht mit der Tatsache ein, dass der Hüllen-Shader aus API-/DDI-Sicht ein einzelner atomarer Shader ist. Die Phasen in diesem Sind Implementierungsdetails.

### <a name="input-registers"></a>Eingaberegister



| Registertyp                                                                       | Anzahl               | R/W | Dimension                           | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|-------------------------------------------------------------------------------------|---------------------|-----|-------------------------------------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                                                   | 4096(r \# +x \# \[ n \] )  | R/W | 4                                   | Nein               | Keine     | Ja          |
| Indizierbares 32-Bit-Temp Array (x \# \[ n \] )                                              | 4096(r \# +x \# \[ n \] )  | R/W | 4                                   | Ja              | Keine     | Ja          |
| 32-Bit-Eingabekontrollpunkte (Scheitelpunktelement \[ \] \[ \] ) (Phase vor der Steuerung)   | 32 Siehe Hinweis 1 unten | R   | 4(Component) \* 32(element) \* 32(vert) | Ja              | Keine     | Ja          |
| 32-Bit-Ausgabekontrollpunkte (vocp \[ \] \[ vertex-Element \] ) (Phase nach der Steuerungspunkt) | 32 Siehe Hinweis 1 unten | R   | 4(Component) \* 32(element) \* 32(vert) | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe \[ (vpc-Element \] ) (Patchkonst constant data)                                 | 32 Siehe Hinweis 2 unten | R   | 4                                   | Ja              | Keine     | Ja          |
| 32-Bit-UINT-EingabeprimitiveID (vPrim)                                               | 1                   | R   | 1                                   | Nein               | –      | Ja          |
| 32-Bit-UINT-EingabejoinstanceID (vJoinInstanceID)                                  | 1                   | R   | 1                                   | Nein               | –      | Ja          |
| Element in einer Eingaberessource (t \# )                                                  | 128                 | R   | 128                                 | Ja              | Keine     | Ja          |
| Sampler (s \# )                                                                       | 16                  | R   | 1                                   | Ja              | Keine     | Ja          |
| ConstantBuffer-Referenz (cb \# \[ index \] )                                            | 15                  | R   | 4                                   | Ja              | Keine     | Ja          |
| Direktverweis auf ConstantBuffer (icb \[ index \] )                                   | 1                   | R   | 4                                   | Ja (Inhalt)   | Keiner     | Ja          |



 

**Hinweis 1:** Die Deklarationen des Eingabekontrollpunktregisters (Control Point Register, Deklarationen) der Hüllen-Shader-Joinphase müssen eine beliebige Teilmenge der Eingangs- (Vorkontrollpunktphase) der Hüllen-Shader-Kontrollpunkt-Eingabe \[ \] sein. Ebenso müssen die Deklarationen für die Eingabe der Ausgabekontrollpunkte (vocp) eine beliebige Teilmenge der Ausgabekontrollpunkte des Hüllen-Shaders (Phase nach der Steuerungspunkt) entlang der Elementachse \[ \] sein.

Entlang der Scheitelpunktachse muss die Anzahl der Steuerpunkte, die für die einzelnen Bzw. vocp gelesen werden sollen, auf ähnliche Weise eine Teilmenge der Anzahl der Eingangskontrollpunkte des Hüllen-Shaders bzw. der Anzahl der Ausgabekontrollpunkte des Hüllen-Shaders \[ \] sein. Wenn beispielsweise die Scheitelpunktachse der vocp-Register mit n Scheitelpunkten deklariert wird, werden die Ausgabekontrollpunkte der Kontrollpunktphase \[ 0..n-1 als schreibgeschützte Eingabe für die Joinphase \] verfügbar.

**Hinweis 2:** Zusätzlich zur Steuerungspunkteingabe werden in der Hüllen-Shader-Joinphase auch die Von den Hüllen-Shader-Forkphasenprogrammen berechneten Patchkonstanzdaten als Eingabe betrachtet. Dies wird in der Hüllen-Shader-Fork-Phase als vpc-Register \# gezeigt. Die VPC-Eingaberegister der Hüllen-Shader-Joinphase verwenden denselben Registerbereich wie die \# Hüllen-Shader-Forkphasenausgabe o \# registers. Die Deklarationen der o-Register dürfen sich nicht mit einem Hüllen-Shader-Fork-Phasesprogramm o Ausgabedeklaration überschneiden. Die Hüllen-Shader-Joinphase wird der aggregierten Patchkonst constant data-Ausgabe für den Hüllen-Shader \# \# hinzugefügt.

### <a name="output-registers"></a>Ausgaberegister



| Registertyp                                   | Anzahl             | R/W | Dimension | Indizierbar durch r\# | Standardeinstellungen | Erfordert DCL |
|-------------------------------------------------|-------------------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Ausgabeelement "Patch Constant Data" (o \# ) | 32 Siehe Hinweis unten | W   | 4         | Ja              | Keine     | Ja          |



 

> [!Note]  
> Die Ausgaben für den Hüllen-Shader fork und die Joinphase sind ein gemeinsamer Satz von vier Registern mit vier Vektoren. Die Ausgaben der einzelnen Fork- oder Joinphasenprogramme dürfen sich nicht überlappen. Vom System interpretierte Werte wie TessFactors stammen aus diesem Bereich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





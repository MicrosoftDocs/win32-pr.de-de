---
title: Register-hs_5_0
description: Ein Hull-Shader besteht aus drei verschiedenen Phasen, der Steuerungspunkt Phase, der Verzweigungs Phase und der joinphase. Jede Phase verfügt über eigene Sätze von Eingabe-und Ausgabe Registern.
ms.assetid: 82F689EF-D3F4-40B5-9A2C-1F97F4CE6501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aca1377c7ca6b56434c361ba06b01cf659319f6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351898"
---
# <a name="registers---hs_5_0"></a>Register-HS \_ 5 \_ 0

Ein Hull-Shader besteht aus drei verschiedenen Phasen: Steuerungspunkt Phase, Verzweigungs Phase und joinphase. Jede Phase verfügt über eigene Sätze von Eingabe-und Ausgabe Registern.

## <a name="control-point-phase"></a>Steuerungspunkt Phase

Die HS- \_ Steuerungs \_ Punkt \_ Phase ist ein Shader-Programm mit dem folgenden Register Modell.

### <a name="input-registers"></a>Eingabe Register



| Registriungstyp                                     | Anzahl                 | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|---------------------------------------------------|-----------------------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                 | 4096 (r \# + x \# \[ n \] )    | R/W | 4         | Nein               | Keine     | Ja          |
| 32-Bit indizierbares temporäres Array (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] )    | R/W | 4         | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe (v- \[ Vertex- \] \[ Element \] )             | 32 (-Element) \* 32 (Vert) | R   | 4         | Ja              | Keine     | Ja          |
| 32-Bit uint-Eingabe voutputcontrolpointid (23,7)     | 1                     | R   | 1         | Nein               | Keine     | Ja          |
| 32-Bit uint Eingabe primitiveid (vprim)             | 1                     | R   | 1         | Nein               | –      | Ja          |
| -Element in einer Eingabe Ressource (t \# )                | 128                   | R   | 128       | Ja              | Keine     | Ja          |
| Sampler (e \# )                                     | 16                    | R   | 1         | Ja              | Keine     | Ja          |
| Constantbuffer-Verweis (CB- \# \[ Index \] )          | 15                    | R   | 4         | Ja              | Keine     | Ja          |
| Sofortiger constantbuffer-Verweis (ICB- \[ Index \] ) | 1                     | R   | 4         | Ja (Inhalt)   | Keine     | Ja          |



 

### <a name="output-registers"></a>Ausgabe Register



| Registriungstyp                           | Anzahl | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Ausgabe-Vertex-Daten Element (o \# ) | 32    | W   | 4         | Ja              | Keine     | Ja          |



 

Jedes Hull-Shader-Steuerelement Punkt-Phasen-Ausgabe Register ist bis zu einem 4-Vektor, von dem bis zu 32 Register deklariert werden können. Außerdem sind zwischen 1 und 32 Ausgabe Steuerungs Punkte deklariert, die die erforderliche Speichermenge skalieren. Wir verweisen auf die maximal zulässige Anzahl von skalaren in allen Hull-Shader-Steuerungspunkt-Phasen Ausgabe als \# CP \_ Output \_ Max.

\#CP \_ Output \_ Max = 3968 Skalars.

Dieser Grenzwert basiert auf einem Entwurfspunkt für bestimmte Hardware des 4096 \* 32-Bit-Speichers. Der Betrag für die Kontrollpunkt Ausgabe ist 3968 = 4096-128, d. h. 32 (Kontrollpunkte) \* 4 (Komponenten) \* 32 (Elemente)-4 (Komponenten) \* 32 (Elemente). Die Subtraktion reserviert 128 skalare (ein Steuerungspunkt), die für die Hull-Shader-Phase 2 und 3 reserviert sind. Die Wahl der Reservierung von 128-skalaren für Patch-Konstanten, anstatt zuzulassen, dass der Betrag einfach nur von den 4096-Skaren des Speichers verwendet wird, wird von den Ausgabe Steuerungs Punkten nicht verwendet, sondern die Grenzwerte eines anderen bestimmten Hardware Entwurfs. In der Steuerungspunkt Phase können 32-Ausgabe Steuerungs Punkte deklariert werden, Sie können jedoch nur vollständig 32-Elemente mit jeweils vier Komponenten sein, da der gesamte Speicher zu hoch wäre.

## <a name="fork-phase"></a>Verzweigungs Phase

Die folgenden Register sind im HS- \_ Verzweigungs \_ Phasenmodell sichtbar.

Die folgenden Eingabe Ressourcen (t \# ), Samplern \# , Konstante Puffer (CB \# ) und unmittelbarer konstanter Puffer (ICB) sind mit allen anderen Hull-Shader-Phasen gemeinsam. Aus der API/DDI-Sicht hat der Hull-Shader also einen einzelnen Satz von Eingabe Ressourcen Status für alle Phasen. Dies hat zur Folge, dass der Hull-Shader aus der API/DDI-Sicht ein einzelner atomarischer Shader ist. die darin enthaltenen Phasen sind Implementierungsdetails.

### <a name="input-registers"></a>Eingabe Register



| Registriungstyp                                                                         | Anzahl              | R/W | Dimension                           | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|---------------------------------------------------------------------------------------|--------------------|-----|-------------------------------------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                                                     | 4096 (r \# + x \# \[ n \] ) | R/W | 4                                   | Nein               | Keine     | Ja          |
| 32-Bit indizierbares temporäres Array (x \# \[ n \] )                                                | 4096 (r \# + x \# \[ n \] ) | R/W | 4                                   | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe Steuerungs Punkte (vicp- \[ Vertex- \] \[ Element \] ) (Pre-Control Point-Phase)     | 32 siehe Hinweis unten  | R   | 4 (Komponente) \* 32 (Element) \* 32 (Vert) | Ja              | Keine     | Ja          |
| 32-Bit-Ausgabe Steuerungs Punkte (vocp- \[ Vertex- \] \[ Element \] \] ) (Post-Steuerungspunkt Phase) | 32 siehe Hinweis unten  | R   | 4 (Komponente) \* 32 (Element) \* 32 (Vert) | Ja              | Keine     | Ja          |
| 32-Bit uint Eingabe primitiveid (vprim)                                                 | 1                  | R   | 1                                   | Nein               | –      | Ja          |
| 32-Bit uint Input forkinstanceid (23,8) (vforkinstanceid)                              | 1                  | R   | 1                                   | Nein               | –      | Ja          |
| -Element in einer Eingabe Ressource (t \# )                                                    | 128                | R   | 128                                 | Ja              | Keine     | Ja          |
| Sampler (e \# )                                                                         | 16                 | R   | 1                                   | Ja              | Keine     | Ja          |
| Constantbuffer-Verweis (CB- \# \[ Index \] )                                              | 15                 | R   | 4                                   | Ja              | Keine     | Ja          |
| Sofortiger constantbuffer-Verweis (ICB- \[ Index \] )                                     | 1                  | R   | 4                                   | Ja (Inhalt)   | Keine     | Ja          |



 

> [!Note]
> Die Typdeklarationen der Eingabe Steuerungspunkt Registrierung (vicp) der Hull-Shader-Verzweigungs Phase müssen auf der Element Achse eine beliebige Teilmenge \[ \] der Eingabe für den Hull-Shader-Steuerungspunkt (Pre-Control Point Phase) sein. Auf ähnliche Weise müssen die Deklarationen zum Einfügen der Ausgabe Steuerungs Punkte (vocp) jede Teilmenge (entlang der \[ Element \] Achse) der Hull-Shader-Ausgabe Steuerungs Punkte (Post-Control Point Phase) sein.
> 
> Entlang der \[ \] vertexachse muss die Anzahl der zu lesenden Steuerungs Punkte für die einzelnen vicp-und vocp-Elemente auf ähnliche Weise eine Teilmenge der Anzahl der Eingabe Kontrollpunkte des Hull-Shaders und der Anzahl der leaseshaderausgabesteuerungspunkte sein. Wenn z. b. die vertexachse der vocp-Register mit n Scheitel Punkten deklariert wird, ist die Ausgabe Steuerung der Steuer Punkt Phase \[ 0.. n-1 \] als schreibgeschützte Eingabe für die Verzweigungs Phase verfügbar.

### <a name="output-registers"></a>Ausgabe Register



| Register                                        | Anzahl               | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|-------------------------------------------------|---------------------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Ausgabe Patch-Konstante Daten Element (o \# ) | 32 siehe Hinweis 1 unten | W   | 4         | Ja              | Keine     | Ja          |



 

> [!Note]  
> Die Hull-Shader-Verzweigung und die joinphasen Ausgaben sind ein gemeinsam genutzter Satz von 4 4-Vektor Registern. Die Ausgaben der einzelnen Verzweigungen oder joinphasen können einander nicht überlappen. Vom System interpretierte Werte, wie z. b. "ttierfactors", kommen in diesem Bereich.

## <a name="join-phase"></a>Einbindungsphase

Die folgenden Register sind im HS Join- \_ \_ Phasenmodell sichtbar. Es gibt drei Sätze von Eingabe Registern: eingabesteuerungspunkte in der Steuerungspunkt-Phase (vicp), vocp-Steuerungs Punkte (vocp) und Patch-Konstanten (VCP). VPC sind die aggregierte Ausgabe aller umlaufungsprogramme der Hull-shaderverzweigung. Die \# Registrierungs Registrierungsstellen-Registrierungs Registrierungsstellen-Registrierungsstellen befinden sich in demselben Register Bereich wie die verlaufungs-stagingphasen der hulll-Shader.

Die folgenden Eingabe Ressourcen (t \# ), Samplern \# , Konstante Puffer (CB \# ) und unmittelbarer konstanter Puffer (ICB) sind mit allen anderen Hull-Shader-Phasen gemeinsam. Aus der API/DDI-Sicht hat der Hull-Shader also einen einzelnen Satz von Eingabe Ressourcen Status für alle Phasen. Dies hat zur Folge, dass der Hull-Shader aus der API/DDI-Sicht ein einzelner atomarischer Shader ist. die darin enthaltenen Phasen sind Implementierungsdetails.

### <a name="input-registers"></a>Eingabe Register



| Registriungstyp                                                                       | Anzahl               | R/W | Dimension                           | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|-------------------------------------------------------------------------------------|---------------------|-----|-------------------------------------|------------------|----------|--------------|
| 32-Bit-Temp (r \# )                                                                   | 4096 (r \# + x \# \[ n \] )  | R/W | 4                                   | Nein               | Keine     | Ja          |
| 32-Bit indizierbares temporäres Array (x \# \[ n \] )                                              | 4096 (r \# + x \# \[ n \] )  | R/W | 4                                   | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe Steuerungs Punkte (vicp- \[ Vertex- \] \[ Element \] ) (Pre-Control Point-Phase)   | 32 siehe Hinweis 1 unten | R   | 4 (Komponente) \* 32 (Element) \* 32 (Vert) | Ja              | Keine     | Ja          |
| 32-Bit-Ausgabe Steuerungs Punkte (vocp- \[ Vertex- \] \[ Element \] ) (Post-Steuerungspunkt Phase) | 32 siehe Hinweis 1 unten | R   | 4 (Komponente) \* 32 (Element) \* 32 (Vert) | Ja              | Keine     | Ja          |
| 32-Bit-Eingabe (VPC- \[ Element \] ) (Patch-Konstante Daten)                                 | 32 siehe Hinweis 2 unten | R   | 4                                   | Ja              | Keine     | Ja          |
| 32-Bit uint Eingabe primitiveid (vprim)                                               | 1                   | R   | 1                                   | Nein               | –      | Ja          |
| 32-Bit uint Input joininstanceid (vjoininstanceid)                                  | 1                   | R   | 1                                   | Nein               | –      | Ja          |
| -Element in einer Eingabe Ressource (t \# )                                                  | 128                 | R   | 128                                 | Ja              | Keine     | Ja          |
| Sampler (e \# )                                                                       | 16                  | R   | 1                                   | Ja              | Keine     | Ja          |
| Constantbuffer-Verweis (CB- \# \[ Index \] )                                            | 15                  | R   | 4                                   | Ja              | Keine     | Ja          |
| Sofortiger constantbuffer-Verweis (ICB- \[ Index \] )                                   | 1                   | R   | 4                                   | Ja (Inhalt)   | Keine     | Ja          |



 

**Hinweis 1:** Die Typdeklarationen der Eingabe Steuerungspunkt Registrierung (vicp) des Hull-Shader-Joins müssen eine beliebige Teilmenge auf der \[ Element \] Achse der Hull-Shader-Steuerungspunkt Eingabe (Pre-Control Point Phase) sein. Auf ähnliche Weise müssen die Deklarationen zum Einfügen der Ausgabe Steuerungs Punkte (vocp) jede Teilmenge (entlang der \[ Element \] Achse) der Hull-Shader-Ausgabe Steuerungs Punkte (Post-Control Point Phase) sein.

Entlang der \[ \] vertexachse muss die Anzahl der zu lesenden Steuerungs Punkte für die einzelnen vicp-und vocp-Elemente auf ähnliche Weise eine Teilmenge der Anzahl der Eingabe Kontrollpunkte des Hull-Shaders und der Anzahl der leaseshaderausgabesteuerungspunkte sein. Wenn z. b. die vertexachse der vocp-Register mit n Scheitel Punkten deklariert wird, ist die Ausgabe Steuerung der Steuer Punkt Phase \[ 0.. n-1 \] als schreibgeschützte Eingabe für die joinphase verfügbar.

**Hinweis 2:** Zusätzlich zur Steuerungspunkt Eingabe sieht die Umstellungsphase des Hull-Shaders auch als Eingabe die von den Hull-Shader-Verzweigungs Phasen (en) berechneten Patch-Konstanten Daten an. Dies wird in der Hull-Shader-Verzweigungs Phase angezeigt, wenn der VPC \# registriert wird. Die Eingabe-VPC-Registrierungsphase der Hull-Shader-Verknüpfung hat \# denselben Register Bereich wie die Registrierungs-shaderphase der Hull-Shader-Verzweigung \# . Die Deklarationen der o- \# Register dürfen sich nicht mit der Ausgabe Deklaration der Hull-Shader-Verzweigungs Phase überschneiden \# . die joinphase des Hull-Shaders fügt der Aggregatdaten Ausgabe für den Hull-Shader hinzu.

### <a name="output-registers"></a>Ausgabe Register



| Registriungstyp                                   | Anzahl             | R/W | Dimension | Indizierbar durch r\# | der Arbeitszeittabelle | Erfordert DCL |
|-------------------------------------------------|-------------------|-----|-----------|------------------|----------|--------------|
| 32-Bit-Ausgabe Patch-Konstante Daten Element (o \# ) | 32 siehe Hinweis unten | W   | 4         | Ja              | Keine     | Ja          |



 

> [!Note]  
> Die Hull-Shader-Verzweigung und die joinphasen Ausgaben sind ein gemeinsam genutzter Satz von 4 4-Vektor Registern. Die Ausgaben der einzelnen Verzweigungen oder joinphasen können einander nicht überlappen. Vom System interpretierte Werte, wie z. b. "ttierfactors", kommen in diesem Bereich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





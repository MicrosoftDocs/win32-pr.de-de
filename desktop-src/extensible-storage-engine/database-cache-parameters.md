---
description: Weitere Informationen finden Sie unter Datenbankcacheparameter.
title: Datenbankcacheparameter
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7e8859eabfa35d37464340958b52e85315a9237655107d6736af3555915757
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786348"
---
# <a name="database-cache-parameters"></a>Datenbankcacheparameter


_**Gilt für:** Windows | Windows Server_

## <a name="database-cache-parameters"></a>Datenbankcacheparameter

Dieses Thema enthält Parameter, die für den Datenbankcache verwendet werden.

*JET_paramBatchIOBufferMax*  
22  

Dieser Parameter steuert die Größe eines zusätzlichen Teils des Datenbankseitencaches, der zum Simulieren von Scatter Gather-E/A verwendet wird, wenn er andernfalls nicht verfügbar ist. Die Größe befindet sich auf Datenbankseiten.

**Windows XP und höher:**  Dieser Parameter ist veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>256</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>0, 2 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramCacheSize*  
41  

Dieser Parameter kann verwendet werden, um die Größe des Datenbankseitencaches zur Laufzeit zu steuern. Normalerweise wird die Größe des Caches automatisch als Funktion der Datenbank- und Computeraktivitätsebenen optimieren. Wenn die Anwendung diesen Parameter auf 0 (null) setzt, wird der Cache seine eigene Größe auf diese Weise optimieren. Wenn die Anwendung diesen Parameter jedoch auf einen Wert von nicht 0 (null) legt, passt sich der Cache an diese Zielgröße (auf Datenbankseiten) an. Der Cache hält dann seine Größe bei diesem Schwellenwert, bis er eine neue Größe erhält, oder bis er freigegeben wird, um seine eigene Größe zu wählen.

**Hinweis:**  Die Cachegröße unterliegt weiterhin den Grenzwerten, die von **JET_paramCacheSizeMin** und **JET_paramCacheSizeMax.**

Wenn dieser Parameter gelesen wird, wird die tatsächliche Größe des Caches auf Datenbankseiten zurückgegeben. Diese Größe kann von der Anwendung als Eingabe verwendet werden, um die manuelle Anpassung der Cachegröße zu erstell.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Sonderfunktionen</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong> 1 – 1048575</p>
<p><strong>Windows XP:</strong> 1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramCacheSizeMin*  
60  

Dieser Parameter konfiguriert die Mindestgröße des Datenbankseitencaches. Die Größe befindet sich auf Datenbankseiten.

Standardmäßig passt der Datenbankcache seine Größe automatisch zwischen den von JET_paramCacheSizeMin und **festgelegten** **JET_paramCacheSizeMax.**

**Windows 2000:**  Ab Windows 2000 sollte dieser Parameter auf einen Wert festgelegt werden, der ungefähr der vierfachen Anzahl von Threads entspricht, die sich gleichzeitig innerhalb der ESE-API befindet. Dies ist erforderlich, um Deadlocks zu vermeiden, die durch eine unzureichende Anzahl von Cachepuffern für Datenbankseiten verursacht werden, um komplexe Vorgänge wie B+-Strukturteilungen durchzuführen.

**Windows XP und höher:**  Der Cache-Manager wird automatisch seine eigene minimale Cachegröße festlegen, um Deadlocks zu vermeiden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000:</strong> 64</p>
<p><strong>Windows XP:</strong> 1</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong> 1 – 1048575</p>
<p><strong>Windows XP:</strong> 1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p><strong>Windows 2000:</strong>  Nein</p>
<p><strong>Windows XP:</strong>  Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p><strong>Windows 2000:</strong>  Nein</p>
<p><strong>Windows XP:</strong>  Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramCacheSizeMax*  
23  

Dieser Parameter konfiguriert die maximale Größe des Datenbankseitencaches. Die Größe befindet sich auf Datenbankseiten.

Standardmäßig passt der Datenbankcache seine Größe automatisch zwischen den von JET_paramCacheSizeMin und **festgelegten** **JET_paramCacheSizeMax.**

**Hinweis:**   Wenn dieser Parameter auf seinen Standardwert festgelegt wird, wird die maximale Größe des Caches auf die Größe des physischen Speichers festgelegt, wenn [JetInit](./jetinit-function.md) aufgerufen wird.

**Windows Vista:**  Ab Windows Vista wurde der Standardwert dieses Parameters geändert, um dieses Verhalten zu verdeutlichen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 512</p>
<p><strong>Windows Vista:</strong> 200000000</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong> 1 – 1048575</p>
<p><strong>Windows XP:</strong> 1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p><strong>Windows 2000:</strong>  Nein</p>
<p><strong>Windows XP:</strong>  Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p><strong>Windows XP und Windows 2000:</strong>  Nein</p>
<p><strong>Windows Vista und Windows Server 2003:</strong>  Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramCheckpointDepthMax*  
24 

Dieser Parameter steuert, wie aggressiv Datenbankseiten aus dem Datenbankseitencache geleert werden, um die Zeit für die Wiederherstellung nach einem Absturz zu minimieren. Der -Parameter ist ein Schwellenwert in Bytes für die Anzahl der Transaktionsprotokolldateien, die nach einem Absturz wiedergegeben werden müssen.

Wenn die zirkuläre Protokollierung mit JET_paramCircularLog aktiviert [wird,](./transaction-log-parameters.md) wird mit diesem Parameter auch die ungefähre Menge an Transaktionsprotokolldateien kontrolliert, die auf dem Datenträger beibehalten werden.

Es ist wichtig, dass dieser Parameter nicht zu niedrig festgelegt wird. Wenn sich der Wert dieses Parameters null nähert, wird der Cache immer aggressiver, wenn Datenbankseiten auf den Datenträger geleert werden. Dies führt nicht nur zu einer erhöhten Anzahl von Schreibvorgängen in die Datenbankdateien, sondern auch indirekt zu einer erhöhten Anzahl von Lesevorgängen in diesen Dateien. Dies kann in einigen Fällen zu erheblichen Leistungsproblemen führen. Leider kann das Festlegen des kleinsten optimalen Werts für diesen Parameter nur mithilfe von Experimenten mit der Zielanwendung erfolgen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>20971520</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0 – 2147483647</p>
<p><strong>Windows Vista:</strong>  Alle Werte</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> Dieser Parameter ist global.</p>
<p><strong>Windows Vista:</strong>  Dieser Parameter gilt pro Instanz.</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramCheckpointIOMax*  
135  

Dieser Parameter steuert die maximale Anzahl gleichzeitiger Schreibvorgänge, die die Datenbank-Engine zum Leeren geänderter Datenbankseiten zum Fortschreiten des Prüfpunkts verwendet. Der Wert dieses Parameters kann verwendet werden, um die Geschwindigkeit, mit der der Prüfpunkt erweitert werden kann, im Vergleich zu den negativen Auswirkungen, die dieser Prozess auf die Antwortzeit für andere E/A-Vorgänge auf die Datenträger mit der Datenbank hat, zu ausgleichen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>96</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>8 – 1024</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Beeinträchtigt die Leistung:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Betrifft Ressourcen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows Vista und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableViewCache*  
127  

Wenn dieser Parameter **true ist,** verwendet die Datenbank-Engine Datenbankdaten direkt aus dem Windows-Dateicache, anstatt die zwischengespeicherten Daten in ihren eigenen privaten Speicher zu kopieren. Alle geänderten Datenbankdaten werden weiterhin im privaten Arbeitsspeicher zwischengespeichert.

Dieser Modus soll die Menge des privaten Arbeitsspeichers, der von der Datenbank-Engine zum Zwischenspeichern von Datenbankdaten verwendet wird, weiter reduzieren.

Der Ansichtscache kann nur verwendet werden, wenn die Verwendung des Windows-Dateicaches aktiviert ist, indem sie JET_paramEnableFileCache **true festlegen.**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>Falsch</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Windows Vista und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKCorrInterval*  
25  

Dieser Parameter legt das Zeitintervall in Mikrosekunden fest, über das zwei Datenbankseitenzugriffe als korreliert betrachtet werden. Dieses Korrelationsintervall steuert die Empfindlichkeit des Seitenersetzungsalgorithmus des Caches (LRU-K) gegenüber aufeinander folgenden Seitenzugriffen. Dies wirkt sich wiederum darauf aus, welche Seiten zwischengespeichert werden sollen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>128000</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0 – 2147483647</p>
<p><strong>Windows Vista:</strong>  Alle Werte</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKHistoryMax*  
26  

Dieser Parameter legt die maximale Anzahl von nicht zwischengespeicherten Datenbankseiten fest, für die die Zugriffszeiten der Datenbankseite beibehalten werden. Diese Verlaufsdatensätze ermöglichen es dem Seitenersetzungsalgorithmus des Caches (LRU-K), beliebte Seiten genauer zu erkennen, die fälschlicherweise aus dem Datenbankseitencache entfernt wurden.

**Windows XP und Windows Server 2003:**  Dieser Parameter wird auf Windows XP und Windows Server 2003 ignoriert und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000:</strong> 1024</p>
<p><strong>Windows Vista:</strong> 100000</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong> 0 – 4194303</p>
<p><strong>Windows Vista:</strong>  Alle Werte</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKPolicy*  
27  

Dieser Parameter konfiguriert die Anzahl der Datenbankseitenzugriffe, die für die Bestimmung der Nützlichkeit der Seite berücksichtigt werden. Dieser Parameter ist im Wesentlichen K in LRU-K, dem Seitenersetzungsalgorithmus des Datenbankseitencaches.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p>1 - 2</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKTimeout*  
28

Dieser Parameter gibt den Zeitraum in Sekunden an, nach dem eine Seite im Datenbankseitencache einen Seitenzugriff verloren hat, um die Nützlichkeit der Seite zu berücksichtigen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>100</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 1 – 2147483647</p>
<p><strong>Windows Vista:</strong> 1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKTrxCorrInterval*  
29  

Dieser Parameter ist veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

*JET_paramStartFlushThreshold*  
31  

Dieser Parameter steuert, wann der Datenbankseitencache beginnt, Seiten aus dem Cache zu entfernen, um Platz für Seiten zu schaffen, die nicht zwischengespeichert werden. Wenn die Anzahl der Seitenpuffer im Cache unter diesen Schwellenwert fällt, wird ein Hintergrundprozess gestartet, um diesen Pool verfügbarer Puffer aufzufüllen. Dieser Schwellenwert ist immer relativ zur maximalen Cachegröße, die von **JET_paramCacheSizeMax** festgelegt wird. Dieser Schwellenwert muss auch immer kleiner als der durch **JET_paramStopFlushThreshold** festgelegte Stoppschwellenwert sein.

Die Entfernungshöhe des Startschwellenwerts bestimmt die Antwortzeit, die der Datenbankseitencache benötigt, um verfügbare Puffer zu erzeugen, bevor die Anwendung sie benötigt. Ein hoher Startschwellenwert gibt dem Hintergrundprozess mehr Zeit zum Reagieren. Ein hoher Startschwellenwert impliziert jedoch einen höheren Stoppschwellenwert, der die effektive Größe des Datenbankseitencaches für geänderte Seiten (Windows 2000) oder für alle Seiten (Windows XP und höher) reduziert.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 5 (1 %)</p>
<p><strong>Windows Vista:</strong> 20000000 (1 %)</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong> 1 – 1048575</p>
<p><strong>Windows XP:</strong> 1 – 4294967295</p>
<p><strong>Windows Vista:</strong>  Alle Werte</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramStopFlushThreshold*  
32  

Dieser Parameter steuert, wann der Datenbankseitencache das Entfernen von Seiten aus dem Cache beendet, um Platz für Seiten zu schaffen, die nicht zwischengespeichert werden. Wenn die Anzahl der Seitenpuffer im Cache diesen Schwellenwert überschreitet, wird der Hintergrundprozess beendet, der gestartet wurde, um diesen Pool verfügbarer Puffer aufzufüllen. Dieser Schwellenwert ist immer relativ zur maximalen Cachegröße, die von **JET_paramCacheSizeMax** festgelegt wird. Dieser Schwellenwert muss auch immer größer als der Startschwellenwert sein, der durch **JET_paramStartFlushThreshold** festgelegt wird.

Der Abstand zwischen dem Startschwellenwert und dem Beendigungsschwellenwert wirkt sich auf die Effizienz aus, mit der Datenbankseiten vom Hintergrundprozess geleert werden. Eine größere Lücke macht es wahrscheinlicher, dass Schreibvorgänge auf benachbarte Seiten kombiniert werden können. Ein hoher Schwellenwert für die Beendigung reduziert jedoch die effektive Größe des Datenbankseitencaches für geänderte Seiten (Windows 2000) oder für alle Seiten (Windows XP und höher).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 10 (2 %)</p>
<p><strong>Windows Vista:</strong> 400000000 (2 %)</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong> 1 – 1048575</p>
<p><strong>Windows XP:</strong> 1 – 4294967295</p>
<p><strong>Windows Vista:</strong>  Alle Werte</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf das physische Layout aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf die Zuverlässigkeit aus:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Wirkt sich auf die Leistung aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Wirkt sich auf Ressourcen aus:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Verfügbarkeit:</p></td>
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Wird in Esent.h deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)

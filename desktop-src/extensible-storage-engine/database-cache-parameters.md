---
description: Weitere Informationen finden Sie in den Daten Bank Cache Parametern.
title: Daten Bank Cache Parameter
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
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360101"
---
# <a name="database-cache-parameters"></a>Daten Bank Cache Parameter


_**Gilt für:** Windows | Windows Server_

## <a name="database-cache-parameters"></a>Daten Bank Cache Parameter

Dieses Thema enthält Parameter, die für den Daten Bank Cache verwendet werden.

*JET_paramBatchIOBufferMax*  
22  

Dieser Parameter steuert die Größe eines zusätzlichen Teils des Datenbankseiten Caches, der zum Simulieren von e/a-Punkt erfassten e/a-Vorgängen verwendet wird, wenn diese andernfalls nicht verfügbar sind. Die Größe befindet sich auf Datenbankseiten.

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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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

Dieser Parameter kann verwendet werden, um die Größe des Datenbankseiten Caches zur Laufzeit zu steuern. Normalerweise wird die Größe des Caches automatisch als Funktion der Datenbank-und Computer Aktivitäts Ebenen optimiert. Wenn die Anwendung diesen Parameter auf 0 (null) festlegt, wird auf diese Weise der Cache seine eigene Größe optimieren. Wenn die Anwendung diesen Parameter jedoch auf einen Wert ungleich 0 (null) festlegt, wird der Cache an die Zielgröße (in Datenbankseiten) angepasst. Der Cache speichert dann seine Größe an diesem Schwellenwert, bis eine neue Größe angegeben wird, oder bis er freigegeben wird, um seine eigene Größe auszuwählen.

**Hinweis**  Die Cache Größe unterliegt weiterhin den von **JET_paramCacheSizeMin** und **JET_paramCacheSizeMax** vorgegebenen Grenzwerten.

Wenn dieser Parameter gelesen wird, wird die tatsächliche Größe des Caches in Datenbankseiten zurückgegeben. Diese Größe kann von der Anwendung als Eingabe verwendet werden, um die manuelle Anpassung der Cache Größe zu steuern.

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
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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

Dieser Parameter konfiguriert die Mindestgröße des Datenbankseiten Caches. Die Größe befindet sich auf Datenbankseiten.

Standardmäßig wird die Größe des Daten Bank Caches automatisch zwischen den von **JET_paramCacheSizeMin** und **JET_paramCacheSizeMax** festgelegten Grenzwerten angepasst.

**Windows 2000:**  Unter Windows 2000 sollte dieser Parameter auf einen Wert festgelegt werden, der ungefähr so groß wie die Anzahl der Threads ist, die gleichzeitig in der ESE-API vorkommen werden. Dies ist erforderlich, um Deadlocks zu vermeiden, die durch eine unzureichende Anzahl von Datenbankseiten Cache Puffern verursacht werden, um komplexe Vorgänge wie B +-Struktur Teilungen auszuführen.

**Windows XP und höher:**  Der Cache-Manager legt automatisch seine eigene minimale Cache Größe fest, um Deadlocks zu vermeiden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000:</strong>  64</p>
<p><strong>Windows XP:</strong>  1</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p><strong>Windows 2000:</strong>  Nein</p>
<p><strong>Windows XP:</strong>  Zwar</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p><strong>Windows 2000:</strong>  Nein</p>
<p><strong>Windows XP:</strong>  Zwar</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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

Dieser Parameter konfiguriert die maximale Größe des Datenbankseiten Caches. Die Größe befindet sich auf Datenbankseiten.

Standardmäßig wird die Größe des Daten Bank Caches automatisch zwischen den von **JET_paramCacheSizeMin** und **JET_paramCacheSizeMax** festgelegten Grenzwerten angepasst.

**Hinweis**   Wenn dieser Parameter auf seinen Standardwert zurückgesetzt wird, wird die maximale Cache Größe auf die Größe des physischen Arbeitsspeichers festgelegt, wenn [jetinit](./jetinit-function.md) aufgerufen wird.

**Windows Vista:**  Ab Windows Vista wurde der Standardwert dieses Parameters geändert, um dieses Verhalten zu verdeutlichen.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  512</p>
<p><strong>Windows Vista:</strong>  2 Milliarden</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p><strong>Windows 2000:</strong>  Nein</p>
<p><strong>Windows XP:</strong>  Zwar</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p><strong>Windows XP und Windows 2000:</strong>  Nein</p>
<p><strong>Windows Vista und Windows Server 2003:</strong>  Zwar</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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

Mit diesem Parameter wird gesteuert, wie aggressiv Datenbankseiten aus dem Datenbankseiten Cache geleert werden, um die Zeitspanne zu minimieren, die für die Wiederherstellung nach einem Absturz benötigt wird. Der-Parameter ist ein Schwellenwert in Bytes, der angibt, wie viele Transaktionsprotokoll Dateien nach einem Absturz wiedergegeben werden müssen.

Wenn die zirkuläre Protokollierung mithilfe [JET_paramCircularLog](./transaction-log-parameters.md) aktiviert wird, steuert dieser Parameter auch die ungefähre Menge an Transaktionsprotokoll Dateien, die auf dem Datenträger beibehalten werden.

Es ist wichtig, dass dieser Parameter nicht zu niedrig festgelegt wird. Da der Wert dieses Parameters NULL ist, wird der Cache beim Leeren von Datenbankseiten auf den Datenträger immer komplexer. Dies führt nicht nur zu einer größeren Anzahl von Schreibvorgängen für die Datenbankdateien, sondern auch indirekt zu einer größeren Anzahl von Lesevorgängen für diese Dateien. Dies kann in einigen Fällen sehr erhebliche Leistungsprobleme verursachen. Leider kann das Festlegen des kleinsten optimalen Werts für diesen Parameter nur mithilfe von Experimenten mit der Zielanwendung erfolgen.

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
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  0 – 2147483647</p>
<p><strong>Windows Vista:</strong>  Alle Werte</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> Dieser Parameter ist Global.</p>
<p><strong>Windows Vista:</strong>  Dieser Parameter ist pro Instanz.</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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

Dieser Parameter steuert die maximale Anzahl von gleichzeitigen Schreibvorgängen, die von der Datenbank-Engine verwendet werden, um geänderte Datenbankseiten zum Zweck der Weiterentwicklung des Prüf Punkts zu leeren. Der Wert dieses Parameters kann verwendet werden, um die Geschwindigkeit auszugleichen, mit der der Prüfpunkt erweitert werden kann, im Vergleich zu den negativen Auswirkungen, die dieser Prozess für die Antwortzeit für andere e/a-Vorgänge auf die Datenträger mit der Datenbank hat.

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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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

Wenn dieser Parameter **true** ist, verwendet die Datenbank-Engine Datenbankdaten direkt aus dem Windows-Dateicache, anstatt die zwischengespeicherten Daten in ihren eigenen privaten Speicher zu kopieren. Alle geänderten Datenbankdaten werden weiterhin im privaten Speicher zwischengespeichert.

Der Zweck dieses Modus besteht darin, den Umfang des privaten Speichers, der von der Datenbank-Engine zum Zwischenspeichern von Datenbankdaten verwendet wird, weiter zu reduzieren.

Der Ansichts Cache kann nur verwendet werden, wenn die Verwendung des Windows-Datei Caches aktiviert ist, indem JET_paramEnableFileCache auf **true** festgelegt wird.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p>False</p></td>
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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Windows Vista und höher</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKCorrInterval*  
25  

Mit diesem Parameter wird das Zeitintervall in Mikrosekunden festgelegt, in dem zwei Datenbankseiten Zugriffe als korreliert angesehen werden. Mit diesem Korrelations Intervall wird die Vertraulichkeit des Seiten Ersetzungs Algorithmus (LRU-K) zwischen Cache und aufeinander folgenden Seiten Zugriffen gesteuert. Dies wirkt sich wiederum auf die Seiten aus, die für die Zwischenspeicherung ausgewählt werden.

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
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003: </strong>    0 – 2147483647</p>
<p><strong>Windows Vista:</strong>  Alle Werte</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKHistoryMax*  
26  

Mit diesem Parameter wird die maximale Anzahl nicht zwischen gespeicherter Datenbankseiten festgelegt, für die Datenbankseiten Zugriffszeiten beibehalten werden. Diese Verlaufs Datensätze ermöglichen es dem Cache mit dem Seiten Ersetzungs Algorithmus (LRU-K), beliebte Seiten, die fälschlicherweise aus dem Datenbankseiten Cache entfernt wurden, genauer zu erkennen.

**Windows XP und Windows Server 2003:**  Dieser Parameter wird unter Windows XP und Windows Server 2003 ignoriert und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000:</strong>  1024</p>
<p><strong>Windows Vista:</strong>  100000</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong>  0 – 4194303</p>
<p><strong>Windows Vista:</strong>  Alle Werte</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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


*JET_paramLRUKPolicy*  
27  

Mit diesem Parameter wird die Anzahl der Datenbankseiten Zugriffe konfiguriert, die zum Ermitteln der Nützlichkeit der Seite berücksichtigt werden. Bei diesem Parameter handelt es sich im Wesentlichen um das k in LRU-K, den Seiten Ersetzungs Algorithmus des Datenbankseiten Caches.

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
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKTimeout*  
28

Dieser Parameter gibt den Zeitraum in Sekunden an, nach dem eine Seite im Datenbankseiten Cache einen Seiten Zugriff verloren hat, um die Nützlichkeit der Seite zu berücksichtigen.

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
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  1 – 2147483647</p>
<p><strong>Windows Vista:</strong>   1 – 4294967295</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>Alle</p></td>
</tr>
</tbody>
</table>


*JET_paramLRUKTrxCorrInterval*  
29  

Dieser Parameter ist veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

*JET_paramStartFlushThreshold*  
31  

Mit diesem Parameter wird gesteuert, wann der Datenbankseiten Cache mit der Erstellung von Seiten aus dem Cache beginnt, um Platz für Seiten zu schaffen, die nicht zwischengespeichert werden. Wenn die Anzahl der Seiten Puffer im Cache unter diesen Schwellenwert fällt, wird ein Hintergrundprozess gestartet, um den Pool der verfügbaren Puffer aufzufüllen. Dieser Schwellenwert ist immer relativ zur maximalen Cache Größe, die von **JET_paramCacheSizeMax** festgelegt wird. Dieser Schwellenwert muss auch immer niedriger als der von **JET_paramStopFlushThreshold** festgelegte Schwellenwert sein.

Die Entfernungs Höhe des Start Schwellenwerts bestimmt die Antwortzeit, die der Datenbankseiten Cache aufweisen muss, damit verfügbare Puffer erstellt werden, bevor die Anwendung Sie benötigt. Ein Schwellenwert für hohe Starts gibt dem Hintergrundprozess mehr Zeit für die Reaktion. Ein Schwellenwert für hohe Starts impliziert jedoch einen höheren Schwellenwert für die Beendigung, wodurch die effektive Größe des Datenbankseiten Caches für geänderte Seiten (Windows 2000) oder für alle Seiten (Windows XP und höher) reduziert wird.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  5 (1%)</p>
<p><strong>Windows Vista:</strong>  20 Millionen (1%)</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p>
<p><strong>Windows Vista:</strong>  Alle Werte</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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


*JET_paramStopFlushThreshold*  
32  

Mit diesem Parameter wird gesteuert, wann der Datenbankseiten Cache das Entfernen von Seiten aus dem Cache beendet, um Platz für nicht zwischengespeicherte Seiten zu schaffen. Wenn die Anzahl der Seiten Puffer im Cache über diesem Schwellenwert liegt, wird der Hintergrundprozess beendet, der zum Auffüllen dieses Pools verfügbarer Puffer gestartet wurde. Dieser Schwellenwert ist immer relativ zur maximalen Cache Größe, die von **JET_paramCacheSizeMax** festgelegt wird. Dieser Schwellenwert muss auch immer größer sein als der Start Schwellenwert, der durch **JET_paramStartFlushThreshold** festgelegt wird.

Der Abstand zwischen dem Start Schwellenwert und dem Schwellenwert für das Abbrechen wirkt sich auf die Effizienz aus, mit der Datenbankseiten durch den Hintergrundprozess geleert werden. Eine größere Lücke macht es wahrscheinlicher, dass Schreibvorgänge auf benachbarte Seiten möglicherweise kombiniert werden. Durch einen Schwellenwert für hohe Beendigung wird jedoch die effektive Größe des Datenbankseiten Caches für geänderte Seiten (Windows 2000) oder für alle Seiten (Windows XP und höher) verringert.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Standardwert:</p></td>
<td><p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong>  10 (2%)</p>
<p><strong>Windows Vista:</strong>  40 Millionen (2%)</p></td>
</tr>
<tr class="even">
<td><p>Typ:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Gültiger Bereich:</p></td>
<td><p><strong>Windows 2000:</strong>  1 – 1048575</p>
<p><strong>Windows XP:</strong>  1 – 4294967295</p>
<p><strong>Windows Vista:</strong>  Alle Werte</p></td>
</tr>
<tr class="even">
<td><p>Umfang:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p>Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p>Hat Auswirkungen auf das physische Layout:</p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p>Beeinträchtigt die Zuverlässigkeit:</p></td>
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
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[Jetkreateingestance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)

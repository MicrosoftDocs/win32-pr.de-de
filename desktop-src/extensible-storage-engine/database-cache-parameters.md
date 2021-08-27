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
ms.openlocfilehash: 43d51be7e2db82d64c70f6fa810be3caf4c6fbd8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984093"
---
# <a name="database-cache-parameters"></a>Datenbankcacheparameter


_**Gilt für:** Windows | Windows Server_

## <a name="database-cache-parameters"></a>Datenbankcacheparameter

Dieses Thema enthält Parameter, die für den Datenbankcache verwendet werden.

*JET_paramBatchIOBufferMax*  
22  

Dieser Parameter steuert die Größe eines zusätzlichen Teils des Datenbankseitencaches, der zum Simulieren von Scatter Gather-E/A verwendet wird, wenn er andernfalls nicht verfügbar ist. Die Größe befindet sich auf Datenbankseiten.

**Windows XP und höher:**  Dieser Parameter ist veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>256</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0, 2 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>No</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramCacheSize*  
41  

Dieser Parameter kann verwendet werden, um die Größe des Datenbankseitencaches zur Laufzeit zu steuern. Normalerweise wird die Größe des Caches automatisch als Funktion der Datenbank- und Computeraktivitätsebenen optimieren. Wenn die Anwendung diesen Parameter auf 0 (null) setzt, wird der Cache seine eigene Größe auf diese Weise optimieren. Wenn die Anwendung diesen Parameter jedoch auf einen Wert von nicht 0 (null) legt, passt sich der Cache an diese Zielgröße (auf Datenbankseiten) an. Der Cache hält dann seine Größe bei diesem Schwellenwert, bis er eine neue Größe erhält, oder bis er freigegeben wird, um seine eigene Größe zu wählen.

**Hinweis:**  Die Cachegröße unterliegt weiterhin den Grenzwerten, die von JET_paramCacheSizeMin **und** **JET_paramCacheSizeMax.**

Wenn dieser Parameter gelesen wird, wird die tatsächliche Größe des Caches auf Datenbankseiten zurückgegeben. Diese Größe kann von der Anwendung als Eingabe verwendet werden, um die manuelle Anpassung der Cachegröße zu erstell.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Sonderfunktionen</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramCacheSizeMin*  
60  

Dieser Parameter konfiguriert die Mindestgröße des Datenbankseitencaches. Die Größe befindet sich auf Datenbankseiten.

Standardmäßig passt der Datenbankcache seine Größe automatisch zwischen den von JET_paramCacheSizeMin und **festgelegten** **JET_paramCacheSizeMax.**

**Windows 2000:**  Ab Windows 2000 sollte dieser Parameter auf einen Wert festgelegt werden, der ungefähr der vierfachen Anzahl von Threads entspricht, die sich gleichzeitig innerhalb der ESE-API befindet. Dies ist erforderlich, um Deadlocks zu vermeiden, die durch eine unzureichende Anzahl von Cachepuffern für Datenbankseiten verursacht werden, um komplexe Vorgänge wie B+-Strukturteilungen durchzuführen.

**Windows XP und höher:**  Der Cache-Manager wird automatisch seine eigene minimale Cachegröße festlegen, um Deadlocks zu vermeiden.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p><strong>Windows 2000:</strong> 64</p><p><strong>Windows XP:</strong> 1</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p><strong>Windows 2000:</strong>  Nein</p><p><strong>Windows XP:</strong>  Ja</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p><strong>Windows 2000:</strong>  Nein</p><p><strong>Windows XP:</strong>  Ja</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramCacheSizeMax*  
23  

Dieser Parameter konfiguriert die maximale Größe des Datenbankseitencaches. Die Größe wird auf Datenbankseiten angezeigt.

Standardmäßig passt der Datenbankcache seine Größe automatisch zwischen den durch JET_paramCacheSizeMin und **JET_paramCacheSizeMax** festgelegten **Grenzwerten an.**

**Hinweis**   Wenn dieser Parameter auf seinen Standardwert festgelegt wird, wird die maximale Größe des Caches auf die Größe des physischen Arbeitsspeichers festgelegt, wenn [JetInit](./jetinit-function.md) aufgerufen wird.

**Windows Vista:**  Ab Windows Vista wurde der Standardwert dieses Parameters geändert, um dieses Verhalten zu verdeutlichen.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 512</p><p><strong>Windows Vista:</strong> 20000000000</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p><strong>Windows 2000:</strong>  Nein</p><p><strong>Windows XP:</strong>  Ja</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p><strong>Windows XP und Windows 2000:</strong>  Nein</p><p><strong>Windows Vista und Windows Server 2003:</strong>  Ja</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramCheckpointDepthMax*  
24 

Dieser Parameter steuert, wie aggressiv Datenbankseiten aus dem Datenbankseitencache geleert werden, um die Zeit zu minimieren, die für die Wiederherstellung nach einem Absturz dauert. Der -Parameter ist ein Schwellenwert in Bytes für die Anzahl der Transaktionsprotokolldateien, die nach einem Absturz wiedergegeben werden müssen.

Wenn die zirkuläre Protokollierung mit [JET_paramCircularLog](./transaction-log-parameters.md) aktiviert ist, steuert dieser Parameter auch die ungefähre Menge der Transaktionsprotokolldateien, die auf dem Datenträger beibehalten werden.

Es ist wichtig, dass dieser Parameter nicht zu niedrig festgelegt wird. Wenn sich der Wert dieses Parameters 0 nähert, wird der Cache immer aggressiver, wenn Datenbankseiten auf den Datenträger geleert werden. Dies führt nicht nur zu einer erhöhten Anzahl von Schreibvorgängen in die Datenbankdateien, sondern auch indirekt zu einer erhöhten Anzahl von Lesevorgängen für diese Dateien. Dies kann in einigen Fällen zu sehr erheblichen Leistungsproblemen führen. Leider kann das Festlegen des kleinsten optimalen Werts für diesen Parameter nur mithilfe von Experimenten mit der Zielanwendung erfolgen.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>20971520</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0 – 2147483647</p><p><strong>Windows Vista:</strong>  Alle Werte</p> | 
| <p>Umfang:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> Dieser Parameter ist global.</p><p><strong>Windows Vista:</strong>  Dieser Parameter ist pro Instanz.</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramCheckpointIOMax*  
135  

Dieser Parameter steuert die maximale Anzahl gleichzeitiger Schreibvorgänge, die die Datenbank-Engine verwendet, um geänderte Datenbankseiten zu leeren, um den Prüfpunkt zu verbessern. Der Wert dieses Parameters kann verwendet werden, um die Geschwindigkeit auszugleichen, mit der der Prüfpunkt erweitert werden kann, im Vergleich zu den negativen Auswirkungen, die dieser Prozess auf die Antwortzeit anderer E/A-Vorgänge auf die Datenträger mit der Datenbank hat.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>96</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>8 – 1024</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows Vista und höher</p> | 



*JET_paramEnableViewCache*  
127  

Wenn dieser Parameter **true ist,** verwendet die Datenbank-Engine Datenbankdaten direkt aus dem Windows-Dateicache, anstatt die zwischengespeicherten Daten in ihren eigenen privaten Speicher zu kopieren. Alle geänderten Datenbankdaten werden weiterhin im privaten Arbeitsspeicher zwischengespeichert.

Dieser Modus soll die Menge des privaten Arbeitsspeichers, der von der Datenbank-Engine zum Zwischenspeichern von Datenbankdaten verwendet wird, weiter reduzieren.

Der Ansichtscache kann nur verwendet werden, wenn die Verwendung des Windows-Dateicaches aktiviert ist, indem sie JET_paramEnableFileCache **true festlegen.**


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Falsch</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>No</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows Vista und höher</p> | 



*JET_paramLRUKCorrInterval*  
25  

Dieser Parameter legt das Zeitintervall in Mikrosekunden fest, über das zwei Datenbankseitenzugriffe als korreliert betrachtet werden. Dieses Korrelationsintervall steuert die Vertraulichkeit des Seitenersetzungsalgorithmus (LRU-K) des Caches gegenüber aufeinander folgenden Seitenzugriffen. Dies wirkt sich wiederum darauf aus, welche Seiten zwischengespeichert werden sollen.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>128000</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0 – 2147483647</p><p><strong>Windows Vista:</strong>  Alle Werte</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Nein</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramLRUKHistoryMax*  
26  

Dieser Parameter legt die maximale Anzahl nicht zwischengespeicherter Datenbankseiten fest, für die Zugriffszeiten für Datenbankseiten beibehalten werden. Diese Verlaufsdatensätze ermöglichen es dem Seitenaustauschalgorithmus (LRU-K) des Caches, beliebte Seiten, die fälschlicherweise aus dem Datenbankseitencache entfernt wurden, genauer zu erkennen.

**Windows XP und Windows Server 2003:**  Dieser Parameter wird auf Windows XP und Windows Server 2003 ignoriert und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p><strong>Windows 2000:</strong> 1024</p><p><strong>Windows Vista:</strong> 100000</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000:</strong> 0 – 4194303</p><p><strong>Windows Vista:</strong>  Alle Werte</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Nein</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramLRUKPolicy*  
27  

Dieser Parameter konfiguriert die Anzahl der Datenbankseitenzugriffe, die für die Bestimmung der Nützlichkeit der Seite berücksichtigt werden. Dieser Parameter ist im Wesentlichen der K in LRU-K, dem Seitenaustauschalgorithmus des Datenbankseitencaches.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>2</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>1 - 2</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Nein</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramLRUKTimeout*  
28

Dieser Parameter gibt den Zeitraum in Sekunden an, nach dem eine Seite im Datenbankseitencache einen Seitenzugriff verloren hat, um die Nützlichkeit der Seite zu berücksichtigen.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>100</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 1 – 2147483647</p><p><strong>Windows Vista:</strong> 1 – 4294967295</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>No</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramLRUKTrxCorrInterval*  
29  

Dieser Parameter ist veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.

*JET_paramStartFlushThreshold*  
31  

Dieser Parameter steuert, wann der Datenbankseitencache damit beginnt, Seiten aus dem Cache zu entfernen, um Platz für Seiten zu machen, die nicht zwischengespeichert werden. Wenn die Anzahl der Seitenpuffer im Cache unter diesen Schwellenwert fällt, wird ein Hintergrundprozess gestartet, um diesen Pool verfügbarer Puffer zu füllen. Dieser Schwellenwert ist immer relativ zur maximalen Cachegröße, die von festgelegt **JET_paramCacheSizeMax.** Dieser Schwellenwert muss auch immer kleiner sein als der Durchsatzschwellenwert, der von festgelegt **JET_paramStopFlushThreshold.**

Die Entfernungshöhe des Startschwellenwerts bestimmt die Antwortzeit, die der Datenbankseitencache benötigt, um verfügbare Puffer zu erzeugen, bevor die Anwendung sie benötigt. Ein hoher Startschwellenwert gibt dem Hintergrundprozess mehr Zeit zum Reagieren. Ein hoher Startschwellenwert impliziert jedoch einen höheren Stoppschwellenwert, der die effektive Größe des Datenbankseitencaches für geänderte Seiten (Windows 2000) oder für alle Seiten (Windows XP und höher) reduziert.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 5 (1 %)</p><p><strong>Windows Vista:</strong> 20000000 (1 %)</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p><p><strong>Windows Vista:</strong>  Alle Werte</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramStopFlushThreshold*  
32  

Dieser Parameter steuert, wann der Datenbankseitencache das Entfernen von Seiten aus dem Cache beendet, um Platz für Seiten zu machen, die nicht zwischengespeichert werden. Wenn die Anzahl der Seitenpuffer im Cache diesen Schwellenwert überschreitet, wird der Hintergrundprozess beendet, der gestartet wurde, um diesen Pool verfügbarer Puffer aufzufüllen. Dieser Schwellenwert ist immer relativ zur maximalen Cachegröße, die von festgelegt **JET_paramCacheSizeMax.** Dieser Schwellenwert muss auch immer größer als der Startschwellenwert sein, der von festgelegt **JET_paramStartFlushThreshold.**

Der Abstand zwischen dem Startschwellenwert und dem Stoppschwellenwert wirkt sich auf die Effizienz aus, mit der Datenbankseiten vom Hintergrundprozess geleert werden. Eine größere Lücke macht es wahrscheinlicher, dass Schreibvorgänge auf benachbarte Seiten kombiniert werden können. Ein hoher Stoppschwellenwert verringert jedoch die effektive Größe des Datenbankseitencaches für geänderte Seiten (Windows 2000) oder für alle Seiten (Windows XP und höher).


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 10 (2%)</p><p><strong>Windows Vista:</strong> 40000000 (2 %)</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p><p><strong>Windows Vista:</strong>  Alle Werte</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)

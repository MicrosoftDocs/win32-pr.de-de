---
description: Weitere Informationen finden Sie unter E/A-Parameter.
title: E/A-Parameter
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 0a980e436dacc020a0606e6a9466492fe687ca0e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473536"
---
# <a name="io-parameters"></a>E/A-Parameter


_**Gilt für:** Windows | Windows Server_

## <a name="io-parameters"></a>E/A-Parameter

Dieses Thema enthält Parameter, die für die Eingabe und Ausgabe (E/A) verwendet werden.

*JET_paramAccessDeniedRetryPeriod*  
53  

**Windows XP und höher:**  Dieser Parameter konfiguriert die Dauer (in Millisekunden), die die Datenbank-Engine für den Zugriff auf eine Datei verwendet, die gesperrt ist, bevor ein Fehler JET_errFileAccessDenied. Diese Zeitverzögerung wurde entwickelt, um Antivirensoftware zu verhindern, die einige der Dateien der Datenbank-Engine kurz nach dem Schließen geöffnet halten kann.

**Hinweis:**  Als Ergebnis der obigen Wiederholungslogik führt jeder Versuch, an eine Datenbank angefügt oder eine Protokolldatei zu verwenden, die bereits von der Datenbank-Engine verwendet wird, zu einer Verzögerung dieser Größe, bevor der API-Aufruf einen (legitimen) Fehler zurückgibt. Dieser Parameter kann verwendet werden, um diese Verzögerung für den Fall zu deaktivieren, dass dies ein häufiges Szenario ist.


| | | <p>Standardwert:</p> | <p>10000</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0 – 4294967295</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Ja</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Ja</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows XP und höher</p> | 



*JET_paramCreatePathIfNotExist*  
100  

Wenn dieser Parameter auf TRUE festgelegt ist, werden alle Ordner, die in einem Dateisystempfad fehlen, der von der Datenbank-Engine verwendet wird, automatisch erstellt. Andernfalls kann der Vorgang, der den fehlenden Dateisystempfad verwendet, nicht JET_errInvalidPath.


| | | <p>Standardwert:</p> | <p>False</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>False, True</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Ja</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>All</p> | 



*JET_paramEnableFileCache*  
126  

Wenn dieser Parameter **true ist,** verwendet die Datenbank-Engine den Windows-Dateicache als Lesecache für alle seine verschiedenen Dateien. Sie wird auch als Schreibcache für die temporäre Datenbank oder für Datenbanken verwendet, die mit deaktivierter Wiederherstellung geöffnet werden. Die Datenbank-Engine muss die Schreibzwischenspeicherung für normale Datenbanken, Transaktionsprotokolldateien und Prüfpunktdateien deaktivieren, um die Transaktionsintegrität der Datenbanken zu schützen.

Beachten Sie, dass durch die Verwendung des Windows-Dateicaches eine zweite Zwischenspeicherungsebene für Datenbankdateien hinzugefügt wird. Der Datenbankcache verwendet weiterhin seinen eigenen Arbeitsspeicher, um die Datenbankdateien zwischenspeichern zu können. Dieser Modus soll es der Anwendung ermöglichen, die Datenbank-Engine mit einem kleinen dedizierten Cache zu konfigurieren und es Windows zu ermöglichen, freien Arbeitsspeicher zu besparen, um die Zwischenspeicherung von Datenbankdaten weiter zu verbessern.


| | | <p>Standardwert:</p> | <p>False</p> | | <p>Typ:</p> | <p>Boolesch</p> | | <p>Gültiger Bereich:</p> | <p>False, True</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Nein</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Ja</p> | | <p>Verfügbarkeit:</p> | <p>Windows Vista und höher</p> | 



*JET_paramIOPriority*  
152  

Dieser Parameter steuert, wie ESE E/A-Vorgänge behandelt. Die Werte können für den normalen Betrieb auf 0 (JET_IOPriorityNormal) oder auf 1 (JET_IOPriorityLow) für den Vorgang mit niedriger Priorität festgelegt werden. Wenn die Priorität auf JET_IOPriorityLow festgelegt ist, verwendet ESE die neue Thread-E/A-Prioritätsfunktion, die in Windows Vista verfügbar ist, um die E/A-Priorität für den Thread zu verringern, sodass nachfolgende E/A-Vorgänge mit der neuen niedrigen Priorität ausgegeben werden.

**Windows Vista:**  JET_paramIOPriority wird in Windows Vista eingeführt.


| | | <p>Standardwert:</p> | <p>0</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0 - 1</p> | | <p>Umfang:</p> | <p>Instanz</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Ja</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows Vista</p> | 



*JET_paramOutstandingIOMax*  
30 

Dieser Parameter steuert, wie viele Datenbankdatei-E/A-Dateien gleichzeitig im Hostbetriebssystem in die Warteschlange gestellt werden können.

Ein größerer Wert für diesen Parameter kann die Leistung einer großen Datenbankanwendung erheblich verbessern.

**Windows XP und Windows Server 2003:**  Dieser Parameter wird auf Windows XP und Windows Server 2003 ignoriert und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.


| | | <p>Standardwert:</p> | <p><strong>Windows 2000:</strong> 64</p><p><strong>Windows Vista:</strong> 1024</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p><strong>Windows 2000:</strong> 8 – 2147483647</p><p><strong>Windows Vista:</strong> 0 – 65536</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Nein</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Ja</p> | | <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramMaxCoalesceReadSize*  
164  

Maximale Anzahl von Bytes, die für einen zusammenfingierten Lesevorgang gruppiert werden können.


| | | <p>Standardwert:</p> | <p>262144</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0-1073741824</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteSize*  
165  

Maximale Anzahl von Bytes, die für einen zusammenfingierten Schreibvorgang gruppiert werden können.


| | | <p>Standardwert:</p> | <p>393216</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0-1073741824</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Beeinträchtigt die Leistung:</p> | <p>Ja</p> | | <p>Betrifft Ressourcen:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceReadGapSize*  
166  

Maximale Anzahl von Bytes, die für einen zusammenfingierten Schreib-E/A-Vorgang gelücket werden können.


| | | <p>Standardwert:</p> | <p>262144</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0-1073741824</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Ja</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteGapSize*  
167  

Maximale Anzahl von Bytes, die für einen zusammengefügten Lese-E/A-Vorgang abgespalt werden können.


| | | <p>Standardwert:</p> | <p>393216</p> | | <p>Typ:</p> | <p>Integer</p> | | <p>Gültiger Bereich:</p> | <p>0-1073741824</p> | | <p>Umfang:</p> | <p>Global</p> | | <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Ja</p> | | <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | | <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | | <p>Wirkt sich auf die Leistung aus:</p> | <p>Ja</p> | | <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | | <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)

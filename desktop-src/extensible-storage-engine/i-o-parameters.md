---
description: 'Weitere Informationen zu: E/A-Parameter'
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
ms.openlocfilehash: 62cc1183f14e3de113ff5f34eaf6367bc2ff0f9a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981983"
---
# <a name="io-parameters"></a>E/A-Parameter


_**Gilt für:** Windows | Windows Server_

## <a name="io-parameters"></a>E/A-Parameter

Dieses Thema enthält Parameter, die für Eingabe und Ausgabe (E/A) verwendet werden.

*JET_paramAccessDeniedRetryPeriod*  
53  

**Windows XP und höher:**  Dieser Parameter konfiguriert die Zeitspanne (in Millisekunden), die die Datenbank-Engine für den Zugriff auf eine gesperrte Datei verwendet, bevor ein Fehler mit JET_errFileAccessDenied. Diese Zeitverzögerung soll Virenschutzsoftware umgehen, die einige Dateien der Datenbank-Engine kurz nach dem Schließen öffnen kann.

**Hinweis**  Aufgrund der oben genannten Wiederholungslogik führt jeder Versuch, eine Datenbank anzufügen oder eine Protokolldatei zu verwenden, die bereits von der Datenbank-Engine verwendet wird, zu einer Verzögerung dieser Größe, bevor der API-Aufruf einen (legitimen) Fehler zurückgibt. Dieser Parameter kann verwendet werden, um diese Verzögerung zu deaktivieren, falls dies ein häufiges Szenario ist.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>10000</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 4294967295</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und höher</p> | 



*JET_paramCreatePathIfNotExist*  
100  

Wenn dieser Parameter auf TRUE festgelegt ist, wird automatisch jeder Ordner erstellt, der in einem Dateisystempfad fehlt, der von der Datenbank-Engine verwendet wird. Andernfalls schlägt der Vorgang, der den fehlenden Dateisystempfad verwendet, mit JET_errInvalidPath fehl.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Falsch</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramEnableFileCache*  
126  

Wenn dieser Parameter **True** ist, verwendet die Datenbank-Engine den Windows-Dateicache als Lesecache für alle seine verschiedenen Dateien. Sie wird auch als Schreibcache für die temporäre Datenbank oder für Datenbanken verwendet, die mit deaktivierter Wiederherstellung geöffnet werden. Die Datenbank-Engine muss die Schreibzwischenspeicherung für normale Datenbanken, Transaktionsprotokolldateien und Prüfpunktdateien deaktivieren, um die Transaktionsintegrität der Datenbanken zu schützen.

Es ist wichtig zu beachten, dass die Verwendung des Windows Dateicaches eine zweite Zwischenspeicherungsebene für Datenbankdateien hinzugibt. Der Datenbankcache verwendet weiterhin seinen eigenen Arbeitsspeicher, um die Datenbankdateien zwischenzuspeichern. Der Zweck dieses Modus besteht darin, der Anwendung zu ermöglichen, die Datenbank-Engine mit einem kleinen dedizierten Cache zu konfigurieren und Windows das Belegen von freiem Arbeitsspeicher zu ermöglichen, um das Zwischenspeichern von Datenbankdaten weiter zu verbessern.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Falsch</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>No</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows Vista und höher</p> | 



*JET_paramIOPriority*  
152  

Dieser Parameter steuert, wie ESE E/A-Vorgänge verarbeitet. Die Werte können für den normalen Betrieb auf 0 (JET_IOPriorityNormal) oder für Vorgänge mit niedriger Priorität auf 1 (JET_IOPriorityLow) festgelegt werden. Wenn die Priorität auf JET_IOPriorityLow festgelegt ist, verwendet ESE die neue Thread-E/A-Prioritätsfunktion, die in Windows Vista verfügbar ist, um die E/A-Priorität im Thread zu reduzieren, sodass nachfolgende E/A-Vorgänge mit der neuen niedrigen Priorität ausgegeben werden.

**Windows Vista:**  JET_paramIOPriority wird in Windows Vista eingeführt.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>0</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 - 1</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows Vista</p> | 



*JET_paramOutstandingIOMax*  
30 

Dieser Parameter steuert, wie viele Datenbankdatei-E/As gleichzeitig im Hostbetriebssystem in die Warteschlange eingereiht werden können.

Ein größerer Wert für diesen Parameter kann die Leistung einer großen Datenbankanwendung erheblich verbessern.

**Windows XP und Windows Server 2003:**  Dieser Parameter wird auf Windows XP und Windows Server 2003 ignoriert und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p><strong>Windows 2000:</strong> 64</p><p><strong>Windows Vista:</strong> 1024</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows 2000:</strong> 8 – 2147483647</p><p><strong>Windows Vista:</strong> 0 – 65536</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>No</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramMaxCoalesceReadSize*  
164  

Maximale Anzahl von Bytes, die für einen zusammengeknüpften Lesevorgang gruppiert werden können.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>262144</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0-1073741824</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteSize*  
165  

Maximale Anzahl von Bytes, die für einen zusammengeknüpften Schreibvorgang gruppiert werden können.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>393216</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0-1073741824</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>No</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceReadGapSize*  
166  

Maximale Anzahl von Bytes, die für einen zusammenfingierten Schreib-E/A-Vorgang gelücket werden können.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>262144</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0-1073741824</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



*JET_paramMaxCoalesceWriteGapSize*  
167  

Maximale Anzahl von Bytes, die für einen zusammenfingierten Lese-E/A-Vorgang gelücket werden können.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>393216</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0-1073741824</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Nein</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows 7</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)

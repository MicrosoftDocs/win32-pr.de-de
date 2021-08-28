---
description: 'Weitere Informationen zu: Ressourcenparameter'
title: Ressourcenparameter
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: a2575f6b6cbdd49380422cb955ad64e246bf6ccf
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984213"
---
# <a name="resource-parameters"></a>Ressourcenparameter


_**Gilt für:** Windows | Windows Server_

## <a name="resource-parameters"></a>Ressourcenparameter

Dieses Thema enthält Parameter, die für Ressourcen verwendet werden.

*JET_paramCachedClosedTables*  
125  

Dieser Parameter steuert die Anzahl der B+-Strukturressourcen, die von der Instanz zwischengespeichert werden, nachdem die von ihnen dargestellten Tabellen von der Anwendung geschlossen wurden.

Große Werte für diesen Parameter bewirken, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, erhöht jedoch die Geschwindigkeit, mit der eine große Anzahl von Tabellen von der Anwendung nach dem Zufallsprinzip geöffnet werden kann. Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>64</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>1 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows Vista und höhere Versionen</p> | 



*JET_paramDisablePerfmon*  
107  

Dieser Parameter kann verwendet werden, um zu verhindern, dass die Datenbank-Engine Daten zur Leistung in Windows veröffentlicht. Dies kann erfolgen, um die Dienstthreadaktivität der Datenbank-Engine zu reduzieren.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>Falsch</p> | 
| <p>Typ:</p> | <p>Boolean</p> | 
| <p>Gültiger Bereich:</p> | <p>False, True</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>No</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows Vista und höhere Versionen</p> | 



*JET_paramGlobalMinVerPages*  
81  

Mit diesem Parameter können Anwendungen, die im Modus mit mehreren Instanzen ausgeführt werden, Speicher für Versionsseiten in einem globalen Pool vorab zuordnen, um das ältere Verhalten zu emulieren. Dies ist nützlich, wenn die Anwendung garantieren möchte, dass Transaktionen einer bestimmten Größe später erfolgreich ausgeführt werden können, auch wenn der Arbeitsspeicher knapp wird.

**Windows 2000:**  Genügend Arbeitsspeicher zum Sichern aller Versionsseiten ist zur [JetInit-Zeit](./jetinit-function.md) immer reserviert.

**Windows XP:**  Ab Windows XP gilt dies auch im Einzelinstanzmodus. Der Versionsseitenspeicher wird jedoch dynamisch zugeordnet, wenn er sich im Modus mit mehreren Instanzen befindet.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>64</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>1 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Nein</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Nein</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Versionen</p> | 



*JET_paramMaxCursors*  
8  

Dieser Parameter reserviert die angeforderte Anzahl von Cursorressourcen für die Verwendung durch eine -Instanz. Eine Cursorressource entspricht direkt einem [JET_TABLEID](./jet-tableid.md) Datentyp. Diese Einstellung wirkt sich darauf aus, wie viele Cursor gleichzeitig verwendet werden können. Eine Cursorressource kann nicht von verschiedenen Sitzungen gemeinsam genutzt werden. Daher muss dieser Parameter auf einen ausreichend großen Wert festgelegt werden, damit jede Sitzung so viele Cursor verwenden kann, wie erforderlich sind.

**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter verbrauchen Adressraum und können die Speicherauslastung erhöhen.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>1024</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>No</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramMaxInstances*  
104  

Dieser Parameter steuert die maximale Anzahl von Instanzen, die in einem einzelnen Prozess erstellt werden können.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>16</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>1-1024</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Nein</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Yes</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und spätere Versionen</p> | 



*JET_paramMaxOpenTables*  
6  

Dieser Parameter reserviert die angeforderte Anzahl von B+-Strukturressourcen für die Verwendung durch eine -Instanz. Diese Einstellung wirkt sich darauf aus, wie viele Tabellen gleichzeitig verwendet werden können. Dieser Parameter muss relativ zum physischen Schema der Datenbanken festgelegt werden, die von der Datenbank-Engine verwendet werden, sodass diese Einstellung nicht so einfach wie möglich ist.

Im Allgemeinen benötigen Sie zwei Ressourcen plus eine Ressource pro sekundärem Index pro Tabelle bei gleichzeitiger Verwendung durch die Anwendung.

**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter verbrauchen Adressraum und können die Speicherauslastung erhöhen.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>300</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>Nein</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramMaxSessions*  
5  

Dieser Parameter reserviert die angeforderte Anzahl von Sitzungsressourcen für die Verwendung durch eine -Instanz. Eine Sitzungsressource [](./jet-sesid.md) entspricht direkt einem JET_SESID-Datentyp. Diese Einstellung wirkt sich darauf aus, wie viele Sitzungen gleichzeitig verwendet werden können.

**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter verbrauchen Adressraum und können die Speicherauslastung erhöhen.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>16</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 30000</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>No</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramMaxTemporaryTables*  
10  

Dieser Parameter reserviert die angeforderte Anzahl temporärer Tabellenressourcen für die Verwendung durch eine -Instanz. Diese Einstellung wirkt sich darauf aus, wie viele temporäre Tabellen gleichzeitig verwendet werden können.

**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter verbrauchen Adressraum und können die Speicherauslastung erhöhen.

**Windows XP und höher:**  Wenn dieser Systemparameter auf 0 (null) festgelegt ist, wird keine temporäre Datenbank erstellt, und jede Aktivität, die die Verwendung der temporären Datenbank erfordert, erzeugt einen Fehler. Diese Einstellung kann nützlich sein, um die E/A zu vermeiden, die zum Erstellen der temporären Datenbank erforderlich ist, wenn bekannt ist, dass sie nicht verwendet wird.

**Hinweis:**  Die Verwendung einer temporären Tabelle erfordert auch eine Cursorressource.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>20</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>No</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramMaxVerPages*  
9  

Dieser Parameter reserviert die angeforderte Anzahl von Versionsspeicherseiten für die Verwendung durch eine -Instanz. Der Versionsspeicher enthält einen Livedatensatz aller verschiedenen Versionen jedes Datensatzes oder Indexeintrags in der Datenbank, die von allen aktiven Transaktionen angezeigt werden können. Diese Versionen werden verwendet, um die Parallelitätssteuerung mit mehreren Versionen zu unterstützen, die von der Datenbank-Engine verwendet wird, um Transaktionen mithilfe der Momentaufnahmeisolation zu unterstützen. Diese Einstellung wirkt sich darauf aus, wie viele Updates gleichzeitig im Arbeitsspeicher gespeichert werden können. Dies wirkt sich entweder auf die maximale Anzahl von Updates aus, die eine einzelne Transaktion ausführen kann, die maximale Dauer, für die eine Transaktion geöffnet gehalten werden kann, die maximale gleichzeitige Last von Updatetransaktionen auf dem System oder eine Kombination dieser Vorgänge.

Jede Mit diesem Parameter konfigurierte Versionsspeicherseite hat eine Größe von 16 KB auf 32-Bit-Computern und 32 KB auf 64-Bit-Computern.

**Windows Vista und höher:**  Die Seitengröße des Versionsspeichers kann über die JET_paramVerPageSize.

**Windows 2000, Windows XP und Windows Server 2003:**  Große Werte für diesen Parameter verbrauchen Adressraum und können die Speicherauslastung erhöhen.

**Hinweis:**  Dies ist bei weitem die am häufigsten von der Datenbank-Engine ausgeschöpfte Ressource. Achten Sie sorgfältig auf die Einstellung des Systemparameters und auf die Transaktionslast der Anwendung, um zu vermeiden, dass diese Ressource im normalen Betrieb erschöpft wird. Wenn diese Ressource erschöpft ist, werden Aktualisierungen der Datenbank mit der JET_errVersionStoreOutOfMemory. Um einige dieser Ressourcen frei zu geben, muss die älteste ausstehende Transaktion abgebrochen werden.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>64</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>1 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Beeinträchtigt die Leistung:</p> | <p>No</p> | 
| <p>Betrifft Ressourcen:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramPageHintCacheSize*  
101  

Dieser Parameter steuert die Größe eines speziellen Caches, der verwendet wird, um die Suche nach untergeordneten B+-Strukturseitenzeern im Datenbankseitencache zu beschleunigen. Die Größe des Caches ist in Bytes.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>262144</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance fest:</a></p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Versionen</p> | 



*JET_paramPreferredMaxOpenTables*  
7  

Dieser Parameter versucht, die Anzahl der verwendeten B+-Strukturressourcen unter dem angegebenen Schwellenwert zu halten.

Wenn dieser Parameter auf 0 (null) festgelegt ist, wird standardmäßig 100 % der **JET_paramMaxOpenTables**.

**Windows Vista und höher:**  Dieser Parameter ist veraltet und wirkt sich nicht auf den Betrieb der Datenbank-Engine aus. Anwendungen sollten stattdessen JET_paramMaxCachedClosedTables verwenden.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>0 (100 % der <strong>JET_paramMaxOpenTables</strong>)</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>0 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramPreferredVerPages*  
63  

Dieser Parameter stellt einen Schwellenwert relativ zu **JET_paramMaxVerPages** dar, der die diskrete Verwendung von Versionsseiten durch die Datenbank-Engine steuert. Wenn die Größe des Versionsspeichers diesen Schwellenwert überschreitet, werden alle Informationen, die nur für optionale Hintergrundtasks verwendet werden, z. B. das Freihalten von gelöschtem Speicherplatz in der Datenbank, nicht beibehalten, um Platz für Transaktionsinformationen zu erhalten.

**Windows 2000 Windows XP und Windows Server 2003:**  Wenn Sie diesen Parameter auf 0 festlegen, wird der Schwellenwert auf 90 % der **JET_paramMaxVerPages** festgelegt.

**Windows Vista und höher:**  Dies wird nicht mehr unterstützt, und der Standardwert dieses Parameters wurde geändert, um sein Verhalten zu verdeutlichen.

Jede version store-Seite, wie von diesem Parameter konfiguriert, hat eine Größe von 16 KB auf 32-Bit-Computern und 32 KB auf 64-Bit-Computern.

**Windows Vista und höher:**  Die Seitengröße des Versionsspeichers kann über JET_paramVerPageSize gelesen und geändert werden.

**Hinweis**  Wenn die Datenbank-Engine zu oft über diesem Schwellenwert arbeitet, kann die Leistung der Datenbank beeinträchtigt werden. Dies liegt daran, dass die Hintergrundprozesse, die die Datenbank bereinigen, ohne die optionalen Informationen, die in diesem Szenario verworfen werden, nicht funktionieren können. Diese Auswirkung wird durch die Online- oder Offlinedefragmentierung beeinträchtigt.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p><strong>Windows 2000, Windows XP und Windows Server 2003:</strong> 0 (90 % der JET_paramMaxVerPages)</p><p><strong>Windows Vista:</strong> 58</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>1 – 2147483647</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>Yes</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Alle</p> | 



*JET_paramVerPageSize*  
128  

Dieser Parameter steuert die Größe der Versionsspeicherseiten, die von der Datenbank-Engine zum Speichern von Transaktionsinformationen verwendet werden. Der Wert dieses Parameters ist die Einheitengröße für alle anderen Systemparameter, die sich auf Versionsseiten (z.B. JET_paramMaxVerPages) bezogen befinden.

Die Datenbank-Engine kann einen größeren Versionsspeicher als angefordert verwenden.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>16384</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p>1024, 2048, 4096, 8192, 16384, 32768, 65536</p> | 
| <p>Umfang:</p> | <p>Global</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Nein</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p>No</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>No</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows Vista und höher</p> | 



*JET_paramVersionStoreTaskQueueMax*  
105  

Dieser Parameter steuert die Anzahl der Arbeitselemente für die Hintergrundbereinigung, die jederzeit in die Warteschlange des Datenbank-Engine-Threadpools eingereiht werden können.


| Bezeichnung | Wert |
|--------|-------|
| <p>Standardwert:</p> | <p>32</p> | 
| <p>Typ:</p> | <p>Integer</p> | 
| <p>Gültiger Bereich:</p> | <p><strong>Windows XP und Windows Server 2003:</strong> 1 – 63</p><p><strong>Windows Vista:</strong> 1 bis 127</p> | 
| <p>Umfang:</p> | <p>Instanz</p> | 
| <p>Legen Sie nach <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>fest:</p> | <p>Yes</p> | 
| <p>Legen Sie nach <a href="gg294068(v=exchg.10).md">JetInit fest:</a></p> | <p><strong>Windows XP und Windows Server 2003:</strong>  Nein</p><p><strong>Windows Vista:</strong>  Ja</p> | 
| <p>Wirkt sich auf das physische Layout aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Zuverlässigkeit aus:</p> | <p>Nein</p> | 
| <p>Wirkt sich auf die Leistung aus:</p> | <p>Yes</p> | 
| <p>Wirkt sich auf Ressourcen aus:</p> | <p>Yes</p> | 
| <p>Verfügbarkeit:</p> | <p>Windows XP und höhere Versionen</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)

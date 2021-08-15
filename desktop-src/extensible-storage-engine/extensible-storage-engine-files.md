---
description: 'Weitere Informationen zu: Erweiterbare Storage-Engine-Dateien'
title: Erweiterbare Storage-Engine-Dateien
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: a955da455cb2a2397010fd7869f6320970ef9f85ac1e1602f4439239dc56b167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118256306"
---
# <a name="extensible-storage-engine-files"></a>Erweiterbare Storage-Engine-Dateien


_**Gilt für:** Windows | Windows Server_

## <a name="extensible-storage-engine-files"></a>Erweiterbare Storage-Engine-Dateien

Die Extensible Storage Engine verwendet die folgenden Dateitypen:

- [Transaktionsprotokolldateien](#transaction-log-files)

- [Temporäre Transaktionsprotokolldateien](#temporary-transaction-log-files)

- [Reservierte Transaktionsprotokolldateien](#reserved-transaction-log-files)

- [Prüfpunktdateien](#checkpoint-files)

- [Datenbankdateien](#database-files)

- [Temporäre Datenbanken](#temporary-databases)

- [Leeren von Zuordnungsdateien](#flush-map-files)

Diese Tabelle enthält eine Übersicht über die Datendateinamen, die von ESE verwaltet werden. Für Windows Vista und höher wirkt sich die einstellung JET_paramLegacyNames auf die verwendeten Dateinamen aus.

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p>Betriebssystem</p>
    </th>
    <th>
      <p>Windows Server 2003 und früher<br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p>Windows Vista und höher (Client) <br />
Windows Server 2008 und höher (Server)
</p>
    </th>
    <th>
      <p>Windows 10 Anniversary Update und höher (Client) <br />
Windows Server 2016 und höher (Server)
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p>
        <strong>einstellung für JET_paramLegacyNames</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>N/A</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>Keine</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>JET_bitESE98FileNames</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>Identisch mit Windows Vista/Server 2008</strong>
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <p>Aktuelles Protokoll</p>
    </td>
    <td>
      <p>&lt;inst &gt; .log</p>
    </td>
    <td>
      <p>&lt;inst &gt; .jtx</p>
    </td>
    <td>
      <p>&lt;inst &gt; .log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Präinitierungsprotokoll</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp.log</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp.jtx</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp.log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Rotierte Protokolle</p>
    </td>
    <td>
      <p>&lt;inst &gt; XXXXX.log</p>
    </td>
    <td>
      <p>&lt;inst &gt; XXXXX.jtx nach dem Wechsel von FFFFF zu &lt; inst &gt; XXXXXXXX.jtx</p>
    </td>
    <td>
      <p>&lt;inst &gt; XXXXX.log nach dem Wechsel von FFFFF zu &lt; inst &gt; XXXXXXXX.log.</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Prüfpunktdateien</a>
      </p>
    </td>
    <td>
      <p>&lt;inst &gt; .chk</p>
    </td>
    <td>
      <p>&lt;inst &gt; .jcp</p>
    </td>
    <td>
      <p>&lt;inst &gt; .chk</p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Temporäre Datenbanken</a>
      </p>
    </td>
    <td>
      <p>&lt;temp db file name &gt; Default: tmp.edb</p>
    </td>
    <td>
      <p>&lt;temp db file name &gt; Default: tmp.edb</p>
    </td>
    <td>
      <p>&lt;temp db file name &gt; Default: tmp.edb</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Reservierte Transaktionsprotokolldateien</a>
      </p>
    </td>
    <td>
      <p>res1.log &amp; res2.log</p>
    </td>
    <td>
      <p>&lt;inst &gt; RESXXXXX.jrs</p>
    </td>
    <td colspan="2">
      <p>&lt;inst &gt; RESXXXXX.jrs</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Datenbankdateien</a>
      </p>
    </td>
    <td>
      <p>&lt;Db-Dateiname&gt;</p>
    </td>
    <td>
      <p>&lt;Db-Dateiname&gt;</p>
    </td>
    <td>
      <p>&lt;Db-Dateiname&gt;</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Leeren von Zuordnungsdateien</a>
      </p>
    </td>
    <td>
      <p>–</p>
    </td>
    <td>
      <p>–</p>
    </td>
    <td>
      <p>–</p>
    </td>
    <td>
      <p>&lt;DB-Dateiname ohne Erweiterung &gt; ".jfm"</p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a>Transaktionsprotokolldateien

Transaktionsprotokolldateien enthalten Vorgänge für Datenbankdateien. Sie enthalten genügend Informationen, um eine Datenbank nach einer unerwarteten Prozessbeendigung oder dem Herunterfahren des Systems in einen logisch konsistenten Zustand zu bringen.

Die Namen der Protokolldateien hängen von einem dreibuchstabigen Basisnamen ab, der mit [JET_paramBaseName](./transaction-log-parameters.md)festgelegt werden kann. In den folgenden Beispielen wird der Basisname "edb" verwendet, da dies der Standardbasisname ist. Die Erweiterung für die Transaktionsprotokolldateien ist entweder LOG oder JTX, je nachdem, ob die JET_bitESE98FileNames im JET_paramLegacyFileNames Parameter festgelegt ist. Weitere Informationen finden Sie unter [Erweiterbare Storage-Engine-Systemparameter.](./extensible-storage-engine-system-parameters.md)

Transaktionsprotokolldateien heißen \<base\> \<generation-number\> .log, beginnend mit 1. Die Protokollgenerierungsnummer hat das Hexadezimalformat. Beispielsweise ist edb00001.log das erste Protokoll und edb000ff.log das 255. Protokoll. Die Protokolldateien enthalten fünf Hexadezimalziffern im Protokolldateinamen, bis zur 1048576. Protokolldatei, ab der die Protokolldateien in einem 11.3-Format benannt werden (z.B. edb00100000.log). \<base\>.log ist immer die Protokolldatei, die derzeit verwendet wird. Wenn die Datenbank-Engine nicht aktiv ist, kann die Generierung von edb.log mit dem folgenden Befehl identifiziert werden: **esentutl.exe -ml edb.log**.

Transaktionsprotokolldateien verfügen zwar über . Log-Erweiterungen, die häufig Textdateien zugeordnet sind, liegen in einem Binärformat vor und sollten niemals von einem Benutzer bearbeitet werden. Datenbankvorgänge werden zuerst in das Protokoll geschrieben. Die Daten können später in die Datenbankdatei geschrieben werden. möglicherweise sofort, möglicherweise viel später. Im Falle eines unerwarteten Prozesses oder einer unerwarteten Systembeendigung sind die Vorgänge weiterhin in den Protokolldateien vorhanden, und für unvollständige Transaktionen kann ein Rollback ausgeführt werden. Die Wiedergabe von Transaktionsprotokolldateien wird als *soft recovery* bezeichnet und erfolgt automatisch, wenn [JetInit](./jetinit-function.md) oder [JetInit2](./jetinit2-function.md) aufgerufen wird. Die weiche Wiederherstellung kann auch manuell mit der Option "-r" des Esentutl.exe Programms ausgeführt werden. Das Wiedergeben von Transaktionsprotokolldateien in einer Datenbank, die aus einer Sicherung wiederhergestellt wird, wird als *harte Wiederherstellung* bezeichnet.

Protokolldateien haben eine feste Größe und können mit [JET_paramLogFileSize](./transaction-log-parameters.md)angepasst werden. Wenn die aktuelle Protokolldatei (d.h. edb.log) gefüllt wird, wird sie \<base\> \<generation-number\> in .log umbenannt, und im Transaktionsprotokollstream wird eine neue Transaktionsprotokolldatei benötigt.

Jeder Datenbankinstanz ist eine einzelne Protokolldateisequenz zugeordnet. Windows XP hat [JetCreateInstance](./jetcreateinstance-function.md)eingeführt, sodass mehrere Sequenzen von Transaktionsprotokolldateien von einem einzelnen Prozess verwendet werden können. Mehrere Transaktionsprotokolldateisequenzen können jedoch nicht im gleichen Verzeichnis vorhanden sein.

Transaktionsprotokolldateien sollten fast nie manuell bearbeitet, umbenannt, verschoben oder gelöscht werden, da datenbeschädigungen entstehen können.

Transaktionsprotokolldateien werden von der Datenbank-Engine während einer vollständigen Sicherung gelöscht (siehe [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)) oder während des normalen Betriebs, wenn die zirkuläre Protokollierung aktiviert ist.

Nachdem eine Transaktionsprotokolldatei aufgefüllt wurde, muss die Datenbank-Engine eine neue Protokolldatei erstellen. Die zirkuläre Protokollierung ist ein Mittel, mit dem Protokolldateien automatisch von der Datenbank-Engine bereinigt werden können, wenn sie für die Wiederherstellung nach Einem Absturz nicht mehr benötigt werden. Dieser Prozess ist eine Alternative zum Entfernen von Protokolldateien als Nebenprodukt der Durchführung einer Sicherung. Die zirkuläre Protokollierung kann mit dem [JET_paramCircularLog](./transaction-log-parameters.md) Systemparameter gesteuert werden. Transaktionsprotokolldateien sollten nicht mit einer anderen Methode gelöscht werden.

### <a name="temporary-transaction-log-files"></a>Temporäre Transaktionsprotokolldateien

Wenn edb.log voll ist, muss ESE eine neue Datei erstellen. Die neue Protokolltransaktionsdatei wird vor der Verwendung durch ESE als temporäre Transaktionsprotokolldatei bezeichnet.

Während eine neue Protokolldatei erstellt und ihre Größe erweitert wird, wird sie \<base\> als tmp.log bezeichnet. Das Erstellen einer neuen Datei kann ein potenziell kostspieliger Vorgang sein, sodass ESE die nächste Protokolldatei proaktiv als Hintergrundaufgabe erstellt.

Da die temporäre Transaktionsprotokolldatei in Erwartung der Notwendigkeit einer neuen Transaktionsprotokolldatei erstellt wird, enthält sie keine nützlichen Informationen.

### <a name="reserved-transaction-log-files"></a>Reservierte Transaktionsprotokolldateien

Die reservierten Transaktionsprotokolldateien werden erstellt, wenn die Engine damit beginnt, wichtige Vorgänge zu protokollieren, um ein sauberes Herunterfahren zu ermöglichen.

**Windows Vista:** In Windows Vista und höher heißen die reservierten Transaktionsprotokolldateien \<base\> RESXXXXX.jrs.

**Windows Server 2003:** In Windows Server 2003 und früher heißen die reservierten Transaktionsprotokolldateien res1.log und res2.log.

Wenn der Datenbank-Engine nicht genügend Speicherplatz zur Verfügung steht, kann keine neue Protokolldatei erstellt werden. Die sicherste Möglichkeit besteht darin, das Herunterfahren sauber durchzuführen, aber einige Vorgänge (z. B. Rollbackvorgänge) müssen weiterhin protokolliert werden. Die meisten Datenbankvorgänge schlagen während dieser Phase fehl.

Da die reservierten Transaktionsprotokolldateien in Erwartung der Notwendigkeit von Transaktionsprotokolldateien in einem Out-of-Disk-Szenario erstellt werden, enthalten sie keine nützlichen Informationen.

### <a name="checkpoint-files"></a>Prüfpunktdateien

In der Prüfpunktdatei wird der Prüfpunkt für eine bestimmte Transaktionsprotokolldateisequenz gespeichert. Die Prüfpunktdatei hat den Namen \<base\> CHK oder \<base\> JCP, je nachdem, ob die JET_bitESE98FileNames im JET_paramLegacyFileNames Parameter festgelegt ist und ihr Speicherort durch [JET_paramSystemPath](./transaction-log-parameters.md)angegeben wird.

Datenbankvorgänge werden zuerst in die Protokolldateien geschrieben und dann im Arbeitsspeicher zwischengespeichert. Zu einem späteren Zeitpunkt werden die Vorgänge in die Datenbankdatei geschrieben, aber aus Leistungsgründen stimmt die Reihenfolge, in der Vorgänge in die Datenbankdatei geschrieben werden, möglicherweise nicht mit der Reihenfolge überein, in der sie ursprünglich protokolliert wurden. Vorgänge, die in die Transaktionsprotokolldatei geschrieben werden, haben einen von zwei Zuständen:

  - Wird in die Transaktionsprotokolldatei und die Datenbankdatei geschrieben.

  - Wird in die Transaktionsprotokolldatei geschrieben und noch nicht in die Datenbankdatei geschrieben.

Viele Datenbankvorgänge können in einer einzelnen Transaktionsprotokolldatei gespeichert werden. Eine bestimmte Protokolldatei kann aus den folgenden Elementen bestehen:

  - Alle In die Datenbankdatei geschriebenen Vorgänge.

  - Keine In die Datenbankdatei geschriebenen Vorgänge

  - Eine Mischung aus Vorgängen, die in die Datenbankdatei geschrieben wurden, und Vorgängen, die noch nicht in die Datenbankdatei geschrieben wurden.

Der Prüfpunkt bezieht sich auf den Zeitpunkt im Transaktionsprotokollstream, zu dem alle Vorgänge vor dem Prüfpunkt in die Datenbankdatei geschrieben wurden. Es gibt keine Garantie für die Vorgänge, die nach dem Prüfpunkt auftreten. einige befinden sich möglicherweise im Arbeitsspeicher, und einige werden möglicherweise in die Datenbank geschrieben.

Da alle Vorgänge in den Protokolldateien vor dem Prüfpunkt in der Datenbankdatei dargestellt werden, werden nur die Transaktionsprotokolldateien nach dem Prüfpunkt für die soft recovery benötigt, um eine bestimmte Datenbank in einen fehlerfreien Zustand zu bringen.

### <a name="database-files"></a>Datenbankdateien

Die Datenbankdatei enthält das Schema für alle Tabellen in der Datenbank, die Datensätze für alle Tabellen in der Datenbank und die Indizes für die Tabellen. Der Speicherort wird mit [JetCreateDatabase,](./jetcreatedatabase-function.md) [JetCreateDatabase2,](./jetcreatedatabase2-function.md) [JetAttachDatabase](./jetattachdatabase-function.md)oder [JetAttachDatabase2](./jetattachdatabase2-function.md)angegeben.

Eine Datenbank wird erst nach einem erfolgreichen Aufruf von [JetTerm](./jetterm-function.md) oder [JetTerm2](./jetterm2-function.md)sauber heruntergefahren.

Das Esentutl.exe Programm kann erkennen, ob eine Datenbank mit der Option "-mh" sauber heruntergefahren wird. Beispielsweise liest "esentutl.exe -mh sample.edb" den Datenbankheader einer Datenbank mit dem Namen sample.edb und gibt den Status von sample.edb aus. Sie kann "Status: Clean Shutdown" oder "State: Dirty Shutdown" (Zustand: Dirty Shutdown) ausdrucken.

Eine Datenbank, die nicht sauber heruntergefahren wurde, befindet sich im Zustand "Dirty Shutdown". Vor Windows XP wurde dieser Zustand als *inkonsistent* bezeichnet. Eine geänderte (inkonsistente) Datenbank kann mit der weichen Wiederherstellung in einen fehlerfreien Zustand gebracht werden. Eine beschädigte Datenbank ist nicht identisch mit einer geänderten ("inkonsistenten") Datenbank.

Eine beschädigte Datenbank bezieht sich auf eine physische oder logische Beschädigung und kann nicht mit der weichen Wiederherstellung behoben werden. Physische Beschädigungen können Bitumkehren sein, die häufig von den Prüfsummen auf den Datenbankseiten abgefangen werden. Eine fehlerhafte Prüfsumme in einer Datenbankdatei wird als JET_errReadVerifyFailure Fehler angezeigt.

Datenbanken können nur sauber heruntergefahren werden, um sie sicher zu verschieben oder umzubenennen. Wenn eine Datenbank nicht sauber heruntergefahren wurde, kann sie nicht automatisch sicher verschoben oder umbenannt werden.

Mehrere Datenbanken können einer einzelnen Transaktionsprotokolldateisequenz zugeordnet werden.

### <a name="temporary-databases"></a>Temporäre Datenbanken

Die temporäre Datenbank wird als Unterstützungsspeicher für verlockbare Zwecke und auch beim Erstellen von Indizes verwendet.

Name und Speicherort werden mit [JET_paramTempPath](./temporary-database-parameters.md)konfiguriert.

Verlockbare Funktionen werden mit [JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2,](./jetopentemptable2-function.md) [JetOpenTempTable3,](./jetopentemptable3-function.md) [JetOpenTemporaryTable](./jetopentemporarytable-function.md)erstellt. Sie werden auch von einigen API-Aufrufen erstellt und verwendet, um Schemainformationen zurückzugeben (z. B. [JetGetIndexInfo](./jetgetindexinfo-function.md)).

## <a name="flush-map-files"></a>Leeren von Zuordnungsdateien

Ab Windows 10 Anniversary Update (Client) und Windows Server 2016 (Server) hat ESE ein zusätzliches Maß an Schutz vor verlorenen Schreibvorgängen (oder verlorenen Leerungen) 1 hinzugefügt, sodass es solche Ereignisse prozessübergreifend neu initialisieren kann2. Dieses Feature erfordert das Beibehalten von Metadaten in einer separaten Datei, die als "Flush Map"-Datei bezeichnet wird.

Eine Flush Map-Datei wird für jede Datenbankdatei erstellt und befindet sich im gleichen Verzeichnis. Die Datei wird ähnlich wie die Datenbankdatei benannt, jedoch mit einer anderen Erweiterung. Wenn die Clientanwendung beispielsweise eine Datenbank mit dem vollständigen Pfad C: \\ MyDirectory \\ MyDabatase.edb erstellt, lautet die entsprechende Leerungszuordnungsdatei C: \\ MyDirectory \\ MyDabatase.jfm.

Durch diese Erweiterung werden zwei Anforderungen für den Namen von Datenbankdateien eingeführt:

  - Zwei Datenbanken im selben Verzeichnis dürfen nicht denselben Dateinamen mit unterschiedlichen Erweiterungen aufweisen. Beispiel: C: \\ MyDirectory \\ MyDabatase.db1 und C: \\ MyDirectory \\ MyDabatase.db2.

  - 2\. Eine Datenbank darf keine JFM-Erweiterung aufweisen.

Wenn Sie eine Datenbankdatei manuell kopieren oder verschieben, sollte die entsprechende Leerungszuordnungsdatei ebenfalls kopiert oder in dasselbe Zielverzeichnis verschoben werden. Wenn zum Zeitpunkt einer neuen Datenbankanfügung keine Zuordnungsdatei zum Leeren vorhanden ist (über [JetAttachDatabase),](./jetattachdatabase-function.md)wird eine neue erstellt und bei Bedarf erneut aufgefüllt, wenn Seiten aus der Datenbank eingelesen werden. Das Mischen von nicht übereinstimmenden Datenbank- und Leerenzuordnungsdateien wird von ESE verarbeitet und erzwingt, dass die nicht übereinstimmende Leerungszuordnung von Grund auf gelöscht und neu erstellt wird.

Die Größe einer Flush Map-Datei ist direkt proportional zur zugeordneten Datenbankdatei und ungefähr gleich (alle Größen in Bytes, ergebnis muss auf das nächste Vielfache von 8.192 aufgerundet werden):

`8,192 + ((<database file size> / <database page size>) / 4)`

Beispiel: Für eine 1,5 GB große Datenbank mit einer Seitengröße von 32 KB beträgt die ungefähre Größe der Leerungszuordnung 24.576 Bytes (oder 24 KB).

Die Zuordnungsdatei zum Leeren muss aktualisiert werden, wenn Datenbankseiten geleert werden. Wenn die Transaktionsprotokollierung aktiviert ist (z. [B. JET_paramRecovery](./transaction-log-parameters.md) auf "on" (Standardeinstellung) festgelegt ist), wird die Aktualisierung der Leerungszuordnung durchgeführt, wenn die Clientanwendung Änderungen an der Datenbank vornimmt. Im Durchschnitt wird die gesamte Leerungszuordnung einmal pro 20 % der [generierten JET_paramCheckpointDepthMax](./database-cache-parameters.md) (in Bytes) von Transaktionsprotokollen auf die nicht flüchtigen Medien geschrieben. Die Anzahl der Schreibvorgänge hängt davon ab, wie die Änderungen in der gesamten Datenbank verteilt sind. Es handelt sich jedoch höchstens um ungefähr (alle Größen in Bytes):

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

Wenn die Transaktionsprotokollierung deaktiviert ist (z. [B. JET_paramRecovery](./transaction-log-parameters.md) auf "off" festgelegt), wird die Leerungszuordnung nur einmal aktualisiert, wenn die Datenbank explizit sauber getrennt wird (über [JetDetachDatabase](./jetdetachdatabase-function.md)oder implizit getrennt, indem die zugeordnete ESE-Instanz beendet wird (über eine der [JetTerm-Funktionen,](./jetterm-function.md) solange [JET_bitTermDirty](./jetterm2-function.md) nicht übergeben wird).

1 Ein verlorener Schreibvorgang (oder verlorene Leerung) wird als Schreibvorgang definiert, der erfolgreich vom Betriebssystem an die ESE-Datenbank-Engine zurückgegeben wird, die tatsächlichen Daten jedoch nie in der Datenbankdatei auf den nicht flüchtigen Medien beibehalten werden. Er wird in der Regel durch einen fehlerhaften oder falsch konfigurierten Speicherstapel (Software oder Hardware) verursacht. Clientanwendungen erhalten möglicherweise einen [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) Fehler von ESE-Funktionen, die das Lesen von Daten aus der Datenbank erfordern, wenn sich die Daten in einer Region befinden, in der ein Verlust des Schreibereignisses verhindert wird.

2 Die Fähigkeit, verlorene Schreibvorgänge innerhalb der Lebensdauer eines Prozesses zu erkennen, ist seit Windows 8 (Client) und Windows Server 2012 (Server) vorhanden.

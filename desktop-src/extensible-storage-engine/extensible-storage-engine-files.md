---
description: Weitere Informationen zu Extensible Storage Engine-Dateien
title: Extensible Storage Engine-Dateien
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: c27bb0104c5923496c5dd7962ef4a9bacdc90af4
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355126"
---
# <a name="extensible-storage-engine-files"></a>Extensible Storage Engine-Dateien


_**Gilt für:** Windows | Windows Server_

## <a name="extensible-storage-engine-files"></a>Extensible Storage Engine-Dateien

Die Extensible Storage-Engine verwendet die folgenden Dateitypen:

- [Transaktionsprotokoll Dateien](#transaction-log-files)

- [Temporäre Transaktionsprotokoll Dateien](#temporary-transaction-log-files)

- [Reservierte Transaktionsprotokoll Dateien](#reserved-transaction-log-files)

- [Prüfpunktdateien](#checkpoint-files)

- [Datenbankdateien](#database-files)

- [Temporäre Datenbanken](#temporary-databases)

- [Zuordnungs Dateien leeren](#flush-map-files)

Diese Tabelle enthält eine Übersicht über die Namen der Datendateien, die von ESE verwaltet werden. Für Windows Vista und höher wirkt sich die JET_paramLegacyNames Einstellung auf die verwendeten Dateinamen aus.

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
        <strong>JET_paramLegacyNames Einstellung</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>nicht zutreffend</strong>
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
      <p>&lt;"Inst &gt; . log"</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . JTX</p>
    </td>
    <td>
      <p>&lt;"Inst &gt; . log"</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Pre-init-Protokoll</p>
    </td>
    <td>
      <p>&lt;Inst &gt; tmp. log</p>
    </td>
    <td>
      <p>&lt;Inst &gt; tmp. JTX</p>
    </td>
    <td>
      <p>&lt;Inst &gt; tmp. log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Gedrehte Protokolle</p>
    </td>
    <td>
      <p>&lt;Inst &gt; XXXXX. log</p>
    </td>
    <td>
      <p>&lt;Inst &gt; XXXXX. JTX nach FFFFF wechseln zu &lt; inst &gt; xxxxxxxx. JTX</p>
    </td>
    <td>
      <p>&lt;Inst &gt; XXXXX. log nach FFFFF wechselt zu &lt; inst &gt; xxxxxxxx. log.</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Prüf Punkt Dateien</a>
      </p>
    </td>
    <td>
      <p>&lt;Inst &gt; . chk</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . JCP</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . chk</p>
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
      <p>&lt;Temp DB-Dateiname &gt; Standard: tmp. edb</p>
    </td>
    <td>
      <p>&lt;Temp DB-Dateiname &gt; Standard: tmp. edb</p>
    </td>
    <td>
      <p>&lt;Temp DB-Dateiname &gt; Standard: tmp. edb</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Reservierte Transaktionsprotokoll Dateien</a>
      </p>
    </td>
    <td>
      <p>Res1. log &amp; Res2. log</p>
    </td>
    <td>
      <p>&lt;Inst &gt; resxxxxx. jrs</p>
    </td>
    <td colspan="2">
      <p>&lt;Inst &gt; resxxxxx. jrs</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Datenbankdateien</a>
      </p>
    </td>
    <td>
      <p>&lt;DB-Dateiname&gt;</p>
    </td>
    <td>
      <p>&lt;DB-Dateiname&gt;</p>
    </td>
    <td>
      <p>&lt;DB-Dateiname&gt;</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Zuordnungs Dateien leeren</a>
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
      <p>&lt;DB-Dateiname ohne Erweiterung &gt; . JFM</p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a>Transaktionsprotokoll Dateien

Transaktionsprotokoll Dateien enthalten Vorgänge für Datenbankdateien. Sie enthalten ausreichend Informationen, um eine Datenbank nach einem unerwarteten Prozess Abbruch oder dem Herunterfahren des Systems in einen logisch konsistenten Zustand zu bringen.

Die Namen der Protokolldateien sind abhängig von einem aus drei Buchstaben bestehenden Basisnamen, der mit [JET_paramBaseName](./transaction-log-parameters.md)festgelegt werden kann. In den folgenden Beispielen wird der Basisname "edb" verwendet, da dies der Standard Basisname ist. Die Erweiterung für die Transaktionsprotokoll Dateien ist entweder ". log" oder ". JTX", je nachdem, ob die JET_bitESE98FileNames im JET_paramLegacyFileNames Parameter festgelegt ist. Weitere Informationen finden Sie unter [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md).

Die Transaktionsprotokoll Dateien heißen \<base\> \<generation-number\> . log, beginnend mit 1. Die Protokoll Generierungs Nummer weist das Hexadezimal Format auf. Beispielsweise ist "Edb00001. log" das erste Protokoll, und "edb000ff. log" ist das 255. log. Die Protokolldateien enthalten fünf hexadezimal Ziffern im Protokoll Dateinamen, bis die Protokolldatei 1048576th lautet. zu diesem Zeitpunkt werden die Protokolldateien in einem 11,3-Format (z. b. edb00100000. log) benannt. \<base\>. log ist immer die Protokolldatei, die zurzeit verwendet wird. Wenn die Datenbank-Engine nicht aktiv ist, kann die Generierung von EDB. log mithilfe des folgenden Befehls identifiziert werden: **esentutl.exe-ml EDB. log**.

Obwohl die Transaktionsprotokoll Dateien über das verfügen. Protokoll Erweiterungen, die häufig mit Textdateien verknüpft sind, haben Transaktionsprotokoll Dateien ein binäres Format und sollten nie von einem Benutzer bearbeitet werden. Daten Bank Vorgänge werden zuerst in das Protokoll geschrieben. Die Daten können später in die Datenbankdatei geschrieben werden. möglicherweise direkt, möglicherweise viel später. Bei unerwartetem Prozess oder System Abbruch sind die Vorgänge weiterhin in den Protokolldateien vorhanden, und für unvollständige Transaktionen kann ein Rollback ausgeführt werden. Der Vorgang der Wiedergabe von Transaktionsprotokoll Dateien wird als *Weiche Wiederherstellung* bezeichnet und wird automatisch durchgeführt, wenn [jetinit](./jetinit-function.md) oder [JetInit2](./jetinit2-function.md) aufgerufen wird. Die weiche Wiederherstellung kann auch manuell mit der Option "-r" des Esentutl.exe Programms ausgeführt werden. Der Vorgang der Wiedergabe von Transaktionsprotokoll Dateien in einer Datenbank, die aus einer Sicherung wieder hergestellt wird, wird als "feste *Wiederherstellung*" bezeichnet.

Protokolldateien haben eine mit [JET_paramLogFileSize](./transaction-log-parameters.md)anpassbare Größe. Wenn die aktuelle Protokolldatei (d. h. edb. log) ausgefüllt wird, wird Sie in \<base\> \<generation-number\> Log umbenannt, und eine neue Transaktionsprotokoll Datei wird im Transaktionsprotokoll Datenstrom benötigt.

Jeder Daten Bank Instanz ist eine einzelne Protokolldatei Sequenz zugeordnet. In Windows XP wurde [jetkreateinstance](./jetcreateinstance-function.md)eingeführt, sodass mehrere Transaktionsprotokoll-Datei Sequenzen von einem einzelnen Prozess verwendet werden können. Mehrere Transaktionsprotokoll-Datei Sequenzen können jedoch nicht im selben Verzeichnis vorhanden sein.

Transaktionsprotokoll Dateien sollten nie manuell bearbeitet, umbenannt, verschoben oder gelöscht werden, da Daten Beschädigungen entstehen können.

Transaktionsprotokoll Dateien werden von der Datenbank-Engine während einer vollständigen Sicherung (siehe [JetBackup](./jetbackup-function.md), [jettruneurelog](./jettruncatelog-function.md), [jettruneureloginstance](./jettruncateloginstance-function.md)) oder während des normalen Betriebs gelöscht, wenn die zirkuläre Protokollierung aktiviert ist.

Nachdem eine Transaktionsprotokoll Datei aufgefüllt wurde, muss die Datenbank-Engine eine neue Protokolldatei erstellen. Die zirkuläre Protokollierung ist eine Methode, mit der Protokolldateien von der Datenbank-Engine automatisch bereinigt werden können, wenn Sie für die Wiederherstellung von Abstürzen nicht mehr benötigt werden. Dieser Prozess ist eine Alternative zum Entfernen von Protokolldateien als ein Produkt, das eine Sicherung ausführt. Die zirkuläre Protokollierung kann mit dem [JET_paramCircularLog](./transaction-log-parameters.md) System-Parameter gesteuert werden. Transaktionsprotokoll Dateien sollten nicht mit einer anderen Methode gelöscht werden.

### <a name="temporary-transaction-log-files"></a>Temporäre Transaktionsprotokoll Dateien

Wenn Edb. log auffüllt, muss ESE eine neue Datei erstellen. Die neue Protokoll Transaktions Datei wird vor deren Verwendung durch ESE als temporäre Transaktionsprotokoll Datei bezeichnet.

Während eine neue Protokolldatei erstellt und ihre Größe erweitert wird, wird Sie als " \<base\> tmp. log" bezeichnet. Das Erstellen einer neuen Datei kann ein potenziell kostspieliger Vorgang sein, sodass die nächste Protokolldatei von ESE proaktiv als Hintergrundaufgabe erstellt wird.

Da die temporäre Transaktionsprotokoll Datei vor dem Bedarf an einer neuen Transaktionsprotokoll Datei erstellt wird, enthält Sie keine nützlichen Informationen.

### <a name="reserved-transaction-log-files"></a>Reservierte Transaktionsprotokoll Dateien

Die reservierten Transaktionsprotokoll Dateien werden erstellt, wenn die Engine startet, um zu ermöglichen, dass wichtige Vorgänge protokolliert werden, um ein sauberes Herunterfahren zu ermöglichen.

**Windows Vista:** In Windows Vista und höher haben die reservierten Transaktionsprotokoll Dateien den Namen \<base\> resxxxxx. jrs.

**Windows Server 2003:** In Windows Server 2003 und früheren Versionen haben die reservierten Transaktionsprotokoll Dateien den Namen "Res1. log" und "Res2. log".

Wenn die Datenbank-Engine nicht über genügend Speicherplatz verfügt, kann Sie keine neue Protokolldatei erstellen. Der sicherste Vorgang ist das ordnungsgemäße Herunterfahren, aber einige Vorgänge (z. b. Rollback-Vorgänge) müssen weiterhin protokolliert werden. Die meisten Daten Bank Vorgänge schlagen in dieser Phase fehl.

Da die reservierten Transaktionsprotokoll Dateien im Hinblick auf den Bedarf an Transaktionsprotokoll Dateien in einem Szenario ohne Datenträger erstellt werden, enthalten Sie keine nützlichen Informationen.

### <a name="checkpoint-files"></a>Prüfpunktdateien

In der Prüf Punkt Datei wird der Prüfpunkt für eine bestimmte Transaktionsprotokoll-Datei Sequenz gespeichert. Die Prüf Punkt Datei hat den Namen " \<base\> . chk" oder " \<base\> . JCP", je nachdem, ob die JET_bitESE98FileNames im JET_paramLegacyFileNames Parameter festgelegt ist und der Speicherort von [JET_paramSystemPath](./transaction-log-parameters.md)angegeben wird.

Daten Bank Vorgänge werden zunächst in die Protokolldateien geschrieben und dann im Arbeitsspeicher zwischengespeichert. Zu einem späteren Zeitpunkt werden die Vorgänge in die Datenbankdatei geschrieben, aber aus Leistungsgründen entspricht die Reihenfolge, in der die Vorgänge in die Datenbankdatei geschrieben werden, möglicherweise nicht der Reihenfolge, in der Sie ursprünglich protokolliert wurden. In die Transaktionsprotokoll Datei geschriebene Vorgänge befinden sich in einem von zwei Zuständen:

  - Wird in die Transaktionsprotokoll Datei und die Datenbankdatei geschrieben.

  - Wird in die Transaktionsprotokoll Datei geschrieben und noch nicht in die Datenbankdatei geschrieben.

Viele Daten Bank Vorgänge können in einer einzelnen Transaktionsprotokoll Datei gespeichert werden. Eine bestimmte Protokolldatei kann aus den folgenden Elementen bestehen:

  - Alle Vorgänge, die in die Datenbankdatei geschrieben werden.

  - Es wurden keine Vorgänge in die Datenbankdatei geschrieben.

  - Eine Mischung aus Vorgängen, die in die Datenbankdatei geschrieben wurden, und Vorgänge, die noch nicht in die Datenbankdatei geschrieben

Der Prüfpunkt bezieht sich auf den Zeitpunkt im Transaktionsprotokoll-Stream, in dem alle Vorgänge vor dem Prüfpunkt in die Datenbankdatei geschrieben wurden. Es gibt keine Garantie für die Vorgänge, die nach dem Prüfpunkt stattfinden. Einige können sich im Arbeitsspeicher befinden, und einige könnten in die Datenbank geschrieben werden.

Da alle Vorgänge in den Protokolldateien vor dem Prüfpunkt in der Datenbankdatei dargestellt werden, sind nur die Transaktionsprotokoll Dateien nach dem Prüfpunkt für die weiche Wiederherstellung erforderlich, um eine bestimmte Datenbank in einen fehlerfreien Zustand zu bringen.

### <a name="database-files"></a>Datenbankdateien

Die Datenbankdatei enthält das Schema für alle Tabellen in der Datenbank, die Datensätze für alle Tabellen in der Datenbank und die Indizes für die Tabellen. Der Speicherort wird mithilfe von [jetkreatedatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [jetattachdatabase](./jetattachdatabase-function.md)oder [JetAttachDatabase2](./jetattachdatabase2-function.md)angegeben.

Eine Datenbank wird ordnungsgemäß heruntergefahren, wenn [jetterm](./jetterm-function.md) oder [JetTerm2](./jetterm2-function.md)erfolgreich aufgerufen wurde.

Das Esentutl.exe Programm kann erkennen, ob eine Datenbank mit der Option "-MH" ordnungsgemäß heruntergefahren wird. Beispielsweise liest "esentutl.exe-MH Sample. edb" den Daten Bank Header einer Datenbank mit dem Namen Sample. edb und druckt den Status von Sample. edb. Möglicherweise wird "State: Clean Shutdown" oder "State: Dirty Shutdown" gedruckt.

Eine Datenbank, die nicht ordnungsgemäß heruntergefahren wurde, befindet sich in einem fehlerhaften Zustand für das Herunterfahren. Vor Windows XP wurde dieser Status als *inkonsistent* bezeichnet. Eine modifizierte (inkonsistente) Datenbank kann mit weicher Wiederherstellung in einen fehlerfreien Zustand versetzt werden. Eine beschädigte Datenbank ist nicht mit einer geänderten ("inkonsistenten") Datenbank identisch.

Eine beschädigte Datenbank bezieht sich auf eine physische oder logische Beschädigung und kann nicht durch eine weiche Wiederherstellung behoben werden. Physische Beschädigungen können bitflips sein, die häufig von den Prüfsummen auf den Datenbankseiten abgefangen werden. Eine fehlgeschlagene Prüfsumme in einer Datenbankdatei manifestiert sich als JET_errReadVerifyFailure Fehler.

Nur sauber Herunterfahren Datenbanken können problemlos verschoben oder umbenannt werden. Wenn eine Datenbank nicht ordnungsgemäß heruntergefahren wurde, kann Sie nicht automatisch verschoben oder umbenannt werden.

Mehrere Datenbanken können einer einzelnen Transaktionsprotokoll-Datei Sequenz zugeordnet werden.

### <a name="temporary-databases"></a>Temporäre Datenbanken

Die temporäre Datenbank wird als Sicherungs Speicher für temptables verwendet und auch beim Erstellen von Indizes verwendet.

Name und Speicherort werden mit [JET_paramTempPath](./temporary-database-parameters.md)konfiguriert.

Temptables werden mit [jetopertemptable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [jetopumtemporarytable](./jetopentemporarytable-function.md)erstellt. Sie werden auch durch einige API-Aufrufe erstellt und zum Zurückgeben von Schema Informationen verwendet (z. b. [jetgetindexinfo](./jetgetindexinfo-function.md)).

## <a name="flush-map-files"></a>Zuordnungs Dateien leeren

Ab Windows 10 Anniversary Update (Client) und Windows Server 2016 (Server) wurde von ESE ein zusätzliches Maß an Schutz vor verlorenen Schreibvorgängen (oder verlorenen Leerungen) 1 hinzugefügt, sodass solche Ereignisse prozessübergreifende reinitialization2 erkannt werden können. Diese Funktion erfordert, dass Metadaten in einer separaten Datei gespeichert werden, die als "Map Map"-Datei bezeichnet wird.

Eine Leerungs Zuordnungs Datei wird für jede Datenbankdatei erstellt und befindet sich im selben Verzeichnis. Die Datei hat denselben Namen wie die Datenbankdatei, aber mit einer anderen Erweiterung. Wenn die Client Anwendung z. b. eine Datenbank mit dem vollständigen Pfad c: \\ mydirectory \\ mydabatase. edb erstellt, ist die zugehörige Leerungs Zuordnungs Datei C: \\ mydirectory \\ mydabatase. JFM.

Diese Erweiterung führt zwei Anforderungen ein, wie Datenbankdateien benannt werden müssen:

  - Zwei Datenbanken im gleichen Verzeichnis dürfen nicht denselben Dateinamen mit unterschiedlichen Erweiterungen aufweisen. Beispiel: c: \\ mydirectory \\ mydabatase. db1 und c: \\ mydirectory \\ mydabatase. DB2.

  - 2\. Eine Datenbank darf nicht über die Erweiterung. JFM verfügen.

Wenn Sie eine Datenbankdatei manuell kopieren oder verschieben, sollte die entsprechende Leerungs Zuordnungs Datei ebenfalls kopiert bzw. in dasselbe Zielverzeichnis verschoben werden. Wenn eine Leerungs Zuordnungs Datei zum Zeitpunkt einer neuen Daten Bank Anlage (über [jetattachdatabase](./jetattachdatabase-function.md)) nicht vorhanden ist, wird eine neue erstellt und bei Bedarf erneut aufgefüllt, wenn Seiten aus der Datenbank gelesen werden. Das Mischen von nicht übereinstimmenden Datenbanken und das Leeren von Zuordnungs Dateien wird von ESE behandelt und erzwingt, dass die nicht übereinstimmende Leerungs Zuordnung gelöscht und neu erstellt wird.

Die Größe einer Leerungs Zuordnungs Datei ist direkt proportional zur zugehörigen Datenbankdatei und ungefähr gleich (alle Größen in Bytes, das Ergebnis muss auf das nächste Vielfache von 8.192 aufgerundet werden):

`8,192 + ((<database file size> / <database page size>) / 4)`

Beispiel: bei einer Datenbank mit einer Größe von 1,5 GB mit einer Seitengröße von 32 KB beträgt die ungefähre Größe der Leerungs Zuordnung 24.576 bytes (oder 24 KB).

Die Leerungs Zuordnungs Datei muss aktualisiert werden, wenn Datenbankseiten geleert werden. Wenn die Transaktions Protokollierung aktiviert ist (z. b. [JET_paramRecovery](./transaction-log-parameters.md) auf "on", die Standardeinstellung festgelegt), wird die Aktualisierung der Leerungs Zuordnung durchgeführt, wenn die Client Anwendung Änderungen an der Datenbank vornimmt. Im Durchschnitt wird die gesamte Leerungs Zuordnung einmal für alle 20% der [JET_paramCheckpointDepthMax](./database-cache-parameters.md) Werte (in Bytes) der generierten Transaktionsprotokolle in das nicht flüchtige Medium geschrieben. Die Anzahl von Schreibvorgängen hängt von der Verteilung der Änderungen in der gesamten Datenbank ab. Es ist höchstens ungefähr (alle Größen in Bytes):

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

Wenn die Transaktions Protokollierung deaktiviert ist (z. b. [JET_paramRecovery](./transaction-log-parameters.md) auf "Off" festgelegt ist), wird die Leerungs Zuordnung nur einmal aktualisiert, wenn die Datenbank ordnungsgemäß (über jetdetachdatabase) ordnungsgemäß getrennt getrennt wird (über [jetdetachdatabase](./jetdetachdatabase-function.md)oder implizit getrennt getrennt, [Wenn die](./jetterm-function.md) zugehörige ESE-Instanz beendet wird, solange [JET_bitTermDirty](./jetterm2-function.md) nicht erfolgreich ist).

1 ein verlorener Schreibvorgang (oder verlorene Leerung) wird als Schreibvorgang definiert, der vom Betriebssystem an die ESE-Datenbank-Engine erfolgreich zurückgegeben wird. die eigentlichen Daten werden jedoch nie in der Datenbankdatei auf dem nicht flüchtigen Medium persistent gespeichert. Dies wird normalerweise durch einen fehlerhaften oder falsch konfigurierten Speicher Stapel (Software oder Hardware) verursacht. Client Anwendungen erhalten möglicherweise einen [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) Fehler von ESE-Funktionen, die das Lesen von Daten aus der Datenbank erfordern, wenn sich die Daten in einer Region befinden, die ein verlorenes Schreib Ereignis unterzogen hat.

2 die Möglichkeit, verlorene Schreibvorgänge innerhalb der Lebensdauer eines Prozesses zu erkennen, ist seit Windows 8 (Client) und Windows Server 2012 (Server) vorhanden.

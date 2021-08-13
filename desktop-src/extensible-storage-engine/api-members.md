---
description: 'Weitere Informationen finden Sie unter: API-Member'
title: API-Member
TOCTitle: Api members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api_members(v=EXCHG.10)
ms:contentKeyID: 55100778
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d1740cf1402e12c8160595e3022d37850d3c5c12fab3f2afca3d56faeb46adb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784672"
---
# <a name="api-members"></a>API-Member

Geschützte Member enthalten  
Geerbte Member enthalten  

Verwaltete Versionen der ESENT-API. Diese Klasse enthält statische Methoden, die der nicht verwalteten ESENT-API entsprechen. Diese Methoden auslösen Ausnahmen, wenn Fehler zurückgegeben werden. Hilfsmethoden für die ESENT-API. Diese umschließen JetMakeKey. Nur interne Methoden der API. Hilfsmethoden für die ESENT-API. Diese datenkonvertierung für JetMakeKey. Hilfsmethoden für die ESENT-API. Diese Methoden behandeln Datenbankmetadaten. Hilfsmethoden für die ESENT-API. Dabei handelt es sich nicht um Interopversionen der API, sondern um sehr häufige Verwendungen der Funktionen. API-Member, die als veraltet markiert sind. Hilfsmethoden für die ESENT-API. Dabei handelt es sich nicht um Interopversionen der API, sondern um sehr häufige Verwendungen der Funktionen. Hilfsmethoden für die ESENT-API. Dies ist eine Datenkonvertierung zum Festlegen von Spalten.

Der [API-Typ](./api-class.md) macht die folgenden Member verfügbar.

## <a name="methods"></a>Methoden

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292138(v=exchg.10).md">DeserializeObjectFromColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Deserialisieren eines Objekts aus einer Spalte.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292115(v=exchg.10).md">DeserializeObjectFromColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Deserialisieren eines Objekts aus einer Spalte.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292114(v=exchg.10).md">EscrowUpdate</a></td>
<td>Führen Sie eine atomarer Addition für eine Spalte aus. Die Spalte muss vom Typ <a href="hh577895(v=exchg.10).md">Long sein.</a> Diese Funktion ermöglicht mehreren Sitzungen, denselben Datensatz ohne Konflikte gleichzeitig zu aktualisieren.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292099(v=exchg.10).md">GetBookmark</a></td>
<td>Ruft das Lesezeichen für den Datensatz ab, der dem Indexeintrag an der aktuellen Position eines Cursors zugeordnet ist. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mit JetGotoBookmark wieder auf denselben Datensatz zu positionieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292098(v=exchg.10).md">GetColumnDictionary</a></td>
<td>Erstellt ein Wörterbuch, das Spaltennamen ihren Spalten-IDs zulädt.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292101(v=exchg.10).md">GetTableColumnid</a></td>
<td>Get the columnid of the specified column.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292090(v=exchg.10).md">GetTableColumns(JET_SESID, JET_TABLEID)</a></td>
<td>Durch iteriert alle Spalten in der Tabelle und gibt Informationen zu den einzelnen Spalten zurück.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292089(v=exchg.10).md">GetTableColumns(JET_SESID, JET_DBID, String)</a></td>
<td>Durch iteriert alle Spalten in der Tabelle und gibt Informationen zu den einzelnen Spalten zurück.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292093(v=exchg.10).md">GetTableIndexes(JET_SESID, JET_TABLEID)</a></td>
<td>Durch iteriert alle Indizes in der Tabelle und gibt Informationen zu jedem Index zurück.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292092(v=exchg.10).md">GetTableIndexes(JET_SESID, JET_DBID, String)</a></td>
<td>Durch iteriert alle Indizes in der Tabelle und gibt Informationen zu jedem Index zurück.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292095(v=exchg.10).md">GetTableNames</a></td>
<td>Gibt die Namen der Tabellen in der Datenbank zurück.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292094(v=exchg.10).md">IntersectIndexes</a></td>
<td>Überschneiden Sie eine Gruppe von Indexbereichen, und geben Sie die Lesezeichen der Datensätze zurück, die in allen Indexbereichen gefunden werden. Siehe auch <a href="dn292212(v=exchg.10).md">JetIntersectIndexes(JET_SESID, [], Int32, JET_RECORDLIST, IntersectIndexesGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292097(v=exchg.10).md">JetAddColumn</a></td>
<td>Fügen Sie einer vorhandenen Tabelle eine neue Spalte hinzu.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292096(v=exchg.10).md">JetAttachDatabase</a></td>
<td>Angefügt eine Datenbankdatei zur Verwendung mit einer Datenbankinstanz. Um die Datenbank verwenden zu können, muss sie anschließend mit <a href="dn292219(v=exchg.10).md">JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit) geöffnet werden.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292100(v=exchg.10).md">JetAttachDatabase2</a></td>
<td>Angefügt eine Datenbankdatei zur Verwendung mit einer Datenbankinstanz. Um die Datenbank verwenden zu können, muss sie anschließend mit <a href="dn292219(v=exchg.10).md">JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit) geöffnet werden.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292102(v=exchg.10).md">JetBackupInstance</a></td>
<td>Führt eine Streamingsicherung einer Instanz, einschließlich aller angefügten Datenbanken, in einem Verzeichnis aus. Da mehrere Sicherungsmethoden von der Engine unterstützt werden, ist dies die einfachste und am meisten gekapselte Funktion.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance</a></td>
<td>Initiiert eine externe Sicherung, während die Engine und die Datenbank online und aktiv sind.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292103(v=exchg.10).md">JetBeginSession</a></td>
<td>Initialisieren Sie eine neue ESENT-Sitzung.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292105(v=exchg.10).md">JetBeginTransaction</a></td>
<td>Bewirkt, dass eine Sitzung eine Transaktion eingibt oder einen neuen Sicherungspunkt in einer vorhandenen Transaktion erstellt.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292106(v=exchg.10).md">JetBeginTransaction2</a></td>
<td>Bewirkt, dass eine Sitzung eine Transaktion eingibt oder einen neuen Sicherungspunkt in einer vorhandenen Transaktion erstellt.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292107(v=exchg.10).md">JetCloseDatabase</a></td>
<td>Schließt eine Datenbankdatei, die zuvor mit <a href="dn292219(v=exchg.10).md">JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a> geöffnet oder mit <a href="dn292118(v=exchg.10).md">JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)</a>erstellt wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292108(v=exchg.10).md">JetCloseFileInstance</a></td>
<td>Schließt eine Datei, die mit JetOpenFileInstance geöffnet wurde, nachdem die Daten aus dieser Datei mit JetReadFileInstance extrahiert wurden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292109(v=exchg.10).md">JetCloseTable</a></td>
<td>Schließen Sie eine geöffnete Tabelle.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292110(v=exchg.10).md">JetCommitTransaction</a></td>
<td>Committet die Änderungen, die während des aktuellen Sicherungspunkts am Zustand der Datenbank vorgenommen wurden, und migriert sie zum vorherigen Sicherungspunkt. Wenn für den äußersten Sicherungspunkt ein Commit ausgeführt wird, werden die während dieses Speicherpunkts vorgenommenen Änderungen in den Zustand der Datenbank übernommen, und die Sitzung beendet die Transaktion.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292112(v=exchg.10).md">JetCompact</a></td>
<td>Erstellt eine Kopie einer vorhandenen Datenbank. Die Kopie wird für die Verwendung in einen optimalen Zustand komprimiert. Die Daten in den kopierten Daten werden entsprechend den Measures gepackt, die für die Indizes bei der Indexerstellung ausgewählt wurden. Auf diese Weise können komprimierte Daten so dichte wie möglich gespeichert werden. Alternativ können komprimierte Daten Speicherplatz für nachfolgende Datensatzvergrößerungen oder Indexeinfügungen reservieren.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292113(v=exchg.10).md">JetComputeStats</a></td>
<td>Führt jeden Index einer Tabelle durch, um die Anzahl der Einträge in einem Index und die Anzahl der unterschiedlichen Schlüssel in einem Index genau zu berechnen. Diese Informationen werden zusammen mit der Anzahl der Datenbankseiten, die einem Index zugeordnet sind, und der aktuellen Berechnungszeit in Indexmetadaten in der Datenbank gespeichert. Diese Daten können anschließend mit Informationsvorgängen abgerufen werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292118(v=exchg.10).md">JetCreateDatabase</a></td>
<td>Erstellt eine Datenbankdatei und fügt sie an.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292120(v=exchg.10).md">JetCreateDatabase2</a></td>
<td>Erstellt eine Datenbankdatei mit einer angegebenen maximalen Datenbankgröße und fügt sie an.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292121(v=exchg.10).md">JetCreateIndex</a></td>
<td>Erstellt einen Index für Daten in einer ESE-Datenbank. Ein Index kann verwendet werden, um bestimmte Daten schnell zu finden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292123(v=exchg.10).md">JetCreateIndex2</a></td>
<td>Erstellt Indizes für Daten in einer ESE-Datenbank.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292122(v=exchg.10).md">JetCreateInstance</a></td>
<td>Ordnet eine neue Instanz der Datenbank-Engine zu.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292126(v=exchg.10).md">JetCreateInstance2</a></td>
<td>Zuordnen einer neuen Instanz der Datenbank-Engine zur Verwendung in einem einzelnen Prozess mit einem angegebenen Anzeigenamen.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292127(v=exchg.10).md">JetCreateTable</a></td>
<td>Erstellen Sie eine leere Tabelle. Die neu erstellte Tabelle wird exklusiv geöffnet.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3</a></td>
<td>Erstellt eine Tabelle, fügt Spalten und Indizes für diese Tabelle hinzu.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292130(v=exchg.10).md">JetDefragment</a></td>
<td>Startet und beendet Datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292145(v=exchg.10).md">JetDefragment2</a></td>
<td>Startet und beendet Datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292131(v=exchg.10).md">JetDelete</a></td>
<td>Löscht den aktuellen Datensatz in einer Datenbanktabelle.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292133(v=exchg.10).md">JetDeleteColumn</a></td>
<td>Löscht eine Spalte aus einer Datenbanktabelle.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292132(v=exchg.10).md">JetDeleteColumn2</a></td>
<td>Löscht eine Spalte aus einer Datenbanktabelle.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292135(v=exchg.10).md">JetDeleteIndex</a></td>
<td>Löscht einen Index aus einer Datenbanktabelle.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292134(v=exchg.10).md">JetDeleteTable</a></td>
<td>Löscht eine Tabelle aus einer Datenbank.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292139(v=exchg.10).md">JetDetachDatabase</a></td>
<td>Gibt eine Datenbankdatei frei, die zuvor an eine Datenbanksitzung angefügt wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292136(v=exchg.10).md">JetDetachDatabase2</a></td>
<td>Gibt eine Datenbankdatei frei, die zuvor an eine Datenbanksitzung angefügt wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292137(v=exchg.10).md">JetDupCursor</a></td>
<td>Dupliziert einen geöffneten Cursor und gibt ein Handle an den duplizierten Cursor zurück. Wenn der cursor, der dupliziert wurde, ein schreibgeschützter Cursor war, ist der duplizierte Cursor auch ein schreibgeschützter Cursor. Jeder Zustand im Zusammenhang mit der Konstruktion eines Suchschlüssels oder dem Aktualisieren eines Datensatzes wird nicht in den duplizierten Cursor kopiert. Darüber hinaus wird die Position des ursprünglichen Cursors nicht im duplizierten Cursor dupliziert. Der duplizierte Cursor wird immer für den gruppierten Index geöffnet, und seine Position befindet sich immer in der ersten Zeile der Tabelle.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292140(v=exchg.10).md">JetDupSession</a></td>
<td>Initialisieren Sie eine neue ESE-Sitzung in derselben Instanz wie die gegebene sesid.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292142(v=exchg.10).md">JetEndExternalBackupInstance</a></td>
<td>Beendet eine externe Sicherungssitzung. Diese API ist die letzte API in einer Reihe von APIs, die aufgerufen werden müssen, um eine erfolgreiche Onlinesicherung (nicht VSS-basiert) auszuführen.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292143(v=exchg.10).md">JetEndExternalBackupInstance2</a></td>
<td>Beendet eine externe Sicherungssitzung. Diese API ist die letzte API in einer Reihe von APIs, die aufgerufen werden müssen, um eine erfolgreiche Onlinesicherung (nicht VSS-basiert) auszuführen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292144(v=exchg.10).md">JetEndSession</a></td>
<td>Beendet eine Sitzung.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292148(v=exchg.10).md">JetEnumerateColumns</a></td>
<td>Ruft effizient eine Gruppe von Spalten und deren Werte aus dem aktuellen Datensatz eines Cursors oder des Kopierpuffers dieses Cursors ab. Die abgerufenen Spalten und Werte können durch eine Liste von Spalten-IDs, itagSequence-Zahlen und anderen Merkmalen eingeschränkt werden. Diese Spaltenabruf-API ist einzigartig, da sie Informationen in dynamisch zugeordneten Arbeitsspeicher zurückgibt, der mithilfe eines vom Benutzer bereitgestellten realloc-kompatiblen Rückrufs ermittelt wird. Diese neue Flexibilität ermöglicht den effizienten Abruf von Spaltendaten mit bestimmten Merkmalen (z. B. Größe und Multiplicität), die dem Aufrufer unbekannt sind. Dadurch entfällt die Notwendigkeit, die Ermittlungsmodi von JetRetrieveColumn zu verwenden, um diese Merkmale zu bestimmen, um einen abschließenden Aufruf von JetRetrieveColumn einzurichten, der die gewünschten Daten erfolgreich abruft.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292150(v=exchg.10).md">JetEscrowUpdate</a></td>
<td>Führt einen atomaren Additionsvorgang für eine Spalte aus. Diese Funktion ermöglicht es mehreren Sitzungen, denselben Datensatz ohne Konflikte gleichzeitig zu aktualisieren. Siehe <a href="dn292114(v=exchg.10).md">auch EscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292147(v=exchg.10).md">JetFreeBuffer</a></td>
<td>Gibt Arbeitsspeicher frei, der durch einen Datenbank-Engine-Aufruf zugeordnet wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292154(v=exchg.10).md">JetGetAttachInfoInstance</a></td>
<td>Wird während einer Sicherung verwendet, die von <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)</a> initiiert wird, um eine Instanz nach den Namen von Datenbankdateien abfragt, die Teil des Sicherungsdateisets werden sollen. Es werden nur Datenbanken berücksichtigt, die derzeit mit <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a> an die Instanz angefügt sind. Diese Dateien können anschließend mit <a href="dn292230(v=exchg.10).md">JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> geöffnet und mit <a href="dn332987(v=exchg.10).md">JetReadFileInstance(JET_INSTANCE, JET_HANDLE, [], Int32, Int32) gelesen</a>werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292149(v=exchg.10).md">JetGetBookmark</a></td>
<td>Ruft das Lesezeichen für den Datensatz ab, der dem Indexeintrag an der aktuellen Position eines Cursors zugeordnet ist. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von <a href="dn292200(v=exchg.10).md">JetGotoBookmark(JET_SESID, JET_TABLEID, [], Int32)</a>wieder zum gleichen Datensatz zu positionieren. Das Lesezeichen ist nicht länger als <a href="dn351215(v=exchg.10).md">BookmarkMost bytes.</a> Siehe auch <a href="dn292099(v=exchg.10).md">GetBookmark(JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292158(v=exchg.10).md">JetGetColumnInfo(JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)</a></td>
<td>Ruft Informationen zu einer Spalte in einer Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292151(v=exchg.10).md">JetGetColumnInfo(JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</a></td>
<td>Ruft Informationen zu einer Tabellenspalte ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292152(v=exchg.10).md">JetGetColumnInfo(JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)</a></td>
<td>Ruft Informationen zu allen Spalten in einer Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292153(v=exchg.10).md">JetGetCurrentIndex</a></td>
<td>Bestimmt den Namen des aktuellen Indexes eines angegebenen Cursors. Dieser Name wird auch verwendet, um diesen Index später mithilfe von <a href="dn334011(v=exchg.10).md">JetSetCurrentIndex(JET_SESID, JET_TABLEID, String)</a>erneut als aktuellen Index auszuwählen. Sie kann auch verwendet werden, um die Eigenschaften dieses Indexes mit JetGetTableIndexInfo zu finden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292155(v=exchg.10).md">JetGetCursorInfo</a></td>
<td>Bestimmen Sie, ob eine Aktualisierung des aktuellen Datensatzes eines Cursors basierend auf dem aktuellen Updatestatus des Datensatzes zu einem Schreibkonflikt führt. Es ist möglich, dass letztendlich ein Schreibkonflikt zurückgegeben wird, auch wenn JetGetCursorInfo erfolgreich zurückgegeben wird. weil der Datensatz von einer anderen Sitzung aktualisiert werden kann, bevor die aktuelle Sitzung denselben Datensatz aktualisieren kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292159(v=exchg.10).md">JetGetDatabaseFileInfo(String, JET_DBINFOMISC, JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen zur angegebenen Datenbank ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292161(v=exchg.10).md">JetGetDatabaseFileInfo(String, Int32, JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen zur angegebenen Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292160(v=exchg.10).md">JetGetDatabaseFileInfo(String, Int64, JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen zur angegebenen Datenbank ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292162(v=exchg.10).md">JetGetDatabaseInfo(JET_SESID, JET_DBID, JET_DBINFOMISC, JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen zur angegebenen Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292164(v=exchg.10).md">JetGetDatabaseInfo(JET_SESID, JET_DBID, Int32, JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen zur angegebenen Datenbank ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292167(v=exchg.10).md">JetGetDatabaseInfo(JET_SESID, JET_DBID, String, JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen zur angegebenen Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292168(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</a></td>
<td><strong>Veraltet.</strong> Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292172(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292166(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292171(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, Int32, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292169(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292173(v=exchg.10).md">JetGetIndexInfo(JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292170(v=exchg.10).md">JetGetInstanceInfo</a></td>
<td>Ruft Informationen zu den ausgeführten Instanzen ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292175(v=exchg.10).md">JetGetLock</a></td>
<td>Reservieren Sie explizit die Möglichkeit, eine Zeile zu aktualisieren, eine Schreibsperre zu schreiben oder explizit zu verhindern, dass eine Zeile von einer anderen Sitzung aktualisiert wird. Lesen Sie die Sperre. Normalerweise werden Zeilenschreibsperren implizit als Ergebnis der Aktualisierung von Zeilen eingerichtet. Lesesperren sind aufgrund der Datensatzversionsierung in der Regel nicht erforderlich. In einigen Fällen möchte eine Transaktion jedoch möglicherweise explizit eine Zeile sperren, um die Serialisierung zu erzwingen oder sicherzustellen, dass ein nachfolgender Vorgang erfolgreich ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292174(v=exchg.10).md">JetGetLogInfoInstance</a></td>
<td>Wird während einer von <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)</a> initiierten Sicherung verwendet, um eine Instanz nach den Namen der Datenbankpatchdateien und Protokolldateien abzufragen, die Teil des Sicherungsdateisatzes werden sollen. Diese Dateien können anschließend mit <a href="dn292230(v=exchg.10).md">JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> geöffnet und mit <a href="dn332987(v=exchg.10).md">JetReadFileInstance(JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>gelesen werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292177(v=exchg.10).md">JetGetLS</a></td>
<td>Ermöglicht es der Anwendung, das Kontexthandle abzurufen, das als Local Storage bezeichnet wird, das einem Cursor oder der tabelle zugeordnet ist, die diesem Cursor zugeordnet ist. Dieses Kontexthandle muss zuvor mit <a href="dn334015(v=exchg.10).md">JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)</a>festgelegt worden sein. JetGetLS kann auch verwendet werden, um gleichzeitig das aktuelle Kontexthandle für einen Cursor oder eine Tabelle abzurufen und dieses Kontexthandle zurückzusetzen.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292179(v=exchg.10).md">JetGetObjectInfo(JET_SESID, JET_DBID, JET_OBJECTLIST)</a></td>
<td>Ruft Informationen zu Datenbankobjekten ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292178(v=exchg.10).md">JetGetObjectInfo(JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)</a></td>
<td>Ruft Informationen zu Datenbankobjekten ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292181(v=exchg.10).md">JetGetRecordPosition</a></td>
<td>Gibt die Bruchposition des aktuellen Datensatzes im aktuellen Index in Form einer <a href="dn335256(v=exchg.10).md">JET_RECPOS-Struktur</a> zurück. Siehe auch <a href="dn292207(v=exchg.10).md">JetGotoPosition(JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292180(v=exchg.10).md">JetGetSecondaryIndexBookmark</a></td>
<td>Ruft ein spezielles Lesezeichen für den sekundären Indexeintrag an der aktuellen Position eines Cursors ab. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von JetGotoSecondaryIndexBookmark effizient zurück zum gleichen Indexeintrag zu positionieren. Dies ist besonders nützlich bei der Neupositionierung in einem sekundären Index, der doppelte Schlüssel oder mehrere Indexeinträge für denselben Datensatz enthält.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292182(v=exchg.10).md">JetGetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</a></td>
<td>Ruft Datenbankkonfigurationsoptionen ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292185(v=exchg.10).md">JetGetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)</a></td>
<td>Ruft Datenbankkonfigurationsoptionen ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292186(v=exchg.10).md">JetGetTableColumnInfo(JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</a></td>
<td>Ruft Informationen zu einer Tabellenspalte ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292187(v=exchg.10).md">JetGetTableColumnInfo(JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)</a></td>
<td>Ruft Informationen zu einer Tabellenspalte ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292189(v=exchg.10).md">JetGetTableColumnInfo(JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)</a></td>
<td>Ruft Informationen zu allen Spalten in der Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292191(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</a></td>
<td><strong>Veraltet.</strong> Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292190(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292196(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292193(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292192(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292195(v=exchg.10).md">JetGetTableIndexInfo(JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes für eine Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a></td>
<td>Ruft verschiedene Informationen zu einer Tabelle in einer Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a></td>
<td>Ruft verschiedene Informationen zu einer Tabelle in einer Datenbank ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a></td>
<td>Ruft verschiedene Informationen zu einer Tabelle in einer Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a></td>
<td>Ruft verschiedene Informationen zu einer Tabelle in einer Datenbank ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a></td>
<td>Ruft verschiedene Informationen zu einer Tabelle in einer Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292199(v=exchg.10).md">JetGetTruncateLogInfoInstance</a></td>
<td>Wird während einer Sicherung verwendet, die von <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)</a> initiiert wurde, um eine Instanz nach den Namen der Transaktionsprotokolldateien abfragt, die nach erfolgreichem Abschluss der Sicherung sicher gelöscht werden können.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292203(v=exchg.10).md">JetGetVersion</a></td>
<td>Ruft die Version der Datenbank-Engine ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292200(v=exchg.10).md">JetGotoBookmark</a></td>
<td>Positioniert einen Cursor an einem Indexeintrag für den Datensatz, der dem angegebenen Lesezeichen zugeordnet ist. Das Lesezeichen kann mit jedem Index verwendet werden, der für eine Tabelle definiert ist. Das Lesezeichen für einen Datensatz kann mit <a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32) abgerufen werden.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292207(v=exchg.10).md">JetGotoPosition</a></td>
<td>Verschiebt einen Cursor an eine neue Position, die ein Bruchteil des Wegs durch den aktuellen Index ist. Siehe auch <a href="dn292181(v=exchg.10).md">JetGetRecordPosition(JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark</a></td>
<td>Positioniert einen Cursor an einem Indexeintrag, der dem angegebenen sekundären Indexzeichen zugeordnet ist. Das sekundäre Indexzeichen muss mit demselben Index für dieselbe Tabelle verwendet werden, aus der es ursprünglich abgerufen wurde. Das sekundäre Indexzeichen für einen Indexeintrag kann mit <a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, [], Int32, [], Int32, GotoSecondaryIndexBookmarkGrbit)</a>abgerufen werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292206(v=exchg.10).md">JetGrowDatabase</a></td>
<td>Erweitert die Größe einer derzeit geöffneten Datenbank.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292208(v=exchg.10).md">JetIdle</a></td>
<td>Führt Leerlaufbereinigungsaufgaben aus oder überprüft den Status des Versionsspeichers in ESE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292209(v=exchg.10).md">JetIndexRecordCount</a></td>
<td>Zählt die Anzahl der Einträge im aktuellen Index von der aktuellen Position nach vorn. Die aktuelle Position ist in der Anzahl enthalten. Die Anzahl kann größer als die Gesamtzahl der Datensätze in der Tabelle sein, wenn sich der aktuelle Index über einer mehrwertigen Spalte befindet und Instanzen der Spalte mehrere Werte haben. Wenn die Tabelle leer ist, wird 0 für die Anzahl zurückgegeben.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292210(v=exchg.10).md">JetInit</a></td>
<td>Initialisieren Sie die ESENT-Datenbank-Engine.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292214(v=exchg.10).md">JetInit2</a></td>
<td>Initialisieren Sie die ESENT-Datenbank-Engine.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292212(v=exchg.10).md">JetIntersectIndexes</a></td>
<td>Berechnet die Schnittmenge zwischen mehreren Sätzen von Indexeinträgen aus verschiedenen sekundären Indizes für dieselbe Tabelle. Dieser Vorgang ist nützlich, um den Satz von Datensätzen in einer Tabelle zu finden, die zwei oder mehr Kriterien entsprechen, die mithilfe von Indexbereichen ausgedrückt werden können. Siehe auch <a href="dn292094(v=exchg.10).md">IntersectIndexes(JET_SESID, [])</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292216(v=exchg.10).md">JetMakeKey</a></td>
<td>Erstellt Suchschlüssel, die dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden können.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292218(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)</a></td>
<td>Navigieren Sie durch einen Index. Der Cursor kann am Anfang oder Ende des Indexes positioniert und durch eine angegebene Anzahl von Indexeinträgen rückwärts und vorwärts verschoben werden. Siehe auch <a href="dn334150(v=exchg.10).md">TryMoveFirst(JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast(JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext(JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious(JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a></td>
<td>Navigieren Sie durch einen Index. Der Cursor kann am Anfang oder Ende des Indexes positioniert und durch eine angegebene Anzahl von Indexeinträgen rückwärts und vorwärts verschoben werden. Siehe auch <a href="dn334150(v=exchg.10).md">TryMoveFirst(JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast(JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext(JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious(JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292219(v=exchg.10).md">JetOpenDatabase</a></td>
<td>Öffnet eine Datenbank, die zuvor mit <a href="dn292096(v=exchg.10).md">JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)</a>angefügt wurde, zur Verwendung mit einer Datenbanksitzung. Diese Funktion kann für dieselbe Datenbank mehrmals aufgerufen werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292230(v=exchg.10).md">JetOpenFileInstance</a></td>
<td>Öffnet eine angefügte Datenbank, eine Datenbankpatchdatei oder eine Transaktionsprotokolldatei einer aktiven Instanz, um eine Streaming-Fuzzysicherung durchzuführen. Die Daten aus diesen Dateien können anschließend mithilfe von JetReadFileInstance über das zurückgegebene Handle gelesen werden. Das zurückgegebene Handle muss mit jetCloseFileInstance geschlossen werden. Eine externe Sicherung der Instanz muss zuvor mit JetBeginExternalBackupInstance initiiert worden sein.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292234(v=exchg.10).md">JetOpenTable</a></td>
<td>Öffnet einen Cursor für eine zuvor erstellte Tabelle.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292231(v=exchg.10).md">JetOpenTempTable</a></td>
<td>Erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert datensätze und ruft sie wie eine gewöhnliche Tabelle ab, die mit JetCreateTableColumnIndex erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um datensätzensätze sehr schnell zu sortieren und doppelte Entfernungen durchzuführen, wenn ausschließlich sequenziell darauf zugegriffen wird. Siehe auch <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292232(v=exchg.10).md">JetOpenTempTable2</a></td>
<td>Erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert datensätze und ruft sie wie eine gewöhnliche Tabelle ab, die mit JetCreateTableColumnIndex erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um datensätzensätze sehr schnell zu sortieren und doppelte Entfernungen durchzuführen, wenn ausschließlich sequenziell darauf zugegriffen wird. Siehe auch <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292233(v=exchg.10).md">JetOpenTempTable3</a></td>
<td>Erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert datensätze und ruft sie wie eine gewöhnliche Tabelle ab, die mit JetCreateTableColumnIndex erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um datensätzensätze sehr schnell zu sortieren und doppelte Entfernungen durchzuführen, wenn ausschließlich sequenziell darauf zugegriffen wird. Siehe auch <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332998(v=exchg.10).md">JetOSSnapshotFreeze</a></td>
<td>Startet eine Momentaufnahme. Während die Momentaufnahme ausgeführt wird, kann keine Schreibaktivität auf den Datenträger durch die Engine erfolgen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292235(v=exchg.10).md">JetOSSnapshotPrepare</a></td>
<td>Beginnt die Vorbereitungen für eine Momentaufnahmesitzung. Eine Momentaufnahmesitzung ist ein kurzes Zeitintervall, in dem die Engine keine Schreib-IOs auf den Datenträger ausgibt, sodass die Engine an einer Volumemomentaufnahmesitzung teilnehmen kann (wenn sie von einem Momentaufnahmewriter gesteuert wird).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332986(v=exchg.10).md">JetOSSnapshotThaw</a></td>
<td>Benachrichtigt die Engine, dass sie den normalen E/A-Betrieb nach einem Einfrieren und einer erfolgreichen Momentaufnahme fortsetzen kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332988(v=exchg.10).md">JetPrepareUpdate</a></td>
<td>Bereiten Sie einen Cursor für das Update vor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332987(v=exchg.10).md">JetReadFileInstance</a></td>
<td>Ruft den Inhalt einer Datei ab, die mit <a href="dn292230(v=exchg.10).md">JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a>geöffnet wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332989(v=exchg.10).md">JetRegisterCallback</a></td>
<td>Ermöglicht der Anwendung, die Datenbank-Engine so zu konfigurieren, dass für bestimmte Ereignisse Benachrichtigungen an die Anwendung ausgegeben werden. Diese Benachrichtigungen sind einer bestimmten Tabelle zugeordnet und bleiben nur wirksam, bis die Instanz, die die Tabelle enthält, mithilfe von <a href="dn334020(v=exchg.10).md">JetTerm(JET_INSTANCE)</a>heruntergefahren wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332990(v=exchg.10).md">JetRenameColumn</a></td>
<td>Ändert den Namen einer vorhandenen Spalte.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332993(v=exchg.10).md">JetRenameTable</a></td>
<td>Ändert den Namen einer vorhandenen Tabelle.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332991(v=exchg.10).md">JetResetSessionContext</a></td>
<td>Trennt eine Sitzung vom aktuellen Thread. Dies sollte in Verbindung mit <a href="dn334027(v=exchg.10).md">JetSetSessionContext(JET_SESID, IntPtr)</a>verwendet werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332994(v=exchg.10).md">JetResetTableSequential</a></td>
<td>Benachrichtigt die Datenbank-Engine, dass die Anwendung nicht mehr den gesamten Index überprüft, auf dem der Cursor positioniert ist. Dieser Aufruf kehrt eine von <a href="dn334018(v=exchg.10).md">JetSetTableSequential(JET_SESID, JET_TABLEID, SetTableSequentialGrbit)</a>gesendete Benachrichtigung um.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332992(v=exchg.10).md">JetRestoreInstance</a></td>
<td>Stellt eine Streamingsicherung einer Instanz einschließlich aller angefügten Datenbanken wieder her und stellt sie wieder her. Sie ist für die Arbeit mit einer Sicherung konzipiert, die mit der <a href="dn292102(v=exchg.10).md">JetBackupInstance(JET_INSTANCE-, String-, BackupGrbit-, JET_PFNSTATUS)-Funktion</a> erstellt wurde. Dies ist die einfachste und am häufigsten gekapselte Wiederherstellungsfunktion.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332995(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursorkopierpuffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Indexeintrag abrufen, der auf den aktuellen Datensatz verweist. Neben dem Abrufen des tatsächlichen Spaltenwerts kann JetRetrieveColumn auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, damit die Größe der Anwendungspuffer entsprechend angepasst werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332997(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursorkopierpuffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Indexeintrag abrufen, der auf den aktuellen Datensatz verweist. Neben dem Abrufen des tatsächlichen Spaltenwerts kann JetRetrieveColumn auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, damit die Größe der Anwendungspuffer entsprechend angepasst werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334004(v=exchg.10).md">JetRetrieveColumns</a></td>
<td>Ruft mehrere Spaltenwerte aus dem aktuellen Datensatz in einem einzelnen Vorgang ab. Ein Array von JET_RETRIEVECOLUMN Strukturen wird verwendet, um den Satz der abzurufenden Spaltenwerte und ausgabepuffer für jeden abzurufenden Spaltenwert zu beschreiben.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334002(v=exchg.10).md">JetRetrieveKey</a></td>
<td>Ruft den Schlüssel für den Indexeintrag an der aktuellen Position eines Cursors ab. Siehe auch <a href="dn334085(v=exchg.10).md">RetrieveKey(JET_SESID, JET_TABLEID, RetrieveKeyGrbit).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334001(v=exchg.10).md">JetRollback</a></td>
<td>Macht die am Zustand der Datenbank vorgenommenen Änderungen rückgängig und kehrt zum letzten Sicherungspunkt zurück. JetRollback schließt auch alle Cursor, die während des Sicherungspunkts geöffnet wurden. Wenn der äußerste Sicherungspunkt rückgängig ist, beendet die Sitzung die Transaktion.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334003(v=exchg.10).md">JetSeek</a></td>
<td>Positioniert einen Cursor effizient auf einen Indexeintrag, der den durch den Suchschlüssel in diesem Cursor angegebenen Suchkriterien und der angegebenen Ungleichheit entspricht. Ein Suchschlüssel muss zuvor mit <a href="dn292216(v=exchg.10).md">JetMakeKey(JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>erstellt worden sein. Siehe auch <a href="dn334145(v=exchg.10).md">TrySeek(JET_SESID, JET_TABLEID, SeekGrbit).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334009(v=exchg.10).md">JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, SetColumnGrbit, JET_SETINFO)</a></td>
<td>Die JetSetColumn-Funktion ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, um eingefügt oder den aktuellen Datensatz zu aktualisieren. Sie kann einen vorhandenen Wert überschreiben, einer Sequenz von Werten in einer mehrwertigen Spalte einen neuen Wert hinzufügen, einen Wert aus einer Sequenz von Werten in einer mehrwertigen Spalte entfernen oder einen ganz oder teilweise eines long-Werts aktualisieren (eine Spalte vom Typ <a href="hh577895(v=exchg.10).md">LongText</a> oder <a href="hh577895(v=exchg.10).md">LongBinary</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334008(v=exchg.10).md">JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, SetColumnGrbit, JET_SETINFO)</a></td>
<td>Die JetSetColumn-Funktion ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, um eingefügt oder den aktuellen Datensatz zu aktualisieren. Sie kann einen vorhandenen Wert überschreiben, einer Sequenz von Werten in einer mehrwertigen Spalte einen neuen Wert hinzufügen, einen Wert aus einer Sequenz von Werten in einer mehrwertigen Spalte entfernen oder einen ganz oder teilweise eines long-Werts aktualisieren (eine Spalte vom Typ <a href="hh577895(v=exchg.10).md">LongText</a> oder <a href="hh577895(v=exchg.10).md">LongBinary</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334010(v=exchg.10).md">JetSetColumnDefaultValue</a></td>
<td>Ändert den Standardwert einer vorhandenen Spalte.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334006(v=exchg.10).md">JetSetColumns</a></td>
<td>Ermöglicht einer Anwendung das Festlegen mehrerer Spaltenwerte in einem einzelnen Vorgang. Ein Array von <a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a> Strukturen wird verwendet, um den Satz der festzulegenden Spaltenwerte und Eingabepuffer für jeden festzulegenden Spaltenwert zu beschreiben.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334011(v=exchg.10).md">JetSetCurrentIndex</a></td>
<td>Legen Sie den aktuellen Index eines Cursors fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334005(v=exchg.10).md">JetSetCurrentIndex2</a></td>
<td>Legen Sie den aktuellen Index eines Cursors fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334012(v=exchg.10).md">JetSetCurrentIndex3</a></td>
<td>Legen Sie den aktuellen Index eines Cursors fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334013(v=exchg.10).md">JetSetCurrentIndex4</a></td>
<td>Legen Sie den aktuellen Index eines Cursors fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334014(v=exchg.10).md">JetSetDatabaseSize</a></td>
<td>Legt die Größe einer ungeöffneten Datenbankdatei fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334024(v=exchg.10).md">JetSetIndexRange</a></td>
<td>Begrenzt vorübergehend den Satz von Indexeinträgen, die der Cursor mit <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a> durchgehen kann, auf diejenigen, die ab dem aktuellen Indexeintrag beginnen und am Indexeintrag enden, der mit den Suchkriterien übereinstimmt, die vom Suchschlüssel in diesem Cursor und den angegebenen gebundenen Kriterien angegeben werden. Ein Suchschlüssel muss zuvor mit <a href="dn292216(v=exchg.10).md">JetMakeKey(JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>erstellt worden sein. Siehe auch <a href="dn334099(v=exchg.10).md">TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334015(v=exchg.10).md">JetSetLS</a></td>
<td>Ermöglicht der Anwendung, einem Cursor oder der diesem Cursor zugeordneten Tabelle ein Kontexthandle zuzuordnen, das als Local Storage bezeichnet wird. Dieses Kontexthandle kann von der Anwendung verwendet werden, um zusätzliche Daten zu speichern, die einem Cursor oder einer Tabelle zugeordnet sind. Die Anwendung wird später mithilfe eines Laufzeitrückrufs benachrichtigt, wenn das Kontexthandle freigegeben werden muss. Dies ermöglicht das Zuordnen eines dynamisch zugeordneten Zustands zu einem Cursor oder einer Tabelle.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334027(v=exchg.10).md">JetSetSessionContext</a></td>
<td>Ordnet dem aktuellen Thread mithilfe des angegebenen Kontexthandle eine Sitzung zu. Diese Zuordnung überschreibt die Standard-Engine-Anforderung, dass eine Transaktion für eine bestimmte Sitzung vollständig im selben Thread erfolgen muss. Verwenden Sie <a href="dn332991(v=exchg.10).md">JetResetSessionContext(JET_SESID),</a> um die Zuordnung zu entfernen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334028(v=exchg.10).md">JetSetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)</a></td>
<td>Legt Datenbankkonfigurationsoptionen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334017(v=exchg.10).md">JetSetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, Int32, String)</a></td>
<td>Legt Datenbankkonfigurationsoptionen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334029(v=exchg.10).md">JetSetSystemParameter(JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)</a></td>
<td>Legt Datenbankkonfigurationsoptionen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334018(v=exchg.10).md">JetSetTableSequential</a></td>
<td>Benachrichtigt die Datenbank-Engine, dass die Anwendung den gesamten Index überprüft, auf dem der Cursor positioniert ist. Folglich werden die Methoden, die für den Zugriff auf die Indexdaten verwendet werden, optimiert, um dieses Szenario so schnell wie möglich zu gestalten. Siehe auch <a href="dn332994(v=exchg.10).md">JetResetTableSequential(JET_SESID, JET_TABLEID, ResetTableSequentialGrbit).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334032(v=exchg.10).md">JetStopBackupInstance</a></td>
<td>Verhindert, dass sicherungsbezogene Streamingaktivitäten auf einer bestimmten ausgeführten Instanz fortgesetzt werden, wodurch die Streamingsicherung auf vorhersagbare Weise beendet wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334035(v=exchg.10).md">JetStopServiceInstance</a></td>
<td>Bereitet eine Instanz für die Beendigung vor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334020(v=exchg.10).md">JetTerm</a></td>
<td>Beenden Sie eine Instanz, die mit <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> oder <a href="dn292122(v=exchg.10).md">JetCreateInstance(JET_INSTANCE, String)</a>erstellt wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334037(v=exchg.10).md">JetTerm2</a></td>
<td>Beenden Sie eine Instanz, die mit <a href="dn292210(v=exchg.10).md">JetInit(JET_INSTANCE)</a> oder <a href="dn292122(v=exchg.10).md">JetCreateInstance(JET_INSTANCE, String)</a>erstellt wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334022(v=exchg.10).md">JetTruncateLogInstance</a></td>
<td>Wird während einer von JetBeginExternalBackup initiierten Sicherung verwendet, um alle Transaktionsprotokolldateien zu löschen, die nach erfolgreichem Abschluss der aktuellen Sicherung nicht mehr benötigt werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334019(v=exchg.10).md">JetUnregisterCallback</a></td>
<td>Konfiguriert die Datenbank-Engine so, dass keine Benachrichtigungen mehr an die Anwendung ausgegeben werden, wie zuvor über <a href="dn332989(v=exchg.10).md">JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</a>angefordert.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334036(v=exchg.10).md">JetUpdate(JET_SESID, JET_TABLEID)</a></td>
<td>Die JetUpdate-Funktion führt einen Aktualisierungsvorgang aus, einschließlich einfügen einer neuen Zeile in eine Tabelle oder Aktualisieren einer vorhandenen Zeile. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von <a href="dn292131(v=exchg.10).md">JetDelete(JET_SESID, JET_TABLEID).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334023(v=exchg.10).md">JetUpdate(JET_SESID, JET_TABLEID, [], Int32, Int32)</a></td>
<td>Die JetUpdate-Funktion führt einen Aktualisierungsvorgang aus, einschließlich einfügen einer neuen Zeile in eine Tabelle oder Aktualisieren einer vorhandenen Zeile. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von <a href="dn292131(v=exchg.10).md">JetDelete(JET_SESID, JET_TABLEID).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334042(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Boolean, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334026(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Byte, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334044(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, [], MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334025(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, DateTime, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334046(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Double, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334030(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334048(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Int16, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334031(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Int32, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334050(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Int64, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334033(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, Single, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334052(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334054(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334034(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334038(v=exchg.10).md">MakeKey(JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der dann von <a href="dn334003(v=exchg.10).md">JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)</a> und <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334058(v=exchg.10).md">MoveAfterLast</a></td>
<td>Positionieren Sie den Cursor nach dem letzten Datensatz in der Tabelle. Ein nachfolgender vorheriger Schritt positioniert den Cursor auf dem letzten Datensatz.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334057(v=exchg.10).md">MoveBeforeFirst</a></td>
<td>Positionieren Sie den Cursor vor dem ersten Datensatz in der Tabelle. Bei einem nachfolgenden nächsten Schritt wird der Cursor auf dem ersten Datensatz positioniert.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334040(v=exchg.10).md">ResetIndexRange</a></td>
<td>Entfernt einen Indexbereich, der mit <a href="dn334024(v=exchg.10).md">JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a> oder <a href="dn334099(v=exchg.10).md">TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>erstellt wurde. Wenn kein Indexbereich vorhanden ist, führt diese Methode nichts aus.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursorkopierpuffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Indexeintrag abrufen, der auf den aktuellen Datensatz verweist. Neben dem Abrufen des tatsächlichen Spaltenwerts kann JetRetrieveColumn auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, damit die Größe der Anwendungspuffer entsprechend angepasst werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334045(v=exchg.10).md">RetrieveColumnAsBoolean(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen booleschen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334078(v=exchg.10).md">RetrieveColumnAsBoolean(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen booleschen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334047(v=exchg.10).md">RetrieveColumnAsByte(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen Bytespaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334074(v=exchg.10).md">RetrieveColumnAsByte(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen Bytespaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334077(v=exchg.10).md">RetrieveColumnAsDateTime(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen datetime-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334051(v=exchg.10).md">RetrieveColumnAsDateTime(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen datetime-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334053(v=exchg.10).md">RetrieveColumnAsDouble(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen double-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334084(v=exchg.10).md">RetrieveColumnAsDouble(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen double-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334056(v=exchg.10).md">RetrieveColumnAsFloat(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen Floatspaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334092(v=exchg.10).md">RetrieveColumnAsFloat(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen Floatspaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334093(v=exchg.10).md">RetrieveColumnAsGuid(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen GUID-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334061(v=exchg.10).md">RetrieveColumnAsGuid(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen GUID-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334062(v=exchg.10).md">RetrieveColumnAsInt16(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334098(v=exchg.10).md">RetrieveColumnAsInt16(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen int16-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334100(v=exchg.10).md">RetrieveColumnAsInt32(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334068(v=exchg.10).md">RetrieveColumnAsInt32(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen int32-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334066(v=exchg.10).md">RetrieveColumnAsInt64(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334091(v=exchg.10).md">RetrieveColumnAsInt64(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334067(v=exchg.10).md">RetrieveColumnAsString(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist. Die Unicode-Codierung wird verwendet.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334103(v=exchg.10).md">RetrieveColumnAsString(JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding)</a></td>
<td>Ruft einen Zeichenfolgenspaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334070(v=exchg.10).md">RetrieveColumnAsString(JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)</a></td>
<td>Ruft einen Zeichenfolgenspaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334069(v=exchg.10).md">RetrieveColumnAsUInt16(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen uint16-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334106(v=exchg.10).md">RetrieveColumnAsUInt16(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen uint16-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334108(v=exchg.10).md">RetrieveColumnAsUInt32(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen uint32-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334073(v=exchg.10).md">RetrieveColumnAsUInt32(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen uint32-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334072(v=exchg.10).md">RetrieveColumnAsUInt64(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen uint64-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334113(v=exchg.10).md">RetrieveColumnAsUInt64(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Ruft einen uint64-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334075(v=exchg.10).md">RetrieveColumns</a></td>
<td>Ruft Spalten in ColumnValue-Objekte ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334076(v=exchg.10).md">RetrieveColumnSize(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft die Größe eines einzelnen Spaltenwerts aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursorkopierpuffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Indexeintrag abrufen, der auf den aktuellen Datensatz verweist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334117(v=exchg.10).md">RetrieveColumnSize(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</a></td>
<td>Ruft die Größe eines einzelnen Spaltenwerts aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der dem Indexeintrag an der aktuellen Position des Cursors zugeordnet ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursorkopierpuffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Indexeintrag abrufen, der auf den aktuellen Datensatz verweist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334085(v=exchg.10).md">RetrieveKey</a></td>
<td>Ruft den Schlüssel für den Indexeintrag an der aktuellen Position eines Cursors ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334120(v=exchg.10).md">SerializeObjectToColumn</a></td>
<td>Schreiben Sie eine serialisierte Form eines Objekts in eine Spalte.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334123(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Boolean)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334080(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Byte)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334121(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [])</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334082(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334125(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Double)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334081(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Guid)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334127(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334083(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334130(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334087(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, Single)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334132(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334086(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334135(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334089(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], SetColumnGrbit)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334136(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334090(v=exchg.10).md">SetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding, SetColumnGrbit)</a></td>
<td>Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334138(v=exchg.10).md">Setcolumns</a></td>
<td>Legt Spalten aus ColumnValue-Objekten fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334139(v=exchg.10).md">TryGetLock</a></td>
<td>Reservieren Sie explizit die Möglichkeit, eine Zeile zu aktualisieren, eine Schreibsperre zu schreiben oder explizit zu verhindern, dass eine Zeile von einer anderen Sitzung aktualisiert wird. Lesesperre. Normalerweise werden Zeilen-Schreibsperren implizit durch aktualisierende Zeilen aktiviert. Lesesperren sind in der Regel nicht erforderlich, da die Datensatzversionsversionen nicht verfügbar sind. In einigen Fällen möchte eine Transaktion jedoch möglicherweise eine Zeile explizit sperren, um die Serialisierung zu erzwingen, oder um sicherzustellen, dass ein nachfolgender Vorgang erfolgreich ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334094(v=exchg.10).md">TryMove</a></td>
<td>Versuchen Sie, durch einen Index zu navigieren. Wenn die Navigation erfolgreich ist, gibt diese Methode TRUE zurück. Wenn kein Datensatz für die Navigation zu dieser Methode vorkommt, wird false zurückgegeben. Für andere Fehler wird eine Ausnahme ausgelöst.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334150(v=exchg.10).md">TryMoveFirst</a></td>
<td>Versuchen Sie, zum ersten Datensatz in der Tabelle zu wechseln. Wenn die Tabelle leer ist, wird false zurückgegeben, wenn ein anderer Fehler auftritt, wird eine Ausnahme ausgelöst.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334140(v=exchg.10).md">TryMoveLast</a></td>
<td>Versuchen Sie, zum letzten Datensatz in der Tabelle zu wechseln. Wenn die Tabelle leer ist, wird false zurückgegeben, wenn ein anderer Fehler auftritt, wird eine Ausnahme ausgelöst.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334095(v=exchg.10).md">TryMoveNext</a></td>
<td>Versuchen Sie, zum nächsten Datensatz in der Tabelle zu wechseln. Wenn kein nächster Datensatz vorhanden ist, wird false zurückgegeben. Wenn ein anderer Fehler auftritt, wird eine Ausnahme ausgelöst.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334144(v=exchg.10).md">TryMovePrevious</a></td>
<td>Versuchen Sie, zum vorherigen Datensatz in der Tabelle zu wechseln. Wenn kein vorheriger Datensatz vorhanden ist, wird false zurückgegeben. Wenn ein anderer Fehler auftritt, wird eine Ausnahme ausgelöst.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334096(v=exchg.10).md">TryOpenTable</a></td>
<td>Versuchen Sie, eine Tabelle zu öffnen.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334145(v=exchg.10).md">TrySeek</a></td>
<td>Positioniert einen Cursor effizient auf einen Indexeintrag, der den durch den Suchschlüssel in diesem Cursor angegebenen Suchkriterien und der angegebenen Ungleichheit entspricht. Ein Suchschlüssel muss zuvor mit JetMakeKey erstellt worden sein.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334099(v=exchg.10).md">TrySetIndexRange</a></td>
<td>Begrenzt vorübergehend den Satz von Indexeinträgen, die der Cursor mit JetMove verwenden kann, auf diejenigen, die ab dem aktuellen Indexeintrag beginnen und am Indexeintrag enden, der den Suchkriterien entspricht, die vom Suchschlüssel in diesem Cursor und den angegebenen gebundenen Kriterien angegeben werden. Ein Suchschlüssel muss zuvor mit JetMakeKey erstellt worden sein. Gibt TRUE zurück, wenn der Indexbereich nicht leer ist, andernfalls FALSE.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

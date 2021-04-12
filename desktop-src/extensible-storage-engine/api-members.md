---
description: 'Weitere Informationen finden Sie hier: API-Member'
title: API-Mitglieder
TOCTitle: Api members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api_members(v=EXCHG.10)
ms:contentKeyID: 55100778
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e1debc551dc644d71568772761cb14500d2fd546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393322"
---
# <a name="api-members"></a>API-Mitglieder

Geschützte Member einschließen  
Geerbte Member einschließen  

Verwaltete Versionen der ESENT-API. Diese Klasse enthält statische Methoden, die der nicht verwalteten ESENT-API entsprechen. Diese Methoden lösen Ausnahmen aus, wenn Fehler zurückgegeben werden. Hilfsmethoden für die ESENT-API. Diese Wrap jetmakekey. Interne Methoden der API. Hilfsmethoden für die ESENT-API. Diese durchführen die Datenkonvertierung für jetmakekey. Hilfsmethoden für die ESENT-API. Diese Methoden behandeln Daten Bank Metadaten. Hilfsmethoden für die ESENT-API. Dabei handelt es sich nicht um Interop-Versionen der API, sondern um sehr häufige Verwendungsmöglichkeiten der Funktionen. API-Member, die als veraltet markiert sind. Hilfsmethoden für die ESENT-API. Dabei handelt es sich nicht um Interop-Versionen der API, sondern um sehr häufige Verwendungsmöglichkeiten der Funktionen. Hilfsmethoden für die ESENT-API. Dies geschieht bei der Datenkonvertierung für das Festlegen von Spalten.

Der [API](./api-class.md) -Typ macht die folgenden Member verfügbar.

## <a name="methods"></a>Methoden

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292138(v=exchg.10).md">Deserializeobjectfromcolumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Deserialisieren eines Objekts aus einer Spalte.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292115(v=exchg.10).md">Deserializeobjectfromcolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Deserialisieren eines Objekts aus einer Spalte.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292114(v=exchg.10).md">Escrowupdate</a></td>
<td>Durchführen einer atomaren Addition für eine Spalte Die Spalte muss den Typ " <a href="hh577895(v=exchg.10).md">Long</a>" aufweisen. Diese Funktion ermöglicht es mehreren Sitzungen, denselben Datensatz gleichzeitig zu aktualisieren, ohne dass Konflikte auftreten.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292099(v=exchg.10).md">GetBookmark</a></td>
<td>Ruft das Lesezeichen für den Datensatz ab, der mit dem Index Eintrag an der aktuellen Position eines Cursors verknüpft ist. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von jetgobackbookmark wieder in denselben Datensatz zu positionieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292098(v=exchg.10).md">Getcolumndictionary</a></td>
<td>Erstellt ein Wörterbuch, das Spaltennamen ihren Spalten-IDs zuordnet.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292101(v=exchg.10).md">Gettablecolumnid</a></td>
<td>Das ColumnID der angegebenen Spalte.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292090(v=exchg.10).md">Gettablecolumns (JET_SESID JET_TABLEID)</a></td>
<td>Durchläuft alle Spalten in der Tabelle, wobei Informationen zu den einzelnen Spalten zurückgegeben werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292089(v=exchg.10).md">Gettablecolumns (JET_SESID, JET_DBID, Zeichenfolge)</a></td>
<td>Durchläuft alle Spalten in der Tabelle, wobei Informationen zu den einzelnen Spalten zurückgegeben werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292093(v=exchg.10).md">Gettableindexes (JET_SESID JET_TABLEID)</a></td>
<td>Durchläuft alle Indizes in der Tabelle, wobei Informationen zu den einzelnen Indizes zurückgegeben werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292092(v=exchg.10).md">Gettableindexes (JET_SESID, JET_DBID, Zeichenfolge)</a></td>
<td>Durchläuft alle Index in der Tabelle, wobei Informationen zu den einzelnen Indizes zurückgegeben werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292095(v=exchg.10).md">Gettablenames</a></td>
<td>Gibt die Namen der Tabellen in der Datenbank zurück.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292094(v=exchg.10).md">Intersectindexes</a></td>
<td>Intersect eine Gruppe von Index Bereichen und gibt die Lesezeichen der Datensätze zurück, die in allen Index Bereichen gefunden werden. Siehe auch <a href="dn292212(v=exchg.10).md">jetintersectindexes (JET_SESID, [], Int32, JET_RECORDLIST, intersectindexesgrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292097(v=exchg.10).md">Jetaddcolumn</a></td>
<td>Fügen Sie einer vorhandenen Tabelle eine neue Spalte hinzu.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292096(v=exchg.10).md">Jetattachdatabase</a></td>
<td>Fügt eine Datenbankdatei für die Verwendung mit einer Daten Bank Instanz an. Damit die Datenbank verwendet werden kann, muss Sie anschließend mit <a href="dn292219(v=exchg.10).md">jetopendatabase (JET_SESID, String, String, JET_DBID, opendatabasegrbit)</a>geöffnet werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292100(v=exchg.10).md">JetAttachDatabase2</a></td>
<td>Fügt eine Datenbankdatei für die Verwendung mit einer Daten Bank Instanz an. Damit die Datenbank verwendet werden kann, muss Sie anschließend mit <a href="dn292219(v=exchg.10).md">jetopendatabase (JET_SESID, String, String, JET_DBID, opendatabasegrbit)</a>geöffnet werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292102(v=exchg.10).md">Jetbackupinstance</a></td>
<td>Führt eine Streamingsicherung einer Instanz, einschließlich aller angefügten Datenbanken, in ein Verzeichnis aus. Mit mehreren Sicherungsmethoden, die von der-Engine unterstützt werden, ist dies die einfachste und gekapselte Funktion.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292104(v=exchg.10).md">Jetbeginexternalbackupinstance</a></td>
<td>Initiiert eine externe Sicherung, während die-Engine und die-Datenbank online und aktiv sind.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292103(v=exchg.10).md">Jetbeginsession</a></td>
<td>Initialisieren Sie eine neue ESENT-Sitzung.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292105(v=exchg.10).md">Jetbegintransaction</a></td>
<td>Bewirkt, dass eine Sitzung eine Transaktion eingibt oder einen neuen Sicherungspunkt in einer vorhandenen Transaktion erstellt.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292106(v=exchg.10).md">JetBeginTransaction2</a></td>
<td>Bewirkt, dass eine Sitzung eine Transaktion eingibt oder einen neuen Sicherungspunkt in einer vorhandenen Transaktion erstellt.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292107(v=exchg.10).md">Jetclosedatabase</a></td>
<td>Schließt eine Datenbankdatei, die zuvor mit <a href="dn292219(v=exchg.10).md">jetopendatabase (JET_SESID, String, String, JET_DBID, opendatabasegrbit)</a> geöffnet wurde oder mit <a href="dn292118(v=exchg.10).md">jetfoatedatabase (JET_SESID, String, String, JET_DBID, kreatedatabasegrbit)</a>erstellt wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292108(v=exchg.10).md">Jetclosefilinput Stance</a></td>
<td>Schließt eine Datei, die mit jetopenfileinstance geöffnet wurde, nachdem die Daten aus dieser Datei mit jetreadfileinstance extrahiert wurden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292109(v=exchg.10).md">Jetclosetable</a></td>
<td>Schließen Sie eine geöffnete Tabelle.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292110(v=exchg.10).md">Jetcommittransaction</a></td>
<td>Führt einen Commit für die Änderungen aus, die an den Zustand der Datenbank während des aktuellen Speicher Punkts vorgenommen werden, und migriert Sie zum vorherigen Sicherungspunkt. Wenn für den äußersten Speicherpunkt ein Commit ausgeführt wird, werden die während dieses Speicher Punkts vorgenommenen Änderungen in den Zustand der Datenbank übertragen, und die Sitzung wird beendet.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292112(v=exchg.10).md">Jetcompact</a></td>
<td>Erstellt eine Kopie einer vorhandenen Datenbank. Die Kopie wird zu einem für die Verwendung optimalen Zustand komprimiert. Die Daten in den kopierten Daten werden entsprechend den Measures verpackt, die bei der Indexerstellung für die Indizes ausgewählt wurden. Auf diese Weise können komprimierte Daten so dicht wie möglich gespeichert werden. Alternativ können durch komprimierte Datenspeicher Platz für nachfolgende Daten Satz Vergrößerung oder Index Einfügungen reserviert werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292113(v=exchg.10).md">Jetcomputestats</a></td>
<td>Führt jeden Index einer Tabelle aus, um die Anzahl der Einträge in einem Index und die Anzahl der unterschiedlichen Schlüssel in einem Index exakt zu berechnen. Diese Informationen werden in Verbindung mit der Anzahl von Datenbankseiten, die für einen Index zugeordnet sind, und dem aktuellen Zeitpunkt der Berechnung in den Index Metadaten in der Datenbank gespeichert. Diese Daten können anschließend mit Informations Vorgängen abgerufen werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292118(v=exchg.10).md">Jetkreatedatabase</a></td>
<td>Erstellt eine Datenbankdatei und fügt Sie an.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292120(v=exchg.10).md">JetCreateDatabase2</a></td>
<td>Erstellt eine Datenbankdatei mit einer angegebenen maximalen Datenbankgröße und fügt Sie an.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292121(v=exchg.10).md">Jetkreateingedex</a></td>
<td>Erstellt einen Index über Daten in einer ESE-Datenbank. Ein Index kann verwendet werden, um bestimmte Daten schnell zu suchen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292123(v=exchg.10).md">JetCreateIndex2</a></td>
<td>Erstellt Indizes für Daten in einer ESE-Datenbank.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292122(v=exchg.10).md">Jetkreateingestance</a></td>
<td>Ordnet eine neue Instanz der Datenbank-Engine zu.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292126(v=exchg.10).md">JetCreateInstance2</a></td>
<td>Weisen Sie eine neue Instanz der Datenbank-Engine für die Verwendung in einem einzelnen Prozess mit einem angegebenen anzeigen Amen zu.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292127(v=exchg.10).md">Jetkreatetable</a></td>
<td>Erstellen Sie eine leere Tabelle. Die neu erstellte Tabelle wird exklusiv geöffnet.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3</a></td>
<td>Erstellt eine Tabelle, fügt der Tabelle Spalten und Indizes hinzu.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292130(v=exchg.10).md">Jetdebug</a></td>
<td>Startet und beendet datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292145(v=exchg.10).md">JetDefragment2</a></td>
<td>Startet und beendet datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292131(v=exchg.10).md">Jetdelete</a></td>
<td>Löscht den aktuellen Datensatz in einer Datenbanktabelle.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292133(v=exchg.10).md">Jetdeletecolumn</a></td>
<td>Löscht eine Spalte aus einer Datenbanktabelle.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292132(v=exchg.10).md">JetDeleteColumn2</a></td>
<td>Löscht eine Spalte aus einer Datenbanktabelle.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292135(v=exchg.10).md">Jetdelta-eindex</a></td>
<td>Löscht einen Index aus einer Datenbanktabelle.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292134(v=exchg.10).md">Jetdeletetable</a></td>
<td>Löscht eine Tabelle aus einer Datenbank.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292139(v=exchg.10).md">Jetdetachdatabase</a></td>
<td>Gibt eine Datenbankdatei frei, die zuvor an eine Daten banksitzung angefügt wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292136(v=exchg.10).md">JetDetachDatabase2</a></td>
<td>Gibt eine Datenbankdatei frei, die zuvor an eine Daten banksitzung angefügt wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292137(v=exchg.10).md">Jetdupcursor</a></td>
<td>Dupliziert einen geöffneten Cursor und gibt ein Handle für den duplizierten Cursor zurück. Wenn der duplizierte Cursor ein Schreib geschützter Cursor war, ist der duplizierte Cursor ebenfalls ein Schreib geschützter Cursor. Jeder Status im Zusammenhang mit dem Erstellen eines Suchschlüssels oder dem Aktualisieren eines Datensatzes wird nicht in den doppelten Cursor kopiert. Außerdem wird der Speicherort des ursprünglichen Cursors nicht in den doppelten Cursor dupliziert. Der doppelte Cursor wird immer auf dem gruppierten Index geöffnet, und sein Speicherort ist immer in der ersten Zeile der Tabelle.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292140(v=exchg.10).md">Jetdupsession</a></td>
<td>Initialisiert eine neue ESE-Sitzung in der gleichen Instanz wie die angegebene-SID.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292142(v=exchg.10).md">Jetendexternalbackupinstance</a></td>
<td>Beendet eine externe Sicherungs Sitzung. Diese API ist die letzte API in einer Reihe von APIs, die aufgerufen werden muss, um eine erfolgreiche (nicht auf VSS basierende) Online Sicherung auszuführen.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292143(v=exchg.10).md">JetEndExternalBackupInstance2</a></td>
<td>Beendet eine externe Sicherungs Sitzung. Diese API ist die letzte API in einer Reihe von APIs, die aufgerufen werden muss, um eine erfolgreiche (nicht auf VSS basierende) Online Sicherung auszuführen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292144(v=exchg.10).md">Jetendsession</a></td>
<td>Beendet eine Sitzung.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292148(v=exchg.10).md">Jetenreeratecolumschlag</a></td>
<td>Ruft effizient eine Gruppe von Spalten und deren Werten aus dem aktuellen Datensatz eines Cursors oder dem Kopier Puffer dieses Cursors ab. Die abgerufenen Spalten und Werte können durch eine Liste von Spalten-IDs, itagsequence-Nummern und anderen Merkmalen eingeschränkt werden. Diese Spalten Abruf-API ist eindeutig, da Sie Informationen in dynamisch zugewiesener Speicher zurückgibt, die mit einem vom Benutzer bereitgestellten rezuordnungskompatiblen Rückruf abgerufen werden. Diese neue Flexibilität ermöglicht das effiziente Abrufen von Spaltendaten mit bestimmten Merkmalen (z. b. Größe und Multiplizität), die dem Aufrufer unbekannt sind. Dadurch ist es nicht mehr erforderlich, die Ermittlungs Modi jetretrievecolumgen zu verwenden, um die Eigenschaften zu bestimmen, um einen letzten Rückruf für jetretrievecolumschlag einzurichten, mit dem die gewünschten Daten erfolgreich abgerufen werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292150(v=exchg.10).md">Jetescrowupdate</a></td>
<td>Führt eine atomarische Additions Operation für eine Spalte aus. Diese Funktion ermöglicht es mehreren Sitzungen, denselben Datensatz gleichzeitig zu aktualisieren, ohne dass Konflikte auftreten. Siehe auch <a href="dn292114(v=exchg.10).md">escrowupdate (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292147(v=exchg.10).md">Jetfrebuffer</a></td>
<td>Gibt Arbeitsspeicher frei, der durch einen Datenbankmodul-Befehl zugeordnet wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292154(v=exchg.10).md">Jetgetattachinfoinstance</a></td>
<td>Wird bei einer von <a href="dn292104(v=exchg.10).md">jetbeginexternalbackupinstance initiierten Sicherung (JET_INSTANCE beginexternalbackupgrbit)</a> verwendet, um eine Instanz nach den Namen von Datenbankdateien abzufragen, die Teil des Sicherungsdatei Satzes werden sollen. Nur Datenbanken, die zurzeit an die Instanz mit <a href="dn292096(v=exchg.10).md">jetattachdatabase (JET_SESID, String, attachdatabasegrbit)</a> angefügt sind, werden berücksichtigt. Diese Dateien können anschließend mit <a href="dn292230(v=exchg.10).md">jetopenfileinstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> geöffnet und mit <a href="dn332987(v=exchg.10).md">jetreadfileinstance (JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>gelesen werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292149(v=exchg.10).md">Jetgetbookmark</a></td>
<td>Ruft das Lesezeichen für den Datensatz ab, der mit dem Index Eintrag an der aktuellen Position eines Cursors verknüpft ist. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von <a href="dn292200(v=exchg.10).md">jetgobackbookmark (JET_SESID, JET_TABLEID, [], Int32)</a>wieder in denselben Datensatz zu positionieren. Das Lesezeichen ist nicht länger als <a href="dn351215(v=exchg.10).md">Lese</a> Zeichen. Siehe auch <a href="dn292099(v=exchg.10).md">GetBookmark (JET_SESID JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292158(v=exchg.10).md">Jetgetcolumninfo (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, JET_COLUMNBASE)</a></td>
<td>Ruft Informationen zu einer Spalte in einer Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292151(v=exchg.10).md">Jetgetcolumninfo (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, JET_COLUMNDEF)</a></td>
<td>Ruft Informationen über eine Tabellenspalte ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292152(v=exchg.10).md">Jetgetcolumninfo (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, JET_COLUMNLIST)</a></td>
<td>Ruft Informationen zu allen Spalten in einer Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292153(v=exchg.10).md">Jetgetcurrentindex</a></td>
<td>Dlegt den Namen des aktuellen Indexes eines angegebenen Cursors fest. Dieser Name wird auch verwendet, um den Index später mithilfe von <a href="dn334011(v=exchg.10).md">jetsetcurrentindex (JET_SESID, JET_TABLEID, String)</a>als aktuellen Index erneut auszuwählen. Sie kann auch verwendet werden, um die Eigenschaften dieses Indexes mithilfe von jetgettableindexinfo zu ermitteln.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292155(v=exchg.10).md">Jetgetcursor Info</a></td>
<td>Bestimmen, ob ein Update des aktuellen Datensatzes eines Cursors zu einem Schreib Konflikt führt, basierend auf dem aktuellen Update Status des Datensatzes. Es ist möglich, dass ein Schreib Konflikt letztendlich zurückgegeben wird, auch wenn jetgetcurrsorinfo erfolgreich zurückgegeben wurde. Da eine andere Sitzung den Datensatz aktualisieren kann, bevor die aktuelle Sitzung denselben Datensatz aktualisieren kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292159(v=exchg.10).md">Jetgetdatabasefileingefo (Zeichenfolge, JET_DBINFOMISC JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen über die angegebene Datenbank ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292161(v=exchg.10).md">Jetgetdatabasefileingefo (String, Int32, JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen über die angegebene Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292160(v=exchg.10).md">Jetgetdatabasefileingefo (String, Int64, JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen über die angegebene Datenbank ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292162(v=exchg.10).md">Jetgetdatabaseingefo (JET_SESID, JET_DBID, JET_DBINFOMISC, JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen über die angegebene Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292164(v=exchg.10).md">Jetgetdatabaseingefo (JET_SESID, JET_DBID, Int32, JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen über die angegebene Datenbank ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292167(v=exchg.10).md">Jetgetdatabaseingefo (JET_SESID, JET_DBID, Zeichenfolge, JET_DbInfo)</a></td>
<td>Ruft bestimmte Informationen über die angegebene Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292168(v=exchg.10).md">Jetgetindexinfo (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, JET_INDEXLIST)</a></td>
<td><strong>Veraltet.</strong> Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292172(v=exchg.10).md">Jetgetindexinfo (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292166(v=exchg.10).md">Jetgetindexinfo (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292171(v=exchg.10).md">Jetgetindexinfo (JET_SESID, JET_DBID, String, String, Int32, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292169(v=exchg.10).md">Jetgetindexinfo (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, Zeichenfolge, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292173(v=exchg.10).md">Jetgetindexinfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292170(v=exchg.10).md">Jetgetinstanceingefo</a></td>
<td>Ruft Informationen zu den Instanzen ab, die ausgeführt werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292175(v=exchg.10).md">Jetgetlock</a></td>
<td>Reservieren Sie explizit die Möglichkeit, eine Zeile zu aktualisieren, eine Sperre zu schreiben oder explizit zu verhindern, dass eine Zeile von einer anderen Sitzung aktualisiert wird, und lesen Sie sperren. Normalerweise werden Zeilen Schreib Sperren implizit durch das Aktualisieren von Zeilen abgerufen. Lese Sperren sind in der Regel aufgrund von Daten Satz Versionsverwaltung nicht erforderlich. In einigen Fällen möchte eine Transaktion jedoch möglicherweise eine Zeile explizit sperren, um die Serialisierung zu erzwingen, oder um sicherzustellen, dass ein nachfolgender Vorgang erfolgreich ausgeführt wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292174(v=exchg.10).md">Jetgetloginfoinstance</a></td>
<td>Wird bei einer von <a href="dn292104(v=exchg.10).md">jetbeginexternalbackupinstance initiierten Sicherung (JET_INSTANCE, beginexternalbackupgrbit)</a> verwendet, um eine Instanz für die Namen von datenbankpatchdateien und Protokolldateien abzufragen, die Teil der Sicherungsdatei Gruppe werden sollen. Diese Dateien können anschließend mit <a href="dn292230(v=exchg.10).md">jetopenfileinstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> geöffnet und mit <a href="dn332987(v=exchg.10).md">jetreadfileinstance (JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>gelesen werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292177(v=exchg.10).md">Jetgetls</a></td>
<td>Ermöglicht der Anwendung das Abrufen des Kontext Handles, das als lokaler Speicher bezeichnet wird, der einem Cursor oder der diesem Cursor zugeordneten Tabelle zugeordnet ist. Dieses Kontext Handle muss zuvor mithilfe von <a href="dn334015(v=exchg.10).md">jetsetls (JET_SESID, JET_TABLEID, JET_LS, lsgrbit)</a>festgelegt werden. Jetgetls kann auch zum gleichzeitigen Abrufen des aktuellen Kontext Handles für einen Cursor oder eine Tabelle und zum Zurücksetzen dieses Kontext Handles verwendet werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292179(v=exchg.10).md">Jetgetobjectinfo (JET_SESID, JET_DBID, JET_OBJECTLIST)</a></td>
<td>Ruft Informationen zu Datenbankobjekten ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292178(v=exchg.10).md">Jetgetobjectinfo (JET_SESID, JET_DBID, JET_objtyp, Zeichenfolge, JET_OBJECTINFO)</a></td>
<td>Ruft Informationen zu Datenbankobjekten ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292181(v=exchg.10).md">Jetgetrecordposition</a></td>
<td>Gibt die Bruch Position des aktuellen Datensatzes im aktuellen Index in Form einer <a href="dn335256(v=exchg.10).md">JET_RECPOS</a> Struktur zurück. Siehe auch <a href="dn292207(v=exchg.10).md">jetgotoposition (JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292180(v=exchg.10).md">Jetgetsecondaryindexbookmark</a></td>
<td>Ruft ein spezielles Lesezeichen für den sekundären Index Eintrag an der aktuellen Position eines Cursors ab. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von jetgoysecondaryindexbookmark effizient wieder in denselben Index Eintrag zu positionieren. Dies ist besonders nützlich, wenn Sie einen sekundären Index neu positionieren, der doppelte Schlüssel enthält oder mehrere Indexeinträge für denselben Datensatz enthält.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292182(v=exchg.10).md">Jetgetsystemparameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</a></td>
<td>Ruft Daten Bank Konfigurationsoptionen ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292185(v=exchg.10).md">Jetgetsystemparameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)</a></td>
<td>Ruft Daten Bank Konfigurationsoptionen ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292186(v=exchg.10).md">Jetgettablecolumninfo (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</a></td>
<td>Ruft Informationen über eine Tabellenspalte ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292187(v=exchg.10).md">Jetgettablecolumninfo (JET_SESID, JET_TABLEID, Zeichenfolge, JET_COLUMNDEF)</a></td>
<td>Ruft Informationen über eine Tabellenspalte ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292189(v=exchg.10).md">Jetgettablecolumninfo (JET_SESID, JET_TABLEID, Zeichenfolge, JET_COLUMNLIST)</a></td>
<td>Ruft Informationen zu allen Spalten in der Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292191(v=exchg.10).md">Jetgettableindexinfo (JET_SESID, JET_TABLEID, Zeichenfolge, JET_INDEXLIST)</a></td>
<td><strong>Veraltet.</strong> Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292190(v=exchg.10).md">Jetgettableindexinfo (JET_SESID, JET_TABLEID, Zeichenfolge, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292196(v=exchg.10).md">Jetgettableindexinfo (JET_SESID, JET_TABLEID, Zeichenfolge, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292193(v=exchg.10).md">Jetgettableindexinfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292192(v=exchg.10).md">Jetgettableindexinfo (JET_SESID, JET_TABLEID, Zeichenfolge, Zeichenfolge, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292195(v=exchg.10).md">Jetgettableindexinfo (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</a></td>
<td>Ruft Informationen zu Indizes in einer Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292197(v=exchg.10).md">Jetgettableinfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a></td>
<td>Ruft verschiedene Informationen zu einer Tabelle in einer-Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292198(v=exchg.10).md">Jetgettableinfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a></td>
<td>Ruft verschiedene Informationen zu einer Tabelle in einer-Datenbank ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292201(v=exchg.10).md">Jetgettableinfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a></td>
<td>Ruft verschiedene Informationen zu einer Tabelle in einer-Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292202(v=exchg.10).md">Jetgettableinfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a></td>
<td>Ruft verschiedene Informationen zu einer Tabelle in einer-Datenbank ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292204(v=exchg.10).md">Jetgettableinfo (JET_SESID, JET_TABLEID, Zeichenfolge, JET_TblInfo)</a></td>
<td>Ruft verschiedene Informationen zu einer Tabelle in einer-Datenbank ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292199(v=exchg.10).md">Jetgettruneureloginfoinstance</a></td>
<td>Wird bei einer von <a href="dn292104(v=exchg.10).md">jetbeginexternalbackupinstance initiierten Sicherung (JET_INSTANCE beginexternalbackupgrbit)</a> verwendet, um eine Instanz nach den Namen der Transaktionsprotokoll Dateien abzufragen, die nach erfolgreichem Abschluss der Sicherung sicher gelöscht werden können.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292203(v=exchg.10).md">Jetgetversion</a></td>
<td>Ruft die Version der Datenbank-Engine ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292200(v=exchg.10).md">Jetgojebookmark</a></td>
<td>Positioniert einen Cursor auf einen Index Eintrag für den Datensatz, der dem angegebenen Lesezeichen zugeordnet ist. Das Lesezeichen kann mit jedem für eine Tabelle definierten Index verwendet werden. Das Lesezeichen für einen Datensatz kann mithilfe von <a href="dn292149(v=exchg.10).md">jetgetbookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>abgerufen werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292207(v=exchg.10).md">Jetgotoposition</a></td>
<td>Verschiebt einen Cursor an eine neue Position, die ein Bruchteil der Art und Weise des aktuellen Indexes ist. Siehe auch <a href="dn292181(v=exchg.10).md">jetgetrecordposition (JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292205(v=exchg.10).md">Jetgoysecondaryindexbookmark</a></td>
<td>Positioniert einen Cursor auf einen Index Eintrag, der dem angegebenen sekundären Index Lesezeichen zugeordnet ist. Das sekundäre Index Lesezeichen muss mit demselben Index für dieselbe Tabelle verwendet werden, aus der es ursprünglich abgerufen wurde. Das sekundäre Index Lesezeichen für einen Index Eintrag kann mithilfe von <a href="dn292205(v=exchg.10).md">jetgoessecondaryindexbookmark (JET_SESID, JET_TABLEID, [], Int32, [], Int32, GOTO secondaryindexbookmarkgrbit)</a>abgerufen werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292206(v=exchg.10).md">Jetgrowdatabase</a></td>
<td>Erweitert die Größe einer Datenbank, die derzeit geöffnet ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292208(v=exchg.10).md">Jetidle</a></td>
<td>Führt Cleanuptasks im Leerlauf aus oder überprüft den Versionsspeicher Status in ESE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292209(v=exchg.10).md">Jetindexrecordcount</a></td>
<td>Zählt die Anzahl der Einträge im aktuellen Index von der aktuellen Position nach vorne. Die aktuelle Position ist in der Anzahl enthalten. Die Anzahl kann größer als die Gesamtanzahl der Datensätze in der Tabelle sein, wenn der aktuelle Index eine mehrwertige Spalte überschreitet und Instanzen der Spalte mehrere Werte aufweisen. Wenn die Tabelle leer ist, wird 0 für die Anzahl zurückgegeben.</td>
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
<td><a href="dn292212(v=exchg.10).md">Jetintersectindexes</a></td>
<td>Berechnet die Schnittmenge zwischen mehreren Sätzen von Indexeinträgen aus unterschiedlichen sekundären Indizes für dieselbe Tabelle. Dieser Vorgang ist nützlich, um die Gruppe von Datensätzen in einer Tabelle zu suchen, die mit zwei oder mehr Kriterien übereinstimmen, die mithilfe von Index Bereichen ausgedrückt werden können. Siehe auch " <a href="dn292094(v=exchg.10).md">intersectindexes" (JET_SESID, [])</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292216(v=exchg.10).md">Jetmakekey</a></td>
<td>Erstellt Suchschlüssel, die dann von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden können.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292218(v=exchg.10).md">Jetmove (JET_SESID, JET_TABLEID, JET_Move, movegrbit)</a></td>
<td>Navigieren Sie durch einen Index. Der Cursor kann am Anfang oder Ende des Indexes positioniert und um eine angegebene Anzahl von Indexeinträgen rückwärts und vorwärts verschoben werden. Siehe auch <a href="dn334150(v=exchg.10).md">trymuvefirst (JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">trymuvelast (JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">trymuvenext (JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">trymuveprevious (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292217(v=exchg.10).md">Jetmove (JET_SESID, JET_TABLEID, Int32, movegrbit)</a></td>
<td>Navigieren Sie durch einen Index. Der Cursor kann am Anfang oder Ende des Indexes positioniert und um eine angegebene Anzahl von Indexeinträgen rückwärts und vorwärts verschoben werden. Siehe auch <a href="dn334150(v=exchg.10).md">trymuvefirst (JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">trymuvelast (JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">trymuvenext (JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">trymuveprevious (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292219(v=exchg.10).md">Jetopumdatabase</a></td>
<td>Öffnet eine Datenbank, die zuvor mit <a href="dn292096(v=exchg.10).md">jetattachdatabase (JET_SESID, String, attachdatabasegrbit)</a>angefügt wurde, damit Sie mit einer Daten banksitzung verwendet werden kann. Diese Funktion kann für dieselbe Datenbank mehrmals aufgerufen werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292230(v=exchg.10).md">Jetopeinfileinstance</a></td>
<td>Öffnet eine angefügte Datenbank, datenbankpatchdatei oder Transaktionsprotokoll Datei einer aktiven Instanz zum Ausführen einer Streaming-Fuzzy-Sicherung. Die Daten aus diesen Dateien können anschließend mithilfe von jetreadfileinstance durch das zurückgegebene Handle gelesen werden. Das zurückgegebene Handle muss mithilfe von jetclosefilinput Stance geschlossen werden. Eine externe Sicherung der Instanz muss mithilfe von jetbeginexternalbackupinstance initiiert werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292234(v=exchg.10).md">Jetopentable</a></td>
<td>Öffnet einen Cursor für eine zuvor erstellte Tabelle.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292231(v=exchg.10).md">Jetopumtemptable</a></td>
<td>Erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird. Siehe auch <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, temptablegrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">Jetopumtemporarytable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292232(v=exchg.10).md">JetOpenTempTable2</a></td>
<td>Erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird. Siehe auch <a href="dn292231(v=exchg.10).md">jetopentemptable (JET_SESID, [], Int32, temptablegrbit, JET_TABLEID, [])</a>, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, temptablegrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">Jetopumtemporarytable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292233(v=exchg.10).md">JetOpenTempTable3</a></td>
<td>Erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird. Siehe auch <a href="dn292231(v=exchg.10).md">jetopentemptable (JET_SESID, [], Int32, temptablegrbit, JET_TABLEID, [])</a>, <a href="dn335326(v=exchg.10).md">jetopentemporarytable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332998(v=exchg.10).md">Jeto ssnapshotfreeze</a></td>
<td>Startet eine Momentaufnahme. Während der Momentaufnahme kann keine Aktivität zum Schreiben von Datenträgern durch die Engine durchgeführt werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn292235(v=exchg.10).md">Jejessnapshotprepare</a></td>
<td>Startet die Vorbereitung für eine Momentaufnahme Sitzung. Eine Momentaufnahme Sitzung ist ein kurzes Zeitintervall, in dem die Engine keine Schreibvorgänge auf dem Datenträger ausgibt, sodass die Engine an einer volumemomentaufnahmensitzung teilnehmen kann (wenn Sie von einem Momentaufnahme-Writer gesteuert wird).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332986(v=exchg.10).md">Jejessnapshotthaw</a></td>
<td>Benachrichtigt die Engine, dass Sie normale e/a-Vorgänge nach einem Sperr Zeitraum und einem erfolgreichen Snapshot fortsetzen kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332988(v=exchg.10).md">Jetprepareupdate</a></td>
<td>Vorbereiten eines Cursors für die Aktualisierung.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332987(v=exchg.10).md">Jetreadfilinput Stance</a></td>
<td>Ruft den Inhalt einer Datei ab, die mit <a href="dn292230(v=exchg.10).md">jetopenfileinstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a>geöffnet wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332989(v=exchg.10).md">Jetregistercallback</a></td>
<td>Ermöglicht der Anwendung, die Datenbank-Engine so zu konfigurieren, dass Benachrichtigungen für bestimmte Ereignisse an die Anwendung ausgegeben werden. Diese Benachrichtigungen sind einer bestimmten Tabelle zugeordnet und bleiben nur wirksam, bis die Instanz, die die Tabelle enthält, mithilfe von <a href="dn334020(v=exchg.10).md">jetterm (JET_INSTANCE)</a>heruntergefahren wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332990(v=exchg.10).md">Jetrenamecolumschlag</a></td>
<td>Ändert den Namen einer vorhandenen Spalte.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332993(v=exchg.10).md">Jetrenametable</a></td>
<td>Ändert den Namen einer vorhandenen Tabelle.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332991(v=exchg.10).md">Jetresessioncontext</a></td>
<td>Trennt eine Sitzung vom aktuellen Thread. Dies sollte in Verbindung mit <a href="dn334027(v=exchg.10).md">jetsetup (JET_SESID, IntPtr)</a>verwendet werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332994(v=exchg.10).md">Jetresettablesequential</a></td>
<td>Benachrichtigt die Datenbank-Engine, dass die Anwendung nicht mehr den gesamten Index scannt, auf dem sich der Cursor befindet. Dieser Rückruf kehrt eine Benachrichtigung um, die von <a href="dn334018(v=exchg.10).md">jetsettablesequential (JET_SESID, JET_TABLEID, settablesequentialgrbit)</a>gesendet wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332992(v=exchg.10).md">Jetrestoreingestance</a></td>
<td>Stellt eine Streamingsicherung einer Instanz, einschließlich aller angefügten Datenbanken, wieder her. Es ist für die Arbeit mit einer Sicherung konzipiert, die mit der <a href="dn292102(v=exchg.10).md">jetbackupinstance (JET_INSTANCE, String, backupgrbit JET_PFNSTATUS)</a> -Funktion erstellt wurde. Dies ist die einfachste und gekapselte Restore-Funktion.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332995(v=exchg.10).md">Jetretrievecolbin (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, retrievecolumgengrbit, JET_RETINFO)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist. Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann jetretrievecolumschlag auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, sodass die Größe der Anwendungs Puffer entsprechend angepasst werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn332997(v=exchg.10).md">Jetretrievecolbin (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, retrievecolumgengrbit, JET_RETINFO)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist. Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann jetretrievecolumschlag auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, sodass die Größe der Anwendungs Puffer entsprechend angepasst werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334004(v=exchg.10).md">Jetretrievecolumschlag</a></td>
<td>Ruft in einem einzelnen Vorgang mehrere Spaltenwerte aus dem aktuellen Datensatz ab. Ein Array von JET_RETRIEVECOLUMN Strukturen wird verwendet, um den Satz von Spaltenwerten zu beschreiben, die abgerufen werden sollen, und um Ausgabepuffer für jeden abzurufenden Spaltenwert zu beschreiben.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334002(v=exchg.10).md">Jetretrievekey</a></td>
<td>Ruft den Schlüssel für den Index Eintrag an der aktuellen Position eines Cursors ab. Siehe auch <a href="dn334085(v=exchg.10).md">retrievekey (JET_SESID, JET_TABLEID, retrievekeygrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334001(v=exchg.10).md">Jetrollback</a></td>
<td>Macht die am Status der Datenbank vorgenommenen Änderungen rückgängig und kehrt zum letzten Sicherungspunkt zurück. Jetrollback schließt auch alle Cursor, die während des Speicher Punkts geöffnet werden. Wenn der äußerste Speicherpunkt rückgängig gemacht wird, beendet die Sitzung die Transaktion.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334003(v=exchg.10).md">JetSeek</a></td>
<td>Positioniert einen Cursor effizient auf einen Index Eintrag, der den Suchkriterien entspricht, die durch den Suchschlüssel in diesem Cursor und die angegebene Ungleichheit angegeben werden. Ein Suchschlüssel muss zuvor mithilfe von <a href="dn292216(v=exchg.10).md">jetmakekey (JET_SESID, JET_TABLEID, [], Int32, makekeygrbit)</a>erstellt worden sein. Siehe auch <a href="dn334145(v=exchg.10).md">tryseek (JET_SESID, JET_TABLEID, seekgrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334009(v=exchg.10).md">Jetsetcolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, setcolumngrbit, JET_SETINFO)</a></td>
<td>Die jetsetcolumn-Funktion ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, um eingefügt zu werden, oder um den aktuellen Datensatz zu aktualisieren. Es kann einen vorhandenen Wert überschreiben, einen neuen Wert zu einer Sequenz von Werten in einer mehrwertigen Spalte hinzufügen, einen Wert aus einer Sequenz von Werten in einer mehrwertigen Spalte entfernen oder den gesamten oder einen Teil eines Long-Werts aktualisieren (eine Spalte vom Typ <a href="hh577895(v=exchg.10).md">LONGTEXT</a> oder <a href="hh577895(v=exchg.10).md">LONGBINARY</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334008(v=exchg.10).md">Jetsetcolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, setcolumngrbit, JET_SETINFO)</a></td>
<td>Die jetsetcolumn-Funktion ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, um eingefügt zu werden, oder um den aktuellen Datensatz zu aktualisieren. Es kann einen vorhandenen Wert überschreiben, einen neuen Wert zu einer Sequenz von Werten in einer mehrwertigen Spalte hinzufügen, einen Wert aus einer Sequenz von Werten in einer mehrwertigen Spalte entfernen oder den gesamten oder einen Teil eines Long-Werts aktualisieren (eine Spalte vom Typ <a href="hh577895(v=exchg.10).md">LONGTEXT</a> oder <a href="hh577895(v=exchg.10).md">LONGBINARY</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334010(v=exchg.10).md">Jetsetcolumndefaultvalue</a></td>
<td>Ändert den Standardwert einer vorhandenen Spalte.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334006(v=exchg.10).md">Jetsetcolumns</a></td>
<td>Ermöglicht einer Anwendung das Festlegen mehrerer Spaltenwerte in einem einzelnen Vorgang. Ein Array von <a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a> Strukturen wird verwendet, um den Satz von Spaltenwerten zu beschreiben, die festgelegt werden sollen, und um Eingabepuffer für jeden festzulegenden Spaltenwert zu beschreiben.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334011(v=exchg.10).md">Jetsetcurrentindex</a></td>
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
<td><a href="dn334014(v=exchg.10).md">Jetsetdatabasesize</a></td>
<td>Legt die Größe einer nicht geöffneten Datenbankdatei fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334024(v=exchg.10).md">Jetsetindexrange</a></td>
<td>Schränkt temporär den Satz der Indexeinträge ein, die der Cursor mithilfe von <a href="dn292217(v=exchg.10).md">jetmove (JET_SESID, JET_TABLEID, Int32, movegrbit)</a> durchlaufen kann, beginnend mit dem aktuellen Index Eintrag und endet mit dem Index Eintrag, der mit den Suchkriterien übereinstimmt, die durch den Suchschlüssel in diesem Cursor und den angegebenen gebundenen Kriterien festgelegt wurden. Ein Suchschlüssel muss zuvor mithilfe von <a href="dn292216(v=exchg.10).md">jetmakekey (JET_SESID, JET_TABLEID, [], Int32, makekeygrbit)</a>erstellt worden sein. Siehe auch <a href="dn334099(v=exchg.10).md">trysetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334015(v=exchg.10).md">Jetsetls</a></td>
<td>Ermöglicht der Anwendung, ein Kontext Handle, das als lokaler Speicher bezeichnet wird, einem Cursor oder der diesem Cursor zugeordneten Tabelle zuzuordnen. Dieses Kontext Handle kann von der Anwendung verwendet werden, um zusätzliche Daten zu speichern, die einem Cursor oder einer Tabelle zugeordnet sind. Die Anwendung wird später mithilfe eines Lauf Zeit Rückrufs benachrichtigt, wenn das Kontext Handle freigegeben werden muss. Dadurch ist es möglich, einem Cursor oder einer Tabelle dynamisch zugeordneten Zustand zuzuordnen.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334027(v=exchg.10).md">Jetabessioncontext</a></td>
<td>Verknüpft eine Sitzung mit dem aktuellen Thread unter Verwendung des angegebenen Kontext Handles. Diese Zuordnung überschreibt die Standard-Engine-Anforderung, dass eine Transaktion für eine bestimmte Sitzung vollständig im gleichen Thread ausgeführt werden muss. Verwenden Sie <a href="dn332991(v=exchg.10).md">jetresessioncontext (JET_SESID)</a> , um die Zuordnung zu entfernen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334028(v=exchg.10).md">Jetsetsystemparameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, Zeichenfolge)</a></td>
<td>Legt Daten Bank Konfigurationsoptionen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334017(v=exchg.10).md">Jetsetsystemparameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String)</a></td>
<td>Legt Daten Bank Konfigurationsoptionen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334029(v=exchg.10).md">Jetsetsystemparameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)</a></td>
<td>Legt Daten Bank Konfigurationsoptionen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334018(v=exchg.10).md">Jetsettablesequential</a></td>
<td>Benachrichtigt die Datenbank-Engine, dass die Anwendung den gesamten Index scannt, auf dem sich der Cursor befindet. Folglich werden die Methoden, die für den Zugriff auf die Indexdaten verwendet werden, optimiert, um dieses Szenario so schnell wie möglich zu gestalten. Siehe auch <a href="dn332994(v=exchg.10).md">jetresettablesequential (JET_SESID, JET_TABLEID, resettablesequentialgrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334032(v=exchg.10).md">Jetstopbackupinstance</a></td>
<td>Verhindert, dass streamingsicherungsbezogene Aktivitäten auf einer bestimmten laufenden Instanz fortgesetzt werden, sodass die Streamingsicherung auf vorhersagbare Weise beendet wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334035(v=exchg.10).md">Jetstopserviczustance</a></td>
<td>Bereitet eine Instanz für die Beendigung vor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334020(v=exchg.10).md">Jetterm</a></td>
<td>Beenden Sie eine Instanz, die mit <a href="dn292210(v=exchg.10).md">jetinit (JET_INSTANCE)</a> oder <a href="dn292122(v=exchg.10).md">jetkreateinstance (JET_INSTANCE, String)</a>erstellt wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334037(v=exchg.10).md">JetTerm2</a></td>
<td>Beenden Sie eine Instanz, die mit <a href="dn292210(v=exchg.10).md">jetinit (JET_INSTANCE)</a> oder <a href="dn292122(v=exchg.10).md">jetkreateinstance (JET_INSTANCE, String)</a>erstellt wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334022(v=exchg.10).md">Jettruneureloginstance</a></td>
<td>Wird bei einer von jetbeginexternalbackup initiierten Sicherung verwendet, um Transaktionsprotokoll Dateien zu löschen, die nicht mehr benötigt werden, nachdem die aktuelle Sicherung erfolgreich abgeschlossen wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334019(v=exchg.10).md">Jetunregistercallback</a></td>
<td>Hiermit wird die Datenbank-Engine so konfiguriert, dass keine Benachrichtigungen mehr an die Anwendung gesendet werden, wie zuvor durch <a href="dn332989(v=exchg.10).md">jetregistercallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</a>angefordert wurden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334036(v=exchg.10).md">Jetupdate (JET_SESID JET_TABLEID)</a></td>
<td>Die jetupdate-Funktion führt einen Aktualisierungs Vorgang aus, einschließlich des Einfügens einer neuen Zeile in eine Tabelle oder der Aktualisierung einer vorhandenen Zeile. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von <a href="dn292131(v=exchg.10).md">jetdelete (JET_SESID JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334023(v=exchg.10).md">Jetupdate (JET_SESID, JET_TABLEID, [], Int32, Int32)</a></td>
<td>Die jetupdate-Funktion führt einen Aktualisierungs Vorgang aus, einschließlich des Einfügens einer neuen Zeile in eine Tabelle oder der Aktualisierung einer vorhandenen Zeile. Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von <a href="dn292131(v=exchg.10).md">jetdelete (JET_SESID JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334042(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, Boolean, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334026(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, Byte, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334044(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, [], makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334025(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, DateTime, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334046(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, Double, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334030(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, Guid, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334048(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, Int16, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334031(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, Int32, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334050(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, Int64, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334033(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, Single, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334052(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, UInt16, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334054(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, UInt32, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334034(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, UInt64, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334038(v=exchg.10).md">Makekey (JET_SESID, JET_TABLEID, String, Encoding, makekeygrbit)</a></td>
<td>Erstellt einen Suchschlüssel, der von <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, seekgrbit)</a> und <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>verwendet werden kann.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334058(v=exchg.10).md">"Muveafterlast"</a></td>
<td>Positionieren Sie den Cursor hinter dem letzten Datensatz in der Tabelle. Bei einer nachfolgenden Verschiebung wird der Cursor auf dem letzten Datensatz positioniert.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334057(v=exchg.10).md">"Muvebeforefirst"</a></td>
<td>Positionieren Sie den Cursor vor dem ersten Datensatz in der Tabelle. Bei einem nachfolgenden Verschiebungs Vorgang wird der Cursor auf dem ersten Datensatz positioniert.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334040(v=exchg.10).md">Resetindexrange</a></td>
<td>Entfernt einen Index Bereich, der mit <a href="dn334024(v=exchg.10).md">jetsetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a> oder <a href="dn334099(v=exchg.10).md">trysetindexrange (JET_SESID, JET_TABLEID, setindexrangegrbit)</a>erstellt wurde. Wenn kein Index Bereich vorhanden ist, führt diese Methode keine Aktion aus.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">Retrievecolumschlag (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">Retrievecolbin (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit, JET_RETINFO)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist. Zusätzlich zum Abrufen des tatsächlichen Spaltenwerts kann jetretrievecolumschlag auch verwendet werden, um die Größe einer Spalte abzurufen, bevor die Spaltendaten selbst abgerufen werden, sodass die Größe der Anwendungs Puffer entsprechend angepasst werden kann.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334045(v=exchg.10).md">Retrievecolaufnasboolean (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen booleschen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334078(v=exchg.10).md">Retrievecolbinasboolean (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen booleschen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334047(v=exchg.10).md">Retrievecolennasbyte (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen Byte Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334074(v=exchg.10).md">Retrievecolbinasbyte (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen Byte Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334077(v=exchg.10).md">Retrievecolaufnasdatetime (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen DateTime-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334051(v=exchg.10).md">Retrievecolbinasdatetime (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen DateTime-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334053(v=exchg.10).md">Retrievecolaufnasdouble (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen Double-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334084(v=exchg.10).md">Retrievecolbinasdouble (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen Double-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334056(v=exchg.10).md">Retrievecolaufnasfloat (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen float-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334092(v=exchg.10).md">Retrievecolbinasfloat (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen float-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334093(v=exchg.10).md">Retrievecolaufnasguid (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen GUID-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334061(v=exchg.10).md">Retrievecolbinasguid (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen GUID-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334062(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334098(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen Int16-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334100(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334068(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen Int32-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334066(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334091(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334067(v=exchg.10).md">Retrievecolennasstring (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen einzelnen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist. Die Unicode-Codierung wird verwendet.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334103(v=exchg.10).md">Retrievecolaufnasstring (JET_SESID, JET_TABLEID, JET_COLUMNID, Codierung)</a></td>
<td>Ruft einen Zeichen folgen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334070(v=exchg.10).md">Retrievecolbinasstring (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, retrievecolenngrbit)</a></td>
<td>Ruft einen Zeichen folgen Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334069(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen UInt16-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334106(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen UInt16-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334108(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen UInt32-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334073(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen UInt32-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334072(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft einen UInt64-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334113(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, retrievecolenngrbit)</a></td>
<td>Ruft einen UInt64-Spaltenwert aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334075(v=exchg.10).md">Abruf Ereignisse</a></td>
<td>Ruft Spalten in ColumnValue-Objekte ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334076(v=exchg.10).md">Retrievecolennsize (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Ruft die Größe eines einzelnen Spaltenwerts aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334117(v=exchg.10).md">Retrievecolbinsize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, retrievecolenngrbit)</a></td>
<td>Ruft die Größe eines einzelnen Spaltenwerts aus dem aktuellen Datensatz ab. Der Datensatz ist der Datensatz, der mit dem Index Eintrag an der aktuellen Position des Cursors verknüpft ist. Alternativ kann diese Funktion eine Spalte aus einem Datensatz abrufen, der im Cursor Kopier Puffer erstellt wird. Diese Funktion kann auch Spaltendaten aus einem Index Eintrag abrufen, der auf den aktuellen Datensatz verweist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334085(v=exchg.10).md">Abruf Schlüssel</a></td>
<td>Ruft den Schlüssel für den Index Eintrag an der aktuellen Position eines Cursors ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334120(v=exchg.10).md">Serializeobjecttocolumn</a></td>
<td>Schreibt eine serialisierte Form eines Objekts in eine Spalte.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334123(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Boolean)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334080(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334121(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [])</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334082(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334125(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Double)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334081(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Guid)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334127(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334083(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334130(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334087(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334132(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334086(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334135(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334089(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], setcolumngrbit)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334136(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Zeichenfolge, Codierung)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334090(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding, setcolumngrbit)</a></td>
<td>Ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, der eingefügt werden soll, oder, um den aktuellen Datensatz zu aktualisieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334138(v=exchg.10).md">SetColumns</a></td>
<td>Legt Spalten aus ColumnValue-Objekten fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334139(v=exchg.10).md">Trygetlock</a></td>
<td>Reservieren Sie explizit die Möglichkeit, eine Zeile zu aktualisieren, eine Sperre zu schreiben oder explizit zu verhindern, dass eine Zeile von einer anderen Sitzung aktualisiert wird, und lesen Sie sperren. Normalerweise werden Zeilen Schreib Sperren implizit durch das Aktualisieren von Zeilen abgerufen. Lese Sperren sind in der Regel aufgrund von Daten Satz Versionsverwaltung nicht erforderlich. In einigen Fällen möchte eine Transaktion jedoch möglicherweise eine Zeile explizit sperren, um die Serialisierung zu erzwingen, oder um sicherzustellen, dass ein nachfolgender Vorgang erfolgreich ausgeführt wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334094(v=exchg.10).md">Trymove</a></td>
<td>Versuchen Sie, durch einen Index zu navigieren. Wenn die Navigation erfolgreich ist, gibt diese Methode true zurück. Wenn kein Datensatz vorhanden ist, um zu dieser Methode zu navigieren, wird false zurückgegeben. für andere Fehler wird eine Ausnahme ausgelöst.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334150(v=exchg.10).md">Trymuvefirst</a></td>
<td>Versuchen Sie, zum ersten Datensatz in der Tabelle zu wechseln. Wenn die Tabelle leer ist, wird false zurückgegeben. Wenn ein anderer Fehler auftritt, wird eine Ausnahme ausgelöst.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334140(v=exchg.10).md">Trymuvelast</a></td>
<td>Versuchen Sie, zum letzten Datensatz in der Tabelle zu wechseln. Wenn die Tabelle leer ist, wird false zurückgegeben. Wenn ein anderer Fehler auftritt, wird eine Ausnahme ausgelöst.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334095(v=exchg.10).md">Trymuvenext</a></td>
<td>Versuchen Sie, zum nächsten Datensatz in der Tabelle zu wechseln. Wenn kein Nächster Datensatz vorhanden ist, wird false zurückgegeben. Wenn ein anderer Fehler auftritt, wird eine Ausnahme ausgelöst.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334144(v=exchg.10).md">Trymuveprevious</a></td>
<td>Versuchen Sie, zum vorherigen Datensatz in der Tabelle zu wechseln. Wenn kein vorheriger Datensatz vorhanden ist, wird false zurückgegeben. Wenn ein anderer Fehler auftritt, wird eine Ausnahme ausgelöst.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334096(v=exchg.10).md">Tryopentable</a></td>
<td>Versuchen Sie, eine Tabelle zu öffnen.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334145(v=exchg.10).md">Tryseek</a></td>
<td>Positioniert einen Cursor effizient auf einen Index Eintrag, der den Suchkriterien entspricht, die durch den Suchschlüssel in diesem Cursor und die angegebene Ungleichheit angegeben werden. Ein Suchschlüssel muss zuvor mithilfe von jetmakekey erstellt worden sein.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn334099(v=exchg.10).md">Trysetindexrange</a></td>
<td>Schränkt die Menge der Indexeinträge, die der Cursor durchlaufen kann, mithilfe von jetmove zu denjenigen ein, die mit dem aktuellen Index Eintrag beginnen und mit dem Index Eintrag enden, der mit den Suchkriterien übereinstimmt, die durch den Suchschlüssel in diesem Cursor und den angegebenen gebundenen Kriterien festgelegt wurden. Ein Suchschlüssel muss zuvor mithilfe von jetmakekey erstellt worden sein. Gibt "true" zurück, wenn der Index Bereich nicht leer ist, andernfalls "false".</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

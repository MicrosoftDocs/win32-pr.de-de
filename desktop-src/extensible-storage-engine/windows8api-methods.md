---
description: 'Weitere Informationen zu: Windows8Api-Methoden'
title: Windows8Api-Methoden (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: Windows8Api methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api_methods(v=EXCHG.10)
ms:contentKeyID: 55104457
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: bdfcbee5e4673068bf98126523dfdd582bedbc3bd82c49efbe8140df68e27e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470870"
---
# <a name="windows8api-methods"></a>Windows8Api-Methoden

Geschützte Member enthalten  
Geerbte Member enthalten  

Der [Windows8Api-Typ](./windows8api-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></td>
<td>Bewirkt, dass eine Sitzung eine Transaktion ein- oder einen neuen Speicherpunkt in einer vorhandenen Transaktion erstellt.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></td>
<td>Commit für die Änderungen, die während des aktuellen Speicherpunkts am Zustand der Datenbank vorgenommen wurden, und migriert sie zum vorherigen Speicherpunkt. Wenn für den äußersten Speicherpunkt ein Committed ausgeführt wird, wird für die während dieses Speicherpunkts vorgenommenen Änderungen ein Committed in den Zustand der Datenbank ausgeführt, und die Sitzung beendet die Transaktion.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></td>
<td>Erstellt Indizes für Daten in einer ESE-Datenbank.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></td>
<td>Erstellt eine Tabelle, fügt Spalten und Indizes für diese Tabelle hinzu. <a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></td>
<td>Ruft erweiterte Informationen zu einem Fehler ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></td>
<td>Erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert und ruft Datensätze genau wie eine normale Tabelle ab, die mit JetCreateTableColumnIndex erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um sehr schnell zu sortieren und doppelte Entfernungen für Datensatzgruppen durchzuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird. Siehe auch <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, []),</a> &quot; Api.JetOpenTempTable2 &quot; , <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></td>
<td>Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffercache befinden, starten Sie asynchrone Leseläufe, um die Datensätze in den Datenbankpuffercache zu übertragen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></td>
<td>Ändern der Größe einer derzeit geöffneten Datenbank.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></td>
<td>Legen Sie ein Array einfacher Filter für <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit) fest.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></td>
<td>Legt einen Parameter für den bereitgestellten Sitzungszustand fest, der für die Lebensdauer dieser Sitzung oder bis zum Zurücksetzen verwendet wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></td>
<td>Bereitet eine -Instanz für die Beendigung vor. Kann auch verwendet werden, um einen vorherigen Ruhepunkt wieder aufzunehmen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></td>
<td>Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffercache befinden, starten Sie asynchrone Leseläufe, um die Datensätze in den Datenbankpuffercache zu übertragen.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></td>
<td>Wenn sich die Datensätze mit den angegebenen Schlüsselbereichen nicht im Puffercache befinden, starten Sie asynchrone Leseläufe, um die Datensätze in den Datenbankpuffercache zu übertragen.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Windows8Api-Klasse](./windows8api-class.md)

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)

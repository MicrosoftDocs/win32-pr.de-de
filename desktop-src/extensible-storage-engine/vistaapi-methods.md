---
description: 'Weitere Informationen zu: vistaapi-Methoden'
title: Vistaapi-Methoden (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: VistaApi methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Vista.VistaApi
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi_methods(v=EXCHG.10)
ms:contentKeyID: 55104186
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4de9098426f0457485377f2274c17f34ea775f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215225"
---
# <a name="vistaapi-methods"></a>Vistaapi-Methoden

Geschützte Member einschließen  
Geerbte Member einschließen  

Der [vistaapi](./vistaapi-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn335319(v=exchg.10).md">Jetgetcolumninfo</a></td>
<td>Ruft Informationen zu einer Spalte in einer Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351258(v=exchg.10).md">Jetgetinstancefehlinfo</a></td>
<td>Ruft Informationen zu einer-Instanz ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335320(v=exchg.10).md">Jetgetrecordsize</a></td>
<td>Ruft Informationen zur Daten Satz Größe vom gewünschten Speicherort ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351264(v=exchg.10).md">Jetgetthreadstats</a></td>
<td>Ruft Leistungsinformationen aus der Datenbank-Engine für den aktuellen Thread ab. Mehrere Aufrufe können verwendet werden, um Statistiken zu sammeln, die die Aktivität der Datenbank-Engine in diesem Thread zwischen diesen Aufrufen widerspiegeln.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351265(v=exchg.10).md">JetInit3</a></td>
<td>Initialisieren Sie die ESENT-Datenbank-Engine.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335326(v=exchg.10).md">Jetopumtemporarytable</a></td>
<td>Erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird. Siehe auch <a href="dn292231(v=exchg.10).md">jetopentemptable (JET_SESID, [], Int32, temptablegrbit, JET_TABLEID, [])</a>, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, temptablegrbit, JET_TABLEID, [])</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351267(v=exchg.10).md">Jeto ssnapshotend</a></td>
<td>Benachrichtigt die Engine, dass die Momentaufnahme Sitzung abgeschlossen wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351269(v=exchg.10).md">Jejessnapshotgetfrezeinfo</a></td>
<td>Ruft die Liste der-Instanzen und-Datenbanken ab, die zu einem beliebigen Zeitpunkt Teil der Momentaufnahme Sitzung sind.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335341(v=exchg.10).md">Jejessnapshotprepareingestance</a></td>
<td>Wählt eine bestimmte-Instanz aus, die Teil der Momentaufnahme Sitzung sein soll.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn335343(v=exchg.10).md">Jeto ssnapshottruneurelog</a></td>
<td>Ermöglicht das Abschneiden von Protokollen für alle Instanzen, die Teil der Momentaufnahme Sitzung sind.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351271(v=exchg.10).md">Jeto ssnapshottruneureloginstance</a></td>
<td>Verkürzt das Protokoll für eine angegebene-Instanz während einer Momentaufnahme Sitzung.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Vistaapi-Klasse](./vistaapi-class.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)

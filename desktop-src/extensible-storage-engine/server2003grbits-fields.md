---
description: 'Weitere Informationen finden Sie hier: Server2003Grbits Fields'
title: Server2003Grbits-Felder (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ed7a99118674d955fc6a882ac08407e45837af77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571005"
---
# <a name="server2003grbits-fields"></a>Server2003Grbits-Felder

Geschützte Member einschließen  
Geerbte Member einschließen  

Der [Server2003Grbits](./server2003grbits-class.md) -Typ macht die folgenden Member verfügbar.

## <a name="fields"></a>Felder

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
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351203(v=exchg.10).md">Enumerateignoreuserdefineddefault</a></td>
<td>Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist und über einen benutzerdefinierten Standardwert verfügt, wird kein Spaltenwert zurückgegeben. Mit dieser Option wird verhindert, dass der Rückruf, der den benutzerdefinierten Standardwert für die Spalte berechnet, beim Auflisten der Werte für diese Spalte aufgerufen wird.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351284(v=exchg.10).md">Nur Weiterleitung</a></td>
<td>Mit dieser Option wird angefordert, dass die temporäre Tabelle nur erstellt wird, wenn der temporäre Tabellen-Manager die für zwischen Abfrageergebnisse optimierte-Implementierung verwenden kann. Wenn ein beliebiges Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl. Ein Nebeneffekt dieser Option besteht darin, zuzulassen, dass die temporäre Tabelle Datensätze mit doppelten Index Schlüsseln enthält. Weitere Informationen finden Sie unter <a href="hh558517(v=exchg.10).md">Unique</a> .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></td>
<td>Alle Transaktionen, für die zuvor von einer Sitzung ein Commit ausgeführt wurde und die noch nicht in die Transaktionsprotokoll Datei geleert wurden, werden sofort geleert. Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden. Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet. Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Server2003Grbits-Klasse](./server2003grbits-class.md)

[Microsoft. ISAM. ESENT. Interop. Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)

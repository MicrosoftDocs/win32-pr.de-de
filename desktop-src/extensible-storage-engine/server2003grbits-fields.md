---
description: 'Weitere Informationen zu: Server2003Grbits-Felder'
title: Server2003Grbits-Felder (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 77db94da9f3a5dbec982b31c0ea3d673ffb6228a58f81adf644ff498a2cf4f84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071672"
---
# <a name="server2003grbits-fields"></a>Server2003Grbits-Felder

Einschließen geschützter Member  
Einschließen geerbter Member  

Der [Server2003Grbits-Typ](./server2003grbits-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></td>
<td>Wenn eine bestimmte Spalte nicht im Datensatz vorhanden ist und über einen benutzerdefinierten Standardwert verfügt, wird kein Spaltenwert zurückgegeben. Diese Option verhindert, dass der Rückruf, der den benutzerdefinierten Standardwert für die Spalte berechnet, beim Auflisten der Werte für diese Spalte aufgerufen wird.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351284(v=exchg.10).md">ForwardOnly</a></td>
<td>Diese Option fordert an, dass die temporäre Tabelle nur erstellt wird, wenn der temporäre Tabellen-Manager die für Zwischenabfrageergebnisse optimierte Implementierung verwenden kann. Wenn ein Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl. Ein Nebeneffekt dieser Option besteht darin, dass die temporäre Tabelle Datensätze mit doppelten Indexschlüsseln enthalten kann. Weitere Informationen finden Sie unter <a href="hh558517(v=exchg.10).md">Eindeutig.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Öffentliches Feld" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></td>
<td>Alle Transaktionen, für die zuvor von einer Sitzung ein Commit ausgeführt wurde, die noch nicht in die Transaktionsprotokolldatei geleert wurden, werden sofort geleert. Diese API wartet, bis die Transaktionen geleert wurden, bevor sie an den Aufrufer zurückgegeben wird. Diese Option kann auch dann verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet. Diese Option kann nicht in Kombination mit einer anderen Option verwendet werden.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Server2003Grbits-Klasse](./server2003grbits-class.md)

[Microsoft.Isam.Esent.Interop.Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)

---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMNID-Eigenschaften'
title: Eigenschaften von JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525028"
---
# <a name="jet_enumcolumnid-properties"></a>Eigenschaften von JET_ENUMCOLUMNID

Geschützte Member einschließen  
Geerbte Member einschließen  

Der [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) -Typ macht die folgenden Member verfügbar.

## <a name="properties"></a>Eigenschaften

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
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335141(v=exchg.10).md">ColumnID</a></td>
<td>Ruft die aufzuzählenden Spalten-ID ab oder legt Sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335092(v=exchg.10).md">ctagsequence</a></td>
<td>Ruft die Anzahl der Spaltenwerte (durch einen einbasierten Index) ab, die für die angegebene Spalten-ID aufgelistet werden sollen, oder legt Sie fest. Wenn ctagsequence gleich 0 (null) ist, wird rgtagsequence ignoriert, und alle Spaltenwerte für die angegebene Spalten-ID werden aufgelistet.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335093(v=exchg.10).md">rgtagsequence</a></td>
<td>Ruft das Array von einbasierten Indizes in das Array von Spaltenwerten für eine angegebene Spalte ab oder legt dieses fest. Bei einem einzelnen Element handelt es sich um eine in JET_RETRIEVECOLUMN definierte itagsequence. Eine itagsequence-Wert von 0 (null) bedeutet &quot; Skip &quot; . Eine itagsequence von 1 bedeutet, dass der erste Spaltenwert der Spalte zurückgegeben wird, der Wert 2 für den zweiten Wert usw.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_ENUMCOLUMNID-Klasse](./jet-enumcolumnid-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMN-Eigenschaften'
title: Eigenschaften von JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103495
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 69d0822e12078a7990615ebd401fb63e474a389e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862532"
---
# <a name="jet_enumcolumn-properties"></a>Eigenschaften von JET_ENUMCOLUMN

Geschützte Member einschließen  
Geerbte Member einschließen  

Der [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn335137(v=exchg.10).md">cbData</a></td>
<td>Ruft die Größe des Werts ab, der für die Spalte aufgelistet wurde. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> gleich <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">cenenumcolumnvalue</a></td>
<td>Ruft die Anzahl der für die Spalte aufgelisteten Spaltenwerte ab. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> nicht <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">ColumnID</a></td>
<td>Ruft die aufgelistete ColumnID-ID ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">irre</a></td>
<td>Ruft den Spalten Statuscode ab, der sich aus der-Enumeration ergibt.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">pvData</a></td>
<td>Ruft den Wert ab, der für die Spalte aufgelistet wurde. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> gleich <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist. Dies verweist auf den Arbeitsspeicher, der mit dem an <a href="dn292148(v=exchg.10).md">jetenumeratecolumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, enumeratecolumnsgrbit)</a>weiter gegebenen Rückruf für den <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> Zuweisung zugeordnet wird. Vergessen Sie nicht, den Arbeitsspeicher zu veröffentlichen</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">rgenenumcolumnvalue</a></td>
<td>Ruft die enumerationsspaltenwerte für die Spalte ab. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> nicht <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_ENUMCOLUMN-Klasse](./jet-enumcolumn-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

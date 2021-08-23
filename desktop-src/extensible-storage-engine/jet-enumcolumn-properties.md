---
description: 'Weitere Informationen zu: JET_ENUMCOLUMN-Eigenschaften'
title: JET_ENUMCOLUMN-Eigenschaften
TOCTitle: JET_ENUMCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103495
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ee11c050d558fbefb15be4783a08b1808744718d043de038b297fdc5ebd9e3fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667920"
---
# <a name="jet_enumcolumn-properties"></a>JET_ENUMCOLUMN-Eigenschaften

Einschließen geschützter Member  
Einschließen geerbter Member  

Der [JET_ENUMCOLUMN-Typ](./jet-enumcolumn-class.md) macht die folgenden Member verfügbar.

## <a name="properties"></a>Eigenschaften

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
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335137(v=exchg.10).md">cbData</a></td>
<td>Ruft die Größe des Werts ab, der für die Spalte aufzählt wurde. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">err</a> gleich <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></td>
<td>Ruft die Anzahl der Spaltenwerte ab, die für die Spalte aufgezählt werden. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">err</a> nicht <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">Columnid</a></td>
<td>Ruft die columnid-ID ab, die aufzählt wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">Err</a></td>
<td>Ruft den Spaltenstatuscode ab, der aus der -Enumeration resultiert.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">pvData</a></td>
<td>Ruft den Wert ab, der für die Spalte aufzählt wurde. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">err</a> gleich <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>ist. Dies verweist auf <a href="hh566077(v=exchg.10).md"></a> den Arbeitsspeicher, der mit dem JET_PFNREALLOC-Zuweisungsrückruf an <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>belegt wird. Denken Sie daran, den Arbeitsspeicher freizugeben, wenn Sie fertig sind.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></td>
<td>Ruft die Aufzählungsspaltenwerte für die Spalte ab. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">err</a> nicht <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>ist.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_ENUMCOLUMN-Klasse](./jet-enumcolumn-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

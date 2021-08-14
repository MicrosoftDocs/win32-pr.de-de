---
description: Weitere Informationen finden Sie unter BoolColumnValue-Eigenschaften.
title: BoolColumnValue-Eigenschaften
TOCTitle: BoolColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.BoolColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.boolcolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55100954
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d338418b8855b8ba45e38b42f192cb7b1352f345f48e301eb78b1d0dc75534a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117902271"
---
# <a name="boolcolumnvalue-properties"></a>BoolColumnValue-Eigenschaften

Geschützte Member enthalten  
Geerbte Member enthalten  

Der [BoolColumnValue-Typ](./boolcolumnvalue-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn334166(v=exchg.10).md">Columnid</a></td>
<td>Ruft die columnid ab, die festgelegt oder abgerufen werden soll, oder legt sie fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Fehler</a></td>
<td>Ruft die Warnung ab, die durch Abrufen oder Festlegen dieser Spalte generiert wird. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Ruft die Spalten itag-Sequenz ab oder legt sie fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334225(v=exchg.10).md">Länge</a></td>
<td>Ruft die Bytelänge eines Spaltenwerts ab, der 0 (null) ist, wenn die Spalte NULL ist. Andernfalls entspricht sie der Größe für diese Spalte mit fester Größe. (Geerbt von <a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; &gt; T</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Ruft Spaltenabrufoptionen ab oder legt sie fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Ruft Spaltenaktualisierungsoptionen ab oder legt sie fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Geschützte Eigenschaft" alt="Protected property" /></td>
<td><a href="dn334107(v=exchg.10).md">Größe</a></td>
<td>Ruft die Größe des Werts in der Spalte ab. Dies gibt 0 für Spalten variabler Größe (d. h. binär und Zeichenfolge) zurück. (Überschreibt <a href="dn334172(v=exchg.10).md">ColumnValue.Size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334180(v=exchg.10).md">Wert</a></td>
<td>Ruft den Wert in der Struktur ab oder legt den Wert fest. (Geerbt von <a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; &gt; T</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334157(v=exchg.10).md">ValueAsObject</a></td>
<td>Ruft den letzten festgelegten oder abgerufenen Wert der Spalte ab. Der Wert wird als generisches Objekt zurückgegeben. (Überschreibt <a href="dn334226(v=exchg.10).md">ColumnValueOfStruct &lt; T &gt; . ValueAsObject</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[BoolColumnValue-Klasse](./boolcolumnvalue-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

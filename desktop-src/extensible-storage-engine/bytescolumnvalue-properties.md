---
description: Weitere Informationen finden Sie unter BytesColumnValue-Eigenschaften.
title: BytesColumnValue-Eigenschaften
TOCTitle: BytesColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.BytesColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55100964
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7973f35a59af3cda2e8bb3bd400d2ef10e43e4f18fe9431f61ed50b62b343f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117902106"
---
# <a name="bytescolumnvalue-properties"></a>BytesColumnValue-Eigenschaften

Geschützte Member enthalten  
Geerbte Member enthalten  

Der [BytesColumnValue-Typ](./bytescolumnvalue-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn334126(v=exchg.10).md">Länge</a></td>
<td>Ruft die Bytelänge eines Spaltenwerts ab, der null ist, wenn die Spalte NULL ist, andernfalls entspricht sie der tatsächlichen Länge des Bytearrays. (Überschreibt <a href="dn334213(v=exchg.10).md">ColumnValue.Length</a>.)</td>
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
<td><a href="dn334176(v=exchg.10).md">Größe</a></td>
<td>Ruft die Größe des Werts in der Spalte ab. Dies gibt 0 für Spalten variabler Größe (d. h. binär und Zeichenfolge) zurück. (Überschreibt <a href="dn334172(v=exchg.10).md">ColumnValue.Size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334129(v=exchg.10).md">Wert</a></td>
<td>Ruft den Wert der Spalte ab oder legt den Wert fest. Verwenden <a href="dn334138(v=exchg.10).md">Sie SetColumns(JET_SESID, JET_TABLEID, []),</a> um einen Datensatz mit dem Spaltenwert zu aktualisieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334177(v=exchg.10).md">ValueAsObject</a></td>
<td>Ruft den letzten festgelegten oder abgerufenen Wert der Spalte ab. Der Wert wird als generisches Objekt zurückgegeben. (Überschreibt <a href="dn334214(v=exchg.10).md">ColumnValue.ValueAsObject</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[BytesColumnValue-Klasse](./bytescolumnvalue-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

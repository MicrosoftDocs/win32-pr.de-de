---
description: 'Weitere Informationen: bytescolumnvalue-Eigenschaften'
title: Bytescolumnvalue-Eigenschaften
TOCTitle: BytesColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.BytesColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55100964
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: bafae34a3fa6dac29cc504ebe9a34c0abd7b870a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350079"
---
# <a name="bytescolumnvalue-properties"></a>Bytescolumnvalue-Eigenschaften

Geschützte Member einschließen  
Geerbte Member einschließen  

Der [bytescolumnvalue](./bytescolumnvalue-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn334166(v=exchg.10).md">ColumnID</a></td>
<td>Ruft das festzulegende oder abzurufende ColumnID ab oder legt es fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Fehler</a></td>
<td>Ruft die Warnung ab, die durch Abrufen oder Festlegen dieser Spalte generiert wird. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">Itagsequence</a></td>
<td>Ruft die ITAG-Spalte der Spalte ab oder legt Sie fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334126(v=exchg.10).md">Länge</a></td>
<td>Ruft die Byte Länge eines Spaltenwerts ab, der 0 (null) ist, wenn die Spalte NULL ist, andernfalls entspricht der tatsächlichen Länge des Byte Arrays. (Überschreibt <a href="dn334213(v=exchg.10).md">ColumnValue. length</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">Retrievegrbit</a></td>
<td>Ruft die Spalten Abruf Optionen ab oder legt Sie fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">Setgrbit</a></td>
<td>Ruft Spalten Aktualisierungs Optionen ab oder legt Sie fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Geschützte Eigenschaft" alt="Protected property" /></td>
<td><a href="dn334176(v=exchg.10).md">Größe</a></td>
<td>Ruft die Größe des Werts in der Spalte ab. Dadurch wird 0 für Spalten variabler Größen (z. b. Binär und Zeichenfolge) zurückgegeben. (Überschreibt <a href="dn334172(v=exchg.10).md">ColumnValue. Size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334129(v=exchg.10).md">Wert</a></td>
<td>Ruft den Wert der Spalte ab oder legt ihn fest. Verwenden Sie <a href="dn334138(v=exchg.10).md">SetColumns (JET_SESID, JET_TABLEID, [])</a> , um einen Datensatz mit dem Spaltenwert zu aktualisieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334177(v=exchg.10).md">Valueasobject</a></td>
<td>Ruft den letzten Satz oder abgerufenen Wert der Spalte ab. Der Wert wird als generisches-Objekt zurückgegeben. (Überschreibt <a href="dn334214(v=exchg.10).md">ColumnValue. valueasobject</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Bytescolumnvalue-Klasse](./bytescolumnvalue-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

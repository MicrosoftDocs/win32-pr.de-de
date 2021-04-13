---
description: 'Weitere Informationen finden Sie hier: JET_SETCOLUMN-Eigenschaften'
title: Eigenschaften von JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103854
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 43f005ce4edb909e842566e43b9b74ed80471c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484483"
---
# <a name="jet_setcolumn-properties"></a>Eigenschaften von JET_SETCOLUMN

Geschützte Member einschließen  
Geerbte Member einschließen  

Der [JET_SETCOLUMN](./jet-setcolumn-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn335266(v=exchg.10).md">cbData</a></td>
<td>Ruft die Größe der festzulegenden Daten ab oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335268(v=exchg.10).md">ColumnID</a></td>
<td>Ruft den Spalten Bezeichner für eine festzulegende Spalte ab oder legt ihn fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335269(v=exchg.10).md">irre</a></td>
<td>Ruft den vom Vorgang zum Festlegen der Spalte zurückgegebenen Fehlercode oder die Warnung ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335270(v=exchg.10).md">grbit</a></td>
<td>Ruft Optionen für den Vorgang zum Festlegen einer Spalte ab oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335271(v=exchg.10).md">ibdata</a></td>
<td>Ruft den Offset der festzulegenden Daten ab oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335272(v=exchg.10).md">iblongvalue</a></td>
<td>Ruft den Offset bis zum ersten Byte ab, das in einer Spalte vom Typ <a href="hh577895(v=exchg.10).md">LONGBINARY</a> oder <a href="hh577895(v=exchg.10).md">LONGTEXT</a>festgelegt werden soll, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335273(v=exchg.10).md">itagsequence</a></td>
<td>Ruft die Sequenznummer des Werts in einer mehrwertigen Spalte ab, die festgelegt werden soll, oder legt Sie fest. Das Array von Werten ist 1-basiert. Der erste Wert ist Sequenz 1, nicht 0 (null). Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als itagsequence übergeben werden, wenn dieser Wert ersetzt wird. Der Wert 0 (null) bedeutet, dass am Ende der Sequenz der Spaltenwerte eine neue Spaltenwert Instanz hinzugefügt wird.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351058(v=exchg.10).md">pvData</a></td>
<td>Ruft einen Zeiger auf die festzulegenden Daten ab oder legt diesen fest.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_SETCOLUMN-Klasse](./jet-setcolumn-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Weitere Informationen finden Sie hier: JET_RETINFO-Eigenschaften'
title: Eigenschaften von JET_RETINFO
TOCTitle: JET_RETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103867
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4724651b0184bae0b4acca049a8a16653282ce85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564798"
---
# <a name="jet_retinfo-properties"></a>Eigenschaften von JET_RETINFO

Geschützte Member einschließen  
Geerbte Member einschließen  

Der [JET_RETINFO](./jet-retinfo-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn335221(v=exchg.10).md">columnidnexttaging</a></td>
<td>Ruft das ColumnID der abgerufenen Spalte mit mehreren Werten oder geringer Dichte ab, wenn alle markierten Spalten abgerufen werden, indem 0 als ColumnID an jetretrievecolbin übergeben wird.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335220(v=exchg.10).md">iblongvalue</a></td>
<td>Ruft den Offset auf das erste Byte ab, das aus einer Spalte vom Typ <a href="hh577895(v=exchg.10).md">LONGBINARY</a>oder <a href="hh577895(v=exchg.10).md">LONGTEXT</a>abgerufen werden soll, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351035(v=exchg.10).md">itagsequence</a></td>
<td>Ruft die Sequenznummer des Werts in einer mehrwertigen Spalte ab oder legt Sie fest. Das Array von Werten ist 1-basiert. Der erste Wert ist Sequenz 1, nicht 0. Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als itagsequence übergeben werden.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_RETINFO-Klasse](./jet-retinfo-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Weitere Informationen finden Sie hier: JET_SETINFO-Eigenschaften'
title: Eigenschaften von JET_SETINFO
TOCTitle: JET_SETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103917
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af54ddfc09cce0a9c9498dea2060fb83baa0d6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128648"
---
# <a name="jet_setinfo-properties"></a>Eigenschaften von JET_SETINFO

Geschützte Member einschließen  
Geerbte Member einschließen  

Der [JET_SETINFO](./jet-setinfo-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn351064(v=exchg.10).md">iblongvalue</a></td>
<td>Ruft den Offset bis zum ersten Byte ab, das in einer Spalte vom Typ <a href="hh577895(v=exchg.10).md">LONGBINARY</a> oder <a href="hh577895(v=exchg.10).md">LONGTEXT</a>festgelegt werden soll, oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351037(v=exchg.10).md">itagsequence</a></td>
<td>Ruft die Sequenznummer des Werts in einer mehrwertigen Spalte ab, die festgelegt werden soll, oder legt Sie fest. Das Array von Werten ist 1-basiert. Der erste Wert ist Sequenz 1, nicht 0 (null). Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als itagsequence übergeben werden, wenn dieser Wert ersetzt wird. Der Wert 0 (null) bedeutet, dass am Ende der Sequenz der Spaltenwerte eine neue Spaltenwert Instanz hinzugefügt wird.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_SETINFO-Klasse](./jet-setinfo-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

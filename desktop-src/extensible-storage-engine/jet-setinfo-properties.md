---
description: Weitere Informationen finden Sie unter JET_SETINFO Eigenschaften.
title: JET_SETINFO Eigenschaften
TOCTitle: JET_SETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103917
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 80dea8d2055464441dbaeb5b228c91c2fa4780f74fa2ec4cfe89d2ab33585e5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093290"
---
# <a name="jet_setinfo-properties"></a>JET_SETINFO Eigenschaften

Geschützte Member enthalten  
Geerbte Member enthalten  

Der [JET_SETINFO](./jet-setinfo-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn351064(v=exchg.10).md">ibLongValue</a></td>
<td>Ruft den Offset auf das erste Byte ab, das in einer Spalte vom Typ <a href="hh577895(v=exchg.10).md">LongBinary</a> oder LongText festgelegt werden soll, oder <a href="hh577895(v=exchg.10).md">legt diesen fest.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351037(v=exchg.10).md">itagSequence</a></td>
<td>Ruft die Sequenznummer des Werts in einer mehrwertigen Spalte ab, die festgelegt werden soll, oder legt diese fest. Das Array von Werten ist 1-basiert. Der erste Wert ist Sequenz 1, nicht 0 (null). Wenn die Datensatzspalte nur einen Wert hat, sollte 1 als itagSequence übergeben werden, wenn dieser Wert ersetzt wird. Der Wert 0 (null) bedeutet, dass am Ende der Sequenz von Spaltenwerten eine neue Spaltenwertinstanz hinzugefügt wird.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_SETINFO-Klasse](./jet-setinfo-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

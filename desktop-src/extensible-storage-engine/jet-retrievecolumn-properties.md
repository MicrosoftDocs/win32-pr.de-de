---
description: 'Weitere Informationen zu: JET_RETRIEVECOLUMN-Eigenschaften'
title: JET_RETRIEVECOLUMN Eigenschaften
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c1e902b7e79111f3e9d9bf0160880d95c3957804de981fd56bbc36db5a9c3fc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107344"
---
# <a name="jet_retrievecolumn-properties"></a>JET_RETRIEVECOLUMN Eigenschaften

Einschließen geschützter Member  
Einschließen geerbter Member  

Der [JET_RETRIEVECOLUMN-Typ](./jet-retrievecolumn-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn335226(v=exchg.10).md">cbActual</a></td>
<td>Ruft die Größe von Daten in Bytes ab, die von einem Vorgang zum Abrufen von Spalten abgerufen werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335228(v=exchg.10).md">cbData</a></td>
<td>Ruft die Größe des <a href="dn351040(v=exchg.10).md">pvData-Puffers</a> in Bytes ab oder legt diese fest. Der Vorgang zum Abrufen von Spalten speichert nicht mehr Daten in pvData als cbData.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335230(v=exchg.10).md">Columnid</a></td>
<td>Ruft den Spaltenbezeichner für die abzurufende Spalte ab oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></td>
<td>Ruft die columnid der markierten, mehrwertigen oder Sparsespalte ab, wenn alle markierten Spalten abgerufen werden, indem 0 als columnid übergeben wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335231(v=exchg.10).md">Err</a></td>
<td>Ruft die Warnung ab, die beim Abrufen der Spalte zurückgegeben wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335232(v=exchg.10).md">grbit</a></td>
<td>Ruft die Optionen für den Spaltenabruf ab oder legt sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335233(v=exchg.10).md">ibData</a></td>
<td>Ruft den Offset im Puffer ab, in dem die Daten gespeichert werden, oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335234(v=exchg.10).md">ibLongValue</a></td>
<td>Ruft den Offset auf das erste Byte ab, das aus einer Spalte vom Typ <a href="hh577895(v=exchg.10).md">LongBinary</a> oder <a href="hh577895(v=exchg.10).md">LongText</a>abgerufen werden soll, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351039(v=exchg.10).md">itagSequence</a></td>
<td>Ruft die Sequenznummer der Werte ab, die in einer mehrwertigen Spalte enthalten sind, oder legt diese fest. Wenn itagSequence 0 ist, wird die Anzahl der Instanzen einer mehrwertigen Spalte anstelle von Spaltendaten zurückgegeben.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351040(v=exchg.10).md">pvData</a></td>
<td>Ruft den Puffer ab, der Daten speichert, die aus der Spalte abgerufen werden, oder legt diesen fest.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_RETRIEVECOLUMN-Klasse](./jet-retrievecolumn-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

---
description: Weitere Informationen zu JET_RECSIZE Eigenschaften
title: JET_RECSIZE Eigenschaften (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 522acb283022150cf6baeb8e82be3ebbe3cabbbe7c7cd50289f8d2312fbccb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118763791"
---
# <a name="jet_recsize-properties"></a>JET_RECSIZE-Eigenschaften

Einschließen geschützter Member  
Einschließen geerbter Member  

Der [JET_RECSIZE-Typ](./jet-recsize-structure2.md) macht die folgenden Member verfügbar.

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
<td><a href="hh557581(v=exchg.10).md">cbData</a></td>
<td>Ruft das Benutzerdatensatz im Datensatz ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></td>
<td>Ruft die komprimierte Größe der Benutzerdaten im Datensatz ab. Dies entspricht <a href="hh557581(v=exchg.10).md">cbData,</a> wenn keine systeminternen Long-Werte komprimiert werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh557913(v=exchg.10).md">cbLongValueData</a></td>
<td>Ruft das Benutzerdatensatz im Datensatz ab, das jedoch in der Struktur mit langen Werten gespeichert ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></td>
<td>Ruft die komprimierte Größe der Benutzerdaten in der Struktur mit langen Werten ab. Dies entspricht <a href="hh557913(v=exchg.10).md">cbLongValueData,</a> wenn keine getrennten long-Werte komprimiert werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></td>
<td>Ruft den Mehraufwand der Daten mit langen Werten ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh565836(v=exchg.10).md">cbOverhead</a></td>
<td>Ruft den Mehraufwand der ESENT-Datensatzstruktur für diesen Datensatz ab. Dies schließt die Schlüsselgröße des Datensatzes ein.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></td>
<td>Ruft die Gesamtzahl der Spalten im Datensatz ab, die komprimiert sind.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh596288(v=exchg.10).md">cLongValues</a></td>
<td>Ruft die Gesamtzahl der langen Werte ab, die in der Long-Value-Struktur für diesen Datensatz gespeichert sind. Dies schließt keine systeminternen long-Werte ein.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh577486(v=exchg.10).md">cMultiValues</a></td>
<td>Ruft die Akkumulation der Gesamtzahl der Werte nach der ersten für alle Spalten im Datensatz ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></td>
<td>Ruft die Gesamtzahl der festen und variablen Spalten ab, die in diesem Datensatz festgelegt sind.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></td>
<td>Ruft die Gesamtzahl der markierten Spalten ab, die in diesem Datensatz festgelegt sind.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_RECSIZE-Struktur](./jet-recsize-structure2.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)

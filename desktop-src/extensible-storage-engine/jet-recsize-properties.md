---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE-Eigenschaften'
title: JET_RECSIZE Eigenschaften (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4733e1d666bdf3f938c91f437c1764811fb10f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868944"
---
# <a name="jet_recsize-properties"></a>Eigenschaften von JET_RECSIZE

Geschützte Member einschließen  
Geerbte Member einschließen  

Der [JET_RECSIZE](./jet-recsize-structure2.md) -Typ macht die folgenden Member verfügbar.

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
<td>Ruft das Benutzer DataSet im Datensatz ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh596280(v=exchg.10).md">cbdatacompressed</a></td>
<td>Ruft die komprimierte Größe der Benutzerdaten im Datensatz ab. Dies ist das gleiche wie bei <a href="hh557581(v=exchg.10).md">cbData</a> , wenn keine systeminternen langen Werte komprimiert werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh557913(v=exchg.10).md">cblongvaluedata</a></td>
<td>Ruft das Benutzer DataSet im Datensatz ab, wird jedoch in der Struktur mit langem Wert gespeichert.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566144(v=exchg.10).md">cblongvaluedatacompressed</a></td>
<td>Ruft die komprimierte Größe von Benutzerdaten in der Struktur mit langem Wert ab. Dies entspricht <a href="hh557913(v=exchg.10).md">cblongvaluedata</a> , wenn keine getrennten langen Werte komprimiert werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh558003(v=exchg.10).md">cblongvalueoverhead</a></td>
<td>Ruft den mehr Aufwand für die Daten des langen Werts ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh565836(v=exchg.10).md">cboverhead</a></td>
<td>Ruft den Aufwand der ESENT-Daten Satzstruktur für diesen Datensatz ab. Dazu gehört auch die Schlüsselgröße des Datensatzes.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566154(v=exchg.10).md">ccompressedcolumns</a></td>
<td>Ruft die Gesamtzahl der Spalten im Datensatz ab, die komprimiert werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh596288(v=exchg.10).md">clongvalues</a></td>
<td>Ruft die Gesamtzahl der Long-Werte ab, die in der Struktur mit dem langen Wert für diesen Datensatz gespeichert sind. Dies schließt keine systeminternen Long-Werte ein.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh577486(v=exchg.10).md">cmultivalues</a></td>
<td>Ruft die Ansammlung der Gesamtzahl der Werte über den ersten für alle Spalten im Datensatz ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578172(v=exchg.10).md">cnontaggedcolumns</a></td>
<td>Ruft die Gesamtanzahl fester und variabler Spalten ab, die in diesem Datensatz festgelegt sind.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566034(v=exchg.10).md">ctaggedcolumns</a></td>
<td>Ruft die Gesamtzahl der markierten Spalten ab, die in diesem Datensatz festgelegt sind.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_RECSIZE Struktur](./jet-recsize-structure2.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)

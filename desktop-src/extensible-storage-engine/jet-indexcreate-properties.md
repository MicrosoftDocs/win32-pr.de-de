---
description: Weitere Informationen finden Sie unter JET_INDEXCREATE Eigenschaften.
title: JET_INDEXCREATE Eigenschaften
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0669d00b9c28e5299c5b9f55f0931ec7d22921eddad5e2b6b4876199057d111d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254267"
---
# <a name="jet_indexcreate-properties"></a>JET_INDEXCREATE Eigenschaften

Geschützte Member enthalten  
Geerbte Member enthalten  

Der [JET_INDEXCREATE](./jet-indexcreate-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn335122(v=exchg.10).md">cbKey</a></td>
<td>Ruft die Länge von szKey einschließlich der beiden endenden NULL-Werte in Zeichen ab oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335156(v=exchg.10).md">cbKeyMost</a></td>
<td>Ruft die maximal zulässige Größe für Schlüssel im Index in Bytes ab oder legt diese fest. Die unterstützte maximale Mindestschlüsselgröße beträgt JET_cbKeyMostMin (255). Dies ist die maximale Legacyschlüsselgröße. Die maximale Schlüsselgröße hängt von der Datenbankseitengröße <a href="hh596135(v=exchg.10).md">DatabasePageSize ab.</a> Die maximale Schlüsselgröße kann mit <a href="dn351156(v=exchg.10).md">KeyMost abgerufen werden.</a> Dieser Parameter wird auf Windows XP und Windows Server 2003 ignoriert. Im Gegensatz zur nicht verwalteten API wird <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) nicht benötigt, sie wird automatisch hinzugefügt.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></td>
<td>Ruft die maximale Länge jeder Spalte in Bytes ab, die im Index gespeichert werden soll, oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></td>
<td>Ruft die Anzahl der bedingten Spalten ab oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335157(v=exchg.10).md">Err</a></td>
<td>Ruft den Fehlercode beim Erstellen dieses Indexes ab oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335119(v=exchg.10).md">grbit</a></td>
<td>Ruft Indexerstellungsoptionen ab oder legt sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335159(v=exchg.10).md">pidxUnicode</a></td>
<td>Ruft die optionalen Unicode-Vergleichsoptionen ab oder legt sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335120(v=exchg.10).md">pSpaceHints</a></td>
<td>Ruft Hinweise zur Speicherplatzzuordnung, Wartung und Nutzung ab oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></td>
<td>Ruft die optionalen bedingten Spalten ab oder legt sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335121(v=exchg.10).md">szIndexName</a></td>
<td>Ruft den Namen des zu erstellenden Indexes ab oder legt den Namen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335161(v=exchg.10).md">szKey</a></td>
<td>Ruft die Beschreibung des Indexschlüssels ab oder legt diese fest. Dies ist eine doppelte null-terminierte Zeichenfolge von Token mit NULL-Trennzeichen. Jedes Token hat das Formular [Richtungsspezifizierer][Spaltenname], wobei direction-specification entweder oder &quot; + &quot; &quot; - &quot; ist. Ein szKey von &quot; +abc\0-def\0+wiederherstellen\0 indiziert z. B. die drei Spalten abc (in aufsteigender &quot; &quot; &quot; Reihenfolge), &quot; def &quot; (in &quot; absteigender Reihenfolge) und (" in aufsteigender &quot; Reihenfolge").</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335162(v=exchg.10).md">ulDensity</a></td>
<td>Ruft die Dichte des Indexes ab oder legt diese fest.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_INDEXCREATE-Klasse](./jet-indexcreate-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

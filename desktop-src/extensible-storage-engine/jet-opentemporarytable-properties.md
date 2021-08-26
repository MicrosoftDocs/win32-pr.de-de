---
description: Weitere Informationen finden Sie unter JET_OPENTEMPORARYTABLE Eigenschaften.
title: JET_OPENTEMPORARYTABLE (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbba2937283ab9a3d008d3bad04329d1fd42b84e0de4a1a42e2e100d99a03854
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016720"
---
# <a name="jet_opentemporarytable-properties"></a>JET_OPENTEMPORARYTABLE Eigenschaften

Geschützte Member enthalten  
Geerbte Member enthalten  

Der [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn335290(v=exchg.10).md">cbKeyMost</a></td>
<td>Ruft die maximale Größe für einen Schlüssel ab, der eine bestimmte Zeile darstellt, oder legt diese fest. Die maximale Schlüsselgröße kann festgelegt werden, um zu steuern, wie Schlüssel abgeschnitten werden. Das Abschneiden von Schlüsseln ist wichtig, da sie sich darauf auswirken kann, wenn Zeilen als eindeutig betrachtet werden. Wenn dieser Parameter auf 0 oder 255 festgelegt ist, bleiben die maximale Schlüsselgröße und ihre Semantik mit der maximalen Schlüsselgröße identisch, die von Windows Server 2003 unterstützt wird. Dieser Parameter kann auch als Funktion der Datenbankseitengröße für die <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>-Instanz auf einen größeren Wert festgelegt werden. Weitere Informationen finden Sie unter <a href="dn335292(v=exchg.10).md">KeyMost.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></td>
<td>Ruft die maximale Datenmenge ab, die aus einer variablen lengthcolumn verwendet wird, um einen Schlüssel für eine bestimmte Zeile zu erstellen, oder legt diese fest. Dieser Parameter kann verwendet werden, um die Menge des Schlüsselspeicherplatzes zu steuern, der von einer bestimmten Schlüsselspalte verbraucht wird. Dieser Grenzwert beträgt byte. Wenn dieser Parameter 0 (null) ist oder mit der <a href="dn335290(v=exchg.10).md">cbKeyMost-Eigenschaft</a> identisch ist, ist kein Grenzwert wirksam.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335287(v=exchg.10).md">ccolumn</a></td>
<td>Ruft die Anzahl der Spalten in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>ab oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351232(v=exchg.10).md">grbit</a></td>
<td>Ruft Optionen für die temporäre Tabelle ab oder legt sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335288(v=exchg.10).md">pidxunicode</a></td>
<td>Ruft die Locale ID und die Normalisierungsflags ab, die zum Vergleichen von Unicode-Schlüsselspaltendaten in der temporären Tabelle verwendet werden, oder legt diese fest. Wenn dieser Parameter NULL ist, wird die Standard-LCID verwendet, um alle Unicode-Schlüsselspalten in der temporären Tabelle zu vergleichen. Die Standard-LCID ist das us-englische Locale. Wenn dieser Parameter NULL ist, werden die Standardnormalisierungsflags verwendet, um alle Unicode-Schlüsselspaltendaten in der temporären Tabelle zu vergleichen. Die Standardnormalisierungsflags sind: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351228(v=exchg.10).md">prgcolumndef</a></td>
<td>Ruft die Spaltendefinitionen für die in der temporären Tabelle erstellten Spalten ab oder legt diese fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351233(v=exchg.10).md">prgcolumnid</a></td>
<td>Ruft den Ausgabepuffer ab, der das Array von Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden, oder legt diesen fest. Die Spalten-IDs in diesem Array entsprechen genau dem Eingabearray von Spaltendefinitionen. Daher muss die Größe dieses Puffers der Größe von <a href="dn351228(v=exchg.10).md">prgcolumndef entsprechen.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335293(v=exchg.10).md">tableid</a></td>
<td>Ruft das Tabellenhand handle für die temporäre Tabelle ab, die als Ergebnis eines erfolgreichen Aufrufs von JetOpenTemporaryTable erstellt wurde.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_OPENTEMPORARYTABLE-Klasse](./jet-opentemporarytable-class.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)

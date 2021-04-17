---
description: 'Weitere Informationen finden Sie hier: JET_RETRIEVECOLUMN Member'
title: Mitglieder JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103877
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9a5eda1d671cfe6225a8419314b2f53558294754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560911"
---
# <a name="jet_retrievecolumn-members"></a>Mitglieder JET_RETRIEVECOLUMN

Geschützte Member einschließen  
Geerbte Member einschließen  

Enthält Eingabe-und Ausgabeparameter für [jetretrievecolumschlag (JET_SESID JET_TABLEID, \[ \] , Int32)](./api.jetretrievecolumns-method.md). Felder in der Struktur beschreiben, welche Spaltenwerte abgerufen werden sollen, wie Sie abgerufen werden und wo die Ergebnisse gespeichert werden sollen.

Der [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) -Typ macht die folgenden Member verfügbar.

## <a name="constructors"></a>Konstruktoren

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></td>
<td></td>
</tr>
</tbody>
</table>


Oben

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
<td><a href="dn335226(v=exchg.10).md">cbactual</a></td>
<td>Ruft die Größe der Daten in Bytes ab, die durch einen Vorgang zum Abrufen einer Spalte abgerufen werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335228(v=exchg.10).md">cbData</a></td>
<td>Ruft die Größe des <a href="dn351040(v=exchg.10).md">pvData</a> -Puffers in Bytes ab oder legt diese fest. Der Vorgang zum Abrufen von Spalten speichert keine weiteren Daten in pvData als cbData.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335230(v=exchg.10).md">ColumnID</a></td>
<td>Ruft den Spalten Bezeichner für die abzurufende Spalte ab oder legt ihn fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335229(v=exchg.10).md">columnidnexttaging</a></td>
<td>Ruft das ColumnID der markierten Spalte mit mehreren Werten oder einer sparsespalte ab, wenn alle markierten Spalten abgerufen werden, indem 0 als ColumnID übergeben wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335231(v=exchg.10).md">irre</a></td>
<td>Ruft die vom Abruf der Spalte zurückgegebene Warnung ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335232(v=exchg.10).md">grbit</a></td>
<td>Ruft die Optionen zum Abrufen von Spalten ab oder legt Sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335233(v=exchg.10).md">ibdata</a></td>
<td>Ruft den Offset im Puffer ab, in dem Daten gespeichert werden, oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335234(v=exchg.10).md">iblongvalue</a></td>
<td>Ruft den Offset zum ersten Byte ab, das aus einer Spalte vom Typ <a href="hh577895(v=exchg.10).md">LONGBINARY</a> oder <a href="hh577895(v=exchg.10).md">LONGTEXT</a>abgerufen werden soll, oder legt diesen fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351039(v=exchg.10).md">itagsequence</a></td>
<td>Ruft die Sequenznummer der in einer mehrwertigen Spalte enthaltenen Werte ab oder legt Sie fest. Wenn itagsequence den Wert 0 hat, wird anstelle von Spaltendaten die Anzahl der Instanzen einer mehrwertigen Spalte zurückgegeben.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351040(v=exchg.10).md">pvData</a></td>
<td>Ruft den Puffer ab, in dem Daten gespeichert werden, die aus der Spalte abgerufen werden, oder legt diesen fest.</td>
</tr>
</tbody>
</table>


Oben

## <a name="methods"></a>Methoden

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn335224(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>darstellt. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_RETRIEVECOLUMN-Klasse](./jet-retrievecolumn-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

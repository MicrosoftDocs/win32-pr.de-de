---
description: 'Weitere Informationen finden Sie hier: JET_SETCOLUMN Member'
title: Mitglieder JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103848
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9c07f372705b20da09f2b3c3f1e5320771712c12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566177"
---
# <a name="jet_setcolumn-members"></a>Mitglieder JET_SETCOLUMN

Geschützte Member einschließen  
Geerbte Member einschließen  

Enthält Eingabe-und Ausgabeparameter für [jetsetcolumns (JET_SESID, JET_TABLEID, \[ \] , Int32)](./api.jetsetcolumns-method.md). Felder in der Struktur beschreiben, welcher Spaltenwert festgelegt werden soll, wie er festgelegt wird und wo die Spalten Satz Daten zu finden sind.

Der [JET_SETCOLUMN](./jet-setcolumn-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn335262(v=exchg.10).md">JET_SETCOLUMN</a></td>
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
<td><a href="dn351056(v=exchg.10).md">Contentequals</a></td>
<td>Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn335264(v=exchg.10).md">Deepclone</a></td>
<td>Gibt eine tiefe Kopie des-Objekts zurück.</td>
</tr>
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
<td><a href="dn335265(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a>darstellt. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_SETCOLUMN-Klasse](./jet-setcolumn-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

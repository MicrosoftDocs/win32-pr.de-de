---
description: 'Weitere Informationen finden Sie hier: JET_INDEXLIST Member'
title: Mitglieder JET_INDEXLIST
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7800ef911366bad40b2d02ee60e23b5d138d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050336"
---
# <a name="jet_indexlist-members"></a>Mitglieder JET_INDEXLIST

Geschützte Member einschließen  
Geerbte Member einschließen  

Informationen zu einer temporären Tabelle, die Informationen zu allen Indizes für eine bestimmte Tabelle enthält.

Der [JET_INDEXLIST](./jet-indexlist-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></td>
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
<td><a href="dn335125(v=exchg.10).md">columnidccolumn</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der Spalten im Index Schlüssel gespeichert wird. Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335126(v=exchg.10).md">columnidcentry</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der Einträge im Index gespeichert wird. Dieser Wert ist nicht aktuell und wird nur von &quot; API. jetcomputestats aktualisiert &quot; . Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335127(v=exchg.10).md">columnidckey</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der eindeutigen Schlüssel im Index gespeichert wird. Dieser Wert ist nicht aktuell und wird nur von &quot; API. jetcomputestats aktualisiert &quot; . Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335129(v=exchg.10).md">columnidcolyp</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der der Spaltentyp der indizierten Spalte gespeichert wird. Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der das ColumnID der indizierten Spalte gespeichert wird. Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der das grbit gespeichert ist, das auf die indizierte Spalte angewendet wird. Siehe <a href="hh579266(v=exchg.10).md">indexkeygrbit</a>. Die Spalte weist den Typ <a href="hh577895(v=exchg.10).md">Text</a>auf.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335168(v=exchg.10).md">columnidcp</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Codepage der indizierten Spalte gespeichert wird. Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Short</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335136(v=exchg.10).md">columnidcpage</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Anzahl der Seiten im Index gespeichert wird. Dieser Wert ist nicht aktuell und wird nur von &quot; API. jetcomputestats aktualisiert &quot; . Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335169(v=exchg.10).md">columnidgrbitcolumn</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der das grbit gespeichert ist, das auf die indizierte Spalte angewendet wird. Siehe <a href="hh579266(v=exchg.10).md">indexkeygrbit</a>. Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335134(v=exchg.10).md">columnidgrbitindex</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, die die für den Index verwendeten grbits speichert. Siehe " <a href="hh578433(v=exchg.10).md">kreateingedexgrbit</a>". Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335170(v=exchg.10).md">columnidicolumn</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der der Index von dieser Spalte im Index Schlüssel gespeichert wird. Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335138(v=exchg.10).md">columnidindexname</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der der Name des Indexes gespeichert wird. Die Spalte weist den Typ <a href="hh577895(v=exchg.10).md">Text</a>auf.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335171(v=exchg.10).md">columnidlangid</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Sprachen-ID (LCID) des Indexes gespeichert wird. Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Short</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335172(v=exchg.10).md">columnidlcmapflags</a></td>
<td>Ruft das ColumnID der Spalte in der temporären Tabelle ab, in der die Unicode-normalisierungs Flags für den Index gespeichert werden. Die Spalte ist vom Typ <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335173(v=exchg.10).md">crecord</a></td>
<td>Ruft die Anzahl der Datensätze in der temporären Tabelle ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335174(v=exchg.10).md">TableID</a></td>
<td>Ruft TableID der temporären Tabelle ab. Dies sollte geschlossen werden, wenn die Tabelle nicht mehr benötigt wird.</td>
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
<td><a href="dn335165(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>darstellt. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_INDEXLIST-Klasse](./jet-indexlist-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

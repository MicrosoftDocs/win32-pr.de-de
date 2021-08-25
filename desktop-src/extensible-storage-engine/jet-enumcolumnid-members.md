---
description: 'Erfahren Sie mehr über: JET_ENUMCOLUMNID Mitglieder'
title: JET_ENUMCOLUMNID Member
TOCTitle: JET_ENUMCOLUMNID members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_members(v=EXCHG.10)
ms:contentKeyID: 55103504
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 6aa360dce8b406e217496ad848be54992a71eaae04d375b2546ca08b75b1e751
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891310"
---
# <a name="jet_enumcolumnid-members"></a>JET_ENUMCOLUMNID Member

Geschützte Member enthalten  
Geerbte Member enthalten  

Aufzählt einen bestimmten Satz von Spalten und optional einen bestimmten Satz von mehreren Werten für diese Spalten, wenn die JetEnumerateColumns-Funktion verwendet wird. JetEnumerateColumns verwendet optional ein Array JET_ENUMCOLUMNID Strukturen.

Der [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></td>
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
<td><a href="dn335141(v=exchg.10).md">Columnid</a></td>
<td>Ruft die columnid-ID ab, die aufzählt werden soll, oder legt sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335092(v=exchg.10).md">ctagSequence</a></td>
<td>Ruft die Anzahl der Spaltenwerte (nach einem basierenden Index) ab, die für die angegebene Spalten-ID aufgezählt werden, oder legt diese fest. Wenn ctagSequence 0 (null) ist, wird rgtagSequence ignoriert, und alle Spaltenwerte für die angegebene Spalten-ID werden aufzählt.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335093(v=exchg.10).md">rgtagSequence</a></td>
<td>Ruft das Array von einsbasierten Indizes im Array von Spaltenwerten für eine bestimmte Spalte ab oder legt dieses fest. Ein einzelnes Element ist eine itagSequence, die in der JET_RETRIEVECOLUMN. Eine itagSequence von 0 (null) bedeutet &quot; &quot; überspringen. Eine itagSequence von 1 bedeutet, dass der erste Spaltenwert der Spalte, 2 die zweite Spalte und so weiter zurückgeben.</td>
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
<td>(Geerbt vom <a href="/dotnet/api/system.object">Objekt</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Geerbt vom <a href="/dotnet/api/system.object">Objekt</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Geerbt vom <a href="/dotnet/api/system.object">Objekt</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">Gettype</a></td>
<td>(Geerbt vom <a href="/dotnet/api/system.object">Objekt</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Geerbt vom <a href="/dotnet/api/system.object">Objekt</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn335091(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die <a href="dn335139(v=exchg.10).md">aktuelle</a>JET_ENUMCOLUMNID. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_ENUMCOLUMNID-Klasse](./jet-enumcolumnid-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

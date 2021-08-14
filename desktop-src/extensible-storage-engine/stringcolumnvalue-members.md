---
description: Weitere Informationen zu StringColumnValue-Membern
title: StringColumnValue-Member
TOCTitle: StringColumnValue members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.StringColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55104040
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 68f0050acea5c838fba3b23b4dc3f4df65177bf72012932fe8f07e568ebedd15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071250"
---
# <a name="stringcolumnvalue-members"></a>StringColumnValue-Member

Einschließen geschützter Member  
Einschließen geerbter Member  

Ein Unicode-Zeichenfolgenspaltenwert.

Der [StringColumnValue-Typ](./stringcolumnvalue-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn351187(v=exchg.10).md">StringColumnValue</a></td>
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
<td><a href="dn334166(v=exchg.10).md">Columnid</a></td>
<td>Ruft die festzulegende oder abzurufende columnid ab oder legt sie fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Fehler</a></td>
<td>Ruft die Warnung ab, die durch Abrufen oder Festlegen dieser Spalte generiert wurde. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Ruft die Itagsequenz der Spalte ab oder legt sie fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351195(v=exchg.10).md">Länge</a></td>
<td>Ruft die Bytelänge eines Spaltenwerts ab, der 0 (null) ist, wenn die Spalte NULL ist, andernfalls entspricht sie der Bytelänge des Zeichenfolgenwerts. Die Bytelänge wird in der Annahme von zwei Bytes pro Zeichen bestimmt. (Überschreibt <a href="dn334213(v=exchg.10).md">ColumnValue.Length.)</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Ruft Spaltenabrufoptionen ab oder legt diese fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Ruft Spaltenaktualisierungsoptionen ab oder legt sie fest. (Geerbt von <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Geschützte Eigenschaft" alt="Protected property" /></td>
<td><a href="dn351137(v=exchg.10).md">Größe</a></td>
<td>Ruft die Größe des Werts in der Spalte ab. Dies gibt 0 für Spalten variabler Größe (d. h. binär und Zeichenfolge) zurück. (Überschreibt <a href="dn334172(v=exchg.10).md">ColumnValue.Size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351204(v=exchg.10).md">Wert</a></td>
<td>Ruft den Wert der Spalte ab oder legt den Wert fest. Verwenden Sie <a href="dn334138(v=exchg.10).md">SetColumns(JET_SESID, JET_TABLEID, []),</a> um einen Datensatz mit dem Spaltenwert zu aktualisieren.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351202(v=exchg.10).md">ValueAsObject</a></td>
<td>Ruft den zuletzt festgelegten oder abgerufenen Wert der Spalte ab. Der Wert wird als generisches -Objekt zurückgegeben. (Überschreibt <a href="dn334214(v=exchg.10).md">ColumnValue.ValueAsObject.)</a></td>
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
<td><a href="dn351134(v=exchg.10).md">GetValueFromBytes</a></td>
<td>Decodieren Sie die Daten mit den aus ESENT abgerufenen Daten, und legen Sie den Wert im ColumnValue-Objekt fest. (Überschreibt <a href="dn334208(v=exchg.10).md">ColumnValue.GetValueFromBytes([], Int32, Int32, Int32)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Geerbt vom <a href="/dotnet/api/system.object">Objekt</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351194(v=exchg.10).md">ToString</a></td>
<td>Ruft eine Zeichenfolgendarstellung dieses -Objekts ab. (Überschreibt <a href="dn334163(v=exchg.10).md">ColumnValue.ToString()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[StringColumnValue-Klasse](./stringcolumnvalue-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

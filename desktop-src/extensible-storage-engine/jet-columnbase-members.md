---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNBASE Member'
title: 'JET_COLUMNBASE-Member '
TOCTitle: JET_COLUMNBASE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase_members(v=EXCHG.10)
ms:contentKeyID: 55103414
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 72f26e02963d1cc0617fb908ce325c0c0099f7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348288"
---
# <a name="jet_columnbase-members"></a>JET_COLUMNBASE-Member 

Geschützte Member einschließen  
Geerbte Member einschließen  

Beschreibt eine Spalte in einer Tabelle einer ESENT-Datenbank.

Der [JET_COLUMNBASE](./jet-columnbase-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn335065(v=exchg.10).md">cbmax</a></td>
<td>Ruft die maximale Länge der Spalte ab. Dies ist nur für Spalten vom Typ <a href="hh577895(v=exchg.10).md">Text</a>, <a href="hh577895(v=exchg.10).md">LONGTEXT</a>, <a href="hh577895(v=exchg.10).md">Binary</a> und <a href="hh577895(v=exchg.10).md">LONGBINARY</a>von Bedeutung.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351019(v=exchg.10).md">colyp</a></td>
<td>Ruft den Typ der Spalte ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335024(v=exchg.10).md">ColumnID</a></td>
<td>Ruft das ColumnID der Spalte ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335066(v=exchg.10).md">cp</a></td>
<td>Ruft die Codepage der Spalte ab. Dies ist nur für Spalten vom Typ " <a href="hh577895(v=exchg.10).md">Text</a> " und " <a href="hh577895(v=exchg.10).md">LONGTEXT</a>" sinnvoll.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351020(v=exchg.10).md">grbit</a></td>
<td>Ruft die Spalten Optionen ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335067(v=exchg.10).md">szbasecolumschlag Name</a></td>
<td>Ruft den Namen der Spalte in der Vorlagen Tabelle ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335026(v=exchg.10).md">szbasetablename</a></td>
<td>Ruft die Tabelle ab, von der die aktuelle Tabelle Ihre DDL erbt.</td>
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
<td><a href="dn335062(v=exchg.10).md">Ist gleich(Objekt)</a></td>
<td>Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist. (Überschreibt <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object. gleich(Objekt)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351009(v=exchg.10).md">Ist gleich(JET_COLUMNBASE)</a></td>
<td>Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn335023(v=exchg.10).md">GetHashCode</a></td>
<td>Gibt den Hashcode für diese Instanz zurück. (Überschreibt <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object. GetHashCode ()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn335064(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn335045(v=exchg.10).md">JET_COLUMNBASE</a>darstellt. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_COLUMNBASE-Klasse](./jet-columnbase-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

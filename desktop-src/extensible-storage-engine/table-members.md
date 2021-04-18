---
description: 'Weitere Informationen finden Sie hier: Tabellen Elemente'
title: 'Tabellenmember '
TOCTitle: Table members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table_members(v=EXCHG.10)
ms:contentKeyID: 55104054
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b4e5bd09cf1c450197978e3126dc63fe96ec6425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571194"
---
# <a name="table-members"></a>Tabellenmember 

Geschützte Member einschließen  
Geerbte Member einschließen  

Eine Klasse, die eine JET_TABLEID in einem verwerfbaren Objekt kapselt. Dadurch wird eine vorhandene Tabelle geöffnet. Verwenden Sie zum Erstellen einer Tabelle die jetkreatetable-Methode.

Der [Tabellentyp](./table-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn351234(v=exchg.10).md">Table</a></td>
<td>Initialisiert eine neue Instanz der Table-Klasse. Die Tabelle wird aus der angegebenen Datenbank geöffnet.</td>
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
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Geschützte Eigenschaft" alt="Protected property" /></td>
<td><a href="dn350578(v=exchg.10).md">Hasresource</a></td>
<td>Ruft einen Wert ab, der angibt, ob die zugrunde liegende Ressource zurzeit zugeordnet ist. (Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351171(v=exchg.10).md">Jettableid</a></td>
<td>Ruft den JET_TABLEID ab, der in dieser Tabelle enthalten ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351170(v=exchg.10).md">Name</a></td>
<td>Ruft den Namen dieser Tabelle ab.</td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">Checkobjectisnotverworfen</a></td>
<td>Löst eine Ausnahme aus, wenn dieses Objekt verworfen wurde. (Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351235(v=exchg.10).md">Schließen</a></td>
<td>Schließen Sie die Tabelle.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Verwerfen ()</a></td>
<td>Löschen Sie dieses Objekt, und veröffentlichen Sie die zugrunde liegende ESENT-Ressource. (Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Verwerfen (Boolean)</a></td>
<td>Wird von verwerfen und dem Finalizer aufgerufen. (Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">Finalize</a></td>
<td>Schließt eine Instanz der esentresource-Klasse ab. (Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn351168(v=exchg.10).md">Releaseresource</a></td>
<td>Freigeben der zugrunde liegenden JET_TABLEID. (Überschreibt <a href="dn350545(v=exchg.10).md">esentresource. releaseresource ()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">Resourcewaszugewiesen</a></td>
<td>Wird von einer Unterklasse aufgerufen, wenn eine Ressource zugeordnet wird. (Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">Resourcewasreleased</a></td>
<td>Wird von einer Unterklasse aufgerufen, wenn eine Ressource freigegeben wird. (Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351237(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die aktuelle <a href="dn351163(v=exchg.10).md">Tabelle</a>darstellt. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="operators"></a>Operatoren

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
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="dn351239(v=exchg.10).md">Implizit (zu JET_TABLEID Tabelle)</a></td>
<td>Impliziter Konvertierungs Operator aus einer Tabelle in einen JET_TABLEID. Dadurch kann eine Tabelle mit APIs verwendet werden, die eine JET_TABLEID erwarten.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Table-Klasse](./table-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

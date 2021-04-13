---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMN Member'
title: Mitglieder JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103614
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: a1281d7d81fc4e0db476c4ca0f9ac688a7a7b055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561021"
---
# <a name="jet_enumcolumn-members"></a>Mitglieder JET_ENUMCOLUMN

Geschützte Member einschließen  
Geerbte Member einschließen  

Listet die Spaltenwerte eines Datensatzes mithilfe der jetenumeratecolumns-Funktion auf. Jetenreeratecolenns gibt ein Array von JET_ENUMCOLUMNVALUE Strukturen zurück. Das Array wird im Arbeitsspeicher zurückgegeben, der mithilfe des Rückrufs zugewiesen wurde, der für diese Funktion angegeben wurde.

Der [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></td>
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
<td><a href="dn335137(v=exchg.10).md">cbData</a></td>
<td>Ruft die Größe des Werts ab, der für die Spalte aufgelistet wurde. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> gleich <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">cenenumcolumnvalue</a></td>
<td>Ruft die Anzahl der für die Spalte aufgelisteten Spaltenwerte ab. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> nicht <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">ColumnID</a></td>
<td>Ruft die aufgelistete ColumnID-ID ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">irre</a></td>
<td>Ruft den Spalten Statuscode ab, der sich aus der-Enumeration ergibt.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">pvData</a></td>
<td>Ruft den Wert ab, der für die Spalte aufgelistet wurde. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> gleich <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist. Dies verweist auf den Arbeitsspeicher, der mit dem an <a href="dn292148(v=exchg.10).md">jetenumeratecolumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, enumeratecolumnsgrbit)</a>weiter gegebenen Rückruf für den <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> Zuweisung zugeordnet wird. Vergessen Sie nicht, den Arbeitsspeicher zu veröffentlichen</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">rgenenumcolumnvalue</a></td>
<td>Ruft die enumerationsspaltenwerte für die Spalte ab. Dieser Member wird nur verwendet, wenn <a href="dn335086(v=exchg.10).md">Err</a> nicht <a href="hh557250(v=exchg.10).md">columnsinglevalue</a>ist.</td>
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
<td><a href="dn335132(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>darstellt. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_ENUMCOLUMN-Klasse](./jet-enumcolumn-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

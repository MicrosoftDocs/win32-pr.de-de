---
description: Weitere Informationen zu ColumnValue-Membern
title: ColumnValue-Elemente
TOCTitle: ColumnValue members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55100951
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f197a18f1ef0f024a51f8d51f00cb269705edcf65ffac713ce91ef416cd9d7f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120066980"
---
# <a name="columnvalue-members"></a>ColumnValue-Elemente

Einschließen geschützter Member  
Einschließen geerbter Member  

Basisklasse für Objekte, die einen festzulegenden Spaltenwert darstellen.

Der [ColumnValue-Typ](./columnvalue-class.md) macht die folgenden Member verfügbar.

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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn334207(v=exchg.10).md">ColumnValue</a></td>
<td>Initialisiert eine neue Instanz der ColumnValue-Klasse.</td>
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
<td>Ruft die festzulegende oder abzurufende columnid ab oder legt sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Fehler</a></td>
<td>Ruft die Warnung ab, die durch Abrufen oder Festlegen dieser Spalte generiert wurde.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Ruft die Itagsequenz der Spalte ab oder legt sie fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334213(v=exchg.10).md">Länge</a></td>
<td>Ruft die Bytelänge eines Spaltenwerts ab, der 0 (null) ist, wenn die Spalte NULL ist. Andernfalls entspricht sie der Größe für Spalten fester Größe und stellt die tatsächliche Wertbytelänge für Spalten variabler Größe (binär und Zeichenfolge) dar. Bei Zeichenfolgen wird die Länge in Annahme von zwei Bytes pro Zeichen bestimmt.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Ruft Spaltenabrufoptionen ab oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Ruft Spaltenaktualisierungsoptionen ab oder legt sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Geschützte Eigenschaft" alt="Protected property" /></td>
<td><a href="dn334172(v=exchg.10).md">Größe</a></td>
<td>Ruft die Größe des Werts in der Spalte ab. Dies gibt 0 für Spalten variabler Größe (d. h. binär und Zeichenfolge) zurück.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn334214(v=exchg.10).md">ValueAsObject</a></td>
<td>Ruft den zuletzt festgelegten oder abgerufenen Wert der Spalte ab. Der Wert wird als generisches -Objekt zurückgegeben.</td>
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
<td><a href="dn334208(v=exchg.10).md">GetValueFromBytes</a></td>
<td>Decodieren Sie die Daten mit den aus ESENT abgerufenen Daten, und legen Sie den Wert im ColumnValue-Objekt fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Geerbt vom <a href="/dotnet/api/system.object">Objekt</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn334163(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die den aktuellen <a href="dn334206(v=exchg.10).md">ColumnValue</a>darstellt. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[ColumnValue-Klasse](./columnvalue-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

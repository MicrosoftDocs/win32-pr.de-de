---
description: 'Erfahren Sie mehr über: JET_RETRIEVECOLUMN Mitglieder'
title: JET_RETRIEVECOLUMN Mitglieder
TOCTitle: JET_RETRIEVECOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103877
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 84a778eb86c09da86f8c524daa321df9e8ca104122af6ecc13de88c2a824b79d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979480"
---
# <a name="jet_retrievecolumn-members"></a>JET_RETRIEVECOLUMN Mitglieder

Geschützte Member enthalten  
Geerbte Member enthalten  

Enthält Eingabe- und Ausgabeparameter für [JetRetrieveColumns(JET_SESID, JET_TABLEID, \[ \] , Int32).](./api.jetretrievecolumns-method.md) Felder in der Struktur beschreiben, welcher Spaltenwert abgerufen werden soll, wie er abgerufen wird und wo Ergebnisse zu speichern sind.

Der [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn335226(v=exchg.10).md">cbActual</a></td>
<td>Ruft die Größe von Daten in Bytes ab, die durch einen Abrufspaltenvorgang abgerufen werden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335228(v=exchg.10).md">cbData</a></td>
<td>Ruft die Größe des <a href="dn351040(v=exchg.10).md">pvData-Puffers</a> in Bytes ab oder legt diese fest. Der Vorgang zum Abrufen der Spalte enthält nicht mehr Daten in pvData als cbData.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335230(v=exchg.10).md">Columnid</a></td>
<td>Ruft den Spaltenbezeichner für die abzurufende Spalte ab oder legt diese fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></td>
<td>Ruft die Columnid der markierten, mehrwertigen oder Sparsespalte ab, wenn alle markierten Spalten abgerufen werden, indem 0 als columnid übergeben wird.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335231(v=exchg.10).md">Err</a></td>
<td>Ruft die Warnung ab, die beim Abrufen der Spalte zurückgegeben wurde.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335232(v=exchg.10).md">grbit</a></td>
<td>Ruft die Optionen für den Spaltenabruf ab oder legt sie fest.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335233(v=exchg.10).md">ibData</a></td>
<td>Ruft den Offset im Puffer ab, in dem Daten gespeichert werden, oder legt diesen fest.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn335234(v=exchg.10).md">ibLongValue</a></td>
<td>Ruft den Offset auf das erste Byte ab, das aus einer Spalte vom Typ <a href="hh577895(v=exchg.10).md">LongBinary</a> oder LongText abgerufen werden soll, oder <a href="hh577895(v=exchg.10).md">legt diesen fest.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351039(v=exchg.10).md">itagSequence</a></td>
<td>Ruft die Sequenznummer der Werte ab, die in einer mehrwertigen Spalte enthalten sind, oder legt diese fest. Wenn itagSequence 0 ist, wird anstelle von Spaltendaten die Anzahl der Instanzen einer mehrwertigen Spalte zurückgegeben.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351040(v=exchg.10).md">pvData</a></td>
<td>Ruft den Puffer ab, in dem daten gespeichert werden, die aus der Spalte abgerufen werden, oder legt diesen fest.</td>
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
<td><a href="dn335224(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die <a href="dn351033(v=exchg.10).md">aktuelle</a>JET_RETRIEVECOLUMN. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_RETRIEVECOLUMN-Klasse](./jet-retrievecolumn-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

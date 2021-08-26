---
description: 'Erfahren Sie mehr über: JET_RECSIZE Mitglieder'
title: JET_RECSIZE Mitglieder (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: JET_RECSIZE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_members(v=EXCHG.10)
ms:contentKeyID: 39510137
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8a39bc4aee3b033b735d5c4ebe818d189c36b1908ba8364200c4cb94b15459cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063740"
---
# <a name="jet_recsize-members"></a>JET_RECSIZE Mitglieder

Geschützte Member enthalten  
Geerbte Member enthalten  

Wird von [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) verwendet, um Informationen über die Nutzungsanforderungen eines Datensatzes im Benutzerdatenbereich, die Anzahl der festgelegten Spalten, die Anzahl von Werten und den Mehraufwand für die ESENT-Datensatzstruktur zurück zu geben.

Der [JET_RECSIZE](./jet-recsize-structure2.md) macht die folgenden Member verfügbar.

## <a name="properties"></a>Eigenschaften

<table>
<thead>
<tr class="header">
<th> </th>
<th>Name</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh557581(v=exchg.10).md">cbData</a></td>
<td>Ruft das Benutzerdatensatz im Datensatz ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></td>
<td>Ruft die komprimierte Größe der Benutzerdaten im Datensatz ab. Dies ist identisch mit <a href="hh557581(v=exchg.10).md">cbData,</a> wenn keine systeminternen Long-Werte komprimiert sind.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh557913(v=exchg.10).md">cbLongValueData</a></td>
<td>Ruft das Benutzerdatensatz im Datensatz ab, das jedoch in der Long-Value-Struktur gespeichert ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></td>
<td>Ruft die komprimierte Größe der Benutzerdaten in der Long-Value-Struktur ab. Dies ist identisch mit <a href="hh557913(v=exchg.10).md">cbLongValueData,</a> wenn keine getrennten long-Werte komprimiert werden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></td>
<td>Ruft den Mehraufwand der Long-Value-Daten ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh565836(v=exchg.10).md">cbOverhead</a></td>
<td>Ruft den Mehraufwand der ESENT-Datensatzstruktur für diesen Datensatz ab. Dies schließt die Schlüsselgröße des Datensatzes ein.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></td>
<td>Ruft die Gesamtzahl der komprimierten Spalten im Datensatz ab.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh596288(v=exchg.10).md">cLongValues</a></td>
<td>Ruft die Gesamtzahl der long-Werte ab, die in der Long-Value-Struktur für diesen Datensatz gespeichert sind. Dies schließt keine systeminternen Long-Werte ein.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh577486(v=exchg.10).md">cMultiValues</a></td>
<td>Ruft die Akkumulation der Gesamtzahl von Werten ab, die über die erste für alle Spalten im Datensatz hinausgehen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></td>
<td>Ruft die Gesamtzahl der festen und variablen Spalten ab, die in diesem Datensatz festgelegt sind.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></td>
<td>Ruft die Gesamtzahl der markierten Spalten ab, die in diesem Datensatz festgelegt sind.</td>
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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh538879(v=exchg.10).md">Add (Hinzufügen)</a></td>
<td>Fügen Sie die Größen in zwei JET_RECSIZE hinzu.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh558506(v=exchg.10).md">Equals(Object)</a></td>
<td>Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist. (Überschreibt <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh577992(v=exchg.10).md">Equals(JET_RECSIZE)</a></td>
<td>Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Geerbt vom <a href="/dotnet/api/system.object">Objekt</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh557078(v=exchg.10).md">GetHashCode</a></td>
<td>Gibt den Hashcode für diese Instanz zurück. (Überschreibt <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>.)</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh579561(v=exchg.10).md">Subtrahieren</a></td>
<td>Berechnen Sie den Größenunterschied zwischen zwei JET_RECSIZE Strukturen.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.valuetype">ValueType</a>.)</td>
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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh578675(v=exchg.10).md">Addition</a></td>
<td>Fügen Sie die Größen in zwei JET_RECSIZE hinzu.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh596362(v=exchg.10).md">Gleichheit</a></td>
<td>Bestimmt, ob zwei angegebene Instanzen JET_RECSIZE gleich sind.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh578809(v=exchg.10).md">Ungleichheit</a></td>
<td>Bestimmt, ob zwei angegebene Instanzen JET_RECSIZE gleich sind.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh596696(v=exchg.10).md">Subtraktion</a></td>
<td>Berechnen Sie den Größenunterschied zwischen zwei JET_RECSIZE Strukturen.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_RECSIZE-Struktur](./jet-recsize-structure2.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)

---
description: 'Weitere Informationen finden Sie hier: JET_THREADSTATS Member'
title: JET_THREADSTATS Mitglieder (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_THREADSTATS members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats_members(v=EXCHG.10)
ms:contentKeyID: 39514028
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f8b824f716d35c3039bb77af745cf6cf08dfc9cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960416"
---
# <a name="jet_threadstats-members"></a>Mitglieder JET_THREADSTATS

Geschützte Member einschließen  
Geerbte Member einschließen  

Enthält kumulative Statistiken für die Arbeit, die von der Datenbank-Engine auf dem aktuellen Thread ausgeführt wird. Diese Informationen werden über jetgetthreadstats zurückgegeben.

Der [JET_THREADSTATS](./jet-threadstats-structure2.md) -Typ macht die folgenden Member verfügbar.

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
<td><a href="hh578305(v=exchg.10).md">cblogdatensatz</a></td>
<td>Ruft die Gesamtgröße (in Bytes) der Transaktionsprotokoll Datensätze ab, die von der Datenbank-Engine im aktuellen Thread generiert wurden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578110(v=exchg.10).md">clogrecord</a></td>
<td>Ruft die Gesamtanzahl der Transaktionsprotokoll-Datensätze ab, die von der Datenbank-Engine im aktuellen Thread generiert wurden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh578651(v=exchg.10).md">cpagedirtied</a></td>
<td>Ruft die Gesamtanzahl der Datenbankseiten ohne ungeschriebene Änderungen ab, die von der Datenbank-Engine im aktuellen Thread geändert wurden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh557376(v=exchg.10).md">cpagepreread</a></td>
<td>Ruft die Gesamtanzahl der Datenbankseiten ab, die von der Datenbank-Engine auf dem aktuellen Thread vorab von der Festplatte abgerufen wurden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh163392(v=exchg.10).md">cpageread</a></td>
<td>Ruft die Gesamtanzahl der Datenbankseiten ab, die von der Datenbank-Engine auf dem aktuellen Thread von der Festplatte abgerufen wurden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh596234(v=exchg.10).md">cPageRedirtied</a></td>
<td>Ruft die Gesamtanzahl der Datenbankseiten mit ungeschriebenen Änderungen ab, die von der Datenbank-Engine im aktuellen Thread geändert wurden.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="hh557174(v=exchg.10).md">cpagereferenziert</a></td>
<td>Ruft die Gesamtanzahl der Datenbankseiten ab, die von der Datenbank-Engine im aktuellen Thread besucht wurden.</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh565584(v=exchg.10).md">Add (Hinzufügen)</a></td>
<td>Fügen Sie die Statistiken in zwei JET_THREADSTATS Strukturen hinzu.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh538903(v=exchg.10).md">Erstellen</a></td>
<td>Erstellen Sie eine neue <a href="hh578565(v=exchg.10).md">JET_THREADSTATS</a> Struktur mit dem angegebenen Wert.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh557146(v=exchg.10).md">Ist gleich(Objekt)</a></td>
<td>Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist. (Überschreibt <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. gleich (Object)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh596601(v=exchg.10).md">Ist gleich(JET_THREADSTATS)</a></td>
<td>Gibt einen Wert zurück, der angibt, ob diese Instanz gleich einer anderen Instanz ist.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh579156(v=exchg.10).md">GetHashCode</a></td>
<td>Gibt den Hashcode für diese Instanz zurück. (Überschreibt <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.)</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh579433(v=exchg.10).md">Subtrahieren</a></td>
<td>Berechnen Sie den Unterschied in den Statistiken zwischen zwei JET_THREADSTATS Strukturen.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="hh558249(v=exchg.10).md">ToString</a></td>
<td>Ruft eine Zeichen folgen Darstellung dieses-Objekts ab. (Überschreibt <a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ValueType.-Zeichenfolge ()</a>.)</td>
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
<td><a href="hh163281(v=exchg.10).md">Zudem</a></td>
<td>Fügen Sie die Statistiken in zwei JET_THREADSTATS Strukturen hinzu.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh558521(v=exchg.10).md">Gleichheit</a></td>
<td>Bestimmt, ob zwei angegebene Instanzen von JET_THREADSTATS gleich sind.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh577527(v=exchg.10).md">Ungleichheit</a></td>
<td>Bestimmt, ob zwei angegebene Instanzen von JET_THREADSTATS nicht gleich sind.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><a href="hh557686(v=exchg.10).md">Subtraktion</a></td>
<td>Berechnen Sie den Unterschied in den Statistiken zwischen zwei JET_THREADSTATS Strukturen.</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_THREADSTATS Struktur](./jet-threadstats-structure2.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)

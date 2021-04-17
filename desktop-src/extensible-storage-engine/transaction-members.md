---
description: 'Weitere Informationen finden Sie hier: Transaktions Elemente'
title: 'Transaktionsmember '
TOCTitle: Transaction members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_members(v=EXCHG.10)
ms:contentKeyID: 55104159
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4a11aba5d3ffdc8a0e02bd166aa0a433d4860af5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561157"
---
# <a name="transaction-members"></a>Transaktionsmember 

Geschützte Member einschließen  
Geerbte Member einschließen  

Eine Klasse, die eine Transaktion für eine JET_SESID kapselt.

Der [Transaktionstyp](./transaction-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn351177(v=exchg.10).md">Transaktion</a></td>
<td>Initialisiert eine neue Instanz der Transaction-Klasse. Dadurch wird automatisch eine Transaktion gestartet. Wenn nicht explizit ein Commit für die Transaktion ausgeführt wird, wird ein Rollback ausgeführt</td>
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
<td><a href="dn351180(v=exchg.10).md">IsInTransaction</a></td>
<td>Ruft einen Wert ab, der angibt, ob dieses-Objekt derzeit in einer Transaktion ist.</td>
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
<td><a href="dn351172(v=exchg.10).md">Starten</a></td>
<td>Beginnen Sie eine Transaktion. Dieses Objekt sollte sich zurzeit nicht in einer Transaktion befinden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">Checkobjectisnotverworfen</a></td>
<td>Löst eine Ausnahme aus, wenn dieses Objekt verworfen wurde. (Geerbt von <a href="dn319890(v=exchg.10).md">esentresource</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351179(v=exchg.10).md">Commit (committransaktiongrbit)</a></td>
<td>Commit für eine Transaktion durchsetzen. Dieses Objekt sollte sich in einer Transaktion befinden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351243(v=exchg.10).md">Commit (committransaktiongrbit, TimeSpan, JET_COMMIT_ID)</a></td>
<td>Commit für eine Transaktion durchsetzen. Dieses Objekt sollte sich in einer Transaktion befinden.</td>
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
<td><a href="dn351176(v=exchg.10).md">Releaseresource</a></td>
<td>Wird aufgerufen, wenn die Transaktion entfernt wird, während Sie aktiv ist. Dadurch sollte für die Transaktion ein Rollback ausgeführt werden. (Überschreibt <a href="dn350545(v=exchg.10).md">esentresource. releaseresource ()</a>.)</td>
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
<td><a href="dn351244(v=exchg.10).md">Rollback</a></td>
<td>Rollback einer Transaktion. Dieses Objekt sollte sich in einer Transaktion befinden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351181(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die aktuelle <a href="dn351174(v=exchg.10).md">Transaktion</a>darstellt. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Transaktionsklasse](./transaction-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

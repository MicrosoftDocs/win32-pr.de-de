---
description: 'Weitere Informationen zu: Transaktionsmember'
title: 'Transaktionsmember '
TOCTitle: Transaction members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_members(v=EXCHG.10)
ms:contentKeyID: 55104159
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1fd83b27d0ac1469395aa829a1526fb9699664b88a72eae136329d01729763b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117702366"
---
# <a name="transaction-members"></a>Transaktionsmember 

Einschließen geschützter Member  
Einschließen geerbter Member  

Eine Klasse, die eine Transaktion auf einem JET_SESID kapselt.

Der [Transaktionstyp](./transaction-class.md) macht die folgenden Member verfügbar.

## <a name="constructors"></a>Konstruktoren

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351177(v=exchg.10).md">Transaktion</a></td>
<td>Initialisiert eine neue Instanz der Transaction-Klasse. Dadurch wird automatisch eine Transaktion gestartet. Für die Transaktion wird ein Rollback ausgeführt, wenn kein expliziter Commit ausgeführt wird.</td>
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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Geschützte Eigenschaft" alt="Protected property" /></td>
<td><a href="dn350578(v=exchg.10).md">HasResource</a></td>
<td>Ruft einen Wert ab, der angibt, ob die zugrunde liegende Ressource derzeit zugeordnet ist. (Geerbt von <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn351180(v=exchg.10).md">IsInTransaction</a></td>
<td>Ruft einen Wert ab, der angibt, ob sich dieses Objekt derzeit in einer Transaktion befindet.</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351172(v=exchg.10).md">Starten</a></td>
<td>Starten Sie eine Transaktion. Dieses Objekt sollte sich derzeit nicht in einer Transaktion befinden.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></td>
<td>Löst eine Ausnahme aus, wenn dieses Objekt verworfen wurde. (Geerbt von <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></td>
<td>Committen einer Transaktion. Dieses Objekt sollte sich in einer Transaktion befindet.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></td>
<td>Committen einer Transaktion. Dieses Objekt sollte sich in einer Transaktion befindet.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose()</a></td>
<td>Verwerfen Sie dieses Objekt, und geben Sie die zugrunde liegende Esent-Ressource frei. (Geerbt von <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></td>
<td>Wird von Dispose und dem Finalizer aufgerufen. (Geerbt von <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></td>
<td>(Geerbt vom <a href="/dotnet/api/system.object">Objekt</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">Finalize</a></td>
<td>Finalisiert eine Instanz der EsentResource-Klasse. (Geerbt von <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn351176(v=exchg.10).md">ReleaseResource</a></td>
<td>Wird aufgerufen, wenn die Transaktion verworfen wird, während sie aktiv ist. Dadurch sollte ein Rollback der Transaktion ausgeführt werden. (Überschreibt <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></td>
<td>Wird von einer Unterklasse aufgerufen, wenn eine Ressource zugeordnet wird. (Geerbt von <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></td>
<td>Wird von einer Unterklasse aufgerufen, wenn eine Ressource freigegeben wird. (Geerbt von <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351244(v=exchg.10).md">Rollback</a></td>
<td>Rollback einer Transaktion. Dieses Objekt sollte sich in einer Transaktion befindet.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn351181(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die aktuelle <a href="dn351174(v=exchg.10).md">Transaktion</a>darstellt. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Transaktionsklasse](./transaction-class.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

---
description: 'Weitere Informationen: Instanzmember'
title: Instanzmember
TOCTitle: Instance members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance_members(v=EXCHG.10)
ms:contentKeyID: 55103299
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8ba8dad079feba566dbb8fca873fcea19af778ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863200"
---
# <a name="instance-members"></a>Instanzmember

Geschützte Member einschließen  
Geerbte Member einschließen  

Eine Klasse, die eine [JET_INSTANCE](./jet-instance-structure.md) in einem verwerfbaren Objekt kapselt. Die Instanz muss zuletzt geschlossen werden, und das Schließen der-Instanz gibt alle anderen Ressourcen für die-Instanz frei.

Der [Instanztyp](./instance-class.md) macht die folgenden Member verfügbar.

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
<td><a href="dn350924(v=exchg.10).md">Instanz (Zeichenfolge)</a></td>
<td>Initialisiert eine neue Instanz der Instanzklasse. Die zugrunde liegende JET_INSTANCE ist zugeordnet, aber nicht initialisiert.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn350927(v=exchg.10).md">Instance (Zeichenfolge, Zeichenfolge)</a></td>
<td>Initialisiert eine neue Instanz der Instanzklasse. Die zugrunde liegende JET_INSTANCE ist zugeordnet, aber nicht initialisiert.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn350948(v=exchg.10).md">Instance (String, String, termgrbit)</a></td>
<td>Initialisiert eine neue Instanz der Instanzklasse. Die zugrunde liegende JET_INSTANCE ist zugeordnet, aber nicht initialisiert.</td>
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
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></td>
<td>(Geerbt von <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350941(v=exchg.10).md">Jetinstance</a></td>
<td>Ruft den JET_INSTANCE ab, den diese Instanz enthält.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350962(v=exchg.10).md">Parameter</a></td>
<td>Ruft die instanceparameters für diese Instanz ab.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><a href="dn350964(v=exchg.10).md">Termgrbit</a></td>
<td>Ruft das termgrbit für diese-Instanz ab oder legt es fest.</td>
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
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Schließen</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">Gefährousadressf</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Verwerfen ()</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Verwerfen (Boolean)</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalize</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn350932(v=exchg.10).md">Init ()</a></td>
<td>Initialisieren Sie die JET_INSTANCE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn350954(v=exchg.10).md">Init (initgrbit)</a></td>
<td>Initialisieren Sie die JET_INSTANCE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn350934(v=exchg.10).md">Init (JET_RSTINFO, initgrbit)</a></td>
<td>Initialisieren Sie die JET_INSTANCE. Diese API erfordert mindestens die Vista-Version von ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></td>
<td>(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></td>
<td>Gibt das Handle für diese Instanz frei. (Überschreibt <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle. ReleaseHandle ()</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">"Ziel"</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">"" Ist "".</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn350935(v=exchg.10).md">Begriff</a></td>
<td>Beenden Sie die JET_INSTANCE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><a href="dn350960(v=exchg.10).md">ToString</a></td>
<td>Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die aktuelle <a href="dn350923(v=exchg.10).md">Instanz</a>darstellt. (Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</td>
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
<td><a href="dn350950(v=exchg.10).md">Implizit (zu JET_INSTANCE Instanz)</a></td>
<td>Bereitstellen der impliziten Konvertierung eines Instanzobjekts in eine JET_INSTANCE Struktur. Dies geschieht, damit eine-Instanz überall dort verwendet werden kann, wo eine JET_INSTANCE erforderlich ist.</td>
</tr>
</tbody>
</table>


Oben

## <a name="fields"></a>Felder

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
<td><img src="../images/dn350944.protfield(exchg.10).gif" title="Geschütztes Feld" alt="Protected field" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">bewältigen</a></td>
<td>(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</td>
</tr>
</tbody>
</table>


Oben

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanzklasse](./instance-class.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

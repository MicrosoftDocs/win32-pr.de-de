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
# <a name="instance-members"></a><span data-ttu-id="ff616-103">Instanzmember</span><span class="sxs-lookup"><span data-stu-id="ff616-103">Instance members</span></span>

<span data-ttu-id="ff616-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="ff616-104">Include protected members</span></span>  
<span data-ttu-id="ff616-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="ff616-105">Include inherited members</span></span>  

<span data-ttu-id="ff616-106">Eine Klasse, die eine [JET_INSTANCE](./jet-instance-structure.md) in einem verwerfbaren Objekt kapselt.</span><span class="sxs-lookup"><span data-stu-id="ff616-106">A class that encapsulates a [JET_INSTANCE](./jet-instance-structure.md) in a disposable object.</span></span> <span data-ttu-id="ff616-107">Die Instanz muss zuletzt geschlossen werden, und das Schließen der-Instanz gibt alle anderen Ressourcen für die-Instanz frei.</span><span class="sxs-lookup"><span data-stu-id="ff616-107">The instance must be closed last and closing the instance releases all other resources for the instance.</span></span>

<span data-ttu-id="ff616-108">Der [Instanztyp](./instance-class.md) macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ff616-108">The [Instance](./instance-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="ff616-109">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="ff616-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ff616-110">Name</span><span class="sxs-lookup"><span data-stu-id="ff616-110">Name</span></span></th>
<th><span data-ttu-id="ff616-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff616-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-113"><a href="dn350924(v=exchg.10).md">Instanz (Zeichenfolge)</a></span><span class="sxs-lookup"><span data-stu-id="ff616-113"><a href="dn350924(v=exchg.10).md">Instance(String)</a></span></span></td>
<td><span data-ttu-id="ff616-114">Initialisiert eine neue Instanz der Instanzklasse.</span><span class="sxs-lookup"><span data-stu-id="ff616-114">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="ff616-115">Die zugrunde liegende JET_INSTANCE ist zugeordnet, aber nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="ff616-115">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-117"><a href="dn350927(v=exchg.10).md">Instance (Zeichenfolge, Zeichenfolge)</a></span><span class="sxs-lookup"><span data-stu-id="ff616-117"><a href="dn350927(v=exchg.10).md">Instance(String, String)</a></span></span></td>
<td><span data-ttu-id="ff616-118">Initialisiert eine neue Instanz der Instanzklasse.</span><span class="sxs-lookup"><span data-stu-id="ff616-118">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="ff616-119">Die zugrunde liegende JET_INSTANCE ist zugeordnet, aber nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="ff616-119">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-121"><a href="dn350948(v=exchg.10).md">Instance (String, String, termgrbit)</a></span><span class="sxs-lookup"><span data-stu-id="ff616-121"><a href="dn350948(v=exchg.10).md">Instance(String, String, TermGrbit)</a></span></span></td>
<td><span data-ttu-id="ff616-122">Initialisiert eine neue Instanz der Instanzklasse.</span><span class="sxs-lookup"><span data-stu-id="ff616-122">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="ff616-123">Die zugrunde liegende JET_INSTANCE ist zugeordnet, aber nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="ff616-123">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff616-124">Oben</span><span class="sxs-lookup"><span data-stu-id="ff616-124">Top</span></span>

## <a name="properties"></a><span data-ttu-id="ff616-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ff616-125">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ff616-126">Name</span><span class="sxs-lookup"><span data-stu-id="ff616-126">Name</span></span></th>
<th><span data-ttu-id="ff616-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff616-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="ff616-129"><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></span><span class="sxs-lookup"><span data-stu-id="ff616-129"><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></span></span></td>
<td><span data-ttu-id="ff616-130">(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-130">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="ff616-132"><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></span><span class="sxs-lookup"><span data-stu-id="ff616-132"><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></span></span></td>
<td><span data-ttu-id="ff616-133">(Geerbt von <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-133">(Inherited from <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="ff616-135"><a href="dn350941(v=exchg.10).md">Jetinstance</a></span><span class="sxs-lookup"><span data-stu-id="ff616-135"><a href="dn350941(v=exchg.10).md">JetInstance</a></span></span></td>
<td><span data-ttu-id="ff616-136">Ruft den JET_INSTANCE ab, den diese Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="ff616-136">Gets the JET_INSTANCE that this instance contains.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="ff616-138"><a href="dn350962(v=exchg.10).md">Parameter</a></span><span class="sxs-lookup"><span data-stu-id="ff616-138"><a href="dn350962(v=exchg.10).md">Parameters</a></span></span></td>
<td><span data-ttu-id="ff616-139">Ruft die instanceparameters für diese Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="ff616-139">Gets the InstanceParameters for this instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Öffentliche Eigenschaft" alt="Public property" /></td>
<td><span data-ttu-id="ff616-141"><a href="dn350964(v=exchg.10).md">Termgrbit</a></span><span class="sxs-lookup"><span data-stu-id="ff616-141"><a href="dn350964(v=exchg.10).md">TermGrbit</a></span></span></td>
<td><span data-ttu-id="ff616-142">Ruft das termgrbit für diese-Instanz ab oder legt es fest.</span><span class="sxs-lookup"><span data-stu-id="ff616-142">Gets or sets the TermGrbit for this instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff616-143">Oben</span><span class="sxs-lookup"><span data-stu-id="ff616-143">Top</span></span>

## <a name="methods"></a><span data-ttu-id="ff616-144">Methoden</span><span class="sxs-lookup"><span data-stu-id="ff616-144">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ff616-145">Name</span><span class="sxs-lookup"><span data-stu-id="ff616-145">Name</span></span></th>
<th><span data-ttu-id="ff616-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff616-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-148"><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Schließen</a></span><span class="sxs-lookup"><span data-stu-id="ff616-148"><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Close</a></span></span></td>
<td><span data-ttu-id="ff616-149">(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-149">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-151"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">Gefährousadressf</a></span><span class="sxs-lookup"><span data-stu-id="ff616-151"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">DangerousAddRef</a></span></span></td>
<td><span data-ttu-id="ff616-152">(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-152">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-154"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></span><span class="sxs-lookup"><span data-stu-id="ff616-154"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></span></span></td>
<td><span data-ttu-id="ff616-155">(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-155">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-157"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></span><span class="sxs-lookup"><span data-stu-id="ff616-157"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></span></span></td>
<td><span data-ttu-id="ff616-158">(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-158">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-160"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Verwerfen ()</a></span><span class="sxs-lookup"><span data-stu-id="ff616-160"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose()</a></span></span></td>
<td><span data-ttu-id="ff616-161">(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-161">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="ff616-163"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Verwerfen (Boolean)</a></span><span class="sxs-lookup"><span data-stu-id="ff616-163"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="ff616-164">(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-164">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-166"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Ist gleich</a></span><span class="sxs-lookup"><span data-stu-id="ff616-166"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="ff616-167">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="ff616-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="ff616-169"><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="ff616-169"><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="ff616-170">(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-170">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-172"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="ff616-172"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="ff616-173">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="ff616-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-175"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="ff616-175"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="ff616-176">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="ff616-176">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-178"><a href="dn350932(v=exchg.10).md">Init ()</a></span><span class="sxs-lookup"><span data-stu-id="ff616-178"><a href="dn350932(v=exchg.10).md">Init()</a></span></span></td>
<td><span data-ttu-id="ff616-179">Initialisieren Sie die JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="ff616-179">Initialize the JET_INSTANCE.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-181"><a href="dn350954(v=exchg.10).md">Init (initgrbit)</a></span><span class="sxs-lookup"><span data-stu-id="ff616-181"><a href="dn350954(v=exchg.10).md">Init(InitGrbit)</a></span></span></td>
<td><span data-ttu-id="ff616-182">Initialisieren Sie die JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="ff616-182">Initialize the JET_INSTANCE.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-184"><a href="dn350934(v=exchg.10).md">Init (JET_RSTINFO, initgrbit)</a></span><span class="sxs-lookup"><span data-stu-id="ff616-184"><a href="dn350934(v=exchg.10).md">Init(JET_RSTINFO, InitGrbit)</a></span></span></td>
<td><span data-ttu-id="ff616-185">Initialisieren Sie die JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="ff616-185">Initialize the JET_INSTANCE.</span></span> <span data-ttu-id="ff616-186">Diese API erfordert mindestens die Vista-Version von ESENT.</span><span class="sxs-lookup"><span data-stu-id="ff616-186">This API requires at least the Vista version of ESENT.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="ff616-188"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">Mitgliedglieder Klon</a></span><span class="sxs-lookup"><span data-stu-id="ff616-188"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="ff616-189">(Von <a href="/dotnet/api/system.object">Objekt</a>geerbt.)</span><span class="sxs-lookup"><span data-stu-id="ff616-189">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="ff616-191"><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></span><span class="sxs-lookup"><span data-stu-id="ff616-191"><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></span></span></td>
<td><span data-ttu-id="ff616-192">Gibt das Handle für diese Instanz frei.</span><span class="sxs-lookup"><span data-stu-id="ff616-192">Release the handle for this instance.</span></span> <span data-ttu-id="ff616-193">(Überschreibt <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle. ReleaseHandle ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-193">(Overrides <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle.ReleaseHandle()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Geschützte Methode" alt="Protected method" /></td>
<td><span data-ttu-id="ff616-195"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">"Ziel"</a></span><span class="sxs-lookup"><span data-stu-id="ff616-195"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">SetHandle</a></span></span></td>
<td><span data-ttu-id="ff616-196">(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-196">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-198"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">"" Ist "".</a></span><span class="sxs-lookup"><span data-stu-id="ff616-198"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">SetHandleAsInvalid</a></span></span></td>
<td><span data-ttu-id="ff616-199">(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-199">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-201"><a href="dn350935(v=exchg.10).md">Begriff</a></span><span class="sxs-lookup"><span data-stu-id="ff616-201"><a href="dn350935(v=exchg.10).md">Term</a></span></span></td>
<td><span data-ttu-id="ff616-202">Beenden Sie die JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="ff616-202">Terminate the JET_INSTANCE.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /></td>
<td><span data-ttu-id="ff616-204"><a href="dn350960(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="ff616-204"><a href="dn350960(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="ff616-205">Gibt eine <a href="/dotnet/api/system.string">Zeichenfolge</a> zurück, die die aktuelle <a href="dn350923(v=exchg.10).md">Instanz</a>darstellt.</span><span class="sxs-lookup"><span data-stu-id="ff616-205">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn350923(v=exchg.10).md">Instance</a>.</span></span> <span data-ttu-id="ff616-206">(Überschreibt <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.-Zeichenfolge ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-206">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff616-207">Oben</span><span class="sxs-lookup"><span data-stu-id="ff616-207">Top</span></span>

## <a name="operators"></a><span data-ttu-id="ff616-208">Operatoren</span><span class="sxs-lookup"><span data-stu-id="ff616-208">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ff616-209">Name</span><span class="sxs-lookup"><span data-stu-id="ff616-209">Name</span></span></th>
<th><span data-ttu-id="ff616-210">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff616-210">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Öffentlicher Operator" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="ff616-213"><a href="dn350950(v=exchg.10).md">Implizit (zu JET_INSTANCE Instanz)</a></span><span class="sxs-lookup"><span data-stu-id="ff616-213"><a href="dn350950(v=exchg.10).md">Implicit(Instance to JET_INSTANCE)</a></span></span></td>
<td><span data-ttu-id="ff616-214">Bereitstellen der impliziten Konvertierung eines Instanzobjekts in eine JET_INSTANCE Struktur.</span><span class="sxs-lookup"><span data-stu-id="ff616-214">Provide implicit conversion of an Instance object to a JET_INSTANCE structure.</span></span> <span data-ttu-id="ff616-215">Dies geschieht, damit eine-Instanz überall dort verwendet werden kann, wo eine JET_INSTANCE erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ff616-215">This is done so that an Instance can be used anywhere a JET_INSTANCE is required.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff616-216">Oben</span><span class="sxs-lookup"><span data-stu-id="ff616-216">Top</span></span>

## <a name="fields"></a><span data-ttu-id="ff616-217">Felder</span><span class="sxs-lookup"><span data-stu-id="ff616-217">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ff616-218">Name</span><span class="sxs-lookup"><span data-stu-id="ff616-218">Name</span></span></th>
<th><span data-ttu-id="ff616-219">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff616-219">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.protfield(exchg.10).gif" title="Geschütztes Feld" alt="Protected field" /></td>
<td><span data-ttu-id="ff616-221"><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">bewältigen</a></span><span class="sxs-lookup"><span data-stu-id="ff616-221"><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">handle</a></span></span></td>
<td><span data-ttu-id="ff616-222">(Geerbt von <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="ff616-222">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff616-223">Oben</span><span class="sxs-lookup"><span data-stu-id="ff616-223">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ff616-224">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff616-224">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ff616-225">Referenz</span><span class="sxs-lookup"><span data-stu-id="ff616-225">Reference</span></span>

[<span data-ttu-id="ff616-226">Instanzklasse</span><span class="sxs-lookup"><span data-stu-id="ff616-226">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="ff616-227">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ff616-227">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

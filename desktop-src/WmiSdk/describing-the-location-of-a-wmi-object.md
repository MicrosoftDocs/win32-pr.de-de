---
description: Konzeptionell vergleichbar mit einem Uniform Resource Locator (URL) ist ein WMI-Objekt Pfad eine Zeichenfolge, die den Namespace auf einem Server, eine Klasse innerhalb eines Namespace oder Instanzen einer Klasse eindeutig identifiziert.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Beschreiben des Speicher Orts eines WMI-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345872"
---
# <a name="describing-the-location-of-a-wmi-object"></a><span data-ttu-id="8e851-103">Beschreiben des Speicher Orts eines WMI-Objekts</span><span class="sxs-lookup"><span data-stu-id="8e851-103">Describing the Location of a WMI Object</span></span>

<span data-ttu-id="8e851-104">Konzeptionell vergleichbar mit einem Uniform Resource Locator (URL) ist ein WMI-Objekt Pfad eine Zeichenfolge, die den Namespace auf einem Server, eine Klasse innerhalb eines Namespace oder Instanzen einer Klasse eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8e851-104">Conceptually similar to a Uniform Resource Locator (URL), a WMI object path is a string that uniquely identifies the namespace on a server, a class within a namespace, or instances of a class.</span></span> <span data-ttu-id="8e851-105">Ein Objekt Pfad ist hierarchisch und enthält mehrere Elemente, die den Speicherort des fraglichen Objekts beschreiben.</span><span class="sxs-lookup"><span data-stu-id="8e851-105">An object path is hierarchical, and contains several elements that describe the location of the object in question.</span></span> <span data-ttu-id="8e851-106">Wie Dateipfade können auch WMI-Objekt Pfade als relativer Pfad beschrieben oder als relativer Pfad angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e851-106">Like file paths, WMI object paths can be described in full or specified as a relative path.</span></span>

<span data-ttu-id="8e851-107">Der Namespace eines WMI-Objekts wird auf der WMI-Referenzseite aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e851-107">The namespace of a WMI object is listed on the WMI reference page.</span></span> <span data-ttu-id="8e851-108">Der Speicherort der meisten Klassen, die von den [cimwin32-WMI-Anbietern](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) unterstützt werden, befindet sich z \\ . b. im root cimv2- \\ Namespace.</span><span class="sxs-lookup"><span data-stu-id="8e851-108">For example, the location of most of the classes supported by the [CIMWin32 WMI Providers](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) are located in the \\root\\cimv2 namespace.</span></span> <span data-ttu-id="8e851-109">Der folgende PowerShell-Code beschreibt einen Rückruf zum Abrufen des [**Win32- \_ Computersystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) -Objekts auf dem lokalen Computer:</span><span class="sxs-lookup"><span data-stu-id="8e851-109">The following PowerShell code describes a call to retrieve the [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) object on your local machine:</span></span>

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

<span data-ttu-id="8e851-110">Alternativ kann eine bestimmte Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) den folgenden Pfad aus der Eigenschaft " [**errbemubject. Path \_**](swbemobject-path-.md) " aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8e851-110">Alternately, a specific instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) may have the following path from the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

<span data-ttu-id="8e851-111">Das folgende Beispiel zeigt den relativen Pfad zu dieser Instanz, wie durch Anzeigen der [**RelPath**](swbemobjectpath-relpath.md) -Eigenschaft des " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts angezeigt, das durch den Aufrufen von " [**errbemubject. Path \_**](swbemobject-path-.md)" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8e851-111">The following example shows the relative path to this instance, as seen by displaying the [**Relpath**](swbemobjectpath-relpath.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the call to [**SWbemObject.Path\_**](swbemobject-path-.md).</span></span>

`Win32_LogicalDisk.DeviceID="A:"`

<span data-ttu-id="8e851-112">Beachten Sie, dass **DeviceID** die Schlüsseleigenschaft der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="8e851-112">Note that **DeviceID** is the key property of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

## <a name="c"></a><span data-ttu-id="8e851-113">C++</span><span class="sxs-lookup"><span data-stu-id="8e851-113">C++</span></span>

<span data-ttu-id="8e851-114">In der folgenden Tabelle sind die Objekt Pfad Typen und die zugehörigen Methoden aufgelistet, die Objekt Pfade erfordern.</span><span class="sxs-lookup"><span data-stu-id="8e851-114">The following table lists object path types and the associated methods that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8e851-115">Objekt Pfadtyp</span><span class="sxs-lookup"><span data-stu-id="8e851-115">Object path type</span></span></th>
<th><span data-ttu-id="8e851-116">Methode</span><span class="sxs-lookup"><span data-stu-id="8e851-116">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e851-117"><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></span><span class="sxs-lookup"><span data-stu-id="8e851-117"><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></span></span></td>
<td><dl><span data-ttu-id="8e851-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices:: OpenNamespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e851-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices::OpenNamespace</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e851-119"><a href="describing-a-class-object-path.md">Klasse</a></span><span class="sxs-lookup"><span data-stu-id="8e851-119"><a href="describing-a-class-object-path.md">Class</a></span></span></td>
<td><dl><span data-ttu-id="8e851-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices:: ExecMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e851-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices::ExecMethod</strong></a></span></span><br />
<span data-ttu-id="8e851-121">[<strong>IWbemServices:: ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span><span class="sxs-lookup"><span data-stu-id="8e851-121">[<strong>IWbemServices::ExecMethodAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e851-122"><a href="describing-a-class-object-path.md">Klasse</a> oder <a href="describing-an-instance-object-path.md">Instanz</a></span><span class="sxs-lookup"><span data-stu-id="8e851-122"><a href="describing-a-class-object-path.md">Class</a> or <a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="8e851-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices:: GetObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e851-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices::GetObject</strong></a></span></span><br />
<span data-ttu-id="8e851-124">[<strong>IWbemServices:: GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span><span class="sxs-lookup"><span data-stu-id="8e851-124">[<strong>IWbemServices::GetObjectAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e851-125"><a href="describing-an-instance-object-path.md">Instanz</a></span><span class="sxs-lookup"><span data-stu-id="8e851-125"><a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="8e851-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::D eleteingestance</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e851-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::DeleteInstance</strong></a></span></span><br />
<span data-ttu-id="8e851-127">[<strong>IWbemServices::D eleteingestanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span><span class="sxs-lookup"><span data-stu-id="8e851-127">[<strong>IWbemServices::DeleteInstanceAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a><span data-ttu-id="8e851-128">Skript</span><span class="sxs-lookup"><span data-stu-id="8e851-128">Script</span></span>

<span data-ttu-id="8e851-129">Objekt Pfade können auf verschiedene Arten erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="8e851-129">Object paths can be constructed in several ways:</span></span>

-   <span data-ttu-id="8e851-130">Rufen Sie die-Eigenschaft einer Methode ab, die ein Objekt vom Typ" [**errbemjectpath**](swbemobjectpath.md) " zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8e851-130">Retrieve the property of a method that returns an [**SWbemObjectPath**](swbemobjectpath.md) object.</span></span>
-   <span data-ttu-id="8e851-131">Rufen Sie die Eigenschaft " [**errbemubject. Path \_**](swbemobject-path-.md) " ab.</span><span class="sxs-lookup"><span data-stu-id="8e851-131">Retrieve the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>
-   <span data-ttu-id="8e851-132">Erstellen Sie eine Zeichen folgen Variable, die den Objekt Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="8e851-132">Create a string variable that contains the object path.</span></span>

<span data-ttu-id="8e851-133">In der folgenden Tabelle werden die Skript Objekte aufgelistet, die Objekt Pfade erfordern.</span><span class="sxs-lookup"><span data-stu-id="8e851-133">The following table lists the scripting objects that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8e851-134">Skript Objekt</span><span class="sxs-lookup"><span data-stu-id="8e851-134">Scripting object</span></span></th>
<th><span data-ttu-id="8e851-135">Methode</span><span class="sxs-lookup"><span data-stu-id="8e851-135">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e851-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e851-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span></span></td>
<td><dl><span data-ttu-id="8e851-137"><a href="swbemservices-associatorsof.md"><strong>Assoziatorsof</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e851-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span></span><br />
<span data-ttu-id="8e851-138">[<strong>Associatorsofasync</strong>] (SWbemServices-associatorsofasync.MD)</span><span class="sxs-lookup"><span data-stu-id="8e851-138">[<strong>AssociatorsOfAsync</strong>](swbemservices-associatorsofasync.md)</span></span><br />
<span data-ttu-id="8e851-139">[<strong>Löschen</strong>] (SWbemServices-DELETE.MD)</span><span class="sxs-lookup"><span data-stu-id="8e851-139">[<strong>Delete</strong>](swbemservices-delete.md)</span></span><br />
<span data-ttu-id="8e851-140">[<strong>Deleteasync</strong>] (SWbemServices-deleteasync.MD)</span><span class="sxs-lookup"><span data-stu-id="8e851-140">[<strong>DeleteAsync</strong>](swbemservices-deleteasync.md)</span></span><br />
<span data-ttu-id="8e851-141">[<strong>ExecMethod</strong>] (SWbemServices-ExecMethod.MD)</span><span class="sxs-lookup"><span data-stu-id="8e851-141">[<strong>ExecMethod</strong>](swbemservices-execmethod.md)</span></span><br />
<span data-ttu-id="8e851-142">[<strong>ExecMethodAsync</strong>] (SWbemServices-ExecMethodAsync.MD)</span><span class="sxs-lookup"><span data-stu-id="8e851-142">[<strong>ExecMethodAsync</strong>](swbemservices-execmethodasync.md)</span></span><br />
<span data-ttu-id="8e851-143">[<strong>Get</strong>] (SWbemServices-Get.MD)</span><span class="sxs-lookup"><span data-stu-id="8e851-143">[<strong>Get</strong>](swbemservices-get.md)</span></span><br />
<span data-ttu-id="8e851-144">[<strong>Getasync</strong>] (SWbemServices-getasync.MD)</span><span class="sxs-lookup"><span data-stu-id="8e851-144">[<strong>GetAsync</strong>](swbemservices-getasync.md)</span></span><br />
<span data-ttu-id="8e851-145">[<strong>Referencesto</strong>] (SWbemServices-referencesto.MD)</span><span class="sxs-lookup"><span data-stu-id="8e851-145">[<strong>ReferencesTo</strong>](swbemservices-referencesto.md)</span></span><br />
<span data-ttu-id="8e851-146">[<strong>Referencestoasync</strong>] (SWbemServices-referencestoasync.MD)</span><span class="sxs-lookup"><span data-stu-id="8e851-146">[<strong>ReferencesToAsync</strong>](swbemservices-referencestoasync.md)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e851-147"><a href="swbemobjectset.md"><strong>Austauschen von "errbemubjectset"</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e851-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span></span></td>
<td><dl><span data-ttu-id="8e851-148"><a href="swbemobjectset-item.md"><strong>Element</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e851-148"><a href="swbemobjectset-item.md"><strong>Item</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 

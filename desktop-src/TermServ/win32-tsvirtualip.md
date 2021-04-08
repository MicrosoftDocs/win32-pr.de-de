---
title: Win32_TSVirtualIP-Klasse
description: Definiert die IP-Virtualisierungseinstellungen (Internet Protocol) für einen Remotedesktop-Sitzungshost Server (RD-Sitzungshost).
ms.assetid: c37d572c-f6db-438b-8290-006a623c6593
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualIP-Klasse Remotedesktopdienste
- Win32_TSVirtualIP Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP
- Win32_TSVirtualIP.Caption
- Win32_TSVirtualIP.Description
- Win32_TSVirtualIP.InstallDate
- Win32_TSVirtualIP.Name
- Win32_TSVirtualIP.Status
- Win32_TSVirtualIP.VirtualIPActive
- Win32_TSVirtualIP.PolicySourceVirtualIPActive
- Win32_TSVirtualIP.VirtualIPMode
- Win32_TSVirtualIP.PolicySourceVirtualIPMode
- Win32_TSVirtualIP.ProgramList
- Win32_TSVirtualIP.PolicySourceProgramList
- Win32_TSVirtualIP.NetworkAdapterDescription
- Win32_TSVirtualIP.NetworkAdapterMacAddress
- Win32_TSVirtualIP.PolicySourceNetworkAdapter
- Win32_TSVirtualIP.NetworkAdapterDescriptionList
- Win32_TSVirtualIP.NetworkAdapterMacList
- Win32_TSVirtualIP.VirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f87db04d61dda0c6034b536544362ec09e0aaa66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740184"
---
# <a name="win32_tsvirtualip-class"></a><span data-ttu-id="72004-105">Win32- \_ Klasse "tvirtualip"</span><span class="sxs-lookup"><span data-stu-id="72004-105">Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="72004-106">Definiert die IP-Virtualisierungseinstellungen (Internet Protocol) für einen Remotedesktop-Sitzungshost Server (RD-Sitzungshost).</span><span class="sxs-lookup"><span data-stu-id="72004-106">Defines Internet protocol (IP) virtualization settings for a Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="72004-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="72004-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72004-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="72004-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSVIRTUALIP_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIP : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   VirtualIPActive;
  uint32   PolicySourceVirtualIPActive;
  uint32   VirtualIPMode;
  uint32   PolicySourceVirtualIPMode;
  string   ProgramList[];
  uint32   PolicySourceProgramList;
  string   NetworkAdapterDescription;
  string   NetworkAdapterMacAddress;
  uint32   PolicySourceNetworkAdapter;
  string   NetworkAdapterDescriptionList[];
  string   NetworkAdapterMacList[];
  uint32   VirtualizeLoopbackAddressesEnabled;
};
```

## <a name="members"></a><span data-ttu-id="72004-109">Member</span><span class="sxs-lookup"><span data-stu-id="72004-109">Members</span></span>

<span data-ttu-id="72004-110">Die Win32-Klasse " **\_ tvirtualip** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="72004-110">The **Win32\_TSVirtualIP** class has these types of members:</span></span>

-   [<span data-ttu-id="72004-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="72004-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="72004-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="72004-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="72004-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="72004-113">Methods</span></span>

<span data-ttu-id="72004-114">Die Win32-Klasse " **\_ tvirtualip** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="72004-114">The **Win32\_TSVirtualIP** class has these methods.</span></span>



| <span data-ttu-id="72004-115">Methode</span><span class="sxs-lookup"><span data-stu-id="72004-115">Method</span></span>                                                                                                   | <span data-ttu-id="72004-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72004-116">Description</span></span>                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72004-117">**Addprogram**</span><span class="sxs-lookup"><span data-stu-id="72004-117">**AddProgram**</span></span>](addprogram-win32-tsvirtualip.md)                                                       | <span data-ttu-id="72004-118">Fügt der Liste der Programme, die die IP-Virtualisierung verwenden, ein Programm hinzu.</span><span class="sxs-lookup"><span data-stu-id="72004-118">Adds a program to the list of programs that use IP virtualization.</span></span><br/>                                                                                                |
| [<span data-ttu-id="72004-119">**Removeprogram**</span><span class="sxs-lookup"><span data-stu-id="72004-119">**RemoveProgram**</span></span>](removeprogram-win32-tsvirtualip.md)                                                 | <span data-ttu-id="72004-120">Entfernt ein Programm aus der Liste der Programme, die die IP-Virtualisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="72004-120">Removes a program from the list of programs that use IP virtualization.</span></span><br/>                                                                                           |
| [<span data-ttu-id="72004-121">**Selectnetworkadapter**</span><span class="sxs-lookup"><span data-stu-id="72004-121">**SelectNetworkAdapter**</span></span>](selectnetworkadapter-win32-tsvirtualip.md)                                   | <span data-ttu-id="72004-122">Legt die Mac-Adresse des Netzwerkadapters fest, der für die IP-Virtualisierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72004-122">Sets the MAC address of the network adapter to use for IP virtualization.</span></span><br/>                                                                                         |
| [<span data-ttu-id="72004-123">**Setprogramlist**</span><span class="sxs-lookup"><span data-stu-id="72004-123">**SetProgramList**</span></span>](setprogramlist-win32-tsvirtualip.md)                                               | <span data-ttu-id="72004-124">Überschreibt die Liste der Programme, die die IP-Virtualisierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="72004-124">Overwrites the list of programs that use IP virtualization.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="72004-125">**Setvirtualipactive**</span><span class="sxs-lookup"><span data-stu-id="72004-125">**SetVirtualIPActive**</span></span>](setvirtualipactive-win32-tsvirtualip.md)                                       | <span data-ttu-id="72004-126">Legt den Wert der **virtualipactive** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="72004-126">Sets the **VirtualIPActive** property value.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="72004-127">**Setvirtualipmode**</span><span class="sxs-lookup"><span data-stu-id="72004-127">**SetVirtualIPMode**</span></span>](setvirtualipmode-win32-tsvirtualip.md)                                           | <span data-ttu-id="72004-128">Legt den Wert der **virtualipmode** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="72004-128">Sets the **VirtualIPMode** property value.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="72004-129">**Setvirtualizeloopbackaddressesaktivierte**</span><span class="sxs-lookup"><span data-stu-id="72004-129">**SetVirtualizeLoopbackAddressesEnabled**</span></span>](setvirtualizeloopbackaddressesenabled-win32-tsvirtualip.md) | <span data-ttu-id="72004-130">Legt den Wert der **virtualizeloopbackaddressesaktivierten** Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="72004-130">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span><br/> <span data-ttu-id="72004-131">**Windows Server 2008 R2:** Diese Methode ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="72004-131">**Windows Server 2008 R2:** This method is not available prior to Windows Server 2012.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="72004-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="72004-132">Properties</span></span>

<span data-ttu-id="72004-133">Die Win32-Klasse " **\_ tvirtualip** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="72004-133">The **Win32\_TSVirtualIP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72004-134">**Caption**</span><span class="sxs-lookup"><span data-stu-id="72004-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="72004-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72004-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72004-137">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="72004-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="72004-138">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="72004-138">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="72004-139">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="72004-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72004-140">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="72004-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="72004-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72004-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-143">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="72004-143">Description of the object.</span></span>

<span data-ttu-id="72004-144">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="72004-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72004-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="72004-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-146">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="72004-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="72004-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72004-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="72004-148">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="72004-149">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="72004-149">The date the object was installed.</span></span> <span data-ttu-id="72004-150">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="72004-150">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="72004-151">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="72004-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72004-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="72004-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="72004-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72004-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-155">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="72004-155">The name of the object.</span></span>

<span data-ttu-id="72004-156">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="72004-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72004-157">**Networkadapterdescription**</span><span class="sxs-lookup"><span data-stu-id="72004-157">**NetworkAdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="72004-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72004-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-160">Die Beschreibung für den Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="72004-160">The description for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="72004-161">**Networkadapterdescriptionlist**</span><span class="sxs-lookup"><span data-stu-id="72004-161">**NetworkAdapterDescriptionList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-162">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="72004-162">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="72004-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-164">Die Liste der Beschreibungen der verfügbaren physischen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="72004-164">The list of descriptions of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="72004-165">**Networkadaptermacaddress**</span><span class="sxs-lookup"><span data-stu-id="72004-165">**NetworkAdapterMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="72004-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72004-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-168">Die Mac-Adresse des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="72004-168">The MAC address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="72004-169">**Networkadaptermaclist**</span><span class="sxs-lookup"><span data-stu-id="72004-169">**NetworkAdapterMacList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-170">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="72004-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="72004-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-172">Die Liste der Mac-Adressen der verfügbaren physischen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="72004-172">The list of MAC addresses of the available physical network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="72004-173">**Policysourcenetworkadapter**</span><span class="sxs-lookup"><span data-stu-id="72004-173">**PolicySourceNetworkAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-174">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72004-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72004-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-176">Gibt an, ob der Netzwerkadapter vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="72004-176">Indicates whether the network adapter is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="72004-177">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="72004-177">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="72004-178">Server</span><span class="sxs-lookup"><span data-stu-id="72004-178">Server</span></span>

</dd> <dt>

<span data-ttu-id="72004-179">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="72004-179">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="72004-180">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="72004-180">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="72004-181">**Policysourceprogramlist**</span><span class="sxs-lookup"><span data-stu-id="72004-181">**PolicySourceProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-182">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72004-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72004-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-184">Gibt an, ob die **Programmlist** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="72004-184">Indicates whether the **ProgramList** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="72004-185">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="72004-185">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="72004-186">Server</span><span class="sxs-lookup"><span data-stu-id="72004-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="72004-187">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="72004-187">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="72004-188">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="72004-188">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="72004-189">**Policysourcevirtualipactive**</span><span class="sxs-lookup"><span data-stu-id="72004-189">**PolicySourceVirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-190">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72004-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72004-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-192">Gibt an, ob die **virtualipactive** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="72004-192">Indicates if the **VirtualIPActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="72004-193">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="72004-193">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="72004-194">Server</span><span class="sxs-lookup"><span data-stu-id="72004-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="72004-195">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="72004-195">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="72004-196">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="72004-196">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="72004-197">**Policysourcevirtualipmode**</span><span class="sxs-lookup"><span data-stu-id="72004-197">**PolicySourceVirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-198">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72004-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72004-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-200">Gibt an, ob die **virtualipmode** -Eigenschaft vom Server oder von der Gruppenrichtlinie konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="72004-200">Indicates if the **VirtualIPMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="72004-201">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="72004-201">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="72004-202">Server</span><span class="sxs-lookup"><span data-stu-id="72004-202">Server</span></span>

</dd> <dt>

<span data-ttu-id="72004-203">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="72004-203">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="72004-204">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="72004-204">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="72004-205">**Programmliste**</span><span class="sxs-lookup"><span data-stu-id="72004-205">**ProgramList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-206">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="72004-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="72004-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-208">Gibt die Programme an, die für die Verwendung der IP-Virtualisierung konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="72004-208">Specifies the programs that are configured to use IP virtualization.</span></span> <span data-ttu-id="72004-209">Dabei kann es sich um einen Programmnamen oder den vollständigen Pfad handelt.</span><span class="sxs-lookup"><span data-stu-id="72004-209">This may a program name or the full path.</span></span>

</dd> <dt>

<span data-ttu-id="72004-210">**Status**</span><span class="sxs-lookup"><span data-stu-id="72004-210">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-211">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="72004-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72004-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72004-213">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="72004-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="72004-214">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="72004-214">Current status of the object.</span></span> <span data-ttu-id="72004-215">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="72004-215">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="72004-216">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="72004-216">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="72004-217">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="72004-217">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="72004-218">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="72004-218">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="72004-219">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="72004-219">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="72004-220">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="72004-220">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="72004-221">("OK")</span><span class="sxs-lookup"><span data-stu-id="72004-221">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="72004-222">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="72004-222">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="72004-223">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="72004-223">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="72004-224">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="72004-224">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="72004-225">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="72004-225">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="72004-226">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="72004-226">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="72004-227">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="72004-227">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="72004-228">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="72004-228">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="72004-229">**Virtualipactive**</span><span class="sxs-lookup"><span data-stu-id="72004-229">**VirtualIPActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-230">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72004-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72004-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72004-232">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="72004-232">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="72004-233">Gibt an, ob die IP-Virtualisierung auf dem Server aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="72004-233">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="72004-234">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="72004-234">This can be one of the following values.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="72004-235"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="72004-235"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="72004-236">Die IP-Virtualisierung ist nicht aktiv.</span><span class="sxs-lookup"><span data-stu-id="72004-236">IP virtualization is not active.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="72004-237"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="72004-237"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="72004-238">Die IP-Virtualisierung ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="72004-238">IP virtualization is active.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="72004-239">**Virtualisierungsmodus**</span><span class="sxs-lookup"><span data-stu-id="72004-239">**VirtualIPMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-240">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72004-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72004-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-242">Gibt an, welcher IP-Virtualisierungsmodus auf dem Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72004-242">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="72004-243">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="72004-243">This can be one of the following values.</span></span>

<dt>

<span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>

<span data-ttu-id="72004-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Pro Sitzung** (0)</span><span class="sxs-lookup"><span data-stu-id="72004-244"><span id="Per-Session"></span><span id="per-session"></span><span id="PER-SESSION"></span>**Per-Session** (0)</span></span>


</dt> <dd>

<span data-ttu-id="72004-245">Der IP-Virtualisierungsmodus ist pro Sitzung.</span><span class="sxs-lookup"><span data-stu-id="72004-245">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>

<span data-ttu-id="72004-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Pro Programm** (1)</span><span class="sxs-lookup"><span data-stu-id="72004-246"><span id="Per-Program"></span><span id="per-program"></span><span id="PER-PROGRAM"></span>**Per-Program** (1)</span></span>


</dt> <dd>

<span data-ttu-id="72004-247">Der IP-Virtualisierungsmodus ist pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="72004-247">The IP virtualization mode is per-user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="72004-248">**Virtualizeloopbackaddressesaktivierte**</span><span class="sxs-lookup"><span data-stu-id="72004-248">**VirtualizeLoopbackAddressesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72004-249">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72004-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72004-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="72004-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72004-251">Gibt an, ob Loopback adressvirtualisierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="72004-251">Specifies whether loopback address virtualization is enabled.</span></span>

<span data-ttu-id="72004-252">**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="72004-252">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="72004-253"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="72004-253"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="72004-254">Nicht aktiviert</span><span class="sxs-lookup"><span data-stu-id="72004-254">Not enabled</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="72004-255"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="72004-255"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="72004-256">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="72004-256">Enabled</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72004-257">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72004-257">Remarks</span></span>

<span data-ttu-id="72004-258">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="72004-258">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="72004-259">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="72004-259">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="72004-260">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72004-260">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="72004-261">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="72004-261">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="72004-262">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72004-262">Requirements</span></span>



| <span data-ttu-id="72004-263">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72004-263">Requirement</span></span> | <span data-ttu-id="72004-264">Wert</span><span class="sxs-lookup"><span data-stu-id="72004-264">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72004-265">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72004-265">Minimum supported client</span></span><br/> | <span data-ttu-id="72004-266">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="72004-266">None supported</span></span><br/>                                                               |
| <span data-ttu-id="72004-267">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72004-267">Minimum supported server</span></span><br/> | <span data-ttu-id="72004-268">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72004-268">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="72004-269">Namespace</span><span class="sxs-lookup"><span data-stu-id="72004-269">Namespace</span></span><br/>                | <span data-ttu-id="72004-270">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="72004-270">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="72004-271">MOF</span><span class="sxs-lookup"><span data-stu-id="72004-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72004-272"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="72004-272"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="72004-273">DLL</span><span class="sxs-lookup"><span data-stu-id="72004-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72004-274"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72004-274"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 


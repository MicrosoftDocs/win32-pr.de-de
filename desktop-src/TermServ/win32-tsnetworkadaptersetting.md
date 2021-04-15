---
title: Win32_TSNetworkAdapterSetting-Klasse
description: Definiert verschiedene Konfigurationseinstellungen für die Win32- \_ Terminal Klasse einschließlich Eigenschaften im Zusammenhang mit dem Netzwerkadapter und die maximal zulässige Anzahl von Verbindungen.
ms.assetid: b8a757e6-801b-4349-902e-76596b06df1f
ms.tgt_platform: multiple
keywords:
- Win32_TSNetworkAdapterSetting-Klasse Remotedesktopdienste
- Win32_TSNetworkAdapterSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting.Caption
- Win32_TSNetworkAdapterSetting.Description
- Win32_TSNetworkAdapterSetting.InstallDate
- Win32_TSNetworkAdapterSetting.Name
- Win32_TSNetworkAdapterSetting.Status
- Win32_TSNetworkAdapterSetting.TerminalName
- Win32_TSNetworkAdapterSetting.DeviceIDList
- Win32_TSNetworkAdapterSetting.MaximumConnections
- Win32_TSNetworkAdapterSetting.NetworkAdapterID
- Win32_TSNetworkAdapterSetting.NetworkAdapterLanaID
- Win32_TSNetworkAdapterSetting.NetworkAdapterList
- Win32_TSNetworkAdapterSetting.NetworkAdapterName
- Win32_TSNetworkAdapterSetting.PolicySourceMaximumConnections
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f2f2f1ac7d6bf4b1fd3fb5f5a92fc4fd5260a92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477700"
---
# <a name="win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="b89f0-105">Win32-Klasse "t \_ Network adaptersetting"</span><span class="sxs-lookup"><span data-stu-id="b89f0-105">Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="b89f0-106">Die Win32-Klasse "t- **\_ networkadaptersetting** " definiert verschiedene Konfigurationseinstellungen für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse, einschließlich Eigenschaften für den Netzwerkadapter und die maximal zulässige Anzahl von Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="b89f0-106">The **Win32\_TSNetworkAdapterSetting** WMI class defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

<span data-ttu-id="b89f0-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="b89f0-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="b89f0-108">Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="b89f0-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="b89f0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b89f0-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSNETWORKADAPTERSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   DeviceIDList[];
  uint32   MaximumConnections;
  string   NetworkAdapterID;
  uint32   NetworkAdapterLanaID;
  string   NetworkAdapterList[];
  string   NetworkAdapterName;
  uint32   PolicySourceMaximumConnections;
};
```

## <a name="members"></a><span data-ttu-id="b89f0-110">Member</span><span class="sxs-lookup"><span data-stu-id="b89f0-110">Members</span></span>

<span data-ttu-id="b89f0-111">Die Win32-Klasse "t **\_ Network adaptersetting** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b89f0-111">The **Win32\_TSNetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="b89f0-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="b89f0-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b89f0-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b89f0-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b89f0-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="b89f0-114">Methods</span></span>

<span data-ttu-id="b89f0-115">Die Win32-Klasse " **\_ znetworkadaptersetting** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b89f0-115">The **Win32\_TSNetworkAdapterSetting** class has these methods.</span></span>



| <span data-ttu-id="b89f0-116">Methode</span><span class="sxs-lookup"><span data-stu-id="b89f0-116">Method</span></span>                                                                                     | <span data-ttu-id="b89f0-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b89f0-117">Description</span></span>                                                                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b89f0-118">**Selectallnetworkadapters**</span><span class="sxs-lookup"><span data-stu-id="b89f0-118">**SelectAllNetworkAdapters**</span></span>](win32-tsnetworkadaptersetting-selectallnetworkadapters.md) | <span data-ttu-id="b89f0-119">Wählt alle Netzwerkadapter aus.</span><span class="sxs-lookup"><span data-stu-id="b89f0-119">Selects all network adapters.</span></span><br/>                                                                 |
| [<span data-ttu-id="b89f0-120">**Selectnetworkadapterip**</span><span class="sxs-lookup"><span data-stu-id="b89f0-120">**SelectNetworkAdapterIP**</span></span>](win32-tsnetworkadaptersetting-selectnetworkadapterip.md)     | <span data-ttu-id="b89f0-121">Wählt einen Netzwerkadapter auf der Grundlage der IP-Adresse des Adapters aus.</span><span class="sxs-lookup"><span data-stu-id="b89f0-121">Selects a network adapter based on the adapter's IP address.</span></span><br/>                                  |
| [<span data-ttu-id="b89f0-122">**Setnetworkadapterlanaid**</span><span class="sxs-lookup"><span data-stu-id="b89f0-122">**SetNetworkAdapterLanaID**</span></span>](setnetworkadapterlanaid-win32-tsnetworkadaptersetting.md)   | <span data-ttu-id="b89f0-123">Gibt die NetBIOS-Nummer des lokalen Netzwerkadapters (Lana) des festzulegenden Netzwerkadapters an.</span><span class="sxs-lookup"><span data-stu-id="b89f0-123">Specifies the NetBIOS Local Area Network Adapter (LANA) number of the network adapter to set.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b89f0-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b89f0-124">Properties</span></span>

<span data-ttu-id="b89f0-125">Die Win32-Klasse "t **\_ Network adaptersetting** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b89f0-125">The **Win32\_TSNetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b89f0-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b89f0-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b89f0-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-129">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b89f0-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-130">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b89f0-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="b89f0-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b89f0-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b89f0-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b89f0-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-135">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b89f0-135">Description of the object.</span></span>

<span data-ttu-id="b89f0-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b89f0-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-137">**Geräteliste**</span><span class="sxs-lookup"><span data-stu-id="b89f0-137">**DeviceIDList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-138">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b89f0-138">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-140">Zeichen folgen Array von verfügbaren Geräte-IDs, die in der Reihenfolge der physischen Netzwerkadapter zurückgegeben werden, die im **NetworkAdapterList** -Eigenschafts Array</span><span class="sxs-lookup"><span data-stu-id="b89f0-140">String array of available device IDs returned in the order of physical network adapters returned in the **NetworkAdapterList** property array.</span></span> <span data-ttu-id="b89f0-141">Der Geräte-ID-Wert ist die **DeviceID** -Eigenschaft im [**Win32- \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) .</span><span class="sxs-lookup"><span data-stu-id="b89f0-141">The device ID value is the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b89f0-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-143">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b89f0-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-145">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="b89f0-145">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-146">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b89f0-146">The date the object was installed.</span></span> <span data-ttu-id="b89f0-147">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b89f0-147">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b89f0-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b89f0-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-149">**MaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="b89f0-149">**MaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b89f0-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b89f0-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-152">Die maximal zulässige Anzahl von Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="b89f0-152">The maximum number of connections allowed.</span></span> <span data-ttu-id="b89f0-153">Der Wert **MAXINT** deutet auf eine unbegrenzte Anzahl von Verbindungen hin.</span><span class="sxs-lookup"><span data-stu-id="b89f0-153">The value **MAXINT** denotes an unlimited number of connections.</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-154">**Name**</span><span class="sxs-lookup"><span data-stu-id="b89f0-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b89f0-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-157">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b89f0-157">The name of the object.</span></span>

<span data-ttu-id="b89f0-158">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b89f0-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-159">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="b89f0-159">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b89f0-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-162">Die GUID, die die ID des festzulegenden Netzwerkadapters darstellt.</span><span class="sxs-lookup"><span data-stu-id="b89f0-162">The GUID that represents the ID of the network adapter to set.</span></span> <span data-ttu-id="b89f0-163">Eine **GUID** , die aus allen Nullen besteht, bezeichnet alle Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="b89f0-163">A **GUID** that consists of all zeros denotes all network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-164">**Networkadapterlanaid**</span><span class="sxs-lookup"><span data-stu-id="b89f0-164">**NetworkAdapterLanaID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-165">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b89f0-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-167">NetBIOS-Nummer des lokalen Netzwerkadapters (Lana) des Netzwerkadapters, der zum Identifizieren des dem Terminal zugewiesenen Netzwerkadapters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b89f0-167">NetBIOS Local Area Network Adapter (LANA) number of the network adapter that is used to identify the network adapter assigned to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-168">**Network Adapter List**</span><span class="sxs-lookup"><span data-stu-id="b89f0-168">**NetworkAdapterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-169">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b89f0-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-171">Zeichen folgen Array von verfügbaren physischen Netzwerkadaptern und den entsprechenden Geräte-IDs.</span><span class="sxs-lookup"><span data-stu-id="b89f0-171">String array of available physical network adapters and the corresponding device IDs.</span></span> <span data-ttu-id="b89f0-172">Die Geräte-IDs sind die **DeviceID** -Eigenschaft im [**Win32- \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span><span class="sxs-lookup"><span data-stu-id="b89f0-172">The device IDs are the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-173">**Network Adapter Name**</span><span class="sxs-lookup"><span data-stu-id="b89f0-173">**NetworkAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b89f0-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-176">Die Beschreibung des festzulegenden Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="b89f0-176">Description of the network adapter to set.</span></span> <span data-ttu-id="b89f0-177">Dieser Wert ist in [**Win32 \_ networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span><span class="sxs-lookup"><span data-stu-id="b89f0-177">This value is in [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-178">**PolicySourceMaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="b89f0-178">**PolicySourceMaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-179">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b89f0-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-181">Gibt an, ob die **MaximumConnections** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="b89f0-181">Indicates whether the **MaximumConnections** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="b89f0-182">0</span><span class="sxs-lookup"><span data-stu-id="b89f0-182">0</span></span>
</dt> <dd>

<span data-ttu-id="b89f0-183">Server</span><span class="sxs-lookup"><span data-stu-id="b89f0-183">Server</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-184">1</span><span class="sxs-lookup"><span data-stu-id="b89f0-184">1</span></span>
</dt> <dd>

<span data-ttu-id="b89f0-185">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b89f0-185">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="b89f0-186">2</span><span class="sxs-lookup"><span data-stu-id="b89f0-186">2</span></span>
</dt> <dd>

<span data-ttu-id="b89f0-187">Standard</span><span class="sxs-lookup"><span data-stu-id="b89f0-187">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b89f0-188">**Status**</span><span class="sxs-lookup"><span data-stu-id="b89f0-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b89f0-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-191">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="b89f0-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-192">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b89f0-192">Current status of the object.</span></span> <span data-ttu-id="b89f0-193">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b89f0-193">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b89f0-194">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="b89f0-194">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b89f0-195">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="b89f0-195">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b89f0-196">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b89f0-196">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b89f0-197">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="b89f0-197">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b89f0-198">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b89f0-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="b89f0-199">("OK")</span><span class="sxs-lookup"><span data-stu-id="b89f0-199">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b89f0-200">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="b89f0-200">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b89f0-201">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="b89f0-201">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b89f0-202">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="b89f0-202">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b89f0-203">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b89f0-203">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b89f0-204">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="b89f0-204">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b89f0-205">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="b89f0-205">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b89f0-206">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="b89f0-206">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b89f0-207">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="b89f0-207">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b89f0-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b89f0-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b89f0-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b89f0-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b89f0-210">Der Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="b89f0-210">The name of the terminal.</span></span>

<span data-ttu-id="b89f0-211">Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b89f0-211">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b89f0-212">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b89f0-212">Remarks</span></span>

<span data-ttu-id="b89f0-213">Beachten Sie, dass die der Konsolen Sitzung zugeordneten Winstations nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="b89f0-213">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="b89f0-214">Wenn ein Versuch unternommen wird, indem "Console" als Wert der Terminalname-Eigenschaft angegeben wird, geben die Methoden dieses Objekts **WBEM \_ E \_ nicht \_ unterstützt** zurück.</span><span class="sxs-lookup"><span data-stu-id="b89f0-214">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="b89f0-215">Dieser Fehlercode wird auch zurückgegeben, wenn eine Fenster Station versucht, Methoden dieses Objekts aufzurufen, um die Sicherheitseigenschaften der Konten "LocalSystem", "LocalService" oder "Network Service" hinzuzufügen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b89f0-215">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="b89f0-216">Zum Herstellen einer Verbindung mit dem \\ Namespace "root cimv2 \\ TerminalServices" muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="b89f0-216">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="b89f0-217">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="b89f0-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="b89f0-218">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="b89f0-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="b89f0-219">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b89f0-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="b89f0-220">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b89f0-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b89f0-221">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b89f0-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b89f0-222">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b89f0-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b89f0-223">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b89f0-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b89f0-224">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b89f0-224">Requirements</span></span>



| <span data-ttu-id="b89f0-225">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b89f0-225">Requirement</span></span> | <span data-ttu-id="b89f0-226">Wert</span><span class="sxs-lookup"><span data-stu-id="b89f0-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b89f0-227">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b89f0-227">Minimum supported client</span></span><br/> | <span data-ttu-id="b89f0-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b89f0-228">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b89f0-229">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b89f0-229">Minimum supported server</span></span><br/> | <span data-ttu-id="b89f0-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b89f0-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b89f0-231">Namespace</span><span class="sxs-lookup"><span data-stu-id="b89f0-231">Namespace</span></span><br/>                | <span data-ttu-id="b89f0-232">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b89f0-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b89f0-233">MOF</span><span class="sxs-lookup"><span data-stu-id="b89f0-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b89f0-234"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b89f0-234"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b89f0-235">DLL</span><span class="sxs-lookup"><span data-stu-id="b89f0-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b89f0-236"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b89f0-236"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b89f0-237">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b89f0-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b89f0-238">**Win32- \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="b89f0-238">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)
</dt> <dt>

[<span data-ttu-id="b89f0-239">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="b89f0-239">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
</dt> <dt>

[<span data-ttu-id="b89f0-240">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="b89f0-240">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="b89f0-241">**Win32-Datei "t-Network \_ adapterlistsetting"**</span><span class="sxs-lookup"><span data-stu-id="b89f0-241">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> </dl>

 


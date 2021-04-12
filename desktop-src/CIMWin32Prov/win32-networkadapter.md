---
description: Die Win32- \_ NetworkAdapter-Klasse ist veraltet. Verwenden Sie stattdessen die MSFT \_ netadapter-Klasse. Die Win32 \_ networkadapterwmi-Klasse stellt einen Netzwerkadapter eines Computers dar, auf dem ein Windows-Betriebssystem ausgeführt wird.
ms.assetid: f79cb2a1-a249-479d-a495-37a44fdea995
ms.tgt_platform: multiple
title: Win32_NetworkAdapter-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter
- Win32_NetworkAdapter.Reset
- Win32_NetworkAdapter.SetPowerState
- Win32_NetworkAdapter.AdapterType
- Win32_NetworkAdapter.AdapterTypeID
- Win32_NetworkAdapter.AutoSense
- Win32_NetworkAdapter.Availability
- Win32_NetworkAdapter.Caption
- Win32_NetworkAdapter.ConfigManagerErrorCode
- Win32_NetworkAdapter.ConfigManagerUserConfig
- Win32_NetworkAdapter.CreationClassName
- Win32_NetworkAdapter.Description
- Win32_NetworkAdapter.DeviceID
- Win32_NetworkAdapter.ErrorCleared
- Win32_NetworkAdapter.ErrorDescription
- Win32_NetworkAdapter.GUID
- Win32_NetworkAdapter.Index
- Win32_NetworkAdapter.InstallDate
- Win32_NetworkAdapter.Installed
- Win32_NetworkAdapter.InterfaceIndex
- Win32_NetworkAdapter.LastErrorCode
- Win32_NetworkAdapter.MACAddress
- Win32_NetworkAdapter.Manufacturer
- Win32_NetworkAdapter.MaxNumberControlled
- Win32_NetworkAdapter.MaxSpeed
- Win32_NetworkAdapter.Name
- Win32_NetworkAdapter.NetConnectionID
- Win32_NetworkAdapter.NetConnectionStatus
- Win32_NetworkAdapter.NetEnabled
- Win32_NetworkAdapter.NetworkAddresses
- Win32_NetworkAdapter.PermanentAddress
- Win32_NetworkAdapter.PhysicalAdapter
- Win32_NetworkAdapter.PNPDeviceID
- Win32_NetworkAdapter.PowerManagementCapabilities
- Win32_NetworkAdapter.PowerManagementSupported
- Win32_NetworkAdapter.ProductName
- Win32_NetworkAdapter.ServiceName
- Win32_NetworkAdapter.Speed
- Win32_NetworkAdapter.Status
- Win32_NetworkAdapter.StatusInfo
- Win32_NetworkAdapter.SystemCreationClassName
- Win32_NetworkAdapter.SystemName
- Win32_NetworkAdapter.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 22718802370995cc0515e3f63e731cc86d37eb0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483798"
---
# <a name="win32_networkadapter-class"></a><span data-ttu-id="3eccb-105">Win32- \_ NetworkAdapter-Klasse</span><span class="sxs-lookup"><span data-stu-id="3eccb-105">Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="3eccb-106">Die **Win32- \_ NetworkAdapter** -Klasse ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="3eccb-106">The **Win32\_NetworkAdapter** class is deprecated.</span></span> <span data-ttu-id="3eccb-107">Verwenden Sie stattdessen die [**MSFT \_ netadapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="3eccb-107">Use the [**MSFT\_NetAdapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) class instead.</span></span> <span data-ttu-id="3eccb-108">Die **Win32 \_ Network Adapter**-[WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt einen Netzwerkadapter eines Computers dar, auf dem ein Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eccb-108">The **Win32\_NetworkAdapter**[WMI class](../wmisdk/retrieving-a-class.md) represents a network adapter of a computer running a Windows operating system.</span></span>

<span data-ttu-id="3eccb-109">**Win32 \_ Network Adapter** stellt nur IPv4-Daten bereit.</span><span class="sxs-lookup"><span data-stu-id="3eccb-109">**Win32\_NetworkAdapter** only supplies IPv4 data.</span></span> <span data-ttu-id="3eccb-110">Weitere Informationen finden Sie [unter IPv6-und IPv4-Unterstützung in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="3eccb-110">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="3eccb-111">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3eccb-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3eccb-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3eccb-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eccb-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="3eccb-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapter : CIM_NetworkAdapter
{
  string   AdapterType;
  uint16   AdapterTypeID;
  boolean  AutoSense;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   GUID;
  uint32   Index;
  datetime InstallDate;
  boolean  Installed;
  uint32   InterfaceIndex;
  uint32   LastErrorCode;
  string   MACAddress;
  string   Manufacturer;
  uint32   MaxNumberControlled;
  uint64   MaxSpeed;
  string   Name;
  string   NetConnectionID;
  uint16   NetConnectionStatus;
  boolean  NetEnabled;
  string   NetworkAddresses[];
  string   PermanentAddress;
  boolean  PhysicalAdapter;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   ServiceName;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="3eccb-114">Member</span><span class="sxs-lookup"><span data-stu-id="3eccb-114">Members</span></span>

<span data-ttu-id="3eccb-115">Die **Win32- \_ netzwerkadapterklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3eccb-115">The **Win32\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="3eccb-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="3eccb-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="3eccb-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3eccb-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3eccb-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="3eccb-118">Methods</span></span>

<span data-ttu-id="3eccb-119">Die **Win32- \_ netzwerkadapterklasse** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-119">The **Win32\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="3eccb-120">Methode</span><span class="sxs-lookup"><span data-stu-id="3eccb-120">Method</span></span>                                                          | <span data-ttu-id="3eccb-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3eccb-121">Description</span></span>                                                                                                                                                                                                                     |
|:----------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3eccb-122">**Ier**</span><span class="sxs-lookup"><span data-stu-id="3eccb-122">**Disable**</span></span>](disable-method-in-class-win32-networkadapter.md) | <span data-ttu-id="3eccb-123">Deaktiviert den Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="3eccb-123">Disables the network adapter.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="3eccb-124">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="3eccb-124">**Enable**</span></span>](enable-method-in-class-win32-networkadapter.md)   | <span data-ttu-id="3eccb-125">Aktiviert den Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="3eccb-125">Enables the network adapter.</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="3eccb-126">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="3eccb-126">**Reset**</span></span>                                                       | <span data-ttu-id="3eccb-127">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-127">Not implemented.</span></span> <span data-ttu-id="3eccb-128">Weitere Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ Network Adapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="3eccb-128">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/>                 |
| <span data-ttu-id="3eccb-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3eccb-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="3eccb-130">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-130">Not implemented.</span></span> <span data-ttu-id="3eccb-131">Weitere Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ Network Adapter**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="3eccb-131">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3eccb-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3eccb-132">Properties</span></span>

<span data-ttu-id="3eccb-133">Die **Win32- \_ netzwerkadapterklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3eccb-133">The **Win32\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3eccb-134">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="3eccb-134">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-137">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("[**Geräte abviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ gen-Medien werden \_ \_ \_ verwendet](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="3eccb-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-138">Netzwerk Medium verwendet.</span><span class="sxs-lookup"><span data-stu-id="3eccb-138">Network medium in use.</span></span> <span data-ttu-id="3eccb-139">Die Netzwerkadapter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3eccb-139">The network adapters are as follows:</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="3eccb-140">**Ethernet 802,3** ("Ethernet 802,3")</span><span class="sxs-lookup"><span data-stu-id="3eccb-140">**Ethernet 802.3** ("Ethernet 802.3")</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="3eccb-141">**TokenRing 802,5** ("TokenRing 802,5")</span><span class="sxs-lookup"><span data-stu-id="3eccb-141">**Token Ring 802.5** ("Token Ring 802.5")</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="3eccb-142">**Fiber verteilter Datenschnittstelle ((** "Fiber verteilter Data Interface, f)")</span><span class="sxs-lookup"><span data-stu-id="3eccb-142">**Fiber Distributed Data Interface (FDDI)** ("Fiber Distributed Data Interface (FDDI)")</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="3eccb-143">**WAN (Wide** Area Network) ("Wide Area Network (WAN)")</span><span class="sxs-lookup"><span data-stu-id="3eccb-143">**Wide Area Network (WAN)** ("Wide Area Network (WAN)")</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="3eccb-144">**LocalTalk** ("LocalTalk")</span><span class="sxs-lookup"><span data-stu-id="3eccb-144">**LocalTalk** ("LocalTalk")</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="3eccb-145">**Ethernet mit Dix-Header Format** ("Ethernet mit Dix-Header Format")</span><span class="sxs-lookup"><span data-stu-id="3eccb-145">**Ethernet using DIX header format** ("Ethernet using DIX header format")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="3eccb-146">**ARCNET** ("ARCNET")</span><span class="sxs-lookup"><span data-stu-id="3eccb-146">**ARCNET** ("ARCNET")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="3eccb-147">**ARCNET (878,2)** ("ARCNET (878,2)")</span><span class="sxs-lookup"><span data-stu-id="3eccb-147">**ARCNET (878.2)** ("ARCNET (878.2)")</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="3eccb-148">**ATM** ("ATM")</span><span class="sxs-lookup"><span data-stu-id="3eccb-148">**ATM** ("ATM")</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="3eccb-149">**Drahtlos** ("drahtlos")</span><span class="sxs-lookup"><span data-stu-id="3eccb-149">**Wireless** ("Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="3eccb-150">**Infrarot drahtlos** ("Infrarot drahtlos")</span><span class="sxs-lookup"><span data-stu-id="3eccb-150">**Infrared Wireless** ("Infrared Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="3eccb-151">**Bpc** ("bpc")</span><span class="sxs-lookup"><span data-stu-id="3eccb-151">**Bpc** ("Bpc")</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="3eccb-152">**Cowan** ("Cowan")</span><span class="sxs-lookup"><span data-stu-id="3eccb-152">**CoWan** ("CoWan")</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="3eccb-153">**1394** ("1394")</span><span class="sxs-lookup"><span data-stu-id="3eccb-153">**1394** ("1394")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3eccb-154">**AdapterTypeId**</span><span class="sxs-lookup"><span data-stu-id="3eccb-154">**AdapterTypeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-155">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3eccb-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-157">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("[**Geräte abviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ gen-Medien werden \_ \_ \_ verwendet](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="3eccb-157">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-158">Netzwerk Medium verwendet.</span><span class="sxs-lookup"><span data-stu-id="3eccb-158">Network medium in use.</span></span> <span data-ttu-id="3eccb-159">Gibt dieselben Informationen wie die **AdapterType** -Eigenschaft zurück, mit dem Unterschied, dass die Informationen in Form einer ganzen Zahl sind.</span><span class="sxs-lookup"><span data-stu-id="3eccb-159">Returns the same information as the **AdapterType** property, except that the information is in the form of an integer.</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="3eccb-160">**Ethernet 802,3** (0)</span><span class="sxs-lookup"><span data-stu-id="3eccb-160">**Ethernet 802.3** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="3eccb-161">**TokenRing 802,5** (1)</span><span class="sxs-lookup"><span data-stu-id="3eccb-161">**Token Ring 802.5** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="3eccb-162">**Fiber verteilte Datenschnittstelle (DDI)** (2)</span><span class="sxs-lookup"><span data-stu-id="3eccb-162">**Fiber Distributed Data Interface (FDDI)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="3eccb-163">**WAN (Wide Area Network)** (3)</span><span class="sxs-lookup"><span data-stu-id="3eccb-163">**Wide Area Network (WAN)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="3eccb-164">**LocalTalk** (4)</span><span class="sxs-lookup"><span data-stu-id="3eccb-164">**LocalTalk** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="3eccb-165">**Ethernet mit Dix-Header Format** (5)</span><span class="sxs-lookup"><span data-stu-id="3eccb-165">**Ethernet using DIX header format** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="3eccb-166">**ARCNET** (6)</span><span class="sxs-lookup"><span data-stu-id="3eccb-166">**ARCNET** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="3eccb-167">**ARCNET (878,2)** (7)</span><span class="sxs-lookup"><span data-stu-id="3eccb-167">**ARCNET (878.2)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="3eccb-168">**ATM** (8)</span><span class="sxs-lookup"><span data-stu-id="3eccb-168">**ATM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="3eccb-169">**Drahtlos** (9)</span><span class="sxs-lookup"><span data-stu-id="3eccb-169">**Wireless** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="3eccb-170">**Infrarot drahtlos** (10)</span><span class="sxs-lookup"><span data-stu-id="3eccb-170">**Infrared Wireless** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="3eccb-171">**Bpc** (11)</span><span class="sxs-lookup"><span data-stu-id="3eccb-171">**Bpc** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="3eccb-172">**Cowan** (12)</span><span class="sxs-lookup"><span data-stu-id="3eccb-172">**CoWan** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="3eccb-173">**1394** (13)</span><span class="sxs-lookup"><span data-stu-id="3eccb-173">**1394** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3eccb-174">**AutoSense**</span><span class="sxs-lookup"><span data-stu-id="3eccb-174">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-175">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3eccb-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-177">Wenn der Wert **true** ist, kann der Netzwerkadapter die Geschwindigkeit der angefügten oder Netzwerk Medien automatisch bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-177">If **True**, the network adapter can automatically determine the speed of the attached or network media.</span></span>

<span data-ttu-id="3eccb-178">Diese Eigenschaft wird vom [**CIM- \_ NetworkAdapter**](cim-networkadapter.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-178">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="3eccb-179">Diese Eigenschaft wurde noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-179">This property has not been implemented yet.</span></span> <span data-ttu-id="3eccb-180">Standardmäßig wird ein **null** -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3eccb-180">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-181">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="3eccb-181">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-182">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3eccb-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-184">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="3eccb-184">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-185">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="3eccb-185">Availability and status of the device.</span></span>

<span data-ttu-id="3eccb-186">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3eccb-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="3eccb-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3eccb-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="3eccb-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="3eccb-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="3eccb-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-190">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="3eccb-190">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="3eccb-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="3eccb-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="3eccb-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="3eccb-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3eccb-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="3eccb-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="3eccb-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="3eccb-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="3eccb-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="3eccb-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="3eccb-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="3eccb-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3eccb-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="3eccb-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="3eccb-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="3eccb-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="3eccb-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="3eccb-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="3eccb-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="3eccb-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-201">Es ist bekannt, dass sich das Gerät in einem Energiespar Zustand befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-201">The device is known to be in a power save state, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="3eccb-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="3eccb-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-203">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-203">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="3eccb-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="3eccb-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-205">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-205">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="3eccb-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="3eccb-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="3eccb-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="3eccb-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-208">Das Gerät befindet sich in einem Warn Status, aber auch in einem Energiespar Zustand.</span><span class="sxs-lookup"><span data-stu-id="3eccb-208">The device is in a warning state, though also in a power save state.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3eccb-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="3eccb-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-210">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="3eccb-210">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="3eccb-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="3eccb-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-212">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="3eccb-212">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="3eccb-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="3eccb-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-214">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-214">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="3eccb-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="3eccb-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-216">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="3eccb-216">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3eccb-217">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3eccb-217">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-218">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-220">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3eccb-220">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-221">Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3eccb-221">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="3eccb-222">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-223">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="3eccb-223">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-224">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3eccb-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-226">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3eccb-226">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-227">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3eccb-227">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="3eccb-228">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-228">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="3eccb-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="3eccb-230"> (0)</span><span class="sxs-lookup"><span data-stu-id="3eccb-230">(0)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-231">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3eccb-231">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="3eccb-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="3eccb-233">(1)</span><span class="sxs-lookup"><span data-stu-id="3eccb-233">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-234">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-234">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3eccb-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="3eccb-236">(2)</span><span class="sxs-lookup"><span data-stu-id="3eccb-236">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="3eccb-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="3eccb-238">(3)</span><span class="sxs-lookup"><span data-stu-id="3eccb-238">(3)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-239">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-239">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3eccb-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="3eccb-241">(4)</span><span class="sxs-lookup"><span data-stu-id="3eccb-241">(4)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-242">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3eccb-242">Device is not working properly.</span></span> <span data-ttu-id="3eccb-243">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-243">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="3eccb-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="3eccb-245">(5)</span><span class="sxs-lookup"><span data-stu-id="3eccb-245">(5)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-246">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3eccb-246">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="3eccb-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="3eccb-248"> (6)</span><span class="sxs-lookup"><span data-stu-id="3eccb-248">(6)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-249">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="3eccb-249">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="3eccb-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="3eccb-251">(7)</span><span class="sxs-lookup"><span data-stu-id="3eccb-251">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="3eccb-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="3eccb-253">(8)</span><span class="sxs-lookup"><span data-stu-id="3eccb-253">(8)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-254">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-254">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="3eccb-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="3eccb-256">(9)</span><span class="sxs-lookup"><span data-stu-id="3eccb-256">(9)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-257">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3eccb-257">Device is not working properly.</span></span> <span data-ttu-id="3eccb-258">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="3eccb-258">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="3eccb-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="3eccb-260">(10)</span><span class="sxs-lookup"><span data-stu-id="3eccb-260">(10)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-261">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-261">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="3eccb-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="3eccb-263">(11)</span><span class="sxs-lookup"><span data-stu-id="3eccb-263">(11)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-264">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="3eccb-264">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="3eccb-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="3eccb-266">(12)</span><span class="sxs-lookup"><span data-stu-id="3eccb-266">(12)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-267">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-267">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="3eccb-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="3eccb-269">(13)</span><span class="sxs-lookup"><span data-stu-id="3eccb-269">(13)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-270">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-270">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="3eccb-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="3eccb-272">(14)</span><span class="sxs-lookup"><span data-stu-id="3eccb-272">(14)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-273">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3eccb-273">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="3eccb-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="3eccb-275">(15)</span><span class="sxs-lookup"><span data-stu-id="3eccb-275">(15)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-276">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3eccb-276">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="3eccb-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="3eccb-278">(16)</span><span class="sxs-lookup"><span data-stu-id="3eccb-278">(16)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-279">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-279">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="3eccb-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="3eccb-281">(17)</span><span class="sxs-lookup"><span data-stu-id="3eccb-281">(17)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-282">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="3eccb-282">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3eccb-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="3eccb-284">(18)</span><span class="sxs-lookup"><span data-stu-id="3eccb-284">(18)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-285">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-285">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="3eccb-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="3eccb-287">(19)</span><span class="sxs-lookup"><span data-stu-id="3eccb-287">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3eccb-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="3eccb-289">(20)</span><span class="sxs-lookup"><span data-stu-id="3eccb-289">(20)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-290">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-290">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="3eccb-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="3eccb-292">(21)</span><span class="sxs-lookup"><span data-stu-id="3eccb-292">(21)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-293">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="3eccb-293">System failure.</span></span> <span data-ttu-id="3eccb-294">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3eccb-294">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="3eccb-295">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-295">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="3eccb-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="3eccb-297">(22)</span><span class="sxs-lookup"><span data-stu-id="3eccb-297">(22)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-298">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-298">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="3eccb-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="3eccb-300">(23)</span><span class="sxs-lookup"><span data-stu-id="3eccb-300">(23)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-301">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="3eccb-301">System failure.</span></span> <span data-ttu-id="3eccb-302">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3eccb-302">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="3eccb-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="3eccb-304">(24)</span><span class="sxs-lookup"><span data-stu-id="3eccb-304">(24)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-305">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-305">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3eccb-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3eccb-307">(25)</span><span class="sxs-lookup"><span data-stu-id="3eccb-307">(25)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-308">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="3eccb-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3eccb-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3eccb-310">(26)</span><span class="sxs-lookup"><span data-stu-id="3eccb-310">(26)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-311">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="3eccb-311">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="3eccb-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="3eccb-313">(27)</span><span class="sxs-lookup"><span data-stu-id="3eccb-313">(27)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-314">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3eccb-314">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="3eccb-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="3eccb-316">(28)</span><span class="sxs-lookup"><span data-stu-id="3eccb-316">(28)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-317">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-317">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="3eccb-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="3eccb-319">(29)</span><span class="sxs-lookup"><span data-stu-id="3eccb-319">(29)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-320">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-320">Device is disabled.</span></span> <span data-ttu-id="3eccb-321">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-321">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="3eccb-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="3eccb-323">(30)</span><span class="sxs-lookup"><span data-stu-id="3eccb-323">(30)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-324">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3eccb-324">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3eccb-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="3eccb-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="3eccb-326">31,5</span><span class="sxs-lookup"><span data-stu-id="3eccb-326">(31)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-327">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3eccb-327">Device is not working properly.</span></span> <span data-ttu-id="3eccb-328">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-328">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3eccb-329">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="3eccb-329">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-330">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3eccb-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-332">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3eccb-332">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-333">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="3eccb-333">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="3eccb-334">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-335">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="3eccb-335">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-336">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-338">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="3eccb-338">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-339">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3eccb-339">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="3eccb-340">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-340">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3eccb-341">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-342">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3eccb-342">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-343">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-345">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="3eccb-345">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-346">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3eccb-346">Description of the object.</span></span>

<span data-ttu-id="3eccb-347">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-348">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3eccb-348">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-349">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-351">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="3eccb-351">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-352">Eindeutiger Bezeichner des Netzwerkadapters von anderen Geräten im System.</span><span class="sxs-lookup"><span data-stu-id="3eccb-352">Unique identifier of the network adapter from other devices on the system.</span></span>

<span data-ttu-id="3eccb-353">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-354">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="3eccb-354">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-355">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3eccb-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-357">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="3eccb-357">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="3eccb-358">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-359">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3eccb-359">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-360">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-362">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. durchzuführenden Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-362">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="3eccb-363">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-364">**GUID**</span><span class="sxs-lookup"><span data-stu-id="3eccb-364">**GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-365">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-367">Global eindeutiger Bezeichner für die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="3eccb-367">Globally unique identifier for the connection.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-368">**Index**</span><span class="sxs-lookup"><span data-stu-id="3eccb-368">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-369">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3eccb-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-371">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="3eccb-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-372">Index Nummer des in der Systemregistrierung gespeicherten Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="3eccb-372">Index number of the network adapter, stored in the system registry.</span></span>

<span data-ttu-id="3eccb-373">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="3eccb-373">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-374">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3eccb-374">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-375">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3eccb-375">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-376">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-377">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="3eccb-377">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-378">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3eccb-378">Date and time the object was installed.</span></span> <span data-ttu-id="3eccb-379">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3eccb-379">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3eccb-380">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3eccb-381">Diese Eigenschaft wurde noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-381">This property has not been implemented yet.</span></span> <span data-ttu-id="3eccb-382">Standardmäßig wird ein **null** -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3eccb-382">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-383">**Installiert**</span><span class="sxs-lookup"><span data-stu-id="3eccb-383">**Installed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-384">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3eccb-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-385">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-386">Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ networkcards \| driverdate")</span><span class="sxs-lookup"><span data-stu-id="3eccb-386">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-387">**True** gibt an, dass der Netzwerkadapter im System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3eccb-387">If **True**, the network adapter is installed in the system.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-388">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="3eccb-388">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-389">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3eccb-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-391">Indexwert, der die lokale Netzwerkschnittstelle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-391">Index value that uniquely identifies the local network interface.</span></span> <span data-ttu-id="3eccb-392">Der Wert in dieser Eigenschaft ist identisch mit dem Wert in der **interfakeindex** -Eigenschaft in der Instanz von [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) , die die Netzwerkschnittstelle in der Routing Tabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-392">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3eccb-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-394">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3eccb-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-395">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-396">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3eccb-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="3eccb-397">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-398">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="3eccb-398">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-399">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-401">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Input and Output Functions \| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span><span class="sxs-lookup"><span data-stu-id="3eccb-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-402">Media Access Control-Adresse für diesen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="3eccb-402">Media access control address for this network adapter.</span></span> <span data-ttu-id="3eccb-403">Eine Mac-Adresse ist eine eindeutige 48-Bit-Nummer, die dem Netzwerkadapter vom Hersteller zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3eccb-403">A MAC address is a unique 48-bit number assigned to the network adapter by the manufacturer.</span></span> <span data-ttu-id="3eccb-404">Dieser Netzwerkadapter wird eindeutig identifiziert und zum Mapping der TCP/IP-Netzwerkkommunikation verwendet.</span><span class="sxs-lookup"><span data-stu-id="3eccb-404">It uniquely identifies this network adapter and is used for mapping TCP/IP network communications.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-405">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="3eccb-405">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-406">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-408">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Network Cards \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="3eccb-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-409">Der Name des Herstellers des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="3eccb-409">Name of the network adapter's manufacturer.</span></span>

<span data-ttu-id="3eccb-410">Beispiel: "3Com"</span><span class="sxs-lookup"><span data-stu-id="3eccb-410">Example: "3COM"</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-411">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="3eccb-411">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-412">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3eccb-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-414">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Bus Port \| 001,9 \| Maximale Anzahl von Anlagen ")</span><span class="sxs-lookup"><span data-stu-id="3eccb-414">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9\|Maximum Number of Attachments")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-415">Maximale Anzahl von direkt adressierbaren Ports, die von diesem Netzwerkadapter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-415">Maximum number of directly addressable ports supported by this network adapter.</span></span> <span data-ttu-id="3eccb-416">Wenn die Zahl unbekannt ist, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-416">A value of 0 (zero) should be used if the number is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-417">**MAXSPEED**</span><span class="sxs-lookup"><span data-stu-id="3eccb-417">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-418">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3eccb-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-420">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="3eccb-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-421">Maximale Geschwindigkeit in Bits pro Sekunde für den Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="3eccb-421">Maximum speed, in bits per second, for the network adapter.</span></span>

<span data-ttu-id="3eccb-422">Diese Eigenschaft wird vom [**CIM- \_ NetworkAdapter**](cim-networkadapter.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-422">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="3eccb-423">Diese Eigenschaft wurde noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-423">This property has not been implemented yet.</span></span> <span data-ttu-id="3eccb-424">Standardmäßig wird ein **null** -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3eccb-424">It returns a **NULL** value by default.</span></span>

<span data-ttu-id="3eccb-425">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3eccb-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-426">**Name**</span><span class="sxs-lookup"><span data-stu-id="3eccb-426">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-427">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-429">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3eccb-429">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-430">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="3eccb-430">Label by which the object is known.</span></span> <span data-ttu-id="3eccb-431">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-431">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="3eccb-432">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-433">**NetConnectionID**</span><span class="sxs-lookup"><span data-stu-id="3eccb-433">**NetConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-434">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-435">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3eccb-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-436">Der Name der Netzwerkverbindung, der in der Systemsteuerung unter " **Netzwerkverbindungen** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3eccb-436">Name of the network connection as it appears in the **Network Connections** Control Panel program.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-437">**NetConnectionStatus**</span><span class="sxs-lookup"><span data-stu-id="3eccb-437">**NetConnectionStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-438">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3eccb-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-439">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-440">Status der Netzwerkadapter Verbindung mit dem Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3eccb-440">State of the network adapter connection to the network.</span></span>

<dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="3eccb-441">**Getrennt** (0)</span><span class="sxs-lookup"><span data-stu-id="3eccb-441">**Disconnected** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="3eccb-442">**Verbindung** wird hergestellt (1)</span><span class="sxs-lookup"><span data-stu-id="3eccb-442">**Connecting** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="3eccb-443">**Verbunden** (2)</span><span class="sxs-lookup"><span data-stu-id="3eccb-443">**Connected** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnecting"></span><span id="disconnecting"></span><span id="DISCONNECTING"></span>

<span data-ttu-id="3eccb-444">**Trennen der Verbindung** (3)</span><span class="sxs-lookup"><span data-stu-id="3eccb-444">**Disconnecting** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Not_Present"></span><span id="hardware_not_present"></span><span id="HARDWARE_NOT_PRESENT"></span>

<span data-ttu-id="3eccb-445">**Hardware nicht vorhanden** (4)</span><span class="sxs-lookup"><span data-stu-id="3eccb-445">**Hardware Not Present** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Disabled"></span><span id="hardware_disabled"></span><span id="HARDWARE_DISABLED"></span>

<span data-ttu-id="3eccb-446">**Hardware deaktiviert** (5)</span><span class="sxs-lookup"><span data-stu-id="3eccb-446">**Hardware Disabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Malfunction"></span><span id="hardware_malfunction"></span><span id="HARDWARE_MALFUNCTION"></span>

<span data-ttu-id="3eccb-447">**Hardware** Fehler (6)</span><span class="sxs-lookup"><span data-stu-id="3eccb-447">**Hardware Malfunction** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Disconnected"></span><span id="media_disconnected"></span><span id="MEDIA_DISCONNECTED"></span>

<span data-ttu-id="3eccb-448">**Medien getrennt** (7)</span><span class="sxs-lookup"><span data-stu-id="3eccb-448">**Media Disconnected** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Authenticating"></span><span id="authenticating"></span><span id="AUTHENTICATING"></span>

<span data-ttu-id="3eccb-449">**Authentifizieren** (8)</span><span class="sxs-lookup"><span data-stu-id="3eccb-449">**Authenticating** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Succeeded"></span><span id="authentication_succeeded"></span><span id="AUTHENTICATION_SUCCEEDED"></span>

<span data-ttu-id="3eccb-450">**Authentifizierung erfolgreich** (9)</span><span class="sxs-lookup"><span data-stu-id="3eccb-450">**Authentication Succeeded** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failed"></span><span id="authentication_failed"></span><span id="AUTHENTICATION_FAILED"></span>

<span data-ttu-id="3eccb-451">Fehler bei der **Authentifizierung** (10).</span><span class="sxs-lookup"><span data-stu-id="3eccb-451">**Authentication Failed** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Address"></span><span id="invalid_address"></span><span id="INVALID_ADDRESS"></span>

<span data-ttu-id="3eccb-452">**Ungültige Adresse** (11)</span><span class="sxs-lookup"><span data-stu-id="3eccb-452">**Invalid Address** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Credentials_Required"></span><span id="credentials_required"></span><span id="CREDENTIALS_REQUIRED"></span>

<span data-ttu-id="3eccb-453">**Erforderliche Anmelde** Informationen (12)</span><span class="sxs-lookup"><span data-stu-id="3eccb-453">**Credentials Required** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3eccb-454">**Andere**</span><span class="sxs-lookup"><span data-stu-id="3eccb-454">**Other**</span></span>


</dt> <dd><span data-ttu-id="3eccb-455">13 – 65535</span><span class="sxs-lookup"><span data-stu-id="3eccb-455">13–65535</span></span></dd> </dl>

</dd> <dt>

<span data-ttu-id="3eccb-456">**NetEnabled**</span><span class="sxs-lookup"><span data-stu-id="3eccb-456">**NetEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-457">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3eccb-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-458">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-459">Gibt an, ob der Adapter aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3eccb-459">Indicates whether the adapter is enabled or not.</span></span> <span data-ttu-id="3eccb-460">**True** gibt an, dass der Adapter aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3eccb-460">If **True**, the adapter is enabled.</span></span> <span data-ttu-id="3eccb-461">Sie können die NIC mithilfe der Methoden [**enable**](enable-method-in-class-win32-networkadapter.md) und [**Deaktivieren**](disable-method-in-class-win32-networkadapter.md) aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3eccb-461">You can enable or disable the NIC by using the [**Enable**](enable-method-in-class-win32-networkadapter.md) and [**Disable**](disable-method-in-class-win32-networkadapter.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-462">**"Networkaddresses"**</span><span class="sxs-lookup"><span data-stu-id="3eccb-462">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-463">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="3eccb-463">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-464">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-465">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Netzwerk Adapter 802-Port \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="3eccb-465">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-466">Array von Netzwerkadressen für einen Adapter.</span><span class="sxs-lookup"><span data-stu-id="3eccb-466">Array of network addresses for an adapter.</span></span>

<span data-ttu-id="3eccb-467">Diese Eigenschaft wird vom [**CIM- \_ NetworkAdapter**](cim-networkadapter.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-467">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="3eccb-468">Diese Eigenschaft wurde noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-468">This property has not been implemented yet.</span></span> <span data-ttu-id="3eccb-469">Standardmäßig wird ein **null** -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3eccb-469">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-470">**Permanent Address**</span><span class="sxs-lookup"><span data-stu-id="3eccb-470">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-471">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-473">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Netzwerk Adapter 802-Port \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="3eccb-473">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-474">Die Netzwerkadresse ist in einem Adapter hart codiert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-474">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="3eccb-475">Diese hart codierte Adresse kann durch ein Firmwareupdate oder eine Softwarekonfiguration geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-475">This hard-coded address may be changed by firmware upgrade or software configuration.</span></span> <span data-ttu-id="3eccb-476">Wenn dies der Fall ist, sollte dieses Feld aktualisiert werden, wenn die Änderung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="3eccb-476">If so, this field should be updated when the change is made.</span></span> <span data-ttu-id="3eccb-477">Die-Eigenschaft sollte leer gelassen werden, wenn für den Netzwerkadapter keine hart codierte Adresse vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3eccb-477">The property should be left blank if no hard-coded address exists for the network adapter.</span></span>

<span data-ttu-id="3eccb-478">Diese Eigenschaft wird vom [**CIM- \_ NetworkAdapter**](cim-networkadapter.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-478">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="3eccb-479">Diese Eigenschaft wurde noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-479">This property has not been implemented yet.</span></span> <span data-ttu-id="3eccb-480">Standardmäßig wird ein **null** -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3eccb-480">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-481">**PhysicalAdapter**</span><span class="sxs-lookup"><span data-stu-id="3eccb-481">**PhysicalAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-482">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3eccb-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-483">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-484">Gibt an, ob es sich bei dem Adapter um einen physischen oder logischen Adapter handelt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-484">Indicates whether the adapter is a physical or a logical adapter.</span></span> <span data-ttu-id="3eccb-485">**True** gibt an, dass der Adapter physisch ist.</span><span class="sxs-lookup"><span data-stu-id="3eccb-485">If **True**, the adapter is physical.</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-486">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="3eccb-486">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-487">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-488">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-489">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3eccb-489">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-490">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="3eccb-490">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="3eccb-491">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3eccb-492">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="3eccb-492">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-493">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="3eccb-493">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-494">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="3eccb-494">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-495">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-496">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="3eccb-496">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="3eccb-497">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3eccb-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="3eccb-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="3eccb-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="3eccb-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3eccb-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="3eccb-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3eccb-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="3eccb-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-502">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3eccb-502">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="3eccb-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="3eccb-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-504">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="3eccb-504">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="3eccb-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="3eccb-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-506">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-506">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="3eccb-507">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-507">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="3eccb-508">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="3eccb-508">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="3eccb-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="3eccb-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-510">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3eccb-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="3eccb-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="3eccb-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3eccb-512">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-512">Timed Power-On Supported</span></span>

<span data-ttu-id="3eccb-513">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3eccb-513">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3eccb-514">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="3eccb-514">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-515">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3eccb-515">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-516">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-517">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="3eccb-517">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="3eccb-518">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="3eccb-518">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="3eccb-519">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-519">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-520">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="3eccb-520">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-521">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-522">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-523">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Network Cards \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="3eccb-523">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-524">Der Produktname des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="3eccb-524">Product name of the network adapter.</span></span>

<span data-ttu-id="3eccb-525">Beispiel: "Fast EtherLink XL"</span><span class="sxs-lookup"><span data-stu-id="3eccb-525">Example: "Fast EtherLink XL"</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-526">**Service Name**</span><span class="sxs-lookup"><span data-stu-id="3eccb-526">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-527">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-528">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-529">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Network Cards \| ProductName")</span><span class="sxs-lookup"><span data-stu-id="3eccb-529">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ProductName")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-530">Der Dienst Name des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="3eccb-530">Service name of the network adapter.</span></span> <span data-ttu-id="3eccb-531">Dieser Name ist in der Regel kürzer als der vollständige Produktname.</span><span class="sxs-lookup"><span data-stu-id="3eccb-531">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="3eccb-532">Beispiel: "Elnkii"</span><span class="sxs-lookup"><span data-stu-id="3eccb-532">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-533">**Geschwindigkeit**</span><span class="sxs-lookup"><span data-stu-id="3eccb-533">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-534">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3eccb-534">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-535">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-535">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-536">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| RFC1213-MIB. IfSpeed "," MIF. DMTF- \| Netzwerk Adapter 802-Port \| 001,5 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (Bits pro Sekunde)</span><span class="sxs-lookup"><span data-stu-id="3eccb-536">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-537">Schätzung der aktuellen Bandbreite in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="3eccb-537">Estimate of the current bandwidth in bits per second.</span></span> <span data-ttu-id="3eccb-538">Für Endpunkte, die die Bandbreite variieren, oder für diejenigen, bei denen keine genaue Schätzung vorgenommen werden kann, sollte diese Eigenschaft die nominale Bandbreite enthalten.</span><span class="sxs-lookup"><span data-stu-id="3eccb-538">For endpoints which vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="3eccb-539">Diese Eigenschaft wird vom [**CIM- \_ NetworkAdapter**](cim-networkadapter.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-539">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="3eccb-540">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3eccb-540">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-541">**Status**</span><span class="sxs-lookup"><span data-stu-id="3eccb-541">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-542">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-543">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-544">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="3eccb-544">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-545">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3eccb-545">Current status of the object.</span></span> <span data-ttu-id="3eccb-546">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-546">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3eccb-547">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="3eccb-547">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3eccb-548">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3eccb-548">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3eccb-549">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="3eccb-549">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3eccb-550">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="3eccb-550">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3eccb-551">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="3eccb-551">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3eccb-552">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3eccb-552">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3eccb-553">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="3eccb-553">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3eccb-554">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="3eccb-554">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3eccb-555">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="3eccb-555">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3eccb-556">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="3eccb-556">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3eccb-557">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="3eccb-557">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3eccb-558">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="3eccb-558">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3eccb-559">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="3eccb-559">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3eccb-560">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3eccb-560">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-561">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3eccb-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-562">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-563">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="3eccb-563">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-564">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="3eccb-564">State of the logical device.</span></span> <span data-ttu-id="3eccb-565">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-565">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="3eccb-566">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-566">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3eccb-567">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="3eccb-567">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3eccb-568">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="3eccb-568">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3eccb-569">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="3eccb-569">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3eccb-570">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="3eccb-570">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3eccb-571">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="3eccb-571">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3eccb-572">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="3eccb-572">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-573">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-573">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-574">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-574">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-575">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="3eccb-575">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-576">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="3eccb-576">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="3eccb-577">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-577">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-578">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="3eccb-578">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-579">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3eccb-579">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-580">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-581">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="3eccb-581">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-582">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="3eccb-582">Name of the scoping system.</span></span>

<span data-ttu-id="3eccb-583">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eccb-583">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eccb-584">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="3eccb-584">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eccb-585">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3eccb-585">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-586">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3eccb-586">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eccb-587">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ \\ \\ 009 \| System Up Time")</span><span class="sxs-lookup"><span data-stu-id="3eccb-587">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Perflib\\\\009\|System Up Time")</span></span>
</dt> </dl>

<span data-ttu-id="3eccb-588">Datum und Uhrzeit der letzten zurück setzung des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="3eccb-588">Date and time the network adapter was last reset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3eccb-589">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3eccb-589">Remarks</span></span>

<span data-ttu-id="3eccb-590">Die **Win32- \_ netzwerkadapterklasse** wird von [**CIM \_ Network Adapter**](cim-networkadapter.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3eccb-590">The **Win32\_NetworkAdapter** class is derived from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="3eccb-591">In der folgenden Liste werden die assoziatorklassen für den **Win32- \_ Netzwerkadapter** beschrieben:</span><span class="sxs-lookup"><span data-stu-id="3eccb-591">The following list describes the Associator classes for **Win32\_NetworkAdapter**:</span></span>

-   [<span data-ttu-id="3eccb-592">**Win32- \_ pnptity**</span><span class="sxs-lookup"><span data-stu-id="3eccb-592">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
-   [<span data-ttu-id="3eccb-593">**Win32- \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="3eccb-593">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
-   [<span data-ttu-id="3eccb-594">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="3eccb-594">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
-   [<span data-ttu-id="3eccb-595">**Win32-Webressource \_**</span><span class="sxs-lookup"><span data-stu-id="3eccb-595">**Win32\_IRQResource**</span></span>](win32-irqresource.md)
-   [<span data-ttu-id="3eccb-596">**Win32 \_ devicememoryaddress**</span><span class="sxs-lookup"><span data-stu-id="3eccb-596">**Win32\_DeviceMemoryAddress**</span></span>](win32-devicememoryaddress.md)
-   [<span data-ttu-id="3eccb-597">**Win32- \_ portresource**</span><span class="sxs-lookup"><span data-stu-id="3eccb-597">**Win32\_PortResource**</span></span>](win32-portresource.md)
-   [<span data-ttu-id="3eccb-598">**Win32- \_ networkprotocol**</span><span class="sxs-lookup"><span data-stu-id="3eccb-598">**Win32\_NetworkProtocol**</span></span>](win32-networkprotocol.md)
-   [<span data-ttu-id="3eccb-599">**Win32- \_ System Treiber**</span><span class="sxs-lookup"><span data-stu-id="3eccb-599">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)

<span data-ttu-id="3eccb-600">Viele Systeme verfügen über eine Reihe von Netzwerkadaptern.</span><span class="sxs-lookup"><span data-stu-id="3eccb-600">Many systems have a number of network adapters on them.</span></span> <span data-ttu-id="3eccb-601">Verwenden Sie Folgendes als Referenz, um die aktuellen Adapter zu finden:</span><span class="sxs-lookup"><span data-stu-id="3eccb-601">Consider using the following as a reference to find the current adapters:</span></span>

``` syntax
AdapterType: "Ethernet 802.3"
MACAddress: String Length > 16
Availability: 3
PNPDeviceID: InStr ( PNPDeviceID, "PCI") = 1
Installed: vbTrue
ConfigManagerErrorCode: 0
: <keep this as an index to Win32_NetworkAdapterConfiguration>
```

<span data-ttu-id="3eccb-602">Selbst bei Verwendung der obigen Qualifizierer werden Sie wahrscheinlich mehr als einen gültigen Netzwerkadapter abrufen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-602">Even using the above qualifiers, you will likely retrieve more than one valid network adapter.</span></span> <span data-ttu-id="3eccb-603">Wenn dies der Fall ist, können Sie die folgenden Informationen verwenden, um die Suche nach Win32 \_ networkadapterconfiguration weiter zu qualifizieren:</span><span class="sxs-lookup"><span data-stu-id="3eccb-603">If that is the case, Then you can use the following information to further qualify your search of the Win32\_NetworkAdapterConfiguration:</span></span>

``` syntax
Index: <match to DeviceID above>
MACAddress: Length > 16
DefaultIPGateway: String Length > 6
DNSServerSearchOrder: Array of strings with length > 6
IPEnabled: vbTrue
IPAddress: Array of strings with length > 6
```

<span data-ttu-id="3eccb-604">Nachdem Sie dies abgeschlossen haben, haben Sie die Liste wahrscheinlich auf einen oder zwei konfigurierte Adapter reduziert.</span><span class="sxs-lookup"><span data-stu-id="3eccb-604">Once you have done so, you will likely have reduced your list to one or two configured adapters.</span></span>

<span data-ttu-id="3eccb-605">Sie können auch das folgende Verfahren verwenden, um den Standard Adapter zu finden:</span><span class="sxs-lookup"><span data-stu-id="3eccb-605">You can also use the following procedure to find the default adapter:</span></span>

1.  <span data-ttu-id="3eccb-606">Führen Sie die folgende Abfrage aus:</span><span class="sxs-lookup"><span data-stu-id="3eccb-606">Run the following query:</span></span>

    `"SELECT InterfaceIndex, Destination FROM Win32_IP4RouteTable WHERE Destination='0.0.0.0'"`

    <span data-ttu-id="3eccb-607">Sie sollten nur über ein Standard Netzwerk Ziel 0.0.0.0 verfügen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-607">You should only have one default network destination 0.0.0.0.</span></span>

2.  <span data-ttu-id="3eccb-608">Verwenden Sie den **interfaceingedex** , um den gewünschten Netzwerk Adapter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-608">Use the **InterfaceIndex** to retrieve the Network Adapter you want.</span></span>

    `"SELECT * FROM Win32_NetworkAdapter WHERE InterfaceIndex=" + insertVariableHere`

## <a name="examples"></a><span data-ttu-id="3eccb-609">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3eccb-609">Examples</span></span>

<span data-ttu-id="3eccb-610">Das PowerShell-Codebeispiel für [WMI-Funktionen](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) in der TechNet Gallery verwendet **Win32 \_ Network Adapter** , um das Windows [Get-netadapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) -Cmdlet neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-610">The [Two WMI Functions](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) PowerShell code example in the TechNet Gallery uses **Win32\_NetworkAdapter** to re-create the Windows [Get-NetAdapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) cmdlet.</span></span>

<span data-ttu-id="3eccb-611">Das PowerShell [-Beispiel Get-ComputerInfo-Query Computer Info from Local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) in der TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32 \_ Network Adapter**, um Informationen über ein lokales oder Remote System anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-611">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapter**, to display information about a local or remote system.</span></span>

<span data-ttu-id="3eccb-612">Im folgenden C- \# Codebeispiel wird der [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) -Namespace verwendet, um die aktuellen Netzwerkadapter auf dem lokalen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-612">The following C\# code sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace to retrieve the current network adapters on the local machine.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapter");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
                Console.WriteLine();
            }

            Console.ReadLine();
        }
```



<span data-ttu-id="3eccb-613">Im folgenden C- \# Codebeispiel wird https://msdn.microsoft.com/library/system.management.aspx der Namespace verwendet, um die aktuellen Netzwerkadapter auf dem lokalen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-613">The following C\# code sample uses https://msdn.microsoft.com/library/system.management.aspx namespace to retrieve the current network adapters on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="3eccb-614"> https://msdn.microsoft.com/library/system.management.aspx enthält die ursprünglichen Klassen, die für den Zugriff auf WMI verwendet werden. Allerdings gelten Sie als langsamer und werden im Allgemeinen nicht ebenso skaliert wie Ihre [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) -Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="3eccb-614">https://msdn.microsoft.com/library/system.management.aspx contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapter");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("MACAddress : {0}", m["Description"]);
                Console.WriteLine();
            }
            Console.ReadLine();

        }
```



<span data-ttu-id="3eccb-615">Im folgenden VBScript-Codebeispiel wird beschrieben, wie die aktuellen Netzwerkadapter auf dem lokalen Computer abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-615">The following VBScript code sample describes how to retrieve the current network adapters on the local machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapter")

For Each objItem in colItems 
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo
Next
```



## <a name="requirements"></a><span data-ttu-id="3eccb-616">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3eccb-616">Requirements</span></span>



| <span data-ttu-id="3eccb-617">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3eccb-617">Requirement</span></span> | <span data-ttu-id="3eccb-618">Wert</span><span class="sxs-lookup"><span data-stu-id="3eccb-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3eccb-619">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3eccb-619">Minimum supported client</span></span><br/> | <span data-ttu-id="3eccb-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eccb-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3eccb-621">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3eccb-621">Minimum supported server</span></span><br/> | <span data-ttu-id="3eccb-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3eccb-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3eccb-623">Namespace</span><span class="sxs-lookup"><span data-stu-id="3eccb-623">Namespace</span></span><br/>                | <span data-ttu-id="3eccb-624">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3eccb-624">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3eccb-625">MOF</span><span class="sxs-lookup"><span data-stu-id="3eccb-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3eccb-626"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3eccb-626"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3eccb-627">DLL</span><span class="sxs-lookup"><span data-stu-id="3eccb-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3eccb-628"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3eccb-628"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eccb-629">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3eccb-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eccb-630">**CIM- \_ Netzwerkadapter**</span><span class="sxs-lookup"><span data-stu-id="3eccb-630">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="3eccb-631">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="3eccb-631">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3eccb-632">WMI-Tasks: Netzwerk</span><span class="sxs-lookup"><span data-stu-id="3eccb-632">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="3eccb-633">IPv6-und IPv4-Unterstützung in WMI</span><span class="sxs-lookup"><span data-stu-id="3eccb-633">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 

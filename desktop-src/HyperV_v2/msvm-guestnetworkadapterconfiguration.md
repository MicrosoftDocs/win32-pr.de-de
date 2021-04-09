---
description: Stellt die Konfiguration eines Netzwerkadapters innerhalb des Gast Betriebssystems dar.
ms.assetid: 154d4a0f-0c57-496a-a351-6caa74011544
title: Msvm_GuestNetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestNetworkAdapterConfiguration
- Msvm_GuestNetworkAdapterConfiguration.InstanceID
- Msvm_GuestNetworkAdapterConfiguration.ProtocolIFType
- Msvm_GuestNetworkAdapterConfiguration.DHCPEnabled
- Msvm_GuestNetworkAdapterConfiguration.IPAddresses
- Msvm_GuestNetworkAdapterConfiguration.Subnets
- Msvm_GuestNetworkAdapterConfiguration.DefaultGateways
- Msvm_GuestNetworkAdapterConfiguration.DNSServers
- Msvm_GuestNetworkAdapterConfiguration.IPAddressOrigins
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ce5738bca4563aa77678cac2b7e33f5c4d5323e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129749"
---
# <a name="msvm_guestnetworkadapterconfiguration-class"></a><span data-ttu-id="f1629-103">MSVM \_ guestnetworkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="f1629-103">Msvm\_GuestNetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f1629-104">Stellt die Konfiguration eines Netzwerkadapters innerhalb des Gast Betriebssystems dar.</span><span class="sxs-lookup"><span data-stu-id="f1629-104">Represents the configuration of a network adapter within the guest operating system.</span></span>

<span data-ttu-id="f1629-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1629-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1629-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1629-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestNetworkAdapterConfiguration
{
  string  InstanceID;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
  UINT16  IPAddressOrigins[];
};
```

## <a name="members"></a><span data-ttu-id="f1629-107">Member</span><span class="sxs-lookup"><span data-stu-id="f1629-107">Members</span></span>

<span data-ttu-id="f1629-108">Die **MSVM \_ guestnetworkadapterconfiguration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f1629-108">The **Msvm\_GuestNetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="f1629-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1629-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1629-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1629-110">Properties</span></span>

<span data-ttu-id="f1629-111">Die **MSVM \_ guestnetworkadapterconfiguration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1629-111">The **Msvm\_GuestNetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1629-112">**Defaultgateways**</span><span class="sxs-lookup"><span data-stu-id="f1629-112">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1629-113">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f1629-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1629-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1629-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1629-115">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="f1629-115">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="f1629-116">Ein Array von Zeichen folgen, die die Standard-IP-Gateways enthalten, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="f1629-116">An array of strings that contain the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="f1629-117">Die maximale Anzahl von Standard-IP-Gateways, die auf einem einzelnen Netzwerkadapter konfiguriert werden können, ist 5.</span><span class="sxs-lookup"><span data-stu-id="f1629-117">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="f1629-118">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="f1629-118">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1629-119">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f1629-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1629-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1629-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1629-121">Gibt an, ob DHCP auf dem Netzwerkadapter innerhalb des Gast Betriebssystems aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f1629-121">Specifies whether DHCP is enabled on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="f1629-122">**DnsServers**</span><span class="sxs-lookup"><span data-stu-id="f1629-122">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1629-123">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f1629-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1629-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1629-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1629-125">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="f1629-125">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="f1629-126">Ein Array von Zeichen folgen, das die DNS-Server enthält, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="f1629-126">An array of strings that contain the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="f1629-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f1629-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1629-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1629-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1629-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1629-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1629-130">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f1629-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f1629-131">Der eindeutige Bezeichner für dieses-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f1629-131">The unique identifier for this object.</span></span>

</dd> <dt>

<span data-ttu-id="f1629-132">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="f1629-132">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1629-133">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f1629-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1629-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1629-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1629-135">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="f1629-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="f1629-136">Ein Array von Zeichen folgen, die die IP-Adressen enthalten, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="f1629-136">An array of strings that contain the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="f1629-137">**Ipaddressorigins**</span><span class="sxs-lookup"><span data-stu-id="f1629-137">**IPAddressOrigins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1629-138">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="f1629-138">Data type: **UINT16** array</span></span>
</dt> <dt>

<span data-ttu-id="f1629-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1629-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1629-140">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="f1629-140">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="f1629-141">Die Quelle der IP-Adressen, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="f1629-141">The source of the IP addresses configured on the network adapter within the guest operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1629-142">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f1629-142">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1629-143">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f1629-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>

<span data-ttu-id="f1629-144">**Statisch** (2)</span><span class="sxs-lookup"><span data-stu-id="f1629-144">**Static** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1629-145">**Protocoliftype**</span><span class="sxs-lookup"><span data-stu-id="f1629-145">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1629-146">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1629-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1629-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1629-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1629-148">Gibt die IP-Protokolle an, auf die die von dieser Instanz angegebenen Einstellungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1629-148">Identifies the IP protocols that the settings specified by this instance apply to.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1629-149">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f1629-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1629-150">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f1629-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="f1629-151">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="f1629-151">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="f1629-152">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="f1629-152">**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="f1629-153">**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="f1629-153">**IPv4/v6** (4098)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1629-154">**Subnetze**</span><span class="sxs-lookup"><span data-stu-id="f1629-154">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1629-155">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f1629-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1629-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1629-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1629-157">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="f1629-157">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="f1629-158">Ein Array von Zeichen folgen, die die Subnetze enthalten, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="f1629-158">An array of strings that contain the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="f1629-159">Jedes Element in diesem Array gilt für das entsprechende Element im **IPADRESSEN** -Array.</span><span class="sxs-lookup"><span data-stu-id="f1629-159">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1629-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1629-160">Requirements</span></span>



| <span data-ttu-id="f1629-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1629-161">Requirement</span></span> | <span data-ttu-id="f1629-162">Wert</span><span class="sxs-lookup"><span data-stu-id="f1629-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1629-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1629-163">Minimum supported client</span></span><br/> | <span data-ttu-id="f1629-164">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1629-164">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f1629-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1629-165">Minimum supported server</span></span><br/> | <span data-ttu-id="f1629-166">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1629-166">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1629-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1629-167">Namespace</span></span><br/>                | <span data-ttu-id="f1629-168">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1629-168">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f1629-169">MOF</span><span class="sxs-lookup"><span data-stu-id="f1629-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1629-170"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f1629-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1629-171">DLL</span><span class="sxs-lookup"><span data-stu-id="f1629-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1629-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1629-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


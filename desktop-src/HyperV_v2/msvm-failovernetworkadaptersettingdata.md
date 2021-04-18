---
description: Stellt die Einstellungen für einen Netzwerkadapter innerhalb des Gast Betriebssystems dar, der zum Zeitpunkt eines Failovers angewendet wird.
ms.assetid: d7f2d471-7328-4181-b94e-b9127814706e
title: Msvm_FailoverNetworkAdapterSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FailoverNetworkAdapterSettingData
- Msvm_FailoverNetworkAdapterSettingData.InstanceID
- Msvm_FailoverNetworkAdapterSettingData.Caption
- Msvm_FailoverNetworkAdapterSettingData.Description
- Msvm_FailoverNetworkAdapterSettingData.ElementName
- Msvm_FailoverNetworkAdapterSettingData.ProtocolIFType
- Msvm_FailoverNetworkAdapterSettingData.DHCPEnabled
- Msvm_FailoverNetworkAdapterSettingData.IPAddresses
- Msvm_FailoverNetworkAdapterSettingData.Subnets
- Msvm_FailoverNetworkAdapterSettingData.DefaultGateways
- Msvm_FailoverNetworkAdapterSettingData.DNSServers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d4989c43dda823be13d604e3ac9b575b62f2f9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354521"
---
# <a name="msvm_failovernetworkadaptersettingdata-class"></a><span data-ttu-id="6ea99-103">MSVM \_ failovernetworkadaptersettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="6ea99-103">Msvm\_FailoverNetworkAdapterSettingData class</span></span>

<span data-ttu-id="6ea99-104">Stellt die Einstellungen für einen Netzwerkadapter innerhalb des Gast Betriebssystems dar, der zum Zeitpunkt eines Failovers angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ea99-104">Represents the settings for a network adapter within the guest operating system, which will be applied at the time of a failover.</span></span>

<span data-ttu-id="6ea99-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6ea99-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea99-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ea99-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FailoverNetworkAdapterSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
};
```

## <a name="members"></a><span data-ttu-id="6ea99-107">Member</span><span class="sxs-lookup"><span data-stu-id="6ea99-107">Members</span></span>

<span data-ttu-id="6ea99-108">Die **MSVM \_ failovernetworkadaptersettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6ea99-108">The **Msvm\_FailoverNetworkAdapterSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="6ea99-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ea99-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ea99-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ea99-110">Properties</span></span>

<span data-ttu-id="6ea99-111">Die **MSVM \_ failovernetworkadaptersettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6ea99-111">The **Msvm\_FailoverNetworkAdapterSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ea99-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6ea99-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea99-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ea99-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ea99-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ea99-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6ea99-115">A short description of the object.</span></span> <span data-ttu-id="6ea99-116">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6ea99-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6ea99-117">**Defaultgateways**</span><span class="sxs-lookup"><span data-stu-id="6ea99-117">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea99-118">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6ea99-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ea99-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-120">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="6ea99-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="6ea99-121">Ein Array von Zeichen folgen, das die Standard-IP-Gateways angibt, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="6ea99-121">An array of strings that specify the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="6ea99-122">Die maximale Anzahl von Standard-IP-Gateways, die auf einem einzelnen Netzwerkadapter konfiguriert werden können, ist 5.</span><span class="sxs-lookup"><span data-stu-id="6ea99-122">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="6ea99-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ea99-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea99-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ea99-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ea99-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ea99-126">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6ea99-126">A description of the object.</span></span> <span data-ttu-id="6ea99-127">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6ea99-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6ea99-128">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="6ea99-128">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea99-129">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6ea99-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ea99-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ea99-131">Gibt an, ob DHCP auf der IPv4-Schnittstelle des Netzwerkadapters innerhalb des Gast Betriebssystems aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6ea99-131">Specifies whether DHCP is enabled on the IPv4 interface of the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="6ea99-132">**DnsServers**</span><span class="sxs-lookup"><span data-stu-id="6ea99-132">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea99-133">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6ea99-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ea99-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-135">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="6ea99-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="6ea99-136">Ein Array von Zeichen folgen, die die DNS-Server angeben, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="6ea99-136">An array of strings that specify the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="6ea99-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6ea99-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea99-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ea99-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ea99-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ea99-140">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6ea99-140">A display name for the object.</span></span> <span data-ttu-id="6ea99-141">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6ea99-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6ea99-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6ea99-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea99-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ea99-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ea99-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-145">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="6ea99-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6ea99-146">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="6ea99-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6ea99-147">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6ea99-147">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6ea99-148">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="6ea99-148">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea99-149">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6ea99-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ea99-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-151">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="6ea99-151">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="6ea99-152">Ein Array von Zeichen folgen, die die IP-Adressen angeben, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="6ea99-152">An array of strings that specify the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="6ea99-153">**Protocoliftype**</span><span class="sxs-lookup"><span data-stu-id="6ea99-153">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea99-154">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ea99-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ea99-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ea99-156">Identifiziert die Internet Protokolle, auf die die von dieser Instanz angegebenen Einstellungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ea99-156">Identifies the Internet protocols that the settings specified by this instance apply to.</span></span> <span data-ttu-id="6ea99-157">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="6ea99-157">This must be one of the following values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ea99-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6ea99-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6ea99-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6ea99-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="6ea99-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="6ea99-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="6ea99-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="6ea99-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="6ea99-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="6ea99-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>


</dt> <dd>

<span data-ttu-id="6ea99-163">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="6ea99-163">IPv4/IPv6</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ea99-164">**Subnetze**</span><span class="sxs-lookup"><span data-stu-id="6ea99-164">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea99-165">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="6ea99-165">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6ea99-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ea99-167">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="6ea99-167">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="6ea99-168">Ein Array von Zeichen folgen, die die Subnetze angeben, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="6ea99-168">An array of strings that specify the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="6ea99-169">Jedes Element in diesem Array gilt für das entsprechende Element im **IPADRESSEN** -Array.</span><span class="sxs-lookup"><span data-stu-id="6ea99-169">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ea99-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ea99-170">Requirements</span></span>



| <span data-ttu-id="6ea99-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ea99-171">Requirement</span></span> | <span data-ttu-id="6ea99-172">Wert</span><span class="sxs-lookup"><span data-stu-id="6ea99-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea99-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ea99-173">Minimum supported client</span></span><br/> | <span data-ttu-id="6ea99-174">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ea99-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ea99-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ea99-175">Minimum supported server</span></span><br/> | <span data-ttu-id="6ea99-176">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ea99-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ea99-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ea99-177">Namespace</span></span><br/>                | <span data-ttu-id="6ea99-178">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6ea99-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6ea99-179">MOF</span><span class="sxs-lookup"><span data-stu-id="6ea99-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ea99-180"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6ea99-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ea99-181">DLL</span><span class="sxs-lookup"><span data-stu-id="6ea99-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ea99-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ea99-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

